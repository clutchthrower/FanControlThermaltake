# Just a quick temporary patch
Learned about [Fan Control](https://github.com/Rem0o/FanControl.Releases) and was past ready to ditch ThermalTakes (not GREAT, but better than the first version) software to quickly learn it would control my fans... Had to get RiingPlus Fans working!

![Screenshot_20230207_035744](https://user-images.githubusercontent.com/63625821/217364490-e2dfe38a-ce68-4e90-a7a4-cc5113b8751f.png)


# Assisted Setup
Worked great, but couldnt see rpms on one of the fans. After the setup you just had to manually pair the speed sensor.


*Issues:*
- The fans will say there is a discrepancy between the target and its value.
    - I just set them all to 'Force Apply'
- You can even open TT RGB Plus to play with the RGB!
    - The fan controller might glitch/not work. Just need to close TT RGB and toggle the switches.






# FanControl Thermaltake Plugin
This is a plugin that let's [Fan Control](https://github.com/Rem0o/FanControl.Releases) connect to a Thermaltake Fan Controller. Right now this is a proof-of-concept thing. The code is sub-optimal and only connects to the controller you get with the Riing Plus fans.

![tt-controller](https://user-images.githubusercontent.com/5355154/179553404-eb8102e8-6ced-4eee-aae5-79912550e278.png)

*Known Issues:*
- Running this plugin and TT RGB Plus at the same time is a problem. You could try to set the fans in TT RGB Plus to manual and 0%.
- Setting the fan power is instant, but the read out takes a few seconds to adjust. So it takes a while before the Fan Control app sees the right RPM and Power values.

*Possible Issues:*
- I have added code for checking it there's more than one TT controller in the system. I wasn't able to test it, since I only had one in my development PC. So it might work, it might not.

*Todo:*
- Make it more modular so I can easily add more TT controllers if needed.
- Implement the Thermaltake controller into my [RazerChromaConnect app](https://github.com/fu-raz/Razer-Chroma-WLED-Connect-App) so you have at least one option to control the RGB if you can't use TTRGB.
- Maybe I can have this plugin take precedence over TTRGB when it comes to the fan speeds.
