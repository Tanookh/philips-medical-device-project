# philips-medical-device-project

## Background
As you all know the number of Corona virus patients that hospitals can handle is limited and
some of the places for them is allocated on account of other hospitals departments.
Our system will aim to predict from the current number of positive tests and from the positive
tests percentage of total tests the number of beds that should be prepared for allocation for the
next week.


## System
### Assumptions
We assume the following about a positive test received:
1. After a week from the test, the person will need to be hospitalized for 1 week
2. After 1 week in hospital 80% are well and go home, 20% continue to another week in the hospital
3. After 2nd week in hospital all go home


## Functionality
### The system will do the following:
1. Receive Corona tests results: how many were positive, how many negative
2. Calculate how many of these positive test will probably need:
  a. to be hospitalized
  b. when they will need it
  c. and for how long
3. Allow reports according to a specific future date how many patients will probably need hospitalization
4. Allow reports according to date range that will infor for each date in date range the number of patients
5. Trigger notifications in form of email, SMS or other to specific accounts when the number of patients calculated for next week is above a certain threshold


## Advanced
### The advanced topics relate to:
1. Hospitals
  a. System will have a list of hospitals and for each of them the max number of Corona patients it can handle
  b. Each test result will include an indication( ie geographic area) that will connect it to a specific hospital
  c. Each hospital can have a status:
    i. Green: Less then 50% of the max patients is occupied
    ii. Yellow: between 50% - 80% of the patients beds are occupied
    iii. Red: more than 80% of the patients beds is occupied
  d. Allow hospitals status reports that lists for a given date the calculated hospitals status
2. Notifications: enable 3 colors of notifications according to the hospital status
3. Country
  a. Country status is calculated according to the total hospital status. Figure it out by yourself how to calculate the country status according to it.
  b. Allow report according to a date of the country calculated status
  c. Allow a date range report that indicates for each date in the date range the Country’s calculated status
4. Add user interface that allows the user to activate the reports that you have implemented by choosing:
  a. The report
  b. The date/date range
  c. Display the report result
5. Data received:
  a. Data can be basic: number of negative and number of positive results
  b. More information: numbers will be for each geographic area
  c. More: list of people IDs and their test results. This will allow additional reports for how many return sick people
