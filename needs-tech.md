# Visit-counter technical needs

Scenario: Recover across restarts of the server that runs the visit-counter

Given that counter system has non-volatile memory
and there is a central server connected to the counter system
and the counter system syncs the count data with the server every hour
and the counter system updates value of counter
in non-volatile memory every half hour
When the counter system fails for any reason,
then system counter loads counter value from both from the central server
and non-volatile memory. System compares the value and if the counter values
are not equal, then system changes value of counter in the central server
to the value present in the non-volatile memory.

Scenario: Reconcile counts if the sensor is offline for a while

Given that counter system has non-volatile memory
and there is a central server connected to the counter system
and the counter system syncs the count data with the server every hour
and the counter system updates value of counter
in non-volatile memory every half hour
When the counter system fails for any reason,
then system counter loads counter value from both from the central server
and non-volatile memory. System compares the value and if the counter values
are not equal, then system changes value of counter in the central server
to the value present in the non-volatile memory.
