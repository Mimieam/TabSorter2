# TabSorter2 - Enhancing your browsing experience 1 click at a time
>
<br>

### This page is to explain which permissions are used and why

```json
{
  "permissions": [
    "tabs",
    "tabGroups",
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
  - **Usage**: used to access the tabs' URL and title for sorting, saving, and some internal filtering
  - **Details**:  https://developer.chrome.com/extensions/tabs

<br>

TabGroups:
  - **Usage**: used to support automatically creating a group for multiple tabs of the same domain
  - **Details**:  [https://developer.chrome.com/extensions/tabs](https://developer.chrome.com/docs/extensions/reference/api/tabGroup)


Storage:
  - **Usage**: used to access the storage used for saving/restoring the state of the extension
  - **Details**: https://developer.chrome.com/extensions/storage

<br>

System.display:
  - **Usage**: used to access the screen dimensions, used to split and stack the windows
  - **Details**: https://developer.chrome.com/extensions/system_display

<br>

Alarms:
  - **Usage**: used to implement an auto discard functionality checking if a tab has been opened for more than 45 minutes and discarding it from memory
  - **details**: https://developer.chrome.com/extensions/alarms

<br>

Downloads:
  - **Usage**: Enables downloading of saved files from the browser.
  - **Details**: https://developer.chrome.com/extensions/downloads

<br>

Host_permissions:
  - **Usage**: used to access the public suffix list, used internally for parsing tabs URL and determine the subdomain, domain, and tld (top-level domain... i.e: .com, .co.uk .org .ci)
  - **Details**: When installing/updating the extension will download the public suffix list from https://publicsuffix.org/list/public_suffix_list.dat and store it.
  This list is used to parse the domain of a tab.

    >**basic use case**:
    >- If you open a tab with the url https://www.google.com/ the parser will return the domain `google.com`
    >- however for like `https://www.google.co.uk` the parser will return `co.uk` as domain which is wrong. the public suffix list is used to correct that.
