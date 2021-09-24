# NRF52840
Stuff related to nRF52840
This repo consists of stuff that I found related to nRF52840
The study material collected is based on the dongle being configured as a beacon. 

NRF SDK 17: https://www.nordicsemi.com/Products/Development-software/nRF5-SDK/Download#infotabs


NRF Connect: https://www.nordicsemi.com/Products/Development-tools/nRF-Connect-for-desktop


nRF Series: Developing on Windows with ARM Keil SDK: https://github.com/anikethj61/NRF52840/blob/main/getting_started_keil.pdf

Following are screenshots in order to elaborate how to test the working of nRF52840 as a beacon using the example code: 

1. Install NRF Connect software by nRF Semiconductors (Can be downloaded from the above)
2. The software requires you to install applications to enable and test features of the dongle. Go ahead, make sure to install Bluetooth Low Enegy, RSSI Viewer and Programmer applications. 


![alttext](https://github.com/anikethj61/NRF52840/blob/main/NRFConnect.png)


3. Once done with installation, plug in the nRF52840 dongle. Open the Bluetooth Low Energy application. On the top left corner there is a device selection drop down menu. If no devices are selected it shows "No Devices Available" and if there is a compatible device detected by the USB ports it shows "Select Device". Select the device from the drop down menu and select YES to the prompt asking if the device needs to be programmed. (Note: In case of any errors or timeout in the log, retry the same process it should work.)



![alttext](https://github.com/anikethj61/NRF52840/blob/main/NRF%20Connect%20-%20BLE.png)



![alttext](https://github.com/anikethj61/NRF52840/blob/main/NRF%20Connect%20-%20BLE_DeviceSelect.png)



![alttext](https://github.com/anikethj61/NRF52840/blob/main/NRF%20Connect%20-%20BLE_DeviceSelect_ConfirmationYES.png)


4. Once the device is selected it will appear on the screen with details about the dongle, click on the settings icon to setup advertising data and initate advertising


![alttext](https://github.com/anikethj61/NRF52840/blob/main/NRF%20Connect%20-%20BLE_AdvertisingSetup.png)


5. Press on start advertising 


![alttext](https://github.com/anikethj61/NRF52840/blob/main/NRF%20Connect%20-%20BLE_Advertising.png)


6. Now open a beacon scanner on phone and scan for devices. 

7. To flash the program onto the dongle, open the programmer app and select the device from the drop down menu. 


![alttext](https://github.com/anikethj61/NRF52840/blob/main/NRF%20Connect%20-%20Programmer.png)


8. To execute the beacon code, Go to the source folder where the NRF SDK has been installed {Path:Drive Name:.......\nRF5_SDK_17.1.0_ddde560\nRF5_SDK_17.1.0_ddde560\examples\ble_peripheral\ble_app_beacon\hex}. In the SDK examples folder -> ble_peripheral -> ble_app_beacon -> hex folder are the saved hex files that can be added. 


![alttext](https://github.com/anikethj61/NRF52840/blob/main/NRF%20Connect%20-%20Programmer_AddHEX.png)


9. Once uploading the hex file, write the code from the device menu on the right -> Wait for the code to be flashes and the device will function as a beacon as soon as powered. 
