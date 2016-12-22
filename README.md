# CPM

```
             _________________________________
            | Updating and managing your cows |
            | just got easy and lot more fun. |
             ---------------------------------
                    o   ^__^
                     o  (OO)\_______
                        (__)\       )\/\
                            ||----w |
                            ||     ||

```

We have package managers for everything today, then why not for cows. They are no less (believe me, I know !).

## Naming convention
* The **barn** refers to the project's home directory (`~/cpm`).
* When adding new fortune cookies to cow files, make sure you use a `,` for delimiting.

## How it works ?
You can fetch a single cow right into your barn -
```
./cpm fetch <cow_name>
```

You can also update your entire barn with all the new cows lurking out there -
```
./cpm fetch
```
Perhaps you might also find the above command useful in case some of your cows fled without you knowing (believe it or not, it happens !).

## Requirements
* [cowsay](https://www.npmjs.com/package/cowsay)
* fortune (available by default in most distros)

## Installation
The installation script is brief -
```
git clone https://github.com/shivrai/cpm.git
shell=$(which $SHELL | rev | cut -f 1 -d '/' | rev)
echo ". ~/cpm/cow_selector" >> ~/."$shell"rc
```

## Want to contribute ?
Have a new ASCII art, pull requests are more than welcome.

After adding new cow(s), run the following -
```
./update_cookie_index
```
This will automatically update the `cow_index` will all the new cow(s).

## Acknowledgements
The sole aim of this project is to make one big index of all the diverse cows out there. All credits to the ASCII arts used goes to their respective designers.

All the ASCII arts were taking from the following websites -
* http://chris.com/ascii/
