# thinternational
Tool to speed up translation of thinBasic scripts


## Setup your script for translation

1. Copy the file _I18N_helper.tbasicu_ to the same path as your main script
2. From _I18N_helper.tbasicu_ **copy** the part of code that is at the top and **paste** it in your main script
3. Uncomment it and make the adjustments you need (language selection).
4. Anywhere you need a _String_ translation, enclose it with _i18nh("your string to translate")_ or _i18nh("your string to translate","any comment to the translator")_


## Build translation file without thinAir integration
**Or see thinAir integration below.**

1. Open your main script in thinAir
2. Right click on the script TAB name
3. From the context menu, _**copy** file name to clipboard_
4. thinAir menu : Script\Command Line ...
5. Right click in the input bar and **paste** the path, then click _OK_
6. Run I18N.tbasic
7. In your main script folder, edit your xml file (I use Notepad++) to complete it with translations.

see thinternational _Sample_ folder fo example.


## thinAir integration (with bundling version)
**Or see thinAir integration without bundling below.**

1. Whithin thinAir build _I18N.tbasic_ to _I18N.exe_
2. Create folder _%thinBasic_Installation_Folder%\thinAir\Tools\thinternational_
3. Move _I18N.exe_ to _%thinBasic_Installation_Folder%\thinAir\Tools\thinternational\_
4. Edit  _%thinBasic_Installation_Folder%\thinAir\Tools\thinAir_Tools.ini_ and append the following section :
<pre>
[thinI18N]
Menu=thinternational
CommandLine=%thinAirinstallpath%\Tools\thinternational\I18N.exe %sourcecodefullpathname%
SaveScriptBefore=true
</pre>
5. Restart thinAir


## thinAir integration (without bundling version)

1. Create folder _%thinBasic_Installation_Folder%\thinAir\Tools\thinternational_
3. Move _I18N.tbasic_ to _%thinBasic_Installation_Folder%\thinAir\Tools\thinternational\_
4. Edit  _%thinBasic_Installation_Folder%\thinAir\Tools\thinAir_Tools.ini_ and append the following section :
<pre>
[thinI18N]
Menu=thinternational
CommandLine=%thinbasicinstallpath%\thinbasicc.exe "%thinAirinstallpath%\Tools\thinternational\i18N.tbasic " %sourcecodefullpathname%
SaveScriptBefore=true
</pre>
5. Restart thinAir


## translation-file building 

1. Open your main script in thinAir, stay on this tab.
2. thinAir menu : Tools\User Tools\thinternational
3. In your main script folder, edit your xml file (I use Notepad++) to complete it with translations.

