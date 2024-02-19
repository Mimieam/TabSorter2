# TabSorter2 - Enhancing your browsing experience 1 click at a time
>
<br>

Welcome to TabSorter2, the Browser extension that helps you sort, merge, and manage your tabs intuitively.

<div markdown="1" style="text-align:center">
<img width="1273" alt="image" src="https://user-images.githubusercontent.com/834291/176143064-f3060618-94fb-4950-83e0-17ec6481ed42.png">
</div>

##### New Website - [TabSorter2.com](https://www.TabSorter2.com)

###### [Features Documentation](Documentation.md)
###### [Permissions Documentation](Permission.md)


#### *Disclaimer: I'm still not a Designer 😅, but I've learned a thing or two over the past few years of working on TabSorter2 and I still welcome feedbacks – please be nice 🙂*


<br>

## New Direction

First of, I would like to thank you all for the love and support, from all your emails and comments! I really wish I could have kept working on TS2 for free, but as the past few years have shown, that isn't sustainable anymore.

>So starting with version 2.0.0, TabSorter2 will be a subscription-based extension following a freemium model.


What was once a little weekend project 6 years ago has turned into a daily commitment with little to no rewards. Don't get me wrong, I truly love working on TS2, especially coming up with fun new features to enhance the browsing experience. I have plans for many new features, options, and enhancements on the [Roadmap] and strongly desire to bring TS2 to other browsers! In short, I want to focus on that without worries of becoming homeless 😅


And if I've learned anything from migrating to Manifest... massive, free refactoring work doesn't pay the bills 🤷🏾‍♂️

So what can you expect with **TabSorter2 v2.0.0**?
- The basic core features, **Merge/Sort/Shuffle/Save/Load** along with bug fixes/security updates, will remain **free forever for everyone**
- The advanced and experimental features will require a small monthly payment of $4.99 to enjoy.

