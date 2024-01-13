# Notes
## `agency_base_01_objective_modules.blo`
Contains mission details (search for `Objective: Agency Destructibles`)
- Various objective conditionals reference the object ID of data in the `quest_dlc03_agency_global.blo`
`Objective: Agency Destructibles [dlc3]` has `quest_global_id` string that references the `quest_id` uint32 in `quest_dlc03_agency_global.blo`
## `quest_dlc03_agency_global.blo`
Contains mission progress data (search for `Quest: Agency Base 01`)
## `packages\agency\world.bin`
Contains the reference to the global mission file
# Current thoughts
Create custom global mission file
Add it to the `world.bin` file
Add references to objectives and such to a custom objective modules file
Add it to the custom global mission file