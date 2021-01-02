# stackabuse-graphql-api

This repository is about a tutorial teaching how to build a GraphQL API with django from a site called stackabuse.com. The link to this tutorial is provided under **References and Sources** section below.

## References and Sources

* <https://stackabuse.com/building-a-graphql-api-with-django/>

## Dependencies

* pip install django
* pip install graphene_django

Note: See [requirements.txt](https://github.com/VanTye/stackabuse-graphql-api/blob/main/requirements.txt) for more information.

## Concepts

* Types
* Queries
* Mutations
  * Input
  * Payload
* Schema

## Notes

### Load Fixtures Data

To load **fixtures/movies.json** into the database, run `python manage.py loaddata fixtures/movies.json`

### GraphiQL

To disable graphiql, edit this line `path('graphql/', GraphQLView.as_view(graphiql=False))` under **django_graphql_movies/urls.py**. To access GraphiQL, go to http://127.0.0.1:8000/graphql/.

### CSRF protection

Add csrf_exempt as such `path('graphql/', csrf_exempt(GraphQLView.as_view(graphiql=False)))` to add protection for communication from external applications.
