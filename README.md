# Qminimize UNMANTAINED
Rofi script to minimize / unminimize multiple windows in qtile

#### Additional requirements :
[EWMH module](https://pypi.org/project/ewmh/)

[fuzzywuzzy module](https://pypi.org/project/fuzzywuzzy/)

#### How to use it :

    - Clone the directory and place the file "Qminimize" in a directory in your $PATH
        E.G. : I have mine in .local/bin but otherwise you can put it in /usr/bin
    
    - Make the file executable with "chmod +x Qminimize"
    
    - Add the keys to the qtile configuration :      
        Key([mod, "shift"], "m", lazy.spawn('Qminimize -u'), desc="Minimize window"), # - u to show the rofi menu
        Key([mod], "m", lazy.spawn("Qminimize -m")), # -m to minimize
        
    - When the rofi menu is open press :
        "Enter" to unminize the select entry 
        "Shift + Enter" to select more choices and then "Enter" to confirm

#### Troubleshooting :
    - If for some reason the program doesn't work, to see what the problem is, launch it by terminal with:
         "Qminimize -m" to minimize the focused window
         "Qminimize -u" to show the rofi menu
