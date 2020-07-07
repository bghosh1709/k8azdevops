FROM mcr.microsoft.com/dotnet/core/aspnet:2.2-stretch-slim
WORKDIR /app

# This will take the artifacts from the publish step (dotnet publish -c Release)
# from before, and copy it into the root folder of this docker container. This means
# we now have everything we need to run the image
COPY ["./aspnet-core-dotnet-core/build", "."]

# As we're running a web-server
# we'd like docker to listen for traffic on port 80 (for http) and port 443 (for https) 
EXPOSE 80
EXPOSE 443

# Run command
ENTRYPOINT ["dotnet", "aspnet-core-dotnet-core.dll"]
