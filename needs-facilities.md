# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given the patient is allowed to have visitors and the hospital is open
  When the visitors visit in the week
  Then increase the number of visitors in that hour/day of the week

Scenario: Alert when seating capacity is full

  Given the hospital is open and more visitors are allowed
  When more visitors visit and no seat is empty
  Then alert that all seats are full
