# Indentity Server 4

## IdentityServer4 Projects Templates

> https://github.com/IdentityServer/IdentityServer4.Templates

* Installation
```powershell
dotnet new install identityserver4.templates
```

* Verify
```powershell
dotnet new list is
```

If you need to set back your dotnet new list to "factory defaults", use this command:
```powershell
dotnet new --debug:reinit
```


## Create In Memory Demo Project

```powershell
mkdir identity-server-demo
cd identity-server-demo

dotnet new sln --name IdentityServer4Demo
dotnet new -o InMemDemo is4inmem
dotnet sln IdentityServer4Demo.sln add InMemDemo/InMemDemo.csproj
```
