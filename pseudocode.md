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

#### User Story
As a patron, I want to wash my hands so they will be clean.

#### Objects / Data Structures
* Sink
* Soap
  * Dispenser (If > 0)
* Hands = 2
* Water
* Towel
* Dirt
  * If true
* If any not present
  * String "Function cannot be completed"

### START

#### PROGRAM washyourhands

INIT()

IF (water = true) {
    Patron.turnOn();
}

IF (soap > 0) {
    Patron.dispense();
}

Patron.rub();
IF (dirt = true) {
    WHILE (dirt = true) {
        Patron.rub();
        setInterval((dirt=false), 30000);
    }
ELSE
    Patron.rub();
}

Patron.dry();

### END