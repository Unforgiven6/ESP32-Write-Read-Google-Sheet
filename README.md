# ESP32-Write-Read-Google-Sheet
The function is to read the data of any sensor/resistor/voltage into ESP32 via different pins (ADC for resistors like photo-resistor or potentiometer). It will send data into Google Sheet with the use of Apps Script. With ESP32 connected to a LCD, the code will also read data onto the LCD to display.

**Components**
ESP32, breadboard, jumper wires, sensor/resistor, LCD, I2C backpack/interface module (to make your life easier), a computer/laptop with Arduino IDE installed, Wi-Fi.

_Optional_: LEDs, 330 Ohms resistors (to limit current)

**Libraries**
HD44780 by Bill Perry

Add any sensor libraries as needed.

**How it works:**
The ESP32 will connect to a Wi-Fi, process and collect the data such as anything sensor-related (temp, humidity, etc), and also anything analogic (resistance, voltage, etc). It will then send the data into Google Sheet using Apps Script's Web URL with proper format as coded in the Apps Script.

In Google Sheet, which should be properly titled, as the title for the document and the sheet itself are vital and used in the coding. Hereby they are titled "ESP32_Google_Spreadsheet" and "ESP32_Google_Sheets_Sheet".

In Apps Script, designate the correct columns and rows that you write the data in, and make sure you correct the timezone as well if needed.

After writing data into Google Sheet, the ESP32 which is connected to the sensor/resistor, a LCD, and a Wi-Fi, will start reading the latest data that was written onto Google Sheet. It will then display the data onto the LCD with expected format. To change the data you want to read, go to the last section of Apps Script code and change the range of 'all_data'.
