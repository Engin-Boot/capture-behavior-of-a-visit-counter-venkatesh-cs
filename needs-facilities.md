# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation
  
Given counter system has synced count data everyday of the week
and the data is accurate
When a new week starts (Defined by the manager)
then aggregate the count of the whole week and generate a PDF which contains
(i) Daily data (ii) Number of patients visited during the week
(iii) Hourly distribution

Scenario: Alert when seating capacity is full
Given there is a display board and
alert system is connected to the counter system
and the alert system is aware of the seating capacity of the hospital
When the number of visitors is greater than available capacity
Then display message on the display board
