# README

## Early Goals:

* Generate Customized Rails Commands Using a FrontEnd UI

* UI could use --flag checkboxes, custom project name, etc (ex: rails new etc)

### End goal would be the generation of most common rails commands such as:
* rails New
* rails migration
* rails scaffold
* rails db:seed,create,reset
* Each with their own customizable flags, parameters and variables through the UI


## Command Model:
* Contains information about the commands

### Example:
```
{
  name: "New Rails API",

  begincommand: "rails new ",

  #(insert project name via ui when displaying for copy paste)

  endcommand: "--api -d postgresql --skip-active-storage",

  uses: 6
}
```

## User Model

* Allows users to save commands to their profile.
### Example:
```
  {
    username: "Gary",

    password: "#JjajALI4DNFNM2FJF ",

    #(password will be bcrypted)
    
    projects : [
      "rails_generator_api",
      "stock_listings_api",
      "my_project"
    ]

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
