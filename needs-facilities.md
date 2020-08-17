# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

  Given the hospital is open and is allowing visitors
  When the visitors visit in the week
  Then increase the number of visitors in that hour/day of the week

Scenario: Alert when seating capacity is full

  Given the hospital is open and is allowing visitors
  When more visitors visit and no seat is empty
  Then alert that all seats are full
