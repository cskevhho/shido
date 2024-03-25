# Project Brainstorming

## Description:

Project Management + Bug Tracking Webapp
Svelte + Sveltekit
TailwindCSS -> DaisyUI? shadcn?
Pocketbase vs Prisma? No need for scaling. Pocketbase? -> SQLite
How to handle API routing, best practices?
API Routing Sveltekit (Slug dynamic stuff?)

Project
|
|
--- Feature
    |
    |
    --- Task
        |
        |
        --- Comment
        |
        |
        --- Bug
            |
            |
            --- Comment

## Features

### Would Be Nice:

- Notifications
- Small Language Model for Task Breakdown?
- Productivity Dashboard (timer, youtube player, task list)

### Should Have:

- User Authentication
- Project Management
- Tasks/Features
- Bug Tracking
- User Roles? No teams with original idea so maybe not


## Tech Stack

- Svelte
- Sveltekit
- TailwindCSS
- SQLite
- Pocketbase


## Project Schema (SQL ERD)

Legend:
+ Primary Key
- Foreign Key
~ Unique
o Optional

[ User ]
+ id
~ username
~ email
~ password
~ created_at
~ updated_at

[ Project ]
+ id
- user_id
~ name
~ description
~ created_at
~ updated_at

[ Feature ]
+ id
- project_id
~ name
~ description
~ created_at
~ updated_at

[ Task ]
+ id
- feature_id
~ name
~ description
~ created_at
~ updated_at

[ Comment ]
+ id
- task_id
~ user_id
~ content
~ created_at
~ updated_at

[ Bug ]
+ id
- task_id
~ name
~ description
~ created_at
~ updated_at

[ BugComment ]
+ id
- bug_id
~ user_id
~ content
~ created_at
~ updated_at

