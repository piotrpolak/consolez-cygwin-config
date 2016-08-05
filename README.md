ConsoleZ custom config
========================================================================================================================

Sets shell to Cygwin Bash `C:\cygwin64\bin\bash.exe -i -l`.

Installing ConsoleZ from Cygwin
------------------------------------------------------------------------------------------------------------------------
First make sure `unzip` is available in your system.

```
echo "Downloading ConzoleZ..." && \
lynx -source https://github.com/cbucher/console/releases/download/1.17.0/ConsoleZ.x64.1.17.0.16129.zip > /cygdrive/c/cygwin64/tmp/ConsoleZ.zip && \
mkdir -p /cygdrive/c/cygwin64/ConsoleZ && \
echo "Downloading ConzoleZ custom config..." && \
lynx -source https://github.com/piotrpolak/consolez-cygwin-config/archive/master.zip > /cygdrive/c/cygwin64/tmp/consolez-cygwin-config.zip && \
echo "Unpacking ConzoleZ..." && \
unzip /cygdrive/c/cygwin64/tmp/ConsoleZ.zip -d /cygdrive/c/cygwin64/ConsoleZ && \
echo "Unpacking ConzoleZ custom config..." && \
unzip  -p /cygdrive/c/cygwin64/tmp/consolez-cygwin-config.zip consolez-cygwin-config-master/console.xml > /cygdrive/c/cygwin64/ConsoleZ/console.xml && \
unlink /cygdrive/c/cygwin64/tmp/ConsoleZ.zip && \
unlink /cygdrive/c/cygwin64/tmp/consolez-cygwin-config.zip && \
echo "Cleaning up and setting permissions" && \
chmod u+x /cygdrive/c/cygwin64/ConsoleZ/*.exe && \
chmod u+x /cygdrive/c/cygwin64/ConsoleZ/*.dll && \
echo "Done! /cygdrive/c/cygwin64/ConsoleZ/Console.exe is ready to be used! You can pin it to your taskbar!"
```

Changes comparing to the original config
------------------------------------------------------------------------------------------------------------------------

* removed shortcuts that conflict with the default UNIX shortcuts (like `CTRL+C`, `CTRL+R`)
* removed window decorators
* enabled copy text on selecting

Changed shortcuts
------------------------------------------------------------------------------------------------------------------------

* `CTRL+S` - settings
* `CTRL+SHIFT+C` - copy
* `CTRL+SHIFT+V` - paste
* `CTRL+T` - new tab
* `CTRL+SHIFT+R` - rename tab
* `SHIFT+LEFT` - select text left
* `SHIFT+RIGTH` - select text right
* `CTRL+F` - find text
* `CTRL+SHIFT+F` - find text new
* `ALT+CTR+T` - activates ConsoleZ (must be running)

Other useful shortcuts
------------------------------------------------------------------------------------------------------------------------

Those are predefined in the default ConsoleZ config. To see all of the shortcuts use `CTRL+S` to open settings dialog.

* `CTRL+TAB` - switch to next tab
* `CTRL+SHIFT+TAB` - switch to previous tab
* `CTRL+W` - close tab
* `ALT+F4` - close ConsoleZ
* `CTRL+SHIFT+O` - split console horizontally
* `CTRL+SHIFT+E` - split console vertically
* `CTRL*SHIFT+W` - close current view
