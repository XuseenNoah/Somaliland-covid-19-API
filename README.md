Covid-19 Somaliland API
GitHub stars GitHub forks HitCount

Covid-19 Somaliland API is an API made for tracking Coronavirus cases in Somaliland, the data is based on the official Somalilandcovid19.com website and it's updated daily.


You can open the URL in your browser to further inspect the response. Or you can make this curl call in your terminal to see the prettified response:


Swagger
You can use the API through the SwaggerUI.


Latest Endpoint
Gets the latest national confirmed, recovered and deaths cases.

GET /latest
Sample response

{
   [
    "confirmed": 6,
    "deaths": 1,
    "recovered": 2
  ]
}
Locations Endpoint
List of all locations
Gets the latest national confirmed, recovered and deaths cases of each location

GET /locations
Sample response

{
   [
    {
    "city": "Hargeysa",
    "confirmed": 3,
    "deaths": 0,
    "id": 1,
    "province": "Maroodijeex",
    "recovered": 0
    },
    {
    "city": "Burco",
    "confirmed": 1,
    "deaths": 0,
    "id": 2,
    "province": "Togdheer",
    "recovered": 1
     }
   ]
 }



Path parameter	Required/Optional	Description	Type
province	OPTIONAL	The name of the city in which the location belongs to. The list of the cities can be found in the locations response: /locations	String
Example Request
GET /locations/city/burao
Sample response

{
    "locations": [
    {
    "city": "Burco",
    "confirmed": 1,
    "deaths": 0,
    "id": 2,
    "province": "Togdheer",
    "recovered": 1
    }
  ]
 }
