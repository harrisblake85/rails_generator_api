# README

## Early Goals:

* Generate Customized Rails Commands Using a FrontEnd UI

* UI could use --flag checkboxes, custom project name, etc (ex: rails new etc)

### End goal would be the generation of most common rails commands such as:
* rails New
* rails migration
* rails scaffold
* rails db:seed,create,reset
* Each with their own customizable flags through


## Command Model:
* Contains information about the commands

### Example:
```
{
  name: "New Rails API",

  project: "rails_generator_api",

  command: "rails new rails_generator_api --api -d postgresql --skip-active-storage",
  uses: 6
}
```

## User Model

* Allows users to save commands to their profile.
### Example:
```
  {
    username: "Gary",

    password: "#JjajALI4DNFNM2FJF (bcrypted)",

    otherdata: {}

  }
```

## Connection Model
* Through Table For User And Command
* Allows many users to have the same command
* Allows one user to save many commands
### Example:
```
  {
    user_id: 5,
    command_id: 2,
    forks:12
  }
```
