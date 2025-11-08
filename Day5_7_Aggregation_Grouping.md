
# Days 5-7: Aggregation & Grouping

COUNT, SUM, AVG, GROUP BY, HAVING

## Day 5

#### Calculate the total number of patients admitted, total patients refused, and the average patient satisfaction across all services and weeks. Round the average satisfaction to 2 decimal places.

```Query : select sum(patients_admitted), sum(patients_refused) , round(avg(patient_satisfaction),2) from services_weekly ```


