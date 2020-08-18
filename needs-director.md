# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given hospital issues an ID card for every visitor
  and the ID card is returned by the visitor after the visit
  When the patient enters the hospital and signs up
  for an ID card
  Then track the number of IDs issued to examine trends

Scenario: Compute parking slots to reserve for visiting specialists

  Given that the hospital has consulting specialists,
  and there is enough additional space in parking lot to reserve parking space
  When a patient gets admitted
  Then track type of specialist needed and reserve parking space accordingly
