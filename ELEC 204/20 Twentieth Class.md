# Twentieth Class
* Laplace transform in circuit analysis
  * Use s-domain equivalent
  * Find expression for desired signal in $s$ domain
  * Use inverse laplace transform to go back
  * Time domain equivalents
    * Resistor 
      * $V=RI\Rightarrow V(s)=RI(s)$
    * Inductor 
      * $V=L\frac{di}{dt}\Rightarrow V(s)=L(sI(s)-I_0$
      * $i=\frac1L\int vd\tau+I_0\Rightarrow I(s)=\frac1{Ls}V(s)+\frac{I_0}s$
    * Capacitor
      * $i=C\frac{dv}{dt}\Rightarrow I(s)=C(sV(s)-V_0)$
      * $V=\frac1C\int id\tau+V_0\Rightarrow V=\frac1{Cs}I+\frac{V_0}s$
* Transistors
  * Comes from words transfer resistor
  * Can be classified as
    * Bipolar junction transistors (BJTs)
    * Field effect transistor (FETs)
      * Depletion mode FETs (e.g. JFETs)
      * Enhancement mode FETs (e.g. MOSFETs)
  * Invented in Bell Labs in 1955
  * First integrated circuit created in 1958
  * First planar integrated circuit 1961
* Moore's law
  * Says that number of transistors per chip doubles every 1.5-2 years
* Bipolar junction transistor
  * Three terminals
    * Emitter
    * Base Collector
  * Can works as either amplifier or switch
* Semiconductors
  * Three types
    * Intrinsic (pure)
    * p-type
      * More positive charges (holes with lack of electrons)
    * n-type
      * More negative charges (more electrons)
  * n and p types are made by introducing impurities with more or less valence electrons than Silicon's 4
  * By putting a p and n type together, you get a diode since current can only from p to n
* Transistor functionality
  * A transistor is a sandwich of a p type between two n types (pnp)
  * Base is middle p semiconductor, collector and emitter are two n types
  * Can also have two p with an n in the middle, in which case it is a pnp transistor
  * (for npn) When current from base to emitter, current from collector to emitter is much larger but proportional
  * Middle semiconductor usually thinner (or less impurities)
  * $I_C=\beta I_B$, usually $50\leq\beta\leq 500$
  * Can be modelled by a diode and a current source
  * For pnp except reverse
  * For BJT base emitter is forward biased and collector base junction is reverse biased
    * For npn collector has to be greater voltage than base
    * Need $V_{CE}\geq 0.2V$
* Amplification
  * Uses superposition of DC and time variant signal
  * DC sources set voltages and currents in BJT so that BE junction is on and BC junction is off
    * Called biasing the transistor
  * Three favoured ways of doing so
    * Common emitter (CE)
    * Common base (CB)
    * Common collector (CC)
  * In real world not perfectly linear function
  * Usually can write $y\approx\alpha_0+\alpha_1 x$
    * $\alpha_0$ can be considered operating bias point and $\alpha_1$ signal gain
    * $\Delta y\approx\alpha_1\Delta x$
* MOS transistors
  * Metal oxide semiconductor
  * Three terminals: gate, source and drain
  * Voltage of the gate determines the type of connection between source and drain
  * NMOS
    * $V_G$ high means device is on and D is shorted, $V_G$ means device is off and D & S are disconnected
    * Electrons go from source to drain
  * PMOS
    * $V_G$ high means device is off and D & S is shorted, $V_G$ means device is on and D are disconnected
    * Current flows from source to drain
  * There is a threshold voltage to turn "on"
    * If $V_{DS}\leq V_{GS}-V_{TH}$ we say the device is operating in riode (or linear) region
    * In this region $I_D=\mu_n\cdot C_{ox}\cdot \frac{W}{L}((V_{GS}-V_{TH})V_{DS}-\frac12V_{DS}^2)$
    * Past the triode region it is the active region
    * Lots of current equations, see the notes for them all
    * Can also say that to be in triode region $V_{TH}>V_{GD}$
* Digital logic
  * Can very easily make logic gates
* Transconductance
  * Drain current of MOSFET in saturation region is ideally a function of gate overdrive voltage (effective voltage)
    * In reality it depends on on $V_{DS}$
  * Makes sense to define a figure that indicates how well it converts voltage to current
  * $g_m=\frac{\partial I_D}{\partial V_{GS}}\bigg|_{V_{DS}}$
  * Transconductance drops if the device enters triode region
* Small signal models
  * $i_D=g_m\cdot v_{GS}+\frac{V_{DS}}{r_0}$
* Single stage amplifiers
  * Common source, common gate and common drain similar to BJT
  * Common source gives negative ground, common drain gives positive gain
* Frequency selective circuits
  * Output signal resides within frequency range
  * Ideally exclude all frequencies outside band of interest
* Transfer function is defined as ratio of laplace transform of output to it's input
  * $H(s)=\frac{Y(s)}{X(s)}$
  * To look at frequency, look at $s=j\omega\Rightarrow Y(j\omega)=H(j\omega)X(j\omega)$
  * $|Y(j\omega)|=|H(j\omega|\times|X(j\omega)|$
  * $\angle Y(j\omega)=\angle H(j\omega)+\angle X(j\omega)$
* Bode plot
  * Shows magnitude of transfer function vs. frequency
* Types of frequency selective circuits
  * Low pass
  * High pass
  * Band pass
  * Band reject
  * Band pass/rejects need more than 1st order
* First order system frequency response
  * $H(s)=\frac{\omega_p}{s+\omega_p}$
  * $|H(j\omega)|=\frac{|\omega_p}{\sqrt{\omega_p^2+\omega^2}}$
  * $\angle H(j\omega=-\arctan\frac{\omega}{\omega_p}$
  * Use decibels to measure
    * Normally $10\log P$, but since we're dealing with voltages instead $20\log V$ since $P=\frac{V^2}{R}$
  * Get $-10\log(1+(\frac{\omega}{\omega_p})^2)$
  * Asymptotically becomes $-20\log\frac{\omega}{\omega_p}$
  * $3dB$ frequency is when output drops by $\frac1{\sqrt2}$
* Second order frequency response
  * $H(s)=\frac k{(s+\omega_{P1})(s+\omega_{p2})}$
  * Asymptotically $20\log|k|-2\log|j\omega+\omega_{p1}|-20\log|j\omega+\omega_{p2}|$
  * $\angle H(j\omega)=-\arctan(\frac\omega{\omega_p})$
    * $\omega=\omega_p\Rightarrow -45\degree$
    * $\omega=0\Rightarrow 0\degree$
    * $\omega\to\infty\Rightarrow -90\degree$
    * Can assume angles are linear as rough assumption
* Transfer function combination
  * When series are in series transfer functions multiply, when in parallel they add
  * For OpAmps, transfer function is ratio between impedances