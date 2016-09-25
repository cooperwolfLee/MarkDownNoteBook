Replace <USER> with correct user name.

Replace <NEW_LOCATION_PATH> with desired location.
```bat
mklink /D "C:\Users\<USER>\AppData\Local\Google\Chrome\User Data"       "<NEW_LOCATION_PATH>\Google Chrome User Data"
mklink /D "C:\Users\<USER>\AppData\Roaming\Tencent\Logs"                "<NEW_LOCATION_PATH>\Tencnet Logs"
mklink /D "C:\Users\<USER>\AppData\Roaming\360safe\LiveUpdateLog"       "<NEW_LOCATION_PATH>\360 Logs"
mklink /D "C:\Users\<USER>\AppData\Roaming\360CloudUI"                  "<NEW_LOCATION_PATH>\360CloudUI"
mklink /D "C:\Users\<USER>\AppData\Roaming\360CloudWin"                 "<NEW_LOCATION_PATH>\360CloudWin"
mklink /D "C:\Users\<USER>\AppData\Roaming\baidu\BaiduYunGuanjia\users" "<NEW_LOCATION_PATH>\Baiduyun Users"
mklink /D "C:\Users\<USER>\AppData\Roaming\BaiduYunGuanjia"             "<NEW_LOCATION_PATH>\BaiduYunGuanjia"
mklink /D "C:\Users\<USER>\AppData\Local\115Chrome\User Data"           "<NEW_LOCATION_PATH>\115 Chrome User Data"
mklink /D "C:\Users\<USER>\AppData\Local\Mozilla\Firefox\Profiles"      "<NEW_LOCATION_PATH>\Firefox Profiles"
mklink /D "C:\Users\<USER>\AppData\Local\Google\Picasa2\db3"            "<NEW_LOCATION_PATH>\Google Picasa db3"
pause
```