My hope is that with your continuous support, I will be able to keep on improving TS2 and release new features every ever 2 to 3 months (I do have a long list of new features as well as other productivity extensions... [WsL](https://chrome.google.com/webstore/detail/workspacelive/dlobignndchnmiaeeoldclglifpbdojo)👀.

<br>

## Roadmap / Backlog

#### **Suggestions:**
  - [ ] Add support for context Menu
  - [ ] Save current tab to Clipboard - (sometimes we might want to copy all the url and not save them first 🤷🏾‍♂️)
  - [x] enhance sort function
  - [ ] ignore on merge - TS2 will ignore specific URLS when merging all windows
  - [x] revisit Deduplicate & ignore after delimiter
  - [ ] <s>Add a whitelist to prevent deduplicating on specifics URLs</s>
  - [ ] ignore params after special characters - #,& ( expected to affect - sorting, deduplicating)
  - [x] Optional sorting on pinned tabs
  - [ ] deduplicate on all windows not just the current one
  - [ ] Welcome page / Wiki and Documentation
  - [x] Safari and Mozilla experimentation

#### **Enhancements:**
  - [ ] add behavioral options to remove redundant all/current buttons?
  - [ ] Undo last 2 action

#### **Wild Ideas:**
These are some ideas that I have been thinking about, but have yet to figure out their feasibility and if they are worth investing dev time.
  - [ ] split in multiple layout patterns.. e.i: 3x1, 4*4
  - [ ] add Group support to sorting/merging/split
  - [x] save and reload tab groups (the tabGroup API isn't sorting friendly...)
  - [ ] user defined functionalities?


<br>

## Version History
**[v2.3.0]** WIP(https://github.com/Mimieam/TabSorter2/discussions/42) by priorities
- tab group
- auto close
- session page
- undo

#
**[v2.2.12]** - 04/08/2023
* Fixed deploy Incident.
* updated webpack prod build 

#
**[v2.2.8]** - 03/31/2023
* Hotfix for version 2.2.0 - a file got ignored by the new packaging system, resulting in the app not working.

#
**[v2.2.0] (https://github.com/Mimieam/TabSorter2/discussions/35)** -  [Released](https://github.com/Mimieam/TabSorter2/projects/5) - 03/30/2023

#### **Added/Done:**
  * [x] Free trials of all features
  * [x] Regular option page 
  * [x] Popup Option on Right Click
  * [x] Click Counter initial implementation
  * [x] Chronological Sorts
      * [x] lto - last tab opened
      * [x] mrv - most recently viewed
  * [x] The Box 😎 (highly experimental)
  * [x] firefox migration investigation

#### **Changed:**
  * [x] UI updates
  * [x] security updates (npm dependencies)
  * [x] fixed storage issue
  * [x] Tab Info Map (TIM) - 2nd Iteration - improved speed
  * [x] fixed internal messaging (some clicks were not received by the service worker)
  * [x] WIP - a library grouping of many of the custom internal functions to reuse in newer projects 

  
 

#
**[v2.1.0](https://github.com/Mimieam/TabSorter2/discussions/33)** - 09/13/2022 (Released - **Current**)
#### **Added:**
  * [x] Basic shortcuts added
    * [x] sort_current: `Alt+Shift+S`
    * [x] merge_all: `Alt+Shift+M`
    * [x] shuffle: `Alt+Shift+F`
    * [x] discard (freeze): `Alt+Shift+D`
  * [x] Behavioral button
    * [x] Auto Sorting (Active Sorting)
    * [x] Pinned Tab auto follow (Active Pinning)
    * [x] Discard tabs after 45min of inactivity
    * [x] Auto Save and Close tabs after 1hr of inactivity (done but disabled - pending session companion page... )
  * [x] Tab Info Map (TIM) - initial implementation
  * [x] Alarms permission (used by TIM to determine when a tab should be discarded)
  * [x] Help Tooltip 

#### **Changed:**
  * [x] fixed pin tab indexing bug
 
 
#
**v2.0.0** - Targeted Release date: August 2022
#### **Added:**
  * [x] Switch to [MV3](https://developer.chrome.com/docs/extensions/mv3/mv2-sunset/)
  * [x] **Focus/Unfocus** functionalities
  * [x] **Reload** extension button
  * [x] **Stack** windows functionality ( stack all windows in a corner of you screen )
  * [x] alarms permission to manifest - workaround to keep SW alive when MV3 tries to kill it every 3minutes... *sigh*


#### **Changed:**
  * [x] complete re-write of the extension
  * [x] full support for MV3 and cross-browser
  * [x] Download permissions is now an optional_permissions
  * [x] Active Sorting - temporarily disabled
  * [x] Active Pinning - temporarily disabled


#### **Removed:**
  * [x] Removed Permissions: activeTab, management, notification
  * [x] Option page (de-prioritized to handle permissions refactoring)
  * [x] disabled Regex Sorting
  * [x] exclusion_list from merge all tabs
  * [x] fuzzy search for tabs - no point anymore ... chrome has it natively
  * [x] Tab Alarm mode - temporarily disabled

#
**<s>v1.2.0, v1.6.0, v1.8.0</s>** - discontinued due to migration to Mv3... (Dec2020 ~ May2021)
  - 8 new features added:
    - focus/Unfocus
    - stack
    - layout preference
    - global fuzzy search
    - Undo x3
    - Time Base Tab Closing
    - reloadAllWindows
    - vertical domain tab: force each new tab to merge be with another one with the same domain...
      a vertical collapsible bar appear to let you navigate the many tabs under a domain
  - 15 enhancements ( smart deduplicate, smart load, bifrost freeze... and so much more :D )
#
**v1.1.0** - 01/05/2020
  - v0.0.6 - Abandoned due to a change in chrome API - 08/21/2019
  - complete redesign and refactoring

  - Options Window:
    - Improve sorting - add options to sort by regex pattern and parameters
    - Upgrade split function to split left on current tab  - split Here
    - auto sort tabs - sort as they are loaded


  - Main Background:
    - added support for subdomain - thanks to [publicsuffix.org](https://publicsuffix.org/list/public_suffix_list.dat)
    - Make load-file backward compatible
    - useActive* function on start
    - split background.js
    - Save pinned tabs
    - Transfer pinned tabs on-close
    - Ignore pinned tabs onClose
    - Add Support for pinned Tabs ( this was surprisingly complicated 😅)
    - Sort and pin tab separately
    - Merge the last 2 windows
    - Subdomain sub-sorting - WIP
    - Options to automatically sort the tabs by title
    - Search my tabs ( 😁 - idk yet how it gonna happen lol ) (*Done but not added to TS2*)
    - Improved design :)

#
**v0.0.5** - 06/22/18
- Added new features and improved icon for visibility
- fixed windows id bug on split
- added tab recycling
- Options to automatically sort the tabs by title
- Isolate a single domain in a separate windows
- Unite - bring all tabs of a domain in the same current window ~~
- Close a domain
- Backward compatible loading of previously saved Tabs **YASSS !!!**
- Stress test split function and memory management
- Freeze - (Discard) remove all tabs in current window from memory but leaves the tab visible in the browser
#
**v0.0.4** - 09/18/17 - Completed the Option page with support for side by side split

**v0.0.3** - 04/08/17 - Updated UI - added Save & Deduplicate

**v0.0.2** - 03/23/17 - Fixed initialization issue.

**v0.0.1** - 03/23/17 - Merge/split/shuffle functionality added.


[Roadmap]: https://github.com/Mimieam/Ts2/edit/webpack2021_MV3/Changelog.md#roadmap--backlog
