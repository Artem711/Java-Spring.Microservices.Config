In case we have multiple environments for the limits_service microservice.
We would store separate configurations for each environment of limits_service by:

1. Storing configuration related to multiple enviromments of a single service in the GitHub repository

   We would create separate files for each enviornment:

   - limits_service.properties => http://localhost:8888/limits_service/default
   - limits_service-qa.properties => http://localhost:8888/limits_service/qa
   - limits_service-dev.properties => http://localhost:8888/limits_service/dev

2. Now, how do we make the application (limits_service) take the values from the Spring Cloud Config Server?

   - To support multiple enviromments of a microservice in a SpringBoot applications, you'd configure Profiles.

   - So, in application.properties add:
     `spring.profiles.active=dev` or `spring.profiles.active=qa` or `spring.profiles.active=default`

3. Consequently, by separating out the configuration from your applications, you are making your operations easier.

   - Your operations team can control all configuration related to all microservices for multiple environments in a single location.

   - So, whenever they would want to make a change to configuration of some environemt of some microservice - they would make a change in this centralised GitHub repositry, commit it and that's it changed is ready and distributed to multiple environments!
