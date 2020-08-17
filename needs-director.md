# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given the hospital is open on working days and holidays
  When patients visit
  Then increase the visit-count by the number of patients visited

Scenario: Compute parking slots to reserve for visiting specialists

  Given the hospital gate is open for vehicles
  When specialists visit in their own vehicle
  Then increase the number of parking slots required
