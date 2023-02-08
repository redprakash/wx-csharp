## API Versioning
### Creae a version.json file in the project
            {
                    "version": "1.0",
                    "publicReleaseRefSpec": [
                      "^refs/heads/main$",
                      "^refs/heads/rel/v\\d+(?:\\.\\d+)?$"
                    ],
                    "nugetPackageVersion": {
                      "semVer": 2
                    }
               }
       
  ### Use the Nerd.GitVersioning Nuget Package
            <PackageReference Include="Nerdbank.GitVersioning" Version="3.5.119">
		           <PrivateAssets>all</PrivateAssets>
		           <IncludeAssets>runtime; build; native; contentfiles; analyzers; buildtransitive</IncludeAssets>
		        </PackageReference>
            
   ### If error of deptha
           steps:
            - checkout: self
              clean: true
              fetchDepth: 0
