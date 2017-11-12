# getting-unicode-characters-work-7-5-windows-2008-R2
-------------------------------------------------------
When trying to get Greek characters to work on IIS7.5 on windows server 2008 I initially thought it would be tricky. In the end is was as simple as running the following command in an elevated command prompt.
reg add HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\w3svc\Parameters /v FastCGIUtf8ServerVariables /t REG_MULTI_SZ /d REQUEST_URI&#92;&#48;PATH_INFO

As soon as you get the "Operation Completed Successfully" message. Just run iisreset.
Related post here: https://www.georgenicolaou.me/getting-unicode-characters-work-7-5-windows-2008-r2/
