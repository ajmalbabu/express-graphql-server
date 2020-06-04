## This project sets up a graphql server that connects to spacex data over REST API and exposes the data as a set of 
## Graphql end points. This project is created by watching [this](https://www.youtube.com/watch?v=SEMTj8w04Z8) video 
## Space X [API](https://docs.spacexdata.com/?version=latest#bc65ba60-decf-4289-bb04-4ca9df01b9c1)

## To run server

npm install
npm run server

and hit graphiql end point at http://localhost:5000/graphql

use below GraphQL queries to reteive data

```
{
     launches {
        flight_number,
        mission_name,
        launch_year,
        launch_success,
        launch_date_local,
        rocket {
          rocket_id,
          rocket_name,
          rocket_type
        }
      }
    }


  {
      launch (flight_number: 2) {
        mission_name,
        launch_year
      }
    }


  {
  	rockets {
      rocket_name
    }
  }
```

## Watch 5 part series on creating graphql server CRUD server with mutation [here](https://www.youtube.com/watch?v=PEcJxkylcRM)

