#### Deconstruct and Identify

* Does patron have running water?
* Does patron have soap?
* Does patron have towel?
* Is there dirt on hands?
* Turn on water
* Use hand one to add soap to hand 2
* Rub hands together until soap on hand 1 = soap on hand 2
* IF dirt on hands, rub hands together under water until dirt is gone
* OR if no dirt, rub hands together under water until soap is gone
* Dry hands on towel

##### Functionality
As a patron, I want to wash my hands so they will be clean.

1. Patron turns on water.
2. Is there soap?
3. Patron puts soap on hands.
4. Is there dirt on hands?
5. Patron scrubs dirt and/or soap off hands under water until gone.
6. Patron dries hands.

##### Objects / Data Structures
* Sink (boolean)
* Soap
  * Dispenser (If > 0)
* Hands = 2
* Water (boolean)
* Towel = 1
* Dirt (boolean)
* If any of the above are not present
  * String "Operation cannot be completed"

### START

#### PROGRAM washyourhands

INIT()

```javascript
IF (water = true) {
    patron.turnOnSink();}
ELSE {
    alert("Operation cannot be completed.");
}
```

```javascript
IF (soap > 0) {
    patron.dispenseSoap();}
ELSE {
    alert("Operation cannot be completed.");
}
```

Patron.scrub(); 
>(Would contain something like the below code)
```javascript
IF (hasDirt = true) {
   WHILE (hasDirt = true) {
       patron.rubHands();
       setInterval((hasDirt = false), 30000);}
   }
}   
ELSE {
   patron.rubHands();
}
```
patron.dryHands();

#### End program

#### Define Objects, Functions
* patron
  * turnOnSink
  * dispenseSoap
  * rubHands
  * dryHands
  * hasDirt

* INIT function
  * CREATE hand 1, hand 2
  * CREATE soap
  * CREATE patron
  * CREATE hasDirt
  * CREATE towel
  * CREATE water
  
* turnOnSink
  * INIT
  * Add water to hands

* dispenseSoap
  * INIT
  * soap > 0
  * Add soap to hands

* scrub
  * INIT
  * IF hasDirt = true
  * WHILE rubHands(), then setInterval(30 seconds)
  * ELSE hasDirt = false, then rubHands()

* rubHands
  * INIT

* dryHands 
  * INIT
  * Subtract water from hands

### END