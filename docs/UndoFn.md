## The Undo button (WIP)

**Purpose**: Undo any last action made by TS2.  

**Background**: The undo functionality is one of the most experimental button currently in development. 
Because mistakes happens when messing around with your tabs, it make sense to have a way to fix them without too much trouble


While it's intent is obvious and simple, it can be a fairly demanding operation, depending on memory and number of tabs open.

**Requirements**:
- Undo should revert to a previous state
- Undo should try to preserve your tabGroups (Not fully supported yet)
- Undo should recycle as much existing tabs as possible (no closing and reopening everything)
- Undo should NEVER close a user tabs
- Undo can reopen closed tabs
- Undo button will only be active if there are undo to be done..
- No Redo 🤷🏽‍♂️


### Scenarios:
  - **Best/Average Case:**
    - `click on any button`
    - `click on undo`
  - **Worse case:**
    - `user clicks on split and get 2 windows`
    - `user closes some tabs in window #2 and creates new tabs in window #1`
    - `user tries to undo the split`
    - solution 1 -> prevent this kind of Undo
    - solution 2 -> allow with specific rules:
      - tabs closed in window #2 will be reopened
      - tabs created in window #1 will Not be closed. 
      - the previous state will be corrupt by a user action and that's fine.. 
