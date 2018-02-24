# Aerovair
Homebuilt airplane you can drive home

# The mythical flying-car and the unabtanium affect 
There have been many attempts at making a "flying car", [so many, not worth listing](http://lmgtfy.com/?q=flying+car).  If one does absolutely everything perfectly, you end up with some chitty-chitty-contraotion that's a meager airplane and a poor excuse for an automobile.  So, let's start there with the bar set WAY WAY low.  If you are still reading, it's because you are ok with sacraficing modern automotive conveniance and the last 20% of an aircraft performance just so you can have one vehicle that is capable of parking in your garage, driving you to the nearest public airport so you can go flying.

There are three current "way out there" concept vehicles that have demonstrated this capability.  _BUT_... You won't see them unless you have over $500,000 USD handy _AND_ you're willing to wait 5+ years.  And to be honest, if history is an indicator, the _far_ better odds are on it never being built at any volume ever.

There is a proactive, do-it-yourself, alternative.  Build it!  Anyone can build/fly a homebuilt aircraft or build/drive a kit car right now, today.  So... what's stopping us?  It's a matter of engineering.

# Goals
## Initial
* Can fly up to 900 miles at 150mph
* Can drive up to 5 miles all electric on batteries
* Can run the gasoline motor to regenerate electricity to continue driving 
* Can Convert to and from flying and driving modes in under one minutes. 

## Future
* Clutched propeller so regen can occur without the propellor spinning
* Mode conversion is actuated and you don't have to leave the cockpit
* You can drive up to 600 miles without stopping

# A car that can fly or a plane that can drive?
One has to find a starting point and I like a plane that can drive.  Here's why...

* I purposely prejudice the primary mission as flying, not driving.  Driving is secondary to achieve improved logistics.
* It's much easier to take something lightweight (aircraft) and make it do more stuff (add weight) than the other way around.
* The fundamental engineering requirements of flight are orders of magnatude harder to achieve than the fundamentals of every-day driving.

# Airframe
The choice of homebuilt airframes is somewhat arbitrary, but the initial airframe will begin with a Van's RV-4.  For clarity this cesses to be refered to or associated in any way with a Vans series aircraft.  It will be a unique airframe using components Vans and others will manufacture.  This is similar to the approach Harmon Rocket has taken.

## What is staying the same..
* Empanage
* Fuselage 
* The majority of the wing structure

## What is being altered...
* Engine will be a gasoline-electric hybrid
* Landing gear - The stock engine-mount landing gear will be removed and converted to leaf-spring with linkage for steered main wheels.  The tailwheel will be fixed, large and driven by a modest electric motor.  This will give improved road stability landing/driving handling more like a Can-Am Spyder.  This should stability should lower the tricycle gear instability associated with ground-looping.
* Wing will be modified to support folding.  See folding wing and mode transition.
   
## Hinging
There are many ways to hinge a wing... Here are my goal "ilities":
* Driving visibility
* Transitionability
* Complexity
* Strength/Weight

# Powerplant
The powerplant includes gasoline engine, electric motor/generator, batteries, drive-wheel motor and all electronics to support those systems.

## Gasoline Engine
The ideal engine is one designed around the requirements of an aircraft but robust and extensible.  There are many choices and one could make good arguments for many other engine choices.  But for this project the Corvair was chosen;

* Readily available and commonly converted, which means there's a large audience of very hands-on knowledgable experts on the every aspect of this engine.
* Simplistic engine layout, intake on top, exhaust on the bottom, cam is always bathed in oil.  I like all that.
* Robust in two ways... It can take punishment, it was an aircraft-inspired automotive engine.  It can take an astonishing amount of abuse and continue to run.  It is robust in the ability to adapt it's core compoents.  I can easily attach a rear-mounted hybriding electric motor and it is directly connected to the shaft and transfering energy to the propeller.  No common aircraft engines have exposed rear shafts and adding a motor in the way would be difficult.

## Motors
A 40kw brushless DC motor will be adapted to fit to the rear of the engine to serve three functions;
* Start the motor
* Drive the crankshaft to increase power when required allowing the engine to use a larger more efficient prop
* Generate electricity to feed the primary high voltage battery system

A 20kw brushless DC motor will be attached to the fixed tailwheel.  This will drive the vehicle when running the engine (spinning prop) is inappropriate; congested areas or parking.  It will also allow for reverse speeds.  It will be strong enough to drive the vehicle at speeds up to 50mph.  Speeds above 50mph could easily be augmented by running the gas engine with the spinning prop in controlled highway environments and when road debris is not an imminent concern.   This same motor will provide primary braking for all normal braking.  A secondary emergecy "scrub" backup/parking brake will engage the tailwheel directly and mechanicaly.

## Battery
A 6kwh Lithium Iron Phosphate (LiFePo4) battery pack will be placed near the nose of the aircraft.  It can be ground charged by a built in 120/240vac charger for short trips, but ultimately serves to buffer the motor and provide limitted all-electric driving capability.

## Electronics
The gasoline engine will be fully electronically controlled and every motor will have an electronic inverter/controller.  They will be connected to the powerplant management computer which is responsible for the orchestration of all these systems to start, stop and run the engine and manage the flow and reserve of electricity to and from the motors and battery.

## Turbo electric compounding hybrid (TECH)
This is perhaps the most novel of systems.  The final efficiency innovations of the internal combusion engines, before the succession of jets in air transport, was something called "Turbo Compound".  This used the waste heat from the engine to spin a turbine that was carefully geared to feed energy back into the crankshaft.  This very complicated and high-maintenance device boosted the specific efficiency of the ICEs by up to 15%.

Due to it's cost complexity and mainteance the concept didn't stick and faded into aviation history.  But the idea is compelling and I'm going to revisit it with a modern twist.  The idea starts with an off-the-shelf turbocharger.  First, increase the size of the turbine so it overpowers the compresion blade.  Second add a small high RPM BLDC motor like one used in a R/C fan jet of approximately 9kw.

Adding this motor is critical, it performs three critical roles;
* Excess turbine energy can be extracted and fed to the battery and ultimately consumed by the engine-driven-motor.
* The BLDC can very precisely control RPM eliminates surging, stalling and overboost
* You can eliminate the throttle body. The compressor at low engine RPMs will be braked by the controller, restricting airflow incucing a partial vacuum as a throttle body would normally do.  The fuel can be directly injected upstream of the compressor blade and precisely metered by the engine-controller to mapping to an appropriate air-fuel-ratio (AFR) given the variables of temperature, atmospheric pressure, turbine and engine RPM and of course power demand.
