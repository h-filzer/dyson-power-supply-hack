# dyson-power-supply-hack

**Warning! I do not provide any guarantee that the modification following this guide will work! You may lose your live or break your lamp! Those who follow the instructions do so at their own risk. Working with mains electricity requires care and is potentially life-threatening, so have the modification performed by a professional**

It seems that the previous Dyson lamps have a design flaw in the power supply. After some time, the power needed for maximum brightness cannot be provided anymore, and the lamp simply turns off.

Unfortunately, Dyson cannot fulfill its warranty promise due to the unavailability of the necessary parts. According to user reports, a new Dyson power supply does not resolve the issues, as the same problem reoccurs after some time. I own the Lightcycle desk. The power supply for the Lightcycle and the Morph should be identical (please verify). The low point was reached when I was frustrated not to receive any solution from the manufacturer for such an expensive, albeit beautiful, lamp. In short, I opened the power supply with a Dremel. This was necessary to understand how the connections to the lamp are wired. A proprietary barrel jack with three connectors. The original power supply is rated for 24V and is designed for constant voltage. So far, so good. After opening it, I suspected an electrolytic capacitor that was already swollen. However, replacing it brought no change. But the question remained, what does the third signal line signify?

I stripped the cable and measured the voltages. I found that the white wire is the 0V line. There were 24.2V between the black and white wires, and 24V between the white and blue wires. Hmm. The white wire goes to the outer part of the barrel plug, the black one to the inner part, and the blue one to the middle pin.

## Analysis

At first, I thought that a signal from the lamp to the power supply passes through the middle pin to regulate the current and thus the brightness. So, I connected an oscilloscope. Nothing, no signals detected. Then I interrupted the blue wire. The lamp cannot be turned on. Hmm. Then I interrupted the black wire and inserted an ammeter, and connected the blue wire again. The lamp lights up, current flows (about 550mA at max. level). As the brightness increases, the current drops. OK. 

## Solution

Then I connected a bench power supply, 24V, 1A, white to negative, black to positive, blue wire through a 10k ohm resistor to black. Lo and behold, the lamp can be turned on, maximum level (coldest light & max brightness), 0.6A current consumption. The solution! Since the old power supply also made strange whistling noises under load, I ordered a branded power supply (MEAN WELL APV-35-24 36 W) for 12 euros, soldered the cable and resistor to the plug, and since then, no more failures. Problem solved.

## Wrap Up
The new power supply isn't a beauty, but since it disappears in my cable duct anyway, I have no problem with it. Generally, any power supply suitable as an LED driver with constant voltage and 24V/1.5A should work. There are models that allow connection to the mains via standard cables, eliminating the need for work on the mains electrical system. These models typically resemble notebook power supplies


