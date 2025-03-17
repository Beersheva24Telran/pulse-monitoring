# Tasks definition
## email-address-provider service
### lambda function
### Gateway API events emitter with GET requests conytaining patientId
### Communicates with PostgreSQL for performing prepared SQL query
### sends responses (200 with email address for sending notification, 400 or 404 with exception text)
## abnormal-values-email-notifier 
### lambda function triggered by DynamoDB data stream with abnormal values
### Communicates with email-address-provider for getting email address
### sends email by the received email (or logging error if emain hyas not be received)
### publishes an apropriate Notification data record to anoth DynamoDB data stream




