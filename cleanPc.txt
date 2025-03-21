@echo off
echo This will clean temporary files without deleting files in use.

:: Cleaning Windows Temp
for %%F in ("C:\Windows\Temp\*.*") do (
    del /q "%%F" 2>nul
)
for /d %%D in ("C:\Windows\Temp\*") do (
    rd /s /q "%%D" 2>nul
)

:: Cleaning Local Temp
for %%F in ("C:\Users\adelr\AppData\Local\Temp\*.*") do (
    del /q "%%F" 2>nul
)
for /d %%D in ("C:\Users\adelr\AppData\Local\Temp\*") do (
    rd /s /q "%%D" 2>nul
)

:: Cleaning Roaming Temp
for %%F in ("C:\Users\adelr\AppData\Roaming\Temp\*.*") do (
    del /q "%%F" 2>nul
)
for /d %%D in ("C:\Users\adelr\AppData\Roaming\Temp\*") do (
    rd /s /q "%%D" 2>nul
)

:: Cleaning Internet Cache
for %%F in ("C:\Users\adelr\AppData\Local\Microsoft\Windows\INetCache\*.*") do (
    del /q "%%F" 2>nul
)
for /d %%D in ("C:\Users\adelr\AppData\Local\Microsoft\Windows\INetCache\*") do (
    rd /s /q "%%D" 2>nul
)

echo Cleanup completed.
