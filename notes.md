# warehousing

## description

This file to keep notes on the warehousing domain



## high level entities

* item (code, upc, ean, description, has_serial_nums, has_pallets, depletion_policy etc)
  * box distribution (e.g. box 1/2, 2/2)
  * quantity per condition code (new, openbox, bad etc)
  * quantity in time axis: available, reserved, expected
* location
  * id, maybe location type, maybe position for distances
  * (storage location, staging location, workstation location, door location etc)
* inventory
  * lowest level inventory tracking (metnally akin to SKU)
    * location
    * item
    * variant (e.g. blue instead of black)
    * serial number
    * lot number
    * individual carton identifier, if any
* orders
  * order type (incoming, outgoing)
* order-entities
  * either supplier with incoming or outgoing (RTV) orders,
  * or customers with outgoing or incoming (RMA) orders
* employees
* tasks
  * what to do on what carton/item, but whom, until when etc.


