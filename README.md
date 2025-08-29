# Anypoint Platform Development: Production-Ready Integrations - DEX670

## Local Path
- PROJECT_HOME=/Users/yehan.jeong/Workspace/AnypointStudio/202508.P_DEX670_2
- STUDENT_FILE=/Users/yehan.jeong/Desktop/CDEV-DEX670-EN-25oct2024-Student-Files

## Anypoint Platform Information
- Mule Account: yehan250829

### Business Group
- Business Group ID: c1c00018-c4df-45c7-9dfc-1493d1455b02
- Client ID: 69ef10704a534e759d36b930eda7015b
- Client Secret: 61bA609846f244d7A6EfFf98BA3F2677

### Connected App
- Exchange Viewer ID: c9ea2ad8b7494479b828544f7c9dbc7a
- Exchange Viewer Secret: b5158aC8C6E94A96916DB6436C346A82
- Exchange Contributor ID: 1027d9d87bfa42328b80c4b85e23fa97
- Exchange Contributor Secret: 072D8945dDea4B17B22Bbf89eBd4E3d5

## Commands
- export PROJECT_HOME=/Users/yehan.jeong/Workspace/AnypointStudio/202508.P_DEX670_2
- export STUDENT_FILE=/Users/yehan.jeong/Desktop/CDEV-DEX670-EN-25oct2024-Student-Files
- mvn clean verify -U -Dencrypt.key=secure12345 -DskipTests=true
- -M-Dencrypt.key=secure12345 -M-Danypoint.platform.gatekeeper=disabled
- curl -ik -X PUT -H "Content-Type: application/json" -d "{\"lastName\" :\"Smith\",\"numBags\":2}" https://localhost:8081/api/v1/tickets/PNR123/checkin
- curl -ik -X PUT -H "Content-Type: application/json" -d "{\"payerID\": \"STJ8222K092ST\", \"paymentID\": \"PAY-1AKD7482FAB9STATKO\"}" https://localhost:8081/api/v1/tickets/N123/paymentApproval
- curl -ik https://localhost:8081/alive
- curl -ik https://localhost:8081/ready
- curl -ik -X PUT -H "Content-Type: application/json" -d "{\"lastName\" :\"Mule\",\"numBags\":2}" https://localhost:8081/api/v1/tickets/PNR123/checkin
- curl -ik -X POST -H "Content-Type: application/json" -d "{\"amount\":12.34, \"description\": \"something\"}" https://localhost:8081/api/v1/payments
- curl -ik -X PUT -H "Content-Type: application/json" -d "{\"payerID\":\"STJ8222K092ST\"}" https://localhost:8081/api/v1/payments/PAY-1B56960729604235TKQQIYVY/approval
- curl -i -X POST -H "Accept: application/json" -H "Accept-Language:en_US" -u "APP-80ANYAIRLINE8184JT3:1929FHDUAL8392K9ABKSNMM" -d "grant_type=client_credentials" https://training-paypal-fake-api-sandbox-mjf1rw.5sc6y6-1.usa-e2.cloudhub.io/v1/oauth2/token
- export atoken=kas8392.QISKEkdls8345_Zsrq9cK9hNsqrEU9xem4QJ6sQa36VHfyuBe
- curl -i -X POST -H "Content-Type: application/json" -H "Authorization: Bearer $atoken" -d "{\"intent\":\"sale\", \"payer\": {\"payment_method\":\"paypal\"}, \"transactions\":[{\"amount\":{\"total\":\"80.00\", \"currency\":\"USD\"}, \"description\": \"Check-In Baggage.\", \"custom\": \"ANYAIRLINE_90048630024435\",\"invoice_number\": \"48787589673\", \"payment_options\":{\"allowed_payment_method\":\"INSTANT_FUNDING_SOURCE\"},\"soft_descriptor\":\"ANYAIRLINE BAGGAGE\"}], \"note_to_payer\":\"Behappy.\"}" https://training-paypal-fake-api-sandbox-mjf1rw.5sc6y6-1.usa-e2.cloudhub.io/v1/payments/payment
- curl -ik -X PUT -H "Content-Type: application/json" -d "{\"lastName\":\"Mule\",\"numBags\":2}" https://localhost:8081/api/v1/tickets/PNR123/checkin
- curl -ik -H "Content-Type:text/xml" -d "<CancellationNotification><PNR>PNR123</PNR><PassengerLastName>Mule</PassengerLastName></CancellationNotification>" https://localhost:8081/api/cancelFlight
- curl -ik -H "Content-Type:text/plain" -d "invalid content type and content" https://localhost:8081/api/cancelFlight