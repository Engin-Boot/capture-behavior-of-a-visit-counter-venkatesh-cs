# Visit-counter technical needs

Scenario: Recover across restarts of the server that runs the visit-counter

Given that the system knows the value of the visit-counter
When the system fails for any reason,
Then store count value in in non-volatile memory.

Scenario: Reconcile counts if the sensor is offline for a while

Given count data is stored in some server and is accessable within reasonable time
When sensor is back on line,
Then read count data from server and start counting from that value