### Prerequisites ###

* The following steps will only work for Mac OS or Linux
* Download the following file and unzip to ~/volumes/ : https://www.dropbox.com/s/eh6u6uchd9syv24/data-portal.zip?dl=0

### Steps to start the application ###

Clone the repo and execute the following command from the root directory to start the application:

```docker-compose -f docker/app.yml up```

The above command will do the following:

* Launch Dremio, Postgres
* Create the following directories in your root folder to persist the data even if you delete the containers: 
    * ~/volumes/data-portal/postgresql/
    * ~/volumes/data-portal/dremio/  
* For Postgres:
    * Creates a database with the name postgres
    * Creates a user with username/password: postgres/postgres
    * Exposes the docker port to use your localhost port: 5432
* For Dremio:
    * Launches Dremio on http://localhost:9047/

