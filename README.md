# TestePratico

<b> 1. Docker </b>

docker pull mcr.microsoft.com/mssql/server
docker run -v ~/docker --name sql_hml_testepratico -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=1q2w3e4r@#$" -p 1433:1433 -d mcr.microsoft.com/mssql/server

<b> 2. Após a criação da instância do docker, será necessário criar a database que será utilizada no projeto. </b>

sqlcmd -S [endereco banco] -U sa
create Database hml_testepratico_sqlserver_br
select name from sys.databases

<b> 3. Referências </b>

dotnet add package Microsoft.EntityFrameworkCore.SqlServer
dotnet add package Microsoft.EntityFrameWorkCore.Design
