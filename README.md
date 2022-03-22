# Vehicle Service
Vehicle service endpoint.

## Tasks
- Clone project from https://github.com/justin-tcsens/vehicle-management, to your local working directory.
- With reference to the vehicle endpoint implementation, complete the task by implementing /summon endpoint.
- Tasks including but not limited to following:-

**Repository**
- Create new SummonRepository.java class under /src/main/java/my/com/tcsens/vehiclemanagement/repository package.
- Annotate class with @Repository spring boot annotation.
- Declare private final variable for DSLContext, and initialize it by dependency injection (DI).
- Create new method with name getSummonByVehicleId(), and implement necessary code to achive the goal.

**Service**
- Create new SummonService.java class under /src/main/java/my/com/tcsens/vehiclemanagement/service package.
- Annotate class with @Service spring boot annotation.
- Declare private final variable for SummonRepository, and initialize it by dependency injection (DI).
- Create new method with name getSummonByVehicleId(), calling the method published on step above.
- Return list of summon from the method.

**Controller**
- Create new SummonController.java class under /src/main/java/my/com/tcsens/vehiclemanagement/controller package.
- Annotate class with @Controller spring boot annotation.
- Implement SummonApi.java to the class, code generated from OpenAPI specification.
- @Override getSummonByCriteria(String carPlateNumber) method in the class.
- Declare private final variable for SummonService, and initialize it by dependency injection (DI).
- Call to the method published on service class, return the result to client.

### Notes:
- Run '.\mvnw clean install' to install necessary package defined in pom.xml
- Run '.\mvnw spring-boot:run' to start the Spring Boot application.
