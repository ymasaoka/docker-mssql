# docker-mssql
Install Microsoft SQL Server on Docker by Docker Compose.  
Official Microsoft repository for SQL Server in Docker resources is [here](https://github.com/Microsoft/mssql-docker).

# How to use

1. **Clone this repository** to a directory of your choice.  
1. Move to the **docker-mssql** directory.  
1. Execute the following command to start the container.  

    ```bash
    docker compose up -d
    ```

1. Run the following command to confirm that the container has started.  

    ```bash
    docker compose ps
    ```

# Login to SQL Server
You can use **SSMS** (SQL Server Managemet Studio) or **ADS** (Azure Data Studio) to log in to the Docker container.  
You can also use `docker` command to log-in to the container and run **sqlcmd**.  
    
```bash
docker exec -it <your-container-id> "bash"
/opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P "<YourNewStrong@Passw0rd>"
```

> You can check the container ID with the `docker ps` command.

For more information on connecting to SQL Server on Docker using sqlcmd, see [here](https://docs.microsoft.com/en-us/sql/linux/quickstart-install-connect-docker?view=sql-server-ver15&pivots=cs1-bash).  