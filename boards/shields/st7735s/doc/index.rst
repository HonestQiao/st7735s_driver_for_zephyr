.. _st7735s_generic:

Generic ST7735S Display Shield
##############################

Overview
********

This is a generic shield for display shields based on ST7735S display
controller. More information about the controller can be found in
`ST7735S Datasheet`_.

Pins Assignment of the Generic ST7735S Display Shield
=====================================================

+-----------------------+--------------------------------------------+
| Arduino Connector Pin | Function                                   |
+=======================+===============+============================+
| D8                    | ST7735S Reset |                            |
+-----------------------+---------------+----------------------------+
| D9                    | ST7735S DC    | (Data/Command)             |
+-----------------------+---------------+----------------------------+
| D10                   | SPI SS        | (Serial Slave Select)      |
+-----------------------+---------------+----------------------------+
| D11                   | SPI MOSI      | (Serial Data Input)        |
+-----------------------+---------------+----------------------------+
| D12                   | SPI MISO      | (Serial Data Out)   None   |
+-----------------------+---------------+----------------------------+
| D13                   | SPI SCK       | (Serial Clock Input)       |
+-----------------------+---------------+----------------------------+

Current supported displays
==========================

+----------------------+------------------------------+
| Display              | Shield Designation           |
|                      |                              |
+======================+==============================+
| luatos             | st7735s_128x160          |
| 128x160 18bit TFT    |                              |
+----------------------+------------------------------+

Requirements
************

This shield can only be used with a board that provides a configuration
for Arduino connectors and defines node aliases for SPI and GPIO interfaces
(see :ref:`shields` for more details).

Programming
***********

Set ``-DSHIELD=st7735s_128x160`` when you invoke ``west build``. For example:

.. zephyr-app-commands::
   :zephyr-app: samples/subsys/display/lvgl
   :board: nrf52840dk_nrf52840
   :shield: st7735s_128x160
   :goals: build

References
**********

.. target-notes::

.. _ST7735S Datasheet:
   https://www.crystalfontz.com/controllers/Sitronix/ST7735S/437/
