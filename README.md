# ESP8266 based Arduino wardriving


## What is this?
A simple/cheap hardware + software setup to do wardriving trips and store as much information as we can on a SD card, using a small Arduino box.

## What do we need?
* [$2.98](http://www.ebay.com/itm/222612803340) ESP8266 board (NodeMCU v3 works great)
* [$0.99](http://www.ebay.com/itm/261720518170) Arduino SD Card shield + SD card (a 10 minute trip could generate a 250KB file)
* [$4.21](http://www.ebay.com/itm/142233250679) Blox GY-NEO6MV2 GPS board
* [$3.07](http://www.ebay.com/itm/222311849398) HD44780 i2c LCD screen
* [$1.25](http://www.ebay.com/itm/332023213881) USB powerbank

## What does this do?
* Checks for a working SD Card
* Waits for GPS signal
* Collects all WiFi signals on 2.4Ghz on every (configurable) GPS sample
* Stores this information as a CSV file

## What does this doesn't do?
* This doesn't capture pcap files due power limitations
* This doesn't attack any network

## What does this need?
* A better/sorted insertion on CSV files to get rid of duplicate network entries
* Fix some race conditions
* A PCB design that I'm working on

## What do I need to configure?
Nothing, but you can:
* Setup CS pin for SD card module on *ARDUINO_USD_CS* variable
* Change log file prefix and suffix on *LOG_FILE_PREFIX* and *LOG_FILE_SUFFIX*
* Remove or add columns to CSV datalog on *log_col_names*
* Define GPS log rate time on *LOG_RATE* (milliseconds)
* Define GPS TX/RX pins on *ARDUINO_GPS_RX* and *ARDUINO_GPS_TX*
