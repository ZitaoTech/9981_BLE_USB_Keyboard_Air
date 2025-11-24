# P9981 BLE&USB Keyboard Air ⌨️
The fully open-sourced P9981 BLE&USB Air Keyboard is the smallest ZMK-powered keyboard and features n-Key rollover that other original blackberry keyboards don't have!
# Image Gallery
<img src="https://github.com/user-attachments/assets/31d46916-c757-48cd-9737-19a4e9769f6e" />

<table>
    <tr>
        <td><img src="https://github.com/user-attachments/assets/f0728470-6353-43b6-a7eb-7a40e88827e2"  style="width:700px;"/></td>
        <td><img src="https://github.com/user-attachments/assets/e7482137-c3f8-4a30-8584-bfd0be0e3d0d" style="width:700px;"/></td>
    </tr>

</table>

## Contents
- [About this keyboard](#About-this-keyboard-)


# About this keyboard [🔼](#contents)
This mini Keyboard uses the cloned P9981 keycap and powered by the NRF52840 Microcontroller and operates under ZMK Firmware with extra custom driver.  

| Main Features      |  |   
| :---        |    :----:   | 
| Processor      | [NRF52840](https://www.nordicsemi.com/products/nrf52840) from Nordic Semiconductor | 
| Firmware   | ZMK firmware  | 
| Backlight | Keyboard with white backlight|
|Battery type| Integrated li-on battery|
|Battery capacity| 750mah with up to 3 months battery life(assume 1 hour per day)|
|USB&BLE Output|Support both wired and wireless connect|
|Small size| The smallest wireless keyboard in the world|
|Aluminium body|The top case is made of aluminium, lower case 3d printed|
|Open source| [Hardware]and [software](https://github.com/ZitaoTech/9981_BLE_USB_Keyboard_Air/tree/main/ZMK%20source%20code)all open sourced|
|__NKRO__|__There are integrated diodes on the keyboard, all the keys can be pressed at the same time__(Other original Blackberry keyboards don't have this feature)|

## Before you buy/use [🔼](#contents)

**Bluetooth version check**: This keyboard can only be paired wirelessly with devices that have **BLE 4.2 module or higher**, please check if your device have the right Bluetooth module, otherwise the keyboard can not work with your device wirelessly!  
How to check the Bluetooth version of your device: google (your device name) like iphone 8 and plus Bluetooth version and you will find the answer like this:
 <img src="https://github.com/ZitaoTech/BB9900-USB_BLE_Keyboard/blob/main/Pics/BLE%20VERSION%20check.png" width = "500" alt="BLE VERSION CHECK" align=center />

## Where to buy [🔼](#contents)
- **If you are outside China**: You can buy the keyboard at Elecrow    
- **If you are in China**: 在闲鱼搜索用户御坂200016号

# How to use this keyboard [🔼](#contents)
- By default the keyboard has 4 Layers, when you just turn on the keyboard, the keyboard is at layer0-the QWERTY layer.  
- When you tap or hold the ```SYM``` key, the keyboard will enter layer1, and the keyboard backlight will start blinking, you can type numbers or symbols at this layer.  
- When you tap or hold the ```aA``` key at the lower right corner, the keyboard will enter layer2 and the keyboard backlight will do a loop effect, you can type some symbols and do some Bluetooth behaviors at this layer.
- The layer 3 basically has no keycode, this layer is reserved for the customer, and the keyboard backlight will blink the twice speed as the layer 1 when you are at layer 3.

**Now let's check the keymap.**  
## Keymap [🔼](#contents)
**Layer0-QWERTY**    

## How to connect this keyboard with your device [🔼](#contents)
- Turn on the Bluetooth on your phone
- Find the device ```p9981``` and pair with it then you should type with the keyboard
> [!CAUTION]
> After you delete the bluetooth profile and if you want to pair with the keyboard with another device when you have already paired with some device before, make sure to enter layer 2 and double tap the ```space key``` to clear the bluetooth profile on the keyboard side. Otherwise there will be error when you want to pair with another device!!! Please use the following steps to delete the bluetooth pairing
- First delete the bluetooth profile(somewhere it's called forget the device or unpair the device) on your device
- Enter layer 2 and doubletap the ```space key```(You can tap the lower right aA key to trigger sticky layer 2 or hold the aA key to enter layer2)
- Refresh the Bluetooth setting page on your device(You can turn on and off the bluetooth) and then you can pair with the keyboard again

## Multi device connect [🔼](#contents)
By default the keyboard can only be paired with 1 device at the same time. But you can add bluetooth pairing keycode on recerved layer to pair with more than one device at the same time like BT_SEL 1 or 2

<p align="center">
<img height="400"  src="https://github.com/user-attachments/assets/7f99c32e-cdc5-490e-a8d0-8e034084d935" />
</p>
And here are the steps how to connect with other devices:  

1. Assume you have already connected this keyboard with one device
2. press the BT_SEL_1 keycode

Now the keyboard is ready to be paired with second device.  
Similarly, you can pair this keyboard with a third and a fourth device.  

3. Once pairing is done, you can switch between the devices the same way.

> [!CAUTION]
> - The BT_CLEAR keycoode — which is triggered by double-tapping the ```space key`` on Layer 2 — is calculated independently for each device. This means that when you trigger BT_CLEAR while connected to the second device, it won’t affect any of the other devices.

## USB&BLE Output select [🔼](#USB&BLE-output-select)
The keyboard supports both USB and BLE output, by default the output is BLE. Assume the keyboard is both connected with a PC and paired with a phone, you can toggle the output by double-tapping the dollar key at layer2, if the output is USB the trackpad led will start blinking every second.

## Realtime Keymap Updating [🔼](#Realtime-keymap-updating)
[ZMK Studio](https://zmk.dev/docs/features/studio) provides runtime update functionality to ZMK powered devices, allowing users to change their keymap layers without flashing new firmware to their keyboards.  

You can use ZMK Studio with ```Chrome/Edge``` at [https://zmk.studio/](https://zmk.studio/).  

Before you use ZMK Studio, you need to ```turn off``` the bluetooth from your phone that the keyboard is paired with, then you can select the port shown on the ZMK Studio page and then start the keymap updating.  

The picture below shows you how it looks like when the keyboard connects with ZMK Studio successfully.

<p align="center">
<img height="600" src="https://github.com/user-attachments/assets/a3330c9a-39dd-4337-a4c1-9d76161f0783" />
</p>

> [!NOTE]
> Currently The ZMK Studio is still beta version, there are some functions that ```can not``` be configured e.g. macro, 
> there is another advanced way to update the keymap, please check the content below

## Advanced Keymap Updating [🔼](#Advanced-keymap-updating)
Since the ZMK Studio is still in beta stage, There’s also a more straightforward method to edit the keymap.  
Please refer to this [page](https://github.com/ZitaoTech/zmk-config-9981-air/tree/main)

## How to update the firmware [🔼](#How-to-update-the-firmware)
Because this keyboard is powered by open sourced ZMK firmware, which allows you to modify different features yourself, and thus you might need to update the firmware yourself. The following are steps to update the firmware.

1. Connect the keyboard with a computer
2. Make the keyboard into bootloader mode(By default you need to enter layer2 and press the dollar key)
3. A new USB Disk will be found by you computer
4. Drag the new .uf2 firmware file into the USB Disk and the keyboard is finished with updating

## Emergency way to enter bootloader [🔼](#Emergency-way-to-enter-bootloader)
There is a hole at the bottom of the keyboard, and inside that's the reset button. After connect the keyboard with a computer, you can quickly tap the reset button using a small pin to force the keyboard into ```bootloader mode```

<p align="center">
<img  height="400" src="https://github.com/user-attachments/assets/8c5fa5aa-a2c3-49b9-909f-f35a01578f6d" />
</p>

# Advanced methods of using this keyboard [🔼](#Advanced-methods-of-using-this-keyboard) 

## Build your own firmware [🔼](#Build-your-own-firmware)
First you need to build the toolchain of ZMK firmware, it's recommended to build it under Github Codespaces. Here are the steps for you to build the toolchain via Codespaces:  
0. Register a Github account if you don't have one
1. Access the zmk firmware [github page](https://github.com/zmkfirmware/zmk)  
2. Create a codespace by clicking this icon:

<p align="center">
<img width="744" height="496" alt="image" src="https://github.com/user-attachments/assets/3c08bbc8-ac93-4895-8304-b2366401aae5" >
 </p>
 
3. When the codespace is finished setting up, type ```cd zmk ``` in the terminal of the codespace
4. type ```west init -l app/``` in the terminal
5. type ```west update``` and wait about 5-10 minutes and the toolchain is finished setting up
6. copy and paste the ```p9981``` [folder](https://github.com/ZitaoTech/9981_BLE_USB_Keyboard_Air/tree/main/ZMK%20source%20code/p9981) into the ```app/boards/arm``` folder
7. compile the firmware by using ```cd app``` and ```west build -p -b p9981``` and zmk will start compiling the firmware
8. the compiled firmware is ```app/build/zephyr/zmk.uf2```. You can download and update the firmware


# Troubleshoot [🔼](#troubleshoot)
- Why did the keyboard feel bad to type on when I first receive it?

Because the keycap is made of silicone, when the keyboard is transported by air, the low temperature can make the silicone stiffen slightly. So when you first receive the keyboard, it may feel bad to type with. Once it warms up to room temperature, the typing feel will improve. The same thing also happens with other BlackBerry keyboards.  

- Why can't my keyboard be paired with my device?

It’s possible that after the previous pairing, the keyboard didn’t clear its pairing information. You need to switch to Layer 2 and double-tap the ```space key``` to erase the keyboard’s pairing data, and then you can start a new pairing.

> [!CAUTION]
> After deleting the pairing on your phone or on the keyboard, it’s important to refresh the Bluetooth page on your device. The easiest way is to just restart Bluetooth module.

- Why is my keyboard not having backlight?

Enter layer 2 and press ‘B’ so you can bring the backlight back again


# Others [🔼](#others) 
## Dimensions of the keyboard [🔼](#dimensions-of-the-keyboard)
The picture below shows the outerline dimension of the keyboard  
<p align="center">
<img width="800" src="https://github.com/user-attachments/assets/beed2a0c-0d9c-486b-b4d5-2ca091762a4f" />
</p>

## Weight [🔼](#Weight)
The total weight of the keyboard is 39.8 g

# Inspiration [🔼](#Inspiration) 
This [page](https://github.com/ZitaoTech/9981_BLE_USB_Keyboard_Air/tree/main/Inspiration)shows what the keyboard can do besides functioning as a standalone Bluetooth keyboard.


