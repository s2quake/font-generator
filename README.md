# font-generator

FreeType Based Font Texture Generator

![main](./image01.png)

![preview](./image02.png)

## Development Environment

[Microsoft Visual Studio Code](https://code.visualstudio.com/) or [Microsoft Visual Studio Community 2019](https://visualstudio.microsoft.com/ko/downloads/)

[.NET Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core/3.1)

## Clone

```powershell
git clone https://github.com/s2quake/font-generator.git --recursive
```

## Build

### Windows

```powershell
dotnet build --framework netcoreapp3.1 --configuration Release
```

### macOS or Linux

Because you cannot build a WPF project in a Linux environment, select and build only the console project.

```powershell
dotnet build ./JSSoft.Fonts/JSSoft.Fonts.ConsoleHost --framework netcoreapp3.1 --configuration Release
```

## Run

### Application(Windows Only)

```powershell
dotnet run --project ./JSSoft.Fonts/JSSoft.Fonts.ApplicationHost --framework netcoreapp3.1 --configuration Release
```

or

```powershell
dotnet ./exe/Release/netcoreapp3.1/application/jsfontApp.dll
```

### Console

```powershell
dotnet run --project ./JSSoft.Fonts/JSSoft.Fonts.ConsoleHost --framework netcoreapp3.1 --configuration Release
```

or

```powershell
dotnet ./exe/Release/netcoreapp3.1/console/jsfont.dll
```

### Export Font Data and Textures

```powershell
dotnet jsfont.dll <font-path> <output-path>
```
