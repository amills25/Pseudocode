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
  * String "Operation cannot be completed"

### START

#### PROGRAM washyourhands

INIT()

IF (water = true) {
    Patron.turnOnSink();
ELSE
    alert("Operation cannot be completed.");
}

IF (soap > 0) {
    Patron.dispenseSoap();
ELSE
    alert("Operation cannot be completed.");
}

Patron.scrub();
IF (hasDirt = true) {
    WHILE (hasDirt = true) {
        Patron.rubHands();
        setInterval((dirt=false), 30000);
    }
ELSE
    Patron.rubHands();
}

Patron.dryHands();

#### End program

#### Define Objects, Functions
* Patron
  * turnOnSink
  * dispenseSoap
  * rubHands
  * dryHands

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