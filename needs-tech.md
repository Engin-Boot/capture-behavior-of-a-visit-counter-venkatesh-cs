# Visit-counter technical needs

Scenario: Recover across restarts of the server that runs the visit-counter

Given that the system knows the value of the visit-counter
When the system fails for any reason,
Then store count value in non-volatile memory.

Scenario: Reconcile counts if the sensor is offline for a while

Given that central server is connected to the sensor system
When sensor is back online,
Then read count data from server and start counting from that value
