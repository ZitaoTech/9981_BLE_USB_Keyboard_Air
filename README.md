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
