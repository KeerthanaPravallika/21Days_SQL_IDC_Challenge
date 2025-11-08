
# Days 1-4: SQL Fundamentals

SELECT, WHERE, ORDER BY, LIMIT

## Day 1

#### Question: List all unique hospital services available in the hospital.

```Query : SELECT distinct(service) as UNIQUE_HOSPITAL_SERVICES FROM services_weekly; ```


## Day 2

#### Question: Find all patients admitted to 'Surgery' service with a satisfaction score below 70, showing their patient_id, name, age, and satisfaction score.

``` Query : select  patient_id, name, age,  satisfaction from patients where service = 'surgery' and satisfaction > 70 ```

## Day 3 

#### Question: Retrieve the top 5 weeks with the highest patient refusals across all services, showing week, service, patients_refused, and patients_request. Sort by patients_refused in descending order.

``` Query : SELECT week, service, patients_refused, patients_request from services_weekly ORDER BY patients_refused DESC LIMIT 5;```

## Day 4

#### Question: Find the 3rd to 7th highest patient satisfaction scores from the patients table, showing patient_id, name, service, and satisfaction. Display only these 5 records.

``` Query : select patient_id, name, service, satisfaction from patients order by satisfaction limit 5 offset 2```



