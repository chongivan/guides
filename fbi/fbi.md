# Fbi Usage Guide


## Facebook App Token

First, we would require an App Token to access Facebook's API

I would love to have included my App Token in this program, so I did a stress test and it turns out, FB throttles API usage. To avoid downtime when too many users hit the API with the same App Token, we wanna use our own

### Create a Developer Account
1. Head over to https://developers.facebook.com/
2. Click on "Get Started", top right of the screen
3. Follow the instructions to completion


### Create an App
1. Head over to https://developers.facebook.com/apps/
2. Click on "Create App", top right of the screen
3. Select the "Business" app type
4. Follow the instructions to completion

### Get our App Token
1. Head over to https://developers.facebook.com/tools/accesstoken/
2. Locate our newly created app
3. Copy the App Token


## Installation

### Open a CLI

#### Windows
1. Press the Windows Key and search for "command prompt"
2. Open Command Prompt

#### Mac

1. Open Spotlight by pressing Command + Space
2. Search for "terminal" and hit Enter

### Install Ruby

#### Windows

1. Head over to https://rubyinstaller.org/downloads/
2. Download the top-most latest version
3. Install and follow the installation wizard's instructions

#### Mac

1. Ruby is already installed on Macs by default, with some limitations
2. Skip this installation step for now, but if we face any issues, follow the instructions [here](https://mac.install.guide/ruby/3.html) to install Ruby


#### Linux

1. Update the system repositories
```
sudo apt update
```
2. Install Ruby
```
sudo apt install ruby-full
```

### Install Fbi

With Ruby installed, we use the RubyGems package manager to install our program via the CLI
```
gem install fbi
```

### Using Fbi

Simply run the following command to start the program
```
fbi
```

#### Input App Token

We'd be asked for our App Token the first time. Input the saved App Token from [Facebook App Token](#facebook-app-token)

The App Token prompt will reappear later if we've entered an invalid App Token



#### Keyword Search

We can now search for keywords, with the following information columns
* Topic
* Disambiguation Category
* Additional Paths

An example for "dog"
![Image](https://raw.githubusercontent.com/chongivan/guides/master/fbi/images/i1.jpg)

Do notice that our keyword ranges are nicely formatted for quick use in our Algo Sheets as well 😉


#### Filters

After we've done a [Keyword Search](#keyword-search), we can narrow down our results via filters

##### Quick Search

Type **one of the following letters and hit Enter** for the corresponding results

| Letter    | Filter    | Result                      |
| :-------: |:---------:| :---------------------------|
| **w**     | Websites  | Rows containing "website"   |
| **t**     | TV        | Rows containing "tv"        |
| **m**     | Magazines | Rows containing "magazine"  |

![Image](https://raw.githubusercontent.com/chongivan/guides/master/fbi/images/i2.jpg)

##### Custom Search

If we want to filter our results with our own seach term, simply type `f mysearchterm` and hit Enter


#### Exit

Simply press `q` and hit Enter
