# TabSorter2
Google Chrome Tab Management Extension - Merge, Sort, split and more :)

- Merge
   - merges all windows
- Sort
   - sort tabs by domain and titles
   - can sort all windows or just a single one
- Split
   - splits a window in 2
- Shuffle
   - will shuffle the tabs within the current window  (it's just fun xD)
- Save 
   - save current window to a text file
   - links are shortened using google URL Shortener 
   - the file content is sorted by page title
- Deduplicate
  - remove deplicate open url tabs from current windo

### Preview 

![Alt text](/tabSorter2.png?raw=true "Optional Title")

### Build quirks
 -> problem css imports ignored
   -> it's gulp-clean-css@2.4.x fault [fix Here](https://github.com/opensensorhub/osh-js/issues/36)
