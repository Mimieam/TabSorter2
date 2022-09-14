# TabSorter2 - Enhancing your browsing experience 1 click at a time
>
<br>

### This page is to explain which permissions are used and why

```json
{
  "permissions": [
    "tabs",
    "storage",
    "system.display",
    "alarms"
  ],
  "optional_permissions": [
    "downloads"
  ],
  "host_permissions": [
    "https://publicsuffix.org/*"
  ]
}
```


Tabs:
  - **usage**: used to access the tabs url and title for the purpose of sorting, saving and some internal filtering
  - **details**:  https://developer.chrome.com/extensions/tabs

<br>

Storage:
  - **usage**: used to access to the storage used for saving/restoring the state of the extension
  - **details**: https://developer.chrome.com/extensions/storage

<br>

System.display:
  - **usage**: used to access the screen dimensions, used for the purpose of splitting and stacking the windows
  - **details**: https://developer.chrome.com/extensions/system_display

<br>

Alarms:
  - **usage**: used to implement an auto discard functionality checking if a tab has been opened for more than 45 minute and discarding it from memory
  - **details**: https://developer.chrome.com/extensions/alarms

<br>

Downloads:
  - **usage**: Enables downloading of saved file from the browser.
  - **details**: https://developer.chrome.com/extensions/downloads

<br>

Host_permissions:
  - **usage**: used to access the public suffix list, used internally for parsing tabs url and determine the subdomain, domain and tld (top level domain... i.e: .com, .co.uk .org .ci)
  - **details**: When installing/updating the extension will download the public suffix list from https://publicsuffix.org/list/public_suffix_list.dat and store it.
  This list is used to parse the domain of a tab.

    >**basic use case**:
    >- If you open a tab with the url https://www.google.com/ the parser will return the domain `google.com`
    >- however for like `https://www.google.co.uk` the parser will return `co.uk` as domain which is wrong. the public suffix list is used to correct that.
