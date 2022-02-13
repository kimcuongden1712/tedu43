wsl
cd /
docker ps


docker run --name sqlserver --hostname sqlserver -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=Admin@123$" -p 1433:1433 -d mcr.microsoft.com/mssql/server:2019-latest

docker run -d --name mongodb -e MONGO_INITDB_ROOT_USERNAME=mongoadmin -e MONGO_INITDB_ROOT_PASSWORD=Admin@123$ -p 127.0.0.1:27017:27017 mongo

#Create solution with CLI
dotnet new sln
dotnet new webapi/classlib -o <OUTPUT_DIRECTORY>

--create xunit
dotnet new xunit -o <OUTPUT_DIRECTORY>

--Add project to sln solution
dotnet sln add <Project.csproj_DIRECTORY> --solution-folder <OUTPUT_DIRECTORY>

--Run build
dotnet build
