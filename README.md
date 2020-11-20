# netlify-dns-js

The purpose of this project is to run a task which updates the given dns records in netlify to the current ip using their api.

This was created to keep the records correct in the event that the ip of the server changed.

## Running
### Docker
To run the project first create a file `compose-variables.env`

This should contain the following variables:
```
HOSTNAMES
NETLIFY_AUTH
NETLIFY_ZONE
```

The hostnames value should be a comma seperated list of domains you wish to keep up to date. for example, `domain.com,subdomain.domain.com`

The project can then be started using docker-compose.
```
docker-compose up -d
```

### Node
To run with node the environment variables will nee to be set on the host system. Then run:
```
npm i
npm start
```