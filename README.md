# WRAPT

[Wrapt](https://wrapt.dev/) Is a scaffolding tooling that from configuration scaffolds web api infrastructure and code.

Install the Craftsman tool globally. Make sure to close your powershell/command prompt/terminal windows after your initial install!
```
PS C:\> dotnet tool install -g craftsman
PS C:\> craftsman -h
PS C:\> craftsman -h  
USAGE:
    craftsman [OPTIONS] <COMMAND>

EXAMPLES:
    craftsman new domain my\file\path.yaml
    craftsman new domain my\file\path.yml
    craftsman new domain my\file\path.json
    craftsman new example
    craftsman new example MyProjectName

OPTIONS:
    -h, --help       Prints help information
    -v, --version    Prints version information

COMMANDS:
    new
    add
    register
```

Scaffolding has limited Providers:
- SqlServer
- Postgres
- MySQL (Coming Soon)

```
dotnet new example Basic
cd .\Basic\
docker-compose up --basic
cd .\Basic\RecipeManagement\src\RecipeManagement
dotnet run
cd .\Basic\RecipeManagement\
craftsman new entity ..\..\ingredient.yaml
cd .\src\RecipeManagement
dotnet ef database update
dotnet run
```