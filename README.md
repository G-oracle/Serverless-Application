# Deploy Backend
Launch the frontend app locally.

* To download all the package dependencies, run the command from the directory `backend/`:
    ```bash
        cd backend

        npm install

        npm install --save-dev serverless-iam-roles-per-function@next 

        serverless

        serverless deploy --verbose    
        ```


# Deploy Frontend

* To download all the package dependencies, run the command from the directory `client/`:

    ```bash
        cd client
        
        npm install

        npm run start
    ```
The client folder contains a web application that can use the API that should be developed in the project.

To use it please edit the config.ts file in the client folder:

 ```bash
             const apiId = '...' API Gateway id
            export const apiEndpoint = `https://${apiId}.execute-api.us-east-1.amazonaws.com/dev`

            export const authConfig = {
            domain: '...',    // Domain from Auth0
            clientId: '...',  // Client id from an Auth0 application
            callbackUrl: 'http://localhost:3000/callback'
            }
```
