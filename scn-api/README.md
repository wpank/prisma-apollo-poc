### Installation

#### Install Node Modules
First run  `yarn install` to install the appropriate node modules. 

#### Generate Prisma Schema & Deploy
Run `yarn deploy`

This script will run `prisma deploy`, which will prompt you to set up a prisma cloud account. 

You should then choose which kind of server to deploy it to. Choose `Demo server`.

This will update the `scn-api/prisma/prisma.yml` config file with the appropriate http endpoint for the prisma server. 

The `prisma.yml` config file then has a post-deploy hook that will run `prisma generate`, which will
scaffold out CRUD based functions for the GraphQL schema defined in `scn-api/primsa/datamodel.prisma`.

#### Run the graphql-yoga server
Finally, run `yarn start` to start up the `graphql-yoga` server. 

You can then go to `http://localhost:4000` to access the the interactive graphql playground. 



