# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given I have access to the server that runs the visit counter
  When the server is back in the working state
  Then recover the server by logging in and refreshing it

Scenario: Reconcile counts if the sensor is offline for a while

  Given the hospital is open and is allowing more people inside
  When the sensor is offline for a while
  Then calculate the average count per hour and increase for the lapsed time.
