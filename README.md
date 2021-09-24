# Instagram Spammer Bot
This script was developed to spam comments with usernames on that boring giveaways that often happen on Instagram platform. (i.e.: *Comment the name of a friend to compete to a product*).

However, this script was modified to beat the shit out of every other contestant (in terms of comments)

It uses mainly `pyautogui` to simulate a person refreshing, clicking and typing in the comment section, in this way, the instagram won't detect that's a bot and you can be 24/7 spawning usernames or whatever you're up to.

## Instructions
### Dependencies
This script was made using `python3`, in order to install all dependencies, please run:
```bashrc
pip install -r requirements.txt
```

Alternatively (this is what I (matt) did), you can install the python libraries "pyautogui", "pandas", and "Xlib" individually. Plenty of stuff online regarding how to do that.


### System dependencies
Appears that `pyautogui` module cannot support Wayland yet, so i strongly recommend to use this script on a unix/linux env with **XORG** support.

### How to use
First, you will need to generate a list with all the usernames you want to spawn. It only needs to be on `.csv` format, stay inside the `./assets` folder and have a column named `username`. To generate mine, i had used a plugin called [*Helper Tools for Instagram*](https://chrome.google.com/webstore/detail/helper-tools-for-instagra/hcdbfckhdcpepllecbkaaojfgipnpbpb) (for Chrome).

To use this script:
1. Open a Instagram post page that you will spam, on your favorite browser (tested on chrome) and put aside.
2. Open the terminal on the project folder and run `python3 spam.py`. In an IDE, like PyCharm for example, you can just click the run button while making sure the python terminal is open.
3. The script will wait a key to be pressed, when waiting, you will move the mouse to the *click* position (where you can type, i.e.: *comment section*) **without clicking** and press `Enter` key on the terminal window, then, the script will save the current mouse (x, y) positions to replicate while the script runs.
4. The script will read the `.csv` files and start to spam. In the assets folder, there will be one .csv file. Open that, and type all your comments in the specified column (one cell per comment). MAKE SURE TO SAVE IT AS A .csv FILE!!!
#### Considerations
+ The script uses a random interval number generation on the range [TIME_TO_SLEEP - 5, TIME_TO_SLEEP + 5), where `TIME_TO_SLEEP` it's a global variable inside `spam.py` that you can tweak if needed.
+ The script always does: Get username, type username and hit `Enter` key, hit `f5` key to reload the page. This is needed because instagram normally blocks text input on comment section after some comments.


***** I would recommend zooming out a bit on the instagram window in your browser just to ensure the comment area is in screenshot after each refresh.

## Authorship
Script developed by FelipeCRamos, with MIT License, without using **anything** from Instagram API.
Modified by matt

Not optimized **at all**, made in 15 minutes just to place a whole lot of comments on a giveaway page.
"# comments" 
