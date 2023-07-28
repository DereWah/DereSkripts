# How to Add DereGPS to Your Resource Pack

In this short tutorial, I will show you how to set up your resource pack to display DereGPS icons. This tutorial is divided into 3 cases:

- You don't have a custom resource pack on your server.
- You have a custom resource pack on your server, but you don't use custom fonts (custom icons).
- You have a custom resource pack on your server and use custom fonts.

## You don't have a custom resource pack on your server

In this case, adding the resource pack is very simple: download it from this link: https://github.com/DereWah/DereSkripts/raw/main/DereGPS/DereGPS.zip and add it to your server's resource packs. By doing this, players will automatically download it and see the fully functional GPS icon.

## You have a custom resource pack on your server, but you don't use custom fonts (custom icons)

If your server doesn't use custom icons, then it's easy to modify your resource pack by combining it with DereGPS. Download the pack from this link: https://github.com/DereWah/DereSkripts/raw/main/DereGPS/DereGPS.zip and move all the folders from `DereGPS\assets\minecraft` to your resource pack, in the same path. Make sure to put all the files in their proper place so that the resource pack works!

To ensure that everything is done correctly, check that:

- The folder `\assets\minecraft\textures\custom` exists and contains all the GPS directions.
- The file `\assets\minecraft\lang\en_us.json` contains characters like `"offset.90": "\uF82B\uF829\uF828\uF822%s\uF80B\uF809\uF808\uF802"`.
- The file `\assets\minecraft\font\default.json` contains a configuration with all the characters, including specific paths for each DereGPS icon.

Now, set the pack as the default resource pack for the server, and your players will be able to see the DereGPS icon!

## You have a custom resource pack on your server and use custom fonts.

If you have a resource pack that uses custom fonts, I assume you know how they work. If you don't, ask the staff member who set them up for you to do the following.

First, follow all the steps from the section above, BUT DO NOT overwrite the file `\assets\minecraft\font\default.json`. Your existing custom icons are there, and overwriting it will cause you to lose the configuration.

Now, open the file `\assets\minecraft\font\default.json`, and among the custom icons you already have, make sure that none of them use characters between E170, E171, E172, E173, ..., E178.

To check, simply make sure none of these characters appear in the "chars" entry of your existing custom icons.

### If they are not already used

Take the default.json file from the DereGPS pack, copy and paste all the new icons into your default.json. **MAKE SURE TO FOLLOW JSON SYNTAX RULES**! Put commas between each entry and section.

Afterward, the pack will be ready to use.

### If they are already used

You can choose either to change your existing icons by assigning them new characters or to change DereGPS icons. Here's how to change DereGPS icons:

Go to this website: https://unicodes.jessetane.com/ and select "Private Use Area" in the bottom right corner.

Choose some "squares" and click on them, then make sure they are not Unicode characters already used in your pack.

Copy the square (the character itself) and also remember its associated Unicode (For example, E0F8 = ).

Open the DereGPS.sk script and paste the square into the options at the top of the script. Also, update the comment next to it with the new value.

Then, open the default.json file and create/copy from the old DereGPS default.json a new section and update it as follows:

```
{
    "type": "bitmap",
    "file": "minecraft:custom/<ARROW DIRECTION>.png",
    "ascent": 9,
    "height": 9,
    "chars": ["\u<SAVED UNICODE ID>"]
},
```

To understand what to put in <ARROW DIRECTION>, refer to the table below:

| Option in DereGPS.sk | File name to be inserted in default.json |
| ------------ | ------------ |
| gps_forward | gpsf.png |
| gps_forwardleft | gpsfl.png |
| gps_left | gsl.png |
| gps_backwardsleft | gpsbl.png |
| gps_backwards | gpsb.png |
| gps_backwardsright | gpsbr.png |
| gps_right | gpsr.png |
| gps_forwardright | gpsfr.png |
| gps_icon | gpsf.png |

However, it's easy to understand that the direction abbreviation corresponds to the initial in the file name.

Afterward, everything will be ready to use, and you can add the pack to the server!

# Possible Issues

If you encounter any problems, feel free to open an issue regarding the skript on GitHub: https://github.com/DereWah/DereSkripts/issues

Alternatively, you can contact me on Telegram: https://t.me/DereWah.
