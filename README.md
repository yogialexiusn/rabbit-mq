Welcome to the rabbit-mq wiki!

Download dockaer image rabbit:3.9.29-management-alpine

# STEP 1 Download and Install Docker Dekstop
# STEP 2 Pull Rabbit MQ Image
docker pull rabbitmq:3.9.29-management-alpine
# STEP 3 Run Rabbit MQ Image into container
docker run --rm -it -p 15672:15672 -p 5672:5672 rabbitmq:3.9.29-management-alpine
# STEP 4 Run rabbit-mq Application
# STEP 5 Test rabbit-mq Application
Test Publisher and Consumer based on link below
curl --location 'http://localhost:8085/api/v1/publish' \
--header 'Content-Type: application/json' \
--data '{
    "id": 2,
    "firstName": "Yogi",
    "lastName": "cacad1"
}'
