# Seventeenth Class
* Diodes
  * Can think of them like a single direction check valve
  * Only permit current flow in one direction
  * For ideal diode negative voltage results in no current, and positive current results in no voltage drop
  * If diode is conducting it is closed/on, when not conducting it is open/off
* Solving circuits with diodes
  * If only one diode in circuit assume it's off and check if the voltage across it is indeed negative (otherwise it is an open circuit)
  * If there are $N$ diodes, there are $2^N$ possibilities instead of just two to check
* Real diodes
  * Real voltage has approximately $0.7V$ drop even when forward biased
  * There is a breakdown at very high reversed biased voltage
* How diodes work
  * Diodes are made of semiconductors
    * e.g. silicon, germanium, ...
    * Semiconductors can either have a free electron or a hole (absence of electron)
  * Doped semiconductors have impurities intentionally diffused into the material to manipulate the majority of the charge carriers to be either electrons (n-type, negative doping) or holes (p-type, positive doping)
  * A diode is formed by a pn junction
    * At the junction, excess electrons on the n side combine with excess holes on the p side, forming a depletion region without charge carriers
    * Results in a barrier ($~0.7V$ for Si), if voltage of the anode (p side) is raised to overcome this barrier, the charge carriers can move again, giving rise to current
  * Because of the voltage barrier a better model for a diode is for $v_D=0.7$ when the voltage applied is $>0.7$ and $0$ otherwise
    * Can also have higher order approximation
    * Even when diode is "off" there is a small amount of current, referred to as reverse current