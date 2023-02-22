# A Very High Level Architectural Description of TribeApp

* Model
* View
* Controller
* Service
* Database

Model

----------
The model is the data. In our spring boot application, the model is the DTO (Data Transfer Object) object.

View

----------
The view is the presentation of the data. In TribeApp, this will be the ionic application. The ionic application is also the client in our architecture.

Controller

----------
The controller is the outside layer of our backend. The controller is the first layer to communicate with our backend. The controller is the business logic. It reads the data from the service and gives that data to the view which in our case is the ionic app. The controlle allows the view to display the data.

Service

----------
The service is the layer that is below the controller. It supports the controller. It handles the business logic related to the domain object. The service interfaces with the database. The service communicates with the database.

Database

----------
The database is the repository for the data and it also contains the entities for the data. The database in our architecture is MySQL. Our current application utilizes an ORM (liquibase) that allows for convenient database migrations.
