# warehousing

## description

This file to keep notes on the warehousing domain



## high level entities (nouns)

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


## high level processes (verbs)

* Standard outbound journey
  * fulfillment order creation (either customer, cross-docking, liquidation, return-to-vendor etc)
  * waving (optimal picking routes, allocating inventory)
  * picking (routes performed to pick things)
  * staging (things in packing stations or conveyors)
  * loading (things loaded in the truck, keep track of what is in what truck)
  * shipping (things marked shipped, out of inventory, historical entries etc)
 
* Standard inbound journey(s)
  * advanced shipping notice creation (from supplier, from returns of customer, from cross-docking etc)
  * anticipated inventory is tracked (even anticipated containers)
  * truckload appointment etc created
  * inventory received on dock
  * qc checks, dimensioning, weighing cartons, possible inbound value-added-services (e.g. overpack)
  * putaway
 
* Standard internal journey(s)
  * Cycle count (periodic, on a rolling cadence, on demand when picking is shorted etc)
  * Replenishment (from cold storage to more speedy picking shelves)
  * Directed moves ???

* Standard administration processes
  * User management
  * Forks / Vehicles management
  * Locations / Stations management
  * ...

