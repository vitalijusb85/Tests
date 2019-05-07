#Depending on the operating system of the host machines(s) that will build or run the containers, the image specified in the FROM statement may need to be changed.
#For more information, please see https://aka.ms/containercompatm

 # Sample contents of Dockerfile
 # Stage 1
FROM microsoft/dotnet:sdk AS build-env
WORKDIR /source

 # caches restore result by copying csproj file separately
COPY *.csproj .
RUN dotnet restore "Test.csproj"

 # copies the rest of your code
 COPY . .
 RUN dotnet publish --output /app/ --configuration Release

 # Stage 2

FROM microsoft/dotnet:aspnetcore-runtime
WORKDIR /app

COPY --from=build-env /app .
ENTRYPOINT ["dotnet", "Test.dll"]

