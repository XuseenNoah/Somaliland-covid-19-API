# Covid-19 Somaliland API
[![GitHub stars](https://github.com/XuseenNoah/Somaliland-covid-19-API)](https://github.com/XuseenNoah/Somaliland-covid-19-API Somaliland API is an API made for tracking Coronavirus cases in Somaliland, the data is based on the [official Somaliland Coronavirus website](https://somalilandcovid19.com)  and it's updated daily.

## API Reference



You can open the URL in your browser to further inspect the response. Or you can make this curl call in your terminal to see the prettified response:

```
```



## API Endpoints

### Latest Endpoint

Gets the latest national confirmed, recovered and deaths cases.

```http
GET /latest
```

__Sample response__
```json
{
  "latest": [
    "confirmed": 6,
    "deaths": 1,
    "recovered": 2
  ]
}
```

```

#### Gets location by city

```http
GET /locations/city/:city
```
__Path Parameters__
| __Path parameter__ | __Required/Optional__ | __Description__                                                                                                                                                          | __Type__ |
| ------------------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | -------- |
| province                 | OPTIONAL              | The name of the city in which the location belongs to. The list of the cities can be found in the locations response: ``/locations`` | String  |

#### Example Request
```http
GET /locations/city/burao
```

__Sample response__
```json
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
