# Overview
## Dashboard features
detailed further down

## Technologies used
Node.js, Azure app service, github/github actions

# Prerequisites
Node, Azure subscription, github account

# Installation
fork and clone this repo

# Configuration
create a .env file with 5 variables
1. COSMOS_ENDPOINT = endpoint url for CosmosDB
2. COSMOS_KEY = CosmosDB primary key
3. COSMOS_DATABASE = RideauCanalDB
4. COSMOS_CONTAINER = SensorAggregations
5. PORT = 3000

# API Endpoints
## List all endpoints with descriptions
/api/all: gets all data. intended for debugging



# Deployment to Azure App Service
## Step-by-step deployment guide
1. create azure web app
2. select basic settings 
3. in deployment, enable continuous deployment and configure deployment to rideau-canal-dashboard repo
4. create

## Configuration settings
in environment variables, create 5 variables:
1. COSMOS_ENDPOINT = endpoint url for CosmosDB
2. COSMOS_KEY = CosmosDB primary key
3. COSMOS_DATABASE = RideauCanalDB
4. COSMOS_CONTAINER = SensorAggregations
5. PORT = 3000


# Dashboard Features
## Real-time updates
updates every 30 seconds to display current information

## Charts and visualizations
displays current info for each of the 3 locations, and overall safety rating for the canal (if one area's rating is unsafe or caution overall rating is the same), as well as trends of the ice thickness and temperature over the last hour

## Safety status indicators
If safety criteria defined in the stream analytics sql query are not met, displays either caution or unsafe. Otherwise displays safe

# Troubleshooting
i somehow had app.js named as ap..js for about 3 hours before i noticed it was wrong. :)