#phisherMan
<p align="center">
<a href="https://t.me/kri shna"><img title="Telegram" src="https://img.shields.io/badge/Telegram-black?style=for-the-badge&logo=Telegram"></a>
<a href="https://instagram.com/krishna_7339_"><img title="instagram" src="https://img.shields.io/badge/instagram-black?style=for-the-badge&logo=instagram"></a>

![badge](https://img.shields.io/badge/version-HACKER.K-blue)
![badge](https://img.shields.io/badge/python-%3E%3D3.8-orange)
![badge](https://img.shields.io/badge/version-S <3 M-blue)

  
### Search for public profile information on Facebook

![screenshot](template.png)

## Installation

```
# clone the repo
$ git clone https://github.com/anonymous-7339/phisherman.git

# change the working directory to phisherMan
$ cd phisherMan

# install the requirements
$ python3 -m pip install -r requirements.txt
```

## Pre-requisites

* Make sure you have the executable "geckodriver" installed on your machine.

## Usage

```
$ python3 phisherman.py --help
usage: phisherman.py [-h] [--version] [-u USERNAME [USERNAME ...] | -i ID
                    [ID ...] | --use-txt TXT_FILE] [-sf]
                    [--specify {0,1,2,3,4,5} [{0,1,2,3,4,5} ...]] [-s] [-b]
                    [--email EMAIL] [--password PASSWORD] [-o] [-c] [-v]

phisherMan: Extract information from facebook profiles....

optional arguments:
  -h, --help            show this help message and exit
  --version             Shows the current version of the program.
  -u USERNAME [USERNAME ...], --username USERNAME [USERNAME ...]
                        Defines one or more users for the search.
  -i ID [ID ...], --id ID [ID ...]
                        Set the profile identification number.
  --use-txt TXT_FILE    Replaces the USERNAME parameter with a user list in a
                        txt.
  -sf, --scrape-family  If this parameter is passed, the information from
                        family members will be scraped if available.
  --specify {0,1,2,3,4,5} [{0,1,2,3,4,5} ...]
                        Use the index number to return a specific part of the
                        page. about: 0, about_contact_and_basic_info: 1,
                        about_family_and_relationships: 2, about_details: 3,
                        about_work_and_education: 4, about_places: 5.
  -s, --several         Returns extra data like profile picture, number of
                        followers and friends.
  -b, --browser         Opens the browser/bot.
  --email EMAIL         If the profile is blocked, you can define your
                        account, however you have the search user in your
                        friends list.
  --password PASSWORD   Set the password for your facebook account, this
                        parameter has to be used with --email.
  -o, --file-output     Save the output data to a .txt file.
  -c, --compact         Compress all .txt files. Use together with -o.
  -v, -d, --verbose, --debug
                        It shows in detail the data search process.
```

To search for a user:

* User name: `python3 phisherman.py -u name name.profile name.profile2`
* ID: `python3 fisherman.py -i 000000000000`

The username must be found on the facebook profile link, such as:

```
https://facebook.com/name.profile/
```

It is also possible to load multiple usernames from a .txt file, this can be useful for a brute force output type:

```
python3 fisherman.py --use-txt filename.txt
```

Some profiles are limited to displaying your information for any account, so you can use your account to extract. Note:
this should be used as the last hypothesis, and the target profile must be on your friends list:

```
python3 phisherman.py --email youremail@email.com --password yourpass
```

### Some situations:

* For complete massive scrape:
  ```
  python3 phisherman.py --use-txt file -o -c -sf
  ```
  With a file with dozens of names on each line, you can make a complete "scan" taking your information and even your
  family members and will be compressed into a .zip at the output.


* For specific parts of the account:
    * Basic data: `python3 phisherman.py -u name --specify 0`
    * Family and relationship: `python3 -u name --specify 2`
    * It is still possible to mix: `python3 phisherman.py -u name --specify 0 2`


* To get additional things like profile picture, how many followers and how many friends:
  ```
  python3 phisherman.py -u name -s
  ```

## *This tool only extracts information that is public, not use for private or illegal purposes.*

## LICENSE © phisherMan Project
Creator - [anonymous-7339](https://github.com/anonymous-7339)
