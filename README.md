sanji-message
=============
規範 sanji bundle message 格式。message json 紀錄所有的 message code


範例說明：
Bundle 若要發出 event message 請參照以下格式

``` javascript
{
    "i18n": "LOGIN_SUCCESS",
    "message": "admin@mox.com login successfully",
    "type": "event",
    "variables": {
       "name": "admin@moxa.com"
    }
}

{
    "i18n": "LOGIN_FAIL",
    "message": "Login fail",
    "type": "alram"
}
```
注意：若訊息沒有變數的話就不會有 `variables` 屬性

格式說明：
<table border="1">
 <tr>
  <td>Property name</td>
  <td>Type</td>
  <td>Note</td>
 </tr>
 <tr>
  <td>i18n</td>
  <td>String</td>
  <td>For web i18n code</td>
 </tr>
 <tr>
  <td>type</td>
  <td>String</td>
  <td>This value could be 'event' and 'alram'</td>
 </tr>
 <tr>
  <td>message</td>
  <td>String</td>
  <td>Fallback message.</td>
 </tr>
 <tr>
  <td>variables</td>
  <td>Object</td>
  <td>For message contains variable.</td>
 </tr>
</table>

Frimware:
``` javascript
{
    "i18n": "FW_UPGRADING",
    "message": "Device cg-123456789715 is upgrading.",
    "type": "event",
    "variables": {
       "id": "cg-123456789715"
    }
}

{
    "i18n": "FW_UPGRADE_SUCCESS",
    "message": "Device cg-123456789715 upgrades successfully.",
    "type": "event",
    "variables": {
       "id": "cg-123456789715"
    }
}

{
    "i18n": "FW_UPGRADE_FAIL",
    "message": "Device cg-123456789715 upgrades fail.",
    "type": "alarm",
    "variables": {
       "id": "cg-123456789715"
    }
}
```

Reboot:
``` javascript
{
    "i18n": "REBOOTING",
    "message": "Device cg-123456789715 is rebooting.",
    "type": "event",
    "variables": {
       "id": "cg-123456789715"
    }
}

{
    "i18n": "REBOOT_SUCCESS",
    "message": "Device cg-123456789715 reboots successfully.",
    "type": "event",
    "variables": {
       "id": "cg-123456789715"
    }
}

{
    "i18n": "REBOOT_FAIL",
    "message": "Device cg-123456789715 reboots fail.",
    "type": "alarm",
    "variables": {
       "id": "cg-123456789715"
    }
}
```
