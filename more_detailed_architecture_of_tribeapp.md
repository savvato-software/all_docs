# Johnathan's talk on a more detailed description of the tribeapp architecture

## 03-09-2023

>Creating a mobile app which is our front end
>It talks to our backend
>Our backend talks to the database
>frontend - angular
>backend - spring
>db - mysql
>mobile app makes a call to the backend
>backend makes a call to the db
>three layers of the complete application
>
>**backend**
>first layer - controller
>second layer -services
>third layer - data - calls db
>
>**frontend**
>layers
>>template - html
>>handlers - typescript code
>css
>test
>module
>handlers will call services to the backend
>no data layer
>
>Attributes - verb, noun, preposition, adverb
>on the mobile app - go to the attributes page
>will get a list of all their attributes
>then they can select one
>edit or delete one
>create a new one
>make a call to the backend
>post the four words to the backend
>validate them
>write them to the to be reviewed table in the db
>return to the frontend
>wait until it gets processed
>
>to be reviewed table
>automated review
>check each word for validity
>do this by calling the words api
>gives details about each word - words api
>verify what part of each it is
>if words come up as valid, marked as groomed
>hasBeenGroomed is set to true otherwise set to false
>the automated process is done
>then need manual process
>need people to verify to review
>make a query to the to be reviewed table
>for the next item
>returned to the frontend
>person will look at it
>frontend has buttons for approved, rejected, skipped
>if approved, then remove it from to be reviewed table
>attribute becomes associated with the user
>if rejected - know not to use it, will go to another table
>
>create attributes - enter word, saved as to be reviewed phrase and have to wait on the frontend
>automated process will run to make sure all phrases are reviewed
>
>user will request item to be reviewed
>
>review attributes
