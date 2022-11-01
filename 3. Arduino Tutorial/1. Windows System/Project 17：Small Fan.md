**Project 17：Small Fan**

1.  **Introduction**

In hot summer, we need electric fans to cool us down, so in this
project, we will use the ESP32 to control a DC motor and small fan
blades to make a small electric fan.

2.  **Components**

<table>
<tbody>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/56053f7126905c6def63919c661d5c0a.jpeg" style="width:2.17847in;height:1.0625in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/e380dd26e4825be9a768973802a55fe6.png" style="width:0.94722in;height:2.32014in" /></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td>ESP32*1</td>
<td>Breadboard*1</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/9197d4aff9356c585b7ef68e33a6881d.png" style="width:0.27986in;height:1.08819in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/5eba8bae9e1d18b959ca425a9cc83fd2.jpeg" style="width:1.07569in;height:0.43472in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/655e6c465cb423279e0908513a983711.png" style="width:0.85694in;height:0.75347in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/df3db6765ee8c86beafa8410e87dd50d.png" style="width:0.77361in;height:0.76944in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/7dcbd02995be3c142b2f97df7f7c03ce.png" style="width:1.05903in;height:0.56667in" /></td>
</tr>
<tr class="even">
<td>NPN Transistor (S8050)*1</td>
<td>DC Motor*1</td>
<td>Fan*1</td>
<td>Jumper Wires</td>
<td>USB Cable*1</td>
</tr>
<tr class="odd">
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/b65d826ca481982fed0212dba2957c7c.jpeg" style="width:1.57361in;height:1.13611in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/6734084c96238569a513a5ff3190621d.png" style="width:1.15486in;height:0.49861in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/a815c48437199c6ab79d74cd2d583de0.png" style="width:0.24722in;height:1.14097in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/098a2730d0b0a2a4b2079e0fc87fd38b.png" style="width:0.90833in;height:0.23681in" /></td>
<td><img src="https://raw.githubusercontent.com/keyestudio/KS5012-Keyestudio-ESP32-Learning-Kit-Basic-Edition-Arduino/master/media/9197d4aff9356c585b7ef68e33a6881d.png" style="width:0.27986in;height:1.08819in" /></td>
</tr>
<tr class="even">
<td>6 AA Battery Holder*1</td>
<td>Keyestudio breadboard special power module*1</td>
<td>No.5 battery (self-provided)*6</td>
<td>1KΩ Resistor*1</td>
<td>PNP Transistor (S8550)*1</td>
</tr>
</tbody>
</table>

**3. Component Knowledge**

**Keyestudio Breadboard Power Supply Module**

![](/media/7ff03f4506988f1ce99c5757892fc6de.jpeg)

**Introduction:**

This breadboard power supply module is compatible with 5V and 3.3V,
which can be applied to MB102 breadboard. The module contains two
channels of independent control, powered by the USB all the way.

The output voltage is constant for the DC5V, and another way is powered
by DC 7-12V, output controlled by the slide switch, respectively for
DC5V and DC3.3V.

If the other power supply is DC 7-12v, when the slide switch is switched
to +5V, the output voltages of the left and right lines of the module
are DC 5V. When the slide switch is switched to +3V, the output voltage
of the USB power supply terminal of the module is DC5V , and the output
voltage of the DC 7-12V power supply terminal of the other power supply
is DC3.3V.

**Specification**

  - Applied to MB102 breadboard

  - Input voltage：DC 7-12V or powered by USB

  - Output voltage：3.3V or 5V

  - Max output current：\<700mA

  - Up and down two channels of independent control, one of which can be
    switched to 3.3V or 5V
    
    Comes with two sets of DC output pins, easy for external use

<!-- end list -->

3.  **Wiring Diagram**
    
    ![](/media/715ae32c3fac7c6537f380fb91e5e83c.png)
    
    (Note: Connect the wires and then install a small fan blade on the
    DC motor. )
    
    **4. Test Code**

<table>
<tbody>
<tr class="odd">
<td><p>//**********************************************************************</p>
<p>/*</p>
<p>* Filename : Small_Fan</p>
<p>* Description : S8050 triode drives the motor working</p>
<p>* Auther : http//www.keyestudio.com</p>
<p>*/</p>
<p>void setup() </p>
<p>void loop() </p>
<p>//**********************************************************************************</p></td>
</tr>
</tbody>
</table>

**5. Test Result 1：**

Upload the code to the ESP32 and power up. The motor rotates for 4s,
stops for 2s, in loop way.

**6. Wiring Diagram 2：**

We use the S8550 PNP transistor to control the motor.

![](/media/04293fbe70eeec27c2d8127f42afbaf2.png)

Note: wire up and connect a fan on the motor.

**7. Test Code 2：**

<table>
<tbody>
<tr class="odd">
<td><p>//**********************************************************************</p>
<p>/*</p>
<p>* Filename : Small_Fan</p>
<p>* Description : S8550 triode drives the motor working</p>
<p>* Auther : http//www.keyestudio.com</p>
<p>*/</p>
<p>void setup() </p>
<p>void loop() </p>
<p>//**********************************************************************************</p></td>
</tr>
</tbody>
</table>

**8. Test Result 2：**

Upload the code to the ESP32 and power up. The motor rotates for 4s,
stops for 2s, in loop way.
