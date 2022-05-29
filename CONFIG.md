In case we have multiple environments for the limits_service microservice.
We would store separate configurations for each environment of limits_service by:

1. Storing configuration related to multiple enviromments of a single service in the GitHub repository

   We would create separate files for each enviornment:

   - limits_service.properties => http://localhost:8888/limits_service/default
   - limits_service-qa.properties => http://localhost:8888/limits_service/qa
   - limits_service-dev.properties => http://localhost:8888/limits_service/dev
