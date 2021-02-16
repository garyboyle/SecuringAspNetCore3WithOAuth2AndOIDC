# OpenID Connect

This is based on [Kevin Dockx's Securing ASP.NET Core 3 with OAuth 2 and OpenID Connect project](https://github.com/KevinDockx/SecuringAspNetCore3WithOAuth2AndOIDC).

A few tweaks were needed to get it to run on MacOS.

Namely the datasource had to change, as LocalDB is not support on MacOS.

An alternative db source can be created with the following command in Docker.

`docker run -e 'ACCEPT_EULA=Y' -e 'SA_PASSWORD=yourStrong(!)Password' -p 1433:1433 -d mcr.microsoft.com/mssql/server:2017-latest`

And then, in `appsettings.json` the `ImageGalleryDBConnectionString` value should be updated to `Server=localhost;Database=ImageGalleryDB;User Id=SA;Password=yourStrong(!)Password`

---

NOTE: Below is the original README.md contents

# Securing ASP.NET Core 3 with OAuth 2 and OpenID Connect

Fully functioning finished sample code for my Securing ASP.NET Core 3 with OAuth2 and OpenID Connect course. Make sure you start up / deploy the IDP, Client & API project when running the finished solution.

The accompanying course can be watched here: https://app.pluralsight.com/library/courses/securing-aspnet-core-3-oauth2-openid-connect/
