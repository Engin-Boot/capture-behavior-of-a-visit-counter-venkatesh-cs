# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given hospital issues an ID card for every visitor
  and the user returns the ID card after visit
  and the counter sensor is reset everyday at 12 PM
  and there is a central server that is connected to the counter sensor system
  When the patient enters the hospital and signs up for an ID card
  Then increase the counter by one and generate a report at 12PM local time
  and push the data to the central server

Scenario: Compute parking slots to reserve for visiting specialists

  Given that the hospital has consulting specialists,
  and there is enough additional space in parking lot to reserve parking space
  When a patient gets admitted
  Then track type of specialist needed and reserve parking space accordingly
  and based on the consultant needed, reserve parking space
