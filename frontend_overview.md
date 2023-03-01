# Frontend overview talk by Johnathan

## 02/28/2023

we do end to end testing in cypress
cypress - writes code that acts like a user
mimics user actions
automated user actions

describes a unit test
i.e. trying to get to new user page
i.e. do we have four input fields
if all true, then assume it works correctly

no md docs should be in the directory structure
All the md docs would make reference in the project readme file

pages folder - to add new pages

profile-page folder - main page
subpage - edit
first page will be a list of items
profile page represents a domain item
domain object - part of name state of application
domain - car, tire, repair person, car bay
nouns that are a part of the problem you are trying to solve
show a list of domain objects
only one profile
can edit our profiles
any unit tests would be in the spec.ts file

services folder - more global

profile model service - object that represents a profile
we have a service called the model
the model helps to abstract outside of the page to be able to use it in other places
like saving the model or copying the model
layer that page uses
model itself uses the layer api service
the page itself is not calling the api resources
if the page needs something, will call api service

profile api service -

validators - for validation of phone numbers, general validation

app module - brings together all resources to display all modules being created
module for each domain page
app module - high level

app routing -

environments - how we are running the application
running in dev - want server to be localhost
if running in production - ready for the world
don't want to change the code
so we have a configuration file and have variables
