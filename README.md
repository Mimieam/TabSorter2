# TabSorter2
Google Chrome Tab Management Extension - Merge, Sort, split and more :)

- Merge
   - merges all windows
- Sort
   - sort tabs by domain and titles
   - can sort all windows or just a single one
   - configurable in option window
- Split
   - splits a window in 2 ( by default )
   - can be change to 3 or 4 in option window (**new**)
   - windows can be seen side by side if the option is checked (**new**)
- Shuffle
   - will shuffle the tabs within the current window  (it's just fun xD)
- Save 
   - save current window to a text file
   - links are shortened using google URL Shortener 
   - the file content is sorted by page title
- Deduplicate
  - remove deplicate open url tabs from current window
- Options (**new**)
  - open the extension option window
  - options need to be saved to persist

### Preview 

![Popup](/tabSorter2.png?raw=true "Popup view")
![Options](/tabSorter2-options.png?raw=true "Option view")
### Build quirks
 -> problem css imports ignored
   -> it's gulp-clean-css@2.4.x fault [fix Here](https://github.com/opensensorhub/osh-js/issues/36)

### TODO:
  - <s> Automatically suspend tab after a configurable delay to save memory ?? </s>
  - <s> Isolate a single domain in a separate windows </s>
  - <s> Unite - bring all tabs of a domain in the same current window </s>
  - <s> Close a domain </s>
  - <s> Backward compatible loading of previously saved Tabs </s>  **YASSS !!!**
  - Upgrade split function to split left on current tab  - split Here
  - Stress test split function and memory management
  - Freeze - (Discard) remove all tabs in current window from memory but leaves the tab visible in the browser
