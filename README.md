# Task definition
## Write service pulse-values-reducer
### computes the average value for a predefined number of values received from the stream pulse_values and sending to another stream average_pulse_values 
## Uses the same record SensorData
### Uses the same LatestValuesSaverImpl like for jump-pulse-recognizer (just another methods) for saving last pulse values for each patientId
### Uses the same MiddlewareDataStream
 put jump data inside new created DynamoDB table "average-pulse-values" as data stream <br>
 for local debugging the TestStream as  MiddlewareDataStream should be used 
### Adds two additional resources inside template.yaml
PulseValuesReducerFunction (lambda function) <br>
AveragePulseValuesStream (DynamoDB table)
### Adds configuration for local debugging


