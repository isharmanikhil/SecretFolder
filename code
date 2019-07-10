cls

@ECHO OFF

title Security

if EXIST "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" goto UNLOCK

if NOT EXIST UNKNOWN goto MDUNKNOWN

:CONFIRM

echo Are you sure you would like to lock this folder? (Y/N)

set/p "cho=>"

if %cho%==Y goto LOCK

if %cho%==y goto LOCK

if %cho%==N goto END

if %cho%==n goto END

echo Invalid Choice.

goto CONFIRM

:LOCK

ren UNKNOWN "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"

attrib +h +s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"

echo Folder Locked.

goto End

:UNLOCK

echo Enter password to Unlock your Secure Folder

set/p "pass=>"

if NOT %pass%== sharma goto FAIL

attrib -h -s "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}"

ren "Control Panel.{21EC2020-3AEA-1069-A2DD-08002B30309D}" UNKNOWN

echo Folder Successfully Unlocked.

goto End

:FAIL

echo Invalid Password.

goto End

:MDUNKNOWN

md UNKNOWN

echo UNKNOWN created successfully

goto End

:END
