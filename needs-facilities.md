# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation
  
Given count data is accurate and is per specification
When a new week starts
Then publish the data of previous week

Scenario: Alert when seating capacity is full
Given both seating and visitor count data is available to the alert sytem
When the number of visitors is greater than available capacity
Then dispay message in display board