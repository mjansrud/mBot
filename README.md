# mBot
A bot trading digital currencies as bitcoin 
mBot is developed using reactJS (frontend), node.js (backend) and postgresql.

# Getting started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

Make sure you have [**Node >= 6**](https://nodejs.org/en/download/),  [**Git**](https://git-scm.com/downloads) and [**PostgreSQL**](https://www.postgresql.org/download/) installed. Create a database named mBot. 

```
git clone https://github.com/mjansrud/mBot.git 
```

***Repeat for every folder**** 
1) Change directory to each sub-repository, command for changing directory will not be repeated
```
cd api
```
2) Install the node modules required
```
npm install
```

Required environmental variables for API server ( /api /)
```
NODE_ENV_AUTH_JWKS_URL=https://your-domain-for-auth.eu.auth0.com/.well-known/jwks.json
NODE_ENV_AUTH_AUDIENCE=https://your-domain.com
NODE_ENV_AUTH_ISSUER=https://your-domain-for-auth.eu.auth0.com
NODE_ENV_POLONIEX_KEY={YOUR_KEY}
NODE_ENV_POLONIEX_SECRET={YOUR_SECRET}
```
Start the service:
```
node server.js
```

Open a new terminal, start the service ( /bot/ ):
```
node server.js
```

Required environmental variables for frontend server ( /frontend/ )
```
REACT_APP_URL=http://localhost:3000
REACT_APP_URL_API=http://localhost:3001
REACT_APP_ENVIRONMENT=development
REACT_APP_AUTH_URL=your-domain-for-auth.eu.auth0.com
REACT_APP_AUTH_CLIENT_ID={YOUR_CLIENT_ID}
REACT_APP_AUTH_SCOPE=example
REACT_APP_AUTH_AUDIENE=https://your-domain.com
```

Open a new terminl, start the reactjs web server :
```
npm run start
```

# TODO
Make a .sh script starting all services.
