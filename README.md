

# Wuerflii

This is the parent repo of backend and frontend.

You can look into the _docker-compose.yml_ for the basic deployement in docker. (Including a postgresql database)


## Deployement

Create the _docker-compose.yml_ and .env in the same directory. Look into the .env.example in the backend repo and edit all variables to your liking. You can add the email section to receive notifications if something went wrong in the backend but you don't have to. Some variables are for development only and will not affect the backend. (If you want to change them you have to edit them in the code itself)
You can choose the frontend-port by changing the first number in

```
ports:
- 10000:80
```

in _docker-compose.yml_ to something like `- 342:80`. Do not change the 80-port unless you tell nginx to listen to another port by editing the _nginx.conf_ in the frontend.
You can expose a port for the postgresql by removing the # in 

```
#    ports:
#      - 20000:5432
```

so that you can connect via a database UI like pgadmin4.
