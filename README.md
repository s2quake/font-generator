# font-generator

FreeType Based Font Texture Generator

![main](./image01.png)

![preview](./image02.png)

## Development Environment

[Microsoft Visual Studio Code](https://code.visualstudio.com/) or [Microsoft Visual Studio Community 2019](https://visualstudio.microsoft.com/ko/downloads/)

[.NET Core 3.1 SDK](https://dotnet.microsoft.com/download/dotnet-core/3.1)

## Clone

```console
git clone https://github.com/s2quake/font-generator.git --recursive
```

## Build

### Windows

```console
dotnet build --framework netcoreapp3.1 --configuration Release
```

### macOS or Linux

Because you cannot build a WPF project in a Linux environment, select and build only the console project.

```console
dotnet build ./JSSoft.Fonts/JSSoft.Fonts.ConsoleHost --framework netcoreapp3.1 --configuration Release
```

## Run

### Application(Windows Only)

```console
dotnet run --project ./JSSoft.Fonts/JSSoft.Fonts.ApplicationHost --framework netcoreapp3.1 --configuration Release
```

or

```console
dotnet ./exe/Release/netcoreapp3.1/application/jsfontApp.dll
```

### Console

```console
dotnet run --project ./JSSoft.Fonts/JSSoft.Fonts.ConsoleHost --framework netcoreapp3.1 --configuration Release
```

or

```console
dotnet ./exe/Release/netcoreapp3.1/console/jsfont.dll
```

## Export Font Data and Textures

### Usage

```console
dotnet jsfont.dll <font-path> <output-path>
```

### Requirements

font-path

```plain
Indicates the font path.
```

output-path

```plain
Indicates the output path.
If no output path is specified, the font information is output.

If the output path is a directory, the file is automatically named based on the font name.
```

### Options

--characters 'value'

```plain
Indicates the Unicode of the character you want to export.
expressed in decimal or hexadecimal form, each character is separated by ','
You can use '-' to specify multiple characters.
e.g. "65, 0x41, 66-90, 0x61-0x7A"

If no value is specified, export all characters.
```

--dpi 'value'

```plain
Indicates the DPI of the font. The default value is 72.
```

--size 'value'

```plain
Indicates the size of the font. The default value is 26.
```

--face 'value'

```plain
Indicates the type of font. The default value is 0.
```

--texture-width 'value'

```plain
Indicates the width of the texture to be printed. The default value is 512.
```

--texture-height 'value'

```plain
Indicates the height of the texture to be output. The default value is 512.
```

--padding 'value'

```plain
Indicates the padding of the character. 
You can set the value for both sides. The default value is 1.
    e.g. 1) --padding 1 sets all padding to 1.
    e.g. 2) --padding "1, 2" sets the left and right padding to 1 and the top and bottom padding to 2.
    e.g. 3) --padding "1 1 0 0" sets left to 1, top to right to 0 and bottom to 0.
```

--spacing 'value'

```plain
Indicates the gap between the character and characters.
You can set horizontal and vertical values. The default value is 1.
    e.g. 1) --spacing 1 sets the horizontal and vertical spacing to 1.
    e.g. 2) --spacing "1 0" sets only the horizontal interval to 1.
```
