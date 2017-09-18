# Newman

Image for running newman in (gitlab)-ci environments


### Versions:

  Alpine: 3.6

  Node: 8.5.0

  Newman: 3.8.2


### Usage Examples


#### gitlab-ci.yml:

```
  testing:
    stage: test
    image: polarbase/newman
    script:
      - newman run my.postman_collection.json -e my.postman_environment.json -r cli,html,json
    artifacts:
      paths:
      - newman/

```


#### local:

```terminal
docker run -t --rm -v ${PWD}:/etc/newman polarbase/newman newman run my.postman_collection.json -e my.postman_environment.json -r cli,html,json
```
