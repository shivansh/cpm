# CPM - The Cow Package Manager

```
                       _________________________________
                      | Updating and managing your cows |
                      | just got easy and lot more fun. |
                       ---------------------------------
                              o
                               o
                                 o   #####
                                   #### _\_
                                   ##=-[•]•]   :::
                                   #(    _\   `'_:
                                    #  \__|    | |
                                     \___/     | |
                                    .'   `-----' |
                                  ( )     ,------'
                                  | |     |         _     _
                                  | |     |        ((_____))
                                  | |     |         [o   o]
                                  |_|==o=={        / \   /
                                  :..     |       /  (o o)
                     .------------'''  Y---------'     U
                    |               |  |              /
                   |                |  |             |
                  :|                }  )            |
                 : |       _        |  |           |
                :  |      / \       |__|_          |
               :   |     /   \      [____)         |
             :     |   /\___/\______________\   |  |
            #      |  /  uuu                 |  |  |
                    | |   | |                |  |  |
                    | |   | |                 | || |
                    | |   | |                 | || |
                    |\\   |\\                 |\\|\\ 
```

We have package managers for everything nowadays, then why keep our beloved cows behind...they are no less (believe me, I know !).

## Naming conventions
* The **barn** refers to the project's home directory (`~/cpm`).
* **Fortune cookie** (or simply **cookie**) refer to a category of fortune messages. <br>
  You can view which categories will be taken into account and their respective probabilities while generating cookies by executing `fortune -f`.

## How it works ?
You can fetch a cow right into your barn (make sure you spell correctly, cows hate it when you misspell their names) -
```
./cpm fetch <cow_name>
```

You can also update your entire barn with all the new cows lurking out there -
```
./cpm fetch
```
Perhaps you might also find the above command useful in case some of your cows fled without you knowing (believe it or not, there have been many such reported cases !).

Each time you fire up your login shell, `cow_selector` script runs. It randomly generates a fortune message, and gets the respective fortune cookie. It then looks in the `cookie_index` for all the cows that are present corresponding to that cookie and randomly picks one.

### But there is a catch !!
While generation of a random cookie is taken care of by the **fortune** command, the cow which gets displayed along is decided by the `cow_selector` script. And for that to happen the generated cookie needs to be associated with **atleast** one cow. The more entries there are in `cookie_index`, the more cow-cookie diversity will be there each time you start your shell. <br>
The `cookie_index` gets populated when you run `update_cookie_index` script. In case the generated cookie is not associated with any cow, the [default cow](cows/default.cow) is used. <br>
So, for the results to get better, more and more cookie entries are required in the cow files. And this is where your valuable contributions come in. Add cookies which you think are most suitable for your favourite cows. The more entries you make, the better your (and everyone's) shell will become. <br>
Currently, the `cow_index` is extremely minimal with a single populated entry.

## Requirements
* [cowsay](https://www.npmjs.com/package/cowsay)
* fortune (available by default in most distros)

## Installation
The [installation script](install) is brief -
```
git clone https://github.com/shivrai/cpm.git
./install
```

## Want to contribute ?
Have a new ASCII art ? Want to associate a cow with new cookies ? Pull requests are more than welcome.

After adding new cows or adding cookies to cow files, run the following command -
```
./update_cookie_index
```
This will automatically update the `cow_index` will all the new cow(s) associated with their corresponding cookies.

Some conventions to be taken care of while making changes -
* When adding new cookies to cow files, make sure you use a `,` for delimiting.
* Avoid using `.` in cow names.
* Do not manually tamper with the `cow_index`. This may break some functionality and produce odd results.

## Todo
* Add feature for specifying probability/score along with cows associated with each cookie to control their chances of occurrence.

## Acknowledgements
The sole aim of this project is to make one big easy to maintain index of all the diverse cows out there. All credits for the ASCII arts used goes to their respective designers.

All the ASCII arts were taking from the following websites -
* http://chris.com/ascii/
