## Day 8  String Functions

#### Question : Create a patient summary that shows patient_id, full name in uppercase, service in lowercase, age category (if age >= 65 then 'Senior', if age >= 18 then 'Adult', else 'Minor'), and name length. Only show patients whose name length is greater than 10 characters.

``` Query : 

select patient_id , upper(name) ,lower(service) , age ,
CASE 
        WHEN age >= 65 THEN 'Senior'
        WHEN age >= 18 THEN 'Adult'
        ELSE 'Minor'
END as category, 
length(name) from patients where length(name) > 10

```
