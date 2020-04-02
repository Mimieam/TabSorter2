# TabSorter2

A Tab Manager for Google Chrome; Merge, Sort, Split, and More :)

- Merge
  - merges all windows
- Sort
  - sort tabs by domain and titles
  - can sort all windows or just a single one
  - configurable in option window
- Split
  - splits a window in 2 ( by default )
  - can be change to 3 or 4 in option window
  - windows can be seen side by side if the option is checked
- Split by Domain (**new**)
- Shuffle
  - will shuffle the tabs within the current window  (it's just fun xD)
- Unite (**new**)
  - bring all the tabs of a domain together at the most right of the current window
- Isolate (**new**)
  - extract all tabs of a domain into a new window
- Freeze (**new**)
  - Discard all open tabs to save on memory - **all pages will turn blank**
  - pages will remain open in your browser
- Close (**new**)
  - Closes all tabs under a domain
  - multiple subdomain are not currently supported
- Save
  - save current window to a text file
  - links are shortened using google URL Shortener
  - the file content is sorted by page title
- Load (**new**)
  - loads all the tabs previously saved in one new window and automatically freeze them
  - backward compatible
  - will load up to 2mb
- Deduplicate
  - remove deplicate open url tabs from current window
- Options
  - open the extension option window
  - options need to be saved to persist

## Preview
### --New v1.1--

![Popup 1.1](/preview_v1.1.png?raw=true "Popup view")


### --Old v0.1~0.5--
![Popup](/tabSorter2.png?raw=true "Popup view")
![Options](/tabSorter2-options.png?raw=true "Option view")

## Build quirks
 - build moved to webpack :) 
 
## Versions

### Ideas and Enhancements - TODO: v1.2.0

  #### HARD and Experimental ...
  - [ ] Undo any steps (partially implemented) 
  - [ ] Alarm mode - a tab will become active and focused after some times- ... ( done - not added)
  #### new features
  - [ ] Add support for shotcuts 
  - [ ] Save current tab to Clipboard - ( sometimes we just want to copy all the url and not save them first 🤷🏾‍♂️ )
  
  #### update to existing features
  - [ ] ignore on merge - TS2 will ignore specific URLS on merge
  - [ ] Create integration test
  - [ ] revisit Deduplicate & ignore after delimiter
  - [ ] ignore params after special characters - #,& ( expected to affect - sorting, deduplicating)
  #### bug fixes
  - [ ] improve handling of pinned_tabs


###  v1.1.0 - WIP  - 01/05/2020 
  - v0.0.6 - Abandoned due to a change in chrome API - 08/21/2019
  - [x] complete redesign and refactoring
  
#### Options Window
  - [x] Improve sorting - add options to sort by regex pattern and parameters
  - [x] Upgrade split function to split left on current tab  - split Here
  - [x] auto sort tabs - sort as they are loaded


#### Main Background
  - [x] added support for subdomain - thanks to [publicsuffix.org](https://publicsuffix.org/list/public_suffix_list.dat)
  - [x] Make loadfile backward compatible

  - [x] useActive* function on start
  - [x] split backgroundjs
  - [x] Save pinned tabs
  - [x] Transfer pinned tabs on-close
  - [x] Ignore pinned tabs onClose
  
  - [x] Add Support for pinned Tabs ( this was suprisingly complicated 😅)
  - [x] Sort and pin tab separatly
  - [x] Merge the last 2 windows
  - [x] Subdomain subsorting - WIP
  - [x] Options to automatically sort the tabs by title
  - [x] Search my tabs ( 😁 - idk yet how it gonna happen lol ) (*Done but not added to TS2*)
  - [x] Improve the design :)

### v0.0.5 - 06/22/18 - Added new features and improved icon for visibility

- fixed windows id bug on split
- added tab recycling
- [x] Options to automatically sort the tabs by title
- [x] Isolate a single domain in a separate windows
- [x] Unite - bring all tabs of a domain in the same current window ~~
- [x] Close a domain
- [x] Backward compatible loading of previously saved Tabs **YASSS !!!**
- [x] Stress test split function and memory management
- [x] Freeze - (Discard) remove all tabs in current window from memory but leaves the tab visible in the browser

v0.0.4 - 09/18/17 - Completed the Option page with support for side by side split

v0.0.3 - 04/08/17 - Updated UI - added Save & Deduplicate

v0.0.2 - 03/23/17 - Fixed initialization issue.

v0.0.1 - 03/23/17 - Merge/split/shuffle functionality added.
