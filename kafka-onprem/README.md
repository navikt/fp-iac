## Kafka oneshot topic config (works only on utviklerimage)

#### From swagger
Copy the whole file content (or only the interesting topics) and use the following swagger services 

- dev (q0, q1, t4) - [Swagger Admin Rest Dev](https://kafka-adminrest.nais.preprod.local/api/v1/apidocs/index.html?url=swagger.json#/OrderedMap%20{%20%22name%22:%20%22Oneshot%22%20}/put_api_v1_oneshot)
- prod - [Swagger Admin Rest Prod](https://kafka-adminrest.nais.adeo.no/api/v1/apidocs/index.html?url=swagger.json#/OrderedMap%20{%20%22name%22:%20%22Oneshot%22%20}/put_api_v1_oneshot)

If the topic already exists it will be updated, as long you have the right MANAGER access rights for the given topic, otherwise it will be ignored.

#### From command line
See kafka folder
- dev - run against https://kafka-adminrest.nais.preprod.local/api/v1/oneshot
- prod - run against https://kafka-adminrest.nais.adeo.no/api/v1/oneshot

```
curl --user $NAV_IDENT:$NAV_PWD -v -X PUT -H "Content-Type: application/json" ${dev|prod} -d @kafka-oneshot-<env>.json
```