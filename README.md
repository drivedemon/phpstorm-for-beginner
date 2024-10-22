# WELCOME to ALL tooltip!

![Alt Text](https://media.giphy.com/media/v9bipbbqgOmCSSpPgl/giphy.gif)

## PHPSTORM TIPS

Download only version 2023.2.3

If you need to improve your coding tool try PHPSTORM :)

- free trial version all time for <b>WINDOW</b>
- PHPSTORM link: <a href="https://www.jetbrains.com/phpstorm/download/other.html">Download and selected version 2023.2.3</a>

### How to Re-trial PHPSTORM after 30day

- Create `retrial-script.bat` file and copy this code into file
- Or download via link: <a href="https://gist.github.com/rjescobar/4b7200d7b2274c029107ca8b9d02f3a3">ReTrial Script!</a>

```
REM Delete eval folder with licence key and options.xml which contains a reference to it
for %%I in ("WebStorm", "IntelliJ", "CLion", "Rider", "GoLand", "PhpStorm", "Resharper", "PyCharm") do (
    for /d %%a in ("%USERPROFILE%\.%%I*") do (
        rd /s /q "%%a/config/eval"
        del /q "%%a\config\options\other.xml"
    )
)

REM Delete registry key and jetbrains folder (not sure if needet but however)
rmdir /s /q "%APPDATA%\JetBrains"
reg delete "HKEY_CURRENT_USER\Software\JavaSoft" /f
```

### recommended plugin

- .env file support
- .ignore
- CSV
- ideolog
- laravel
- nyan progress bar (nyan nyan :3)
- CamelCase
- PHP annotations
- symfony support

## XDEBUG (PHPSTORM)

If you're still using debug like this => `dd()` `echo` `print_r`

And then you need something powerful and improve yourself just follow below.

### Step 1 (Download XDebug)

- get `phpinfo()` in your app
- open website and click `view page source`
- copy source and paste into > link <a href="https://xdebug.org/wizard">Xdebug detect version and download</a>

### Step 2 (Setup config in Server)

- after download `xdebug.dll` file copy and paste into folder `server\bin\php\your-php-version\ext`
- config xdebug in `php.ini`
```
    [XDebug]
    xdebug.remote_enable=1
    xdebug.mode=debug,develop
    xdebug.start_with_request=yes
    xdebug.discover_client_host=1
    xdebug.idekey=phpstorm
    xdebug.client_port=9003

    zend_extension="C:/laragon/bin/php/php-8.2.9-nts-Win32-vs16-x64/ext/php_xdebug.dll"
```

### Step 3 (Setup config in PHPSTORM)

- After done in server path then open `PHPSTORM` and go to right top near bug icon :3
- Click `Edit Configuration`
- Add `New Remote Debug`
- Checked `filter debug connection by IDE key`
- Add new Server in `3dot`
- Setup
  - Host `http://127.0.0.1`
  - Port `80`
  - Debugger `Xdebug`
- Checked and Added `Path Mapping` (mapping 3 path)
  - root project path
  - public path
  - index file inside public folder
- Add IDE Key session `PHPSTORM`

## Done! let start deBuggg :)

## CLEANCODE

improve your code style to readable and easier to maintain

for advance level after you finished clean code concept and more.

- basic clean code blog V1: <a href="https://medium.com/design-microservices-architecture-with-patterns/clean-architecture-with-dependency-rule-dff96d479a60">medium</a>
- basic clean code blog V2: <a href="https://www.saladpuk.com/basic/clean-code">saladpuk</a>
- solid principles (OOP): <a href="https://www.freecodecamp.org/news/solid-principles-explained-in-plain-english/">solid principles</a>
- solid principles TH Ver: <a href="https://nobrain.codes/solid-principles-%E0%B8%84%E0%B8%B7%E0%B8%AD%E0%B8%AD%E0%B8%B0%E0%B9%84%E0%B8%A3/">solid thai version</a>
- adapter pattern blog: <a href="https://www.saladpuk.com/beginner-1/design-patterns/structural/adapter-pattern">saladpuk</a>

## Shortcut for PHPSTORM (window)

### Everyday used and help you to improve and funny

```
ctrl + C = copy
ctrl + V = paste
ctrl + shift + N = open file
ctrl + F = search in file
ctrl + shift + F = search all
ctrl + R = search and replace
ctrl + shift + R = search and replace all
ctrl + E = open current file
ctrl + W = close current file
ctrl + G = go to line
ctrl + D = duplicate line
alt + Backspace = delete current line
ctrl + left click = go to base function (link index to base)
=====================
ctrl + alt + L = auto reformat code
ctrl + alt + shift + L = setup config reformat code
alt + J = find and selection for next occurrence
alt + shift + J = unselection from next occurrence
ctrl + alt + shift + J = find and selection for all occurrence
alt + -> = move to right file
alt + <- = move to left file
=====================
alt + shift + U = Reformat to camel/snake case (require CamelCase plugin)
```