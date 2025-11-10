
# Days 5-7: Aggregation & Grouping

COUNT, SUM, AVG, GROUP BY, HAVING

## Day 5

#### Calculate the total number of patients admitted, total patients refused, and the average patient satisfaction across all services and weeks. Round the average satisfaction to 2 decimal places.

```Query : select sum(patients_admitted), sum(patients_refused) , round(avg(patient_satisfaction),2) from services_weekly ```

## Day 6

#### For each hospital service, calculate the total number of patients admitted, total patients refused, and the admission rate (percentage of requests that were admitted). Order by admission rate descending.

``` Query : 

select service, sum(patients_admitted), sum(patients_refused),
	ROUND(
        (SUM(patients_admitted) * 100.0) / NULLIF(SUM(patients_request), 0),
        2
    ) AS admission_rate  
    from services_weekly 
    group by service 
    order by admission_rate desc
```

## Day 7

#### Identify services that refused more than 100 patients in total and had an average patient satisfaction below 80. Show service name, total refused, and average satisfaction.

``` Query :
SELECT 
    service,
    SUM(patients_refused) AS total_refused,
    AVG(patient_satisfaction) AS avg_satisfaction
FROM 
    services_weekly
GROUP BY 
    service
HAVING 
    SUM(patients_refused) > 100 AND AVG(patient_satisfaction) < 80;
```

