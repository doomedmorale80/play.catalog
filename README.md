# Play.Catalog
Play Economy Catalog microservice

## Create and publish the NuGet package
```powershell
$version="1.0.2"
$owner="dotnetmicroservices"
$gh_pat="[PAT HERE]"

dotnet pack src\Play.Catalog.Contracts\ --configuration Release -p:PackageVersion=$version -p:RepositoryUrl=https://github.com/$owner/play.catalog -o ..\packages

dotnet nuget push ..\packages\Play.Catalog.Contracts.$version.nupkg --api-key $gh_pat --source "github"
```