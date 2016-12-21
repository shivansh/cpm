# CPM

```
             _________________________________
            /                                 \
            | Updating and managing your cows |
            \ just got easy and lot more fun. /
             ---------------------------------
                    o   ^__^
                     o  (OO)\_______
                        (__)\       )\/\
                            ||----w |
                            ||     ||

```

We have package managers for everything today, then why not for cows. They are no less (believe me, I know !).

## How it works ?

## Naming convention

## Requirements
* [cowsay](https://www.npmjs.com/package/cowsay)
* fortune (available by default in most distros)

## Installation
The installation script is brief -
```
shell=$(which $SHELL | rev | cut -f 1 -d '/' | rev)
echo ". ~/cpm/cow_selector" >> ~/."$shell"rc
```

## Contributing
Have a new ASCII art, pull requests are more than welcome.

**PS:** Don't forget to run `[update_cow_index](update_cow_index)` to update the `cow_index` after adding new cow(s).

## Acknowledgements
The sole aim of this project is to make one big index of all diverse cows. All credits to the ASCII arts used goes to their respective designers.

All the ASCII arts were taking from the following websites -
* http://chris.com/ascii/
