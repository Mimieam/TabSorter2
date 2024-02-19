## The Collapse button (idea)

**Purpose**: Collapse existing domains exceeding a threshold (# of opened tabs) into TabGroups

**Background**: Too many tabs opened, even sorted, can be challenging to navigate. The proposed solution here
is to collapse domains with too many tabs opened.

**Requirements**:
- place each regular and dynamic domain in their respective group
- reuse existing groups for specific domains or create new ones as needed.
- for ease of implementation always create a group at the most right of a window (because of some chrome bugs with position..)
- group naming should be relative to the domain
- reduce the amount of tab displacement needed
- prevent creating new windows if possible
- any tab not grouped is part of the `orphan` group - `id=-999`
- if the tab is already grouped, check that their group is a collapsed one. (maybe use a special character in the group title?)
      - ```isCollapsedGroup == True ? reuse this group: ignore unless bypass existing group option selected```
          

    
