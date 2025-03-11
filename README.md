# Task definition

## Write service abnormal-values-recognizer

### checks a current pulse value for patient id against a provided range

range is provided by some local implementation of the interface RangeProviderClient <br>
the interface RangeProviderClient inside the project abnormal-values-recognizer has method getRange(long patientId) returning record Range with minimal and maximal allowed values

### all abnormal values should be pushed in a Data Stream as AnormalPulseValue

AbnormalPulseValue is the Record with patientId, value and Range fields

### Local invocation using local debugger of VSCode for testing purpose
