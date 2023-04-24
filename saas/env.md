## APP_URL:
This is an Important Variable, 
Your site url, make sure to add `https://` or `http://` at the beginging. and make sure it doesn't point to a pathname
ex: `https://example.com` or `https://www.example.com/`


## DATABASE_URL

- Make a database using [Railway](https://railway.app)
make sure it's a mysql database Not anything else. (otherwise change the provider in the prisma/schema.prisma).

- Navigate to `Connect` then  in `Available Variables` copy the `MYSQL_URL` 


## SHADOW_DATABASE_URL

- Make another database using [Railway](https://railway.app)
make sure it's a mysql database Not anything else. (otherwise change the provider in the prisma/schema.prisma).

- Navigate to `Connect` then  in `Available Variables` copy the `MYSQL_URL` 


## DATA_PROXY_URL
- After you create your databases.
- navigate to `https://cloud.prisma.io/` and create a new project.
- paste the same connection string as your `DATABASE_URL`.
- chose the closest to your region. then create.
- copy the prisma connection string (starts with: `prisma://...`) that will be your `DATA_PROXY_URL`


# Google Authentication
GOOGLE_CLIENT, GOOGLE_SECRET

1.  Go to OAuth consent screen, select External, and click Create to create an app.
2.  On the OAuth consent screen step, fill in the required fields, then save and continue.
3.  On the Scopes step, add the openid scope, then save and continue to complete the remaining steps.
4.  Go to [Credentials](https://console.cloud.google.com/apis/credentials) and obtain client ID and secret: 
    1.  Click Create credentials to select OAuth client ID.
    2.  In Application type, select Web application.
    3.  Provide an informative name for your application.
    4.  In Authorized redirect URIs, add the following URL:
        
        `https://<YOUR_DOMAIN_NAME>/api/auth/callback/google`
        
        Where <YOUR_DOMAIN_NAME> is the name of your Domain ex: example.com
        
        Use https:// if your installation is configured to use HTTPS.
        
    5.  Click Create.
    6.  Copy the client ID and secret that display and store them in a file.




# Email Service
### **EMAIL_FROM:**
email that will send the emails. ex: `Support@example.com`

### **EMAIL_SERVER_USER:**
email username. ex: `Support123

### **EMAIL_SERVER_PASSWORD:**
email password. ex: `Password123`

### **EMAIL_SERVICE:** 
The email server url, ex: `smtp.zoho.eu:465`
You need to follow a specific form `URL:PORT`.

