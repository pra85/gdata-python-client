# Sample #

This short sample will create a new Google Spreadsheet after you have authenticated using AuthSub.

```
import gdata.spreadsheet.text_db

client = gdata.spreadsheet.text_db.DatabaseClient()
auth_url = client._GetDocsClient().GenerateAuthSubURL(next=YOUR_WEB_APPS_URL,
    scope='http://spreadsheets.google.com/feeds/ http://docs.google.com/feeds/documents/')
```

The page listed as `YOUR_WEB_APPS_URL` will need to examine it's URL and extract the value from the 'token' URL parameter.

```
client._GetDocsClient().SetAuthSubToken(token)
client._GetDocsClient().UpgradeToSessionToken()
client._GetSpreadsheetsClient().SetAuthSubToken(client._GetDocsClient().GetAuthSubToken())

db = client.CreateDatabase('google_spreadsheets_db auth sub test')
```