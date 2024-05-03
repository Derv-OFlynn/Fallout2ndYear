# <mark style="background: #69E772;">03. Data Transmission</mark>

#DataComms 

### <mark style="background:#69E772;">Model of Communications System:</mark>

![](https://i.imgur.com/lP2Albf.png)


### <mark style="background:#69E772;">Example of Communications System:</mark>

![](https://i.imgur.com/IAlUgAE.png)


### <mark style="background:#69E772;">Data Transmission:</mark>

Data Transmission occurs between the <mark style="background:#69E772;">transmitter</mark> and the <mark style="background:#69E772;">receiver</mark>

The data is <mark style="background:#69E772;">encoded</mark> onto a <mark style="background:#69E772;">transmission signal</mark> and the signal is transmitted across a <mark style="background:#69E772;">transmission system</mark>

<mark style="background:#69E772;">Encoding</mark> involves changing a characteristic of the signal to represent the data. The more changes that can be made to a signal increases the amount of data that can be transmitted

### <mark style="background:#69E772;">Transmission Signals:</mark>

The <mark style="background:#69E772;">transmission signal</mark> is either some form of electro-magnetic wave (<mark style="background:#69E772;">EM</mark>) or an electrical signal:
- Examples of e-m waves used for data transmission include radio waves, light waves, microwaves
- Examples of electrical signals include Alternating-Current (A/C), Voltage pulses, etc.
- The simplest form of a signal is a <mark style="background:#69E772;">Sine Wave</mark>
	

### <mark style="background:#69E772;">Transmission System:</mark>

In its simplest form, a <mark style="background:#69E772;">transmission system</mark> is some type of transmission medium which may be either:
- <mark style="background:#69E772;">Guided</mark>, e.g. Electric Cable, Fibre Optic Cable
- <mark style="background:#69E772;">Unguided</mark>, e.g. Electromagnetic Waves in Space
	

### <mark style="background:#69E772;">Successful Data Transmission:</mark>

The successful transmission of data depends upon <mark style="background:#69E772;">two</mark> factors:
- The <mark style="background:#69E772;">quality</mark> of the transmission signal
- The <mark style="background:#69E772;">characteristics</mark> of the transmission system/medium

### <mark style="background:#69E772;">Signal Characteristics:</mark>

<mark style="background:#69E772;">Continuous:</mark>
- No breaks or discontinuities within signal
- Example is a speech signal
	
<mark style="background:#69E772;">Discrete:</mark>
- Contains a finite number of discrete values
- Example is computer or binary data
	
<mark style="background:#69E772;">Periodic:</mark>
- Repeats itself after some fixed time
	
<mark style="background:#69E772;">Aperiodic:</mark>
- No repetition of signal pattern
	

### <mark style="background:#69E772;">Continuous and discrete signals:</mark>

![](https://i.imgur.com/XztBxPT.png)


### <mark style="background:#69E772;">Periodic Signals:</mark>

![](https://i.imgur.com/MUyk26B.png)

### <mark style="background:#69E772;">Sine Wave Characteristics:</mark>

The general equation applies:

``s(t) = Asin(2π.ft + Ø)

Where:
- <mark style="background:#69E772;">Amplitude (A)</mark> is the peak value of the waveform
- <mark style="background:#69E772;">Frequency (f)</mark> is the number of repetitions per sec. Measured in <mark style="background:#69E772;">Hertz (Hz)</mark>. Inverse of the period
- <mark style="background:#69E772;">Phase (Ø)</mark> is a measure of the relative position within a cycle of a signal. Measured in degrees or radians

All three characteristics can be varied to give different wave forms

### <mark style="background:#69E772;">Varying Sine Waves Characteristics:</mark>

![](https://i.imgur.com/lrluwqx.png)


### <mark style="background:#69E772;">Addition of Frequency Components:</mark>

![](https://i.imgur.com/Ywr51LZ.png)


### <mark style="background:#69E772;">Time Domain and Frequency Domain:</mark>

![](https://i.imgur.com/fRjMNha.png)

### <mark style="background:#69E772;">Fourier Analysis:</mark>

By <mark style="background:#69E772;">Fourier Analysis</mark>, <mark style="background:#69E772;">any</mark> signal can be exposed as the <mark style="background:#69E772;">sum</mark> of a <mark style="background:#69E772;">series</mark> of sinusoidal components of different frequencies

<mark style="background:#69E772;">IMPORTANT:</mark> The <mark style="background:#69E772;">effects</mark> of <mark style="background:#69E772;">transmission media</mark> on a <mark style="background:#69E772;">signal</mark> can be analysed by examining the effects on these <mark style="background:#69E772;">component sinusoids</mark>

### <mark style="background:#69E772;">Signalling Concepts:</mark>

<mark style="background:#69E772;">Spectrum:</mark>
- The range of frequencies contained in a signal
- For the above sample signal the spectrum ranges from f1 to 3f1
	
<mark style="background:#69E772;">Absolute Bandwidth = width of spectrum</mark>
- For the above sample signal, the bandwidth is 2f
	
<mark style="background:#69E772;">Effective bandwidth:</mark>
- Signals with sharp rising and falling edges in the time domain have very wide absolute bandwidth
- Most energy is contained in a relatively narrow band called the effective bandwidth

<mark style="background:#69E772;">DC Component:</mark>
- Signals with a component at zero frequency

### <mark style="background:#69E772;">Full Representation of Square Wave:</mark>

![](https://i.imgur.com/EFtKBhS.png)


### <mark style="background:#69E772;">Transmission System Characteristics:</mark>

All Transmission Systems (Tx Systems) are limited in the range of signal frequencies that they can carry

This restriction is known as the <mark style="background:#69E772;">system bandwidth</mark> and results from:
- The physical properties of the components that comprise the system
- The physical properties of matter and energy	

### <mark style="background:#69E772;">Relationship between data rate and bandwidth:</mark>

The <mark style="background:#69E772;">bandwidth</mark> of a <mark style="background:#69E772;">transmission system</mark> can be described as "the fastest continuously oscillating signal that can be transmitted across the transmission. It is represented in <mark style="background:#69E772;">Hertz</mark> (Hz)"

The effects of System Bandwidth is to limit the speed of transmission of data (<mark style="background:#69E772;">Data rate</mark>)

![](https://i.imgur.com/WRqd3xH.png)


<mark style="background:#69E772;">Explanation:</mark>
- The Source transmits a digital signal with the bit pattern shown (010000100)
- The first Tx System imposes a significant BW restriction on the signal such that only one component passes through
- The last Tx System allows more components to pass through, which results in a more 'readable' signal
	

### <mark style="background:#69E772;">Relationship between Data Rate & Bandwidth:</mark>

This limitation has a direct effect on the maximum <mark style="background:#69E772;">data rate</mark> achievable across a transmission system

Consider a transmission system that has a bandwidth of 15MHz

Examples given in class use simplistic sine waves and composite waveforms to demonstrate the effect of Tx Sys BW on the received signals:
- <mark style="background:#69E772;">Observation:</mark> To preserve the shape of the received signal requires the speed of transmission of the signal (frequency) to be reduced
- The same effects can be shown for more complicated signals such as a pulse train


### <mark style="background:#69E772;">Varying the Data Rate:</mark>

![](https://i.imgur.com/Q6howBi.png)

![](https://i.imgur.com/FnuODQf.png)

![](https://i.imgur.com/nlkgbuZ.png)


The slide shows a pulse train representing a binary sequence

The table shows how many harmonics are received by the receiver at various data rates

The faster the pulse rate is transmitted, the less harmonics are received at the Receiver. This reduces the intelligibility of the signal

For a <mark style="background:#69E772;">transmission system</mark>, the greater the bandwidth of the <mark style="background:#69E772;">system</mark>, the higher the data rate that can be achieved

For a <mark style="background:#69E772;">transmission signal</mark>, the greater the speed (frequency) of the <mark style="background:#69E772;">signal</mark>, the greater the bandwidth and the more data that can be transmitted

### <mark style="background:#69E772;">Conclusions:</mark>

In <mark style="background:#69E772;">digital</mark> transmission, the <mark style="background:#69E772;">square wave</mark> is usually used to encode data

From previous discussions:
- A <mark style="background:#69E772;">digital</mark> waveform has an <mark style="background:#69E772;">infinite</mark> number of harmonics (frequency components)
- All Tx Systems have a <mark style="background:#69E772;">limited bandwidth</mark>
- The more limited the bandwidth of the Tx System, the greater the <mark style="background:#69E772;">distortion</mark> i.e. <mark style="background:#69E772;">not all</mark> components will get through

In general for a <mark style="background:#69E772;">digital signal</mark>, carrying data at a rate of <mark style="background:#69E772;">W bps</mark>, very good representation can be achieved with a Tx system bandwidth of <mark style="background:#69E772;">W/2 Hz</mark>.
- For example, if the data rate of a signal is fixed at <mark style="background:#69E772;">2Mbps</mark> the Tx System Bandwidth required to facilitate this data rate would be approximately <mark style="background:#69E772;">1Mhz</mark>
- Be aware that this approximation is a guide and not an absolute value

Hence, there is a relationship between <mark style="background:#69E772;">data rate</mark> and <mark style="background:#69E772;">Tx System Bandwidth</mark>

The next slides show the effects of increasing the data rate across a Tx System of fixed bandwidth

### <mark style="background:#69E772;">Data and Signals - Concepts:</mark>

Consider the following entities:
- <mark style="background:#69E772;">Data:</mark> Entities that convey meaning
- <mark style="background:#69E772;">Signal:</mark> Electromagnetic wave with encoded data
- <mark style="background:#69E772;">Transmission System:</mark> The entity over which the signal is transmitted

Each entity can be considered in terms of <mark style="background:#69E772;">Analogue</mark> or <mark style="background:#69E772;">Digital</mark> as follows

<mark style="background:#69E772;">Analogue Data:</mark> Take on continuous values on some interval e.g. voice, temperature, pressure, etc.

<mark style="background:#69E772;">Digital Data:</mark> Take on discrete values e.g. integers, text

### <mark style="background:#69E772;">Signals - Defined:</mark>

<mark style="background:#69E772;">Analogue Signal:</mark> Continuously varying electromagnetic wave (representing data) that may be propagated over a transmission medium

<mark style="background:#69E772;">Digital Signal:</mark> Sequence of discrete, discontinuous voltage pulses (representing data) that may be propagated over a transmission medium

### <mark style="background:#69E772;">Data Transmission - Defined:</mark>

Data Transmission is the communication of data by the propagation and processing of signals
- <mark style="background:#69E772;">Analogue data</mark> can be conveyed by an <mark style="background:#69E772;">analogue signal</mark> e.g. ordinary telephone
- <mark style="background:#69E772;">Digital data</mark> can also be conveyed by an <mark style="background:#69E772;">analogue signal</mark> when a <mark style="background:#69E772;">MODEM</mark> is used
- <mark style="background:#69E772;">Analogue data</mark> can be conveyed by a <mark style="background:#69E772;">digital signal</mark> when a <mark style="background:#69E772;">CODEC</mark> is used
- <mark style="background:#69E772;">Digital data</mark> can be conveyed by a <mark style="background:#69E772;">digital signal</mark> e.g. a digital transmitter


### <mark style="background:#69E772;">Analogue Transmission - Defined:</mark>

<mark style="background:#69E772;">Analogue transmission</mark> is the propagation of analogue signal <mark style="background:#69E772;">only</mark> i.e. A physical quantity that changes continuously as a function over time (e.g. voltage)

There is <mark style="background:#69E772;">no</mark> regard to the <mark style="background:#69E772;">content</mark> of the signal

As the transmitted analogue signal becomes <mark style="background:#69E772;">attenuated</mark> with distance, an <mark style="background:#69E772;">amplifier</mark> can extend the range

However, this also boosts noise so the signal eventually becomes <mark style="background:#69E772;">distorted</mark>

### <mark style="background:#69E772;">Digital Transmission - Defined:</mark>

Digital transmission is the propagation of:
- Analogue (with encoded digital) <mark style="background:#69E772;">or</mark> digital signals
- Digital transmission have regard to the encoded data
	
As the transmitted digital becomes <mark style="background:#69E772;">attenuated</mark> with distance a repeater can extend the range

A repeater receives the attenuated signal, recovers the digital data and re-transmits a new signal with no noise added

### <mark style="background:#69E772;">Analogue V Digital Transmission:</mark>

Digital is superior:
- Low cost of digital electronics
- <mark style="background:#69E772;">Data Integrity:</mark> Signal can be maintained free of noise
- <mark style="background:#69E772;">Capacity Utilisation:</mark> Different digital signals can be "multiplexed" and "de-multiplexed" more easily and thus share a signal channel
- <mark style="background:#69E772;">Security:</mark> Encryption can be more easily applied to digital data
- <mark style="background:#69E772;">Integration:</mark> Digitised analogue data can be mixed with digital and share the same facilities as other digital data

# <mark style="background: #69E772;">04. Data Impairments</mark>


A transmitted signal becomes distorted due to <mark style="background:#69E772;">transmission impairments</mark>

For <mark style="background:#69E772;">Analogue</mark> signals, the quality can become <mark style="background:#69E772;">degraded</mark>

For <mark style="background:#69E772;">Digital</mark> signal, <mark style="background:#69E772;">bit errors</mark> can be introduced

Types of Impairment:
- Attenuation and Attenuation distortion
- Noise

### <mark style="background:#69E772;">Attenuation and Attenuation distortion:</mark>

<mark style="background:#69E772;">Attenuation</mark> - where the signal becomes weaker over distance

<mark style="background:#69E772;">Attenuation</mark> is a function of <mark style="background:#69E772;">frequency</mark>

<mark style="background:#69E772;">Attenuation distortion</mark> affects the <mark style="background:#69E772;">intelligibility</mark> of the received signal, especially <mark style="background:#69E772;">signal pulses</mark> which can become distorted

One technique for addressing this problem is to use equalising amplifiers. This boosts higher frequency components which evens out signal pulses

![](https://i.imgur.com/eB2EcNS.png)


### <mark style="background:#69E772;">Noise:</mark>

<mark style="background:#69E772;">Noise</mark> is the insertion of unwanted signals onto the transmission signal. Its effect is to distort the signal during transmission (refer to diagram on slide entitled Effects of Impulse and Thermal Noise)

It particularly affects digital signals, the greater the noise the greater the <mark style="background:#69E772;">bit error rate</mark>

<mark style="background:#69E772;">Three categories of Noise:</mark>
- Thermal Noise
- Cross talk
- Impulse Noise	

### <mark style="background:#69E772;">Thermal Noise:</mark>

Caused by the thermal agitation of electrons within a conductor

<mark style="background:#69E772;">Characteristics:</mark>
- Present in all electronic devices and conductors
- It is a function of <mark style="background:#69E772;">temperature</mark> i.e. increased temperature leads to increase in thermal noise
- It is uniformly distributed across frequency spectrum, also known as <mark style="background:#69E772;">white noise</mark>
	
The presence of Thermal Noise places an upper limit on the data carrying capacity of a transmission system
- Must ensure that the strength of the data-carrying signal is much greater than the noise signal
- Term used to describe this relationship is <mark style="background:#69E772;">SNR</mark> (Signal to Noise Ratio)


### <mark style="background:#69E772;">Cross Talk:</mark>

Unwanted <mark style="background:#69E772;">coupling</mark> between signals on neighbouring transmission paths
- The term <mark style="background:#69E772;">coupling</mark> means connecting without actually touching
- Coupling can occur between cables in close proximity or between radio signals close to the same frequency	

### <mark style="background:#69E772;">Impulse Noise:</mark>

Irregular pulses or <mark style="background:#69E772;">noise spikes</mark> of short duration and high amplitude

<mark style="background:#69E772;">Causes:</mark>
- Lightning and heavy static charges
- Switching of heavy electrical loads
- Faults within the transmission system
	
Analogue signals are less affected by this type of noise, e.g. a voice transmission, whilst affected by impulse noise, can still be received intelligibly

Digital signals are very susceptible, it can lead to corruption of data i.e. changing one to zero and vice versa

![](https://i.imgur.com/DhD955V.png)


### <mark style="background:#69E772;">Channel Capacity:</mark>

Channel capacity allows us to study the inter-relationships between Signal BW, System BW and Signal Impairments

<mark style="background:#69E772;">Channel Capacity</mark> is the maximum rate at which data can be transmitted over a communications path or channel

The objective is to make the best use of a given bandwidth/channel, however channel capacity is limited in practice by transmission impairments of which the main constraint is <mark style="background:#69E772;">noise</mark>

Two distinguished scientists on this topic: Nyquist and Shannon

### <mark style="background:#69E772;">Nyquist's Noise Free Channel:</mark>

According to Nyquist, the limitation on data rate is simply the bandwidth of the channel

<mark style="background:#69E772;">Nyquist's theorem:</mark>

![](https://i.imgur.com/27E61eO.png)

- <mark style="background:#69E772;">C</mark> = Maximum data rate measured in bits per sec
- <mark style="background:#69E772;">B</mark> = Bandwidth of the transmission system Hz
- <mark style="background:#69E772;">M</mark> = Number of discrete states in digital signal


### <mark style="background:#69E772;">Limitation on Channel Capacity:</mark>

It appears from Nyquist's theorem that any data rate is achievable by:
- Increasing the bandwidth of the system
- Encoding more bits per cycle

However, as the Data Rate increases:
- The <mark style="background:#69E772;">bit error rate</mark> increases
- It becomes more and more difficult for the receiver to distinguish different signal <mark style="background:#69E772;">states</mark>

Noise and other transmission impairments put a practical limit on M, hence the maximum Data Rate achievable

### <mark style="background:#69E772;">Noise and Data Rate:</mark>

Noise distorts a signal during transmission

The greater the noise the greater the bit error rate for digital signals

Key factor is Signal to Noise Ration (SNR)

Measured in Decibels

![](https://i.imgur.com/qj2aUYq.png)

<mark style="background:#69E772;">S</mark> = Average signal power

<mark style="background:#69E772;">N</mark> = Average noise power

### <mark style="background:#69E772;">Shannon's Noisy Channel:</mark>

Shannon extended Nyquist's work and took into account the effects of <mark style="background:#69E772;">noise</mark>

Shannon's Capacity Formula:

![](https://i.imgur.com/rBu9A21.png)

<mark style="background:#69E772;">Observations:</mark>
- Increasing the bandwidth increases the maximum data rate
- Increasing the noise reduces the maximum data rate
- Shannon's Law defines an upper limit on the achievable data rate
- Hence the data rate is limited by <mark style="background:#69E772;">bandwidth</mark> and <mark style="background:#69E772;">noise</mark>

### <mark style="background:#69E772;">Limitation on Channel Capacity:</mark>

According to Shannon the maximum data rate achievable is determined by:
- The bandwidth of the system/channel and,
- The noise on the channel
- i.e. every system/channel has a maximum data carrying capacity that cannot exceeded

This is a more practical and realistic reflection on Channel Capacity as it takes into consideration the effects of noise

# <mark style="background: #69E772;">05. Transmission Media</mark>

The Transmission Media is the path along which the signal travels

The type of medium determines the type of signal to be used and can affect the reliability of communications

### <mark style="background: #69E772;">Conventional networks use copper wire:</mark>

Low resistance to electrical current

The terms <mark style="background:#69E772;">copper</mark> and <mark style="background:#69E772;">wire</mark> are used interchangeably

Prone to interference from other wires close-by

This interference can be minimised by using <mark style="background:#69E772;">Twisted Pair</mark> wiring and <mark style="background:#69E772;">co-axial</mark> cable

### <mark style="background:#69E772;">TP, Co-ax and Optical Fibre Cables:</mark>

![](https://i.imgur.com/z5QHRov.png)


### <mark style="background:#69E772;">Twisted Pair:</mark>

<mark style="background:#69E772;">Characteristics:</mark>
- Comprised of 2 insulated copper wires twisted together
- These twists reduce cross talk
- Typically many pairs are bundled in a protective sheath
- Very cheap and easy to use
- BW: Cat 3 = 16MHz, Cat 5 = 100MHz, Cat 6 = 250MHz

<mark style="background:#69E772;">Applications:</mark>
- In office buildings for phone and computer connectivity
- Residential telephone - the local loop

![](https://i.imgur.com/eV41Hv4.png)


### <mark style="background:#69E772;">Coaxial Cable:</mark>

<mark style="background:#69E772;">Characteristics:</mark>
- Comprised of central copper conductor and a hollow outer cylindrical conductor
- A surrounding sheath holds the inner conductors in place
- BW: 1GHz

<mark style="background:#69E772;">Applications:</mark>
- Cable TV
- Long distance telephone network
- Computer connectivity (LANs)

![](https://i.imgur.com/MlyqsRi.png)


### <mark style="background:#69E772;">Optical Fibre:</mark>

<mark style="background:#69E772;">Characteristics:</mark>
- Comprised of thin, flexible, transparent glass fibre core
- This core is surrounded by glass or plastic cladding with a lower refractive index
- Outer sheath provides rigidity and protection
- Several fibres may be bound in a single jacket


Two types of light source used:
- <mark style="background:#69E772;">Light Emitting Diode</mark> (<mark style="background:#69E772;">LED</mark>) - low cost
- <mark style="background:#69E772;">Injection Laser Diode</mark> (<mark style="background:#69E772;">ILD</mark>) for higher data rates and greater distances
 ![](https://i.imgur.com/IbtWnBA.png)

<mark style="background:#69E772;">Applications:</mark>
- Long distance telephone connections
- Metropolitan trunks
- Rural exchange trunks
- Local loop
- LANs

### <mark style="background:#69E772;">Optical Fibre Vs Coaxial Cable:</mark>

Optical Fibre cables offer the following advantages over co-axial cables:
- Electromagnetic isolation i.e. no interference
- Lower attenuation, hence greater repeating spacing (50km vs 5km for copper)

Greater Capacity - up to 10 Gbps over many kms

Requires only single core for complete circuit, hence smaller in size, lighter in weight

### <mark style="background:#69E772;">Wireless Transmission:</mark>

<mark style="background: #69E772;">Two configurations:</mark>
- <mark style="background:#69E772;">Omni-directional</mark> e.g. radio station
- <mark style="background:#69E772;">Directional</mark> e.g. microwave/satellite links

##### <mark style="background:#69E772;">Radio Transmission Characteristics:</mark>

Networks that use EM radio waves are known as <mark style="background:#69E772;">Radio Frequency</mark> (<mark style="background:#69E772;">RF</mark>) networks

There is no physical connection between stations

Transmission is achieved using an antenna

### <mark style="background:#69E772;">Terrestrial Microwave Characteristics:</mark>

Microwaves travel at higher frequency than RF. Typically 2-40 GHz

This higher frequency allows for a larger bandwidth which implies a high data rate e.g. 120 Mbps

Waves are focused into a narrow beam by a parabolic dish antenna

Waves are received by a similar dish antenna

Line of sight required (although not always possible)

Prone to interference from rainfall and other dishes

Prone to misalignment in storm

### <mark style="background:#69E772;">Terrestrial Microwave Links:</mark>

![](https://i.imgur.com/iRInPzg.png)


### <mark style="background:#69E772;">Terrestrial Microwave Applications:</mark>

Back-to-back installations used on long haul links (this is their main application)

Also used where there are difficulties laying cables e.g. mountain top installations

Very common with mobile phone networks e.g. the 3 Network relies heavily on MW links

### <mark style="background:#69E772;">Satellite Microwave (aka Satellites):</mark>

Satellites can link two or more ground stations i.e. they act as a <mark style="background:#69E772;">relay</mark>

Satellites use two different bands (frequency ranges) to communicate:
- Different frequencies allow full duplex comms
- There are <mark style="background:#69E772;">up</mark> and <mark style="background:#69E772;">down</mark> links each using different frequencies

Two types of Satellite (<mark style="background:#69E772;">GEOs</mark> and <mark style="background:#69E772;">LEOs</mark>):
- <mark style="background:#69E772;">GEOs</mark> remain stationary over a point on earth
- <mark style="background:#69E772;">LEOs</mark> move rapidly across the sky

### <mark style="background:#69E772;">Satellites:</mark>

<mark style="background:#69E772;">Characteristics:</mark>
- Originally operated in range 1-10GHz
- The 4/6 GHz is now saturated
- 12/14 GHz now open for service
- Inherent propagation delay, approx 0.25sec

<mark style="background:#69E772;">Applications:</mark>
- Television distribution,
- Long distance telephone transmission
- Private business networks

### <mark style="background:#69E772;">The Iridium Satellite Network:</mark>

![](https://i.imgur.com/t4PWxzd.png)

![](https://i.imgur.com/tTTPBlW.png)

### <mark style="background:#69E772;">Starlink:</mark>

![](https://i.imgur.com/egnJVHY.png)

### <mark style="background:#69E772;">Infrared:</mark>

<mark style="background:#69E772;">Characteristics:</mark>
- Does not require antennae or special license to operate,
- Uses LED,
- Very low cost
- Cannot penetrate obstacles i.e. requires line of sight

##### <mark style="background:#69E772;">Applications:</mark>
- Remote controls,
- Computer-to-computer connectivity e.g. mobile phones

### <mark style="background:#69E772;">Bluetooth:</mark>

<mark style="background:#69E772;">Characteristics:</mark>
- Uses the 2.4 GHz ISM band (Industrial, Scientific and medical)
- Uses low power which implies a short range (approx. 10m)
- Comprises 79 channels of 1 MHz each,
- Uses a type of encoding called FSK which provides for 1 bit per Hz i.e. 1 Mbps per channel

<mark style="background:#69E772;">Applications:</mark>
- Connections of a variety of computing devices

### <mark style="background:#69E772;">The E-M Spectrum:</mark>

![](https://i.imgur.com/VAEu6Ie.png)
