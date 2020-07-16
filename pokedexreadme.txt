Notes :
=======

Scope of persistence of user acount data is within the server instance running. If the server is shutdown all user data is lost.

A user's account is only maintained when a server instance is active and the user can only log in and out as many times as possible. 

Only the json data exists and the user would not be able to view pokemon account in a previous session from a prior server instance

Procedure
=========
navigate to the PokeDex App folder
e.g. cd PokeApp 
mvn spring-boot:run
List of API Requests

Specify how many pokemon should be returned by the endpoint


Filter the pokemon by name or type or stats
http://localhost:8080/pokeapp/getAll?filter=&sort=&type=&qty=5
http://localhost:8080/pokeapp/getAll?filter=&sort=&type=&qty=5
http://localhost:8080/pokeapp/getAll?filter=name:Bulbasaur&sort=&qty=
http://localhost:8080/pokeapp/getAll?filter=types:118&sort=&qty=5
http://localhost:8080/pokeapp/getAll?filter=stats:baseAttack:118&sort=name&qty=
http://localhost:8080/pokeapp/getAll?filter=stats:baseAttack:118&sort=&qty=5
http://localhost:8080/pokeapp/getAll?filter=baseAttack:231&sort=&qty=

Sort the pokemon by name or type or stats
http://localhost:8080/pokeapp/getAll?filter=&sort=stats:baseAttack&qty=

Login to the server by sending a JSON object containing an email
address and a password
http://localhost:8080/pokeapp/login?={"email":"test@domain.com","password":"pass1234"

Display a list of pokemon that he has caught
http://localhost:8080/pokeapp/add?email=test@domain.com&name=1


Add a pokemon caught to an account
http://localhost:8080/pokeapp/add?email=test@domain.com&name=1


Update a pokemon's stats for a pokemon that he has caught 
http://localhost:8080/pokeapp/update?name=2&baseAttack=118&baseDefense=200&baseStamina=100


Remove a pokemon from his account


Logout




