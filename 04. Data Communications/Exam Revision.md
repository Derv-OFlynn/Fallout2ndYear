#DataComms 


This course is concerned with the <mark style="background: #69E772;">communications problem</mark>

"How can two remote entities communicate with each other <mark style="background: #69E772;">effectively</mark> and <mark style="background: #69E772;">efficiently</mark>?"

### <mark style="background: #69E772;">Model of Communications Systems:</mark>

![](https://i.imgur.com/iyUq5EZ.png)

<mark style="background: #69E772;">Communications Model Components:</mark>
- <mark style="background: #69E772;">Source:</mark> Device that generates data
- <mark style="background: #69E772;">Transmitter:</mark> Transforms and encodes data
- <mark style="background: #69E772;">Transmission System:</mark> The physical system connecting the source and destination devices
- <mark style="background: #69E772;">Receiver:</mark> Performs reverse functions of transmitter
- <mark style="background: #69E772;">Destination:</mark> Receives the incoming data

<mark style="background: #69E772;">Course Topics:</mark>
    
- <mark style="background: #69E772;">Introduction:</mark> Communications Model/Tasks
- <mark style="background: #69E772;">Signal Analysis:</mark> Signalling concepts, Bandwidth concepts, Relationship between Data Rate and bandwidth
- <mark style="background: #69E772;">Data Transmission concepts:</mark> Digital versus analogue data/signals/systems
- <mark style="background: #69E772;">Transmission Impairments:</mark> Attenuation/Distortion/Noise
- Channel Capacity
- <mark style="background: #69E772;">Transmission Media:</mark> Wired/Wireless
- <mark style="background: #69E772;">Data Encoding:</mark> Digital/Analogue Data onto Digital/Analogue signals
- <mark style="background: #69E772;">Synchronus/Asynchronus</mark>
- Flow Control techniques
- Error Detection techniques
- Error Control techniques
- Sample Link Protocol
- Multiplexing
- Switching Networks
- <mark style="background: #69E772;">Local Area Networks:</mark> Topologies and operation, protocols, Access Control techniques

# <mark style="background: #69E772;">0.2 Data Transmission:</mark>
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

``s(t) = Asin(2π.ft + Ø)``

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

All Transmission Systems (Tx Systems) are limited in the range of signal frequencies that they can carry.

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
# <mark style="background: #69E772;">07. Data and Digital Signal Encoding:</mark>
### <mark style="background:#69E772;">Analogue Data/Digital Signals:</mark>

As stated before a <mark style="background:#69E772;">CODEC</mark> is used to generate a <mark style="background:#69E772;">Digital Signal</mark>:
- Hence this is the device to be considered here,
- This device was also used to encode digital data onto a digital signal:
- Recall the use of NRZ, Bipolar AMI and Manchester techniques

There are two encoding methods to consider:
- Pulse Code Modulation
- Delta Modulation

To encode <mark style="background:#69E772;">analogue data</mark> onto a <mark style="background:#69E772;">digital signals</mark> requires <mark style="background:#69E772;">two</mark> steps:
- Convert <mark style="background:#69E772;">analogue data</mark> into <mark style="background:#69E772;">digital data</mark>,
- Encode the <mark style="background:#69E772;">digital data</mark> onto a <mark style="background:#69E772;">digital signal</mark>

The first step requires the use of <mark style="background:#69E772;">Sampling</mark>:
- This is necessary as an Analogue Data signal has an infinite amount of data. Consequently, it is not feasible to send all of the Analogue Data.

Nyquist also did some work on sampling ⇒ The Sampling Theorem:
- “If a signal f(t) is sampled at regular intervals of time and at a rate higher than twice the highest signal frequency, then the samples will contain all the information necessary for the reconstruction of the original signal.”

### <mark style="background:#69E772;">Pulse Code Modulation:</mark>

The original analogue signal is <mark style="background:#69E772;">sampled</mark> at regular intervals to produce <mark style="background:#69E772;">PAMS</mark>

The PAMS are quantised, i.e. assigned a binary value

There are considerations to be given to each number of bits to use to represent each sample

Regardless of the number of bits chosen, there will always be some level of rounding
- This is known as <mark style="background:#69E772;">quantisation</mark>, which gives rise to <mark style="background:#69E772;">quantisation error</mark> or <mark style="background:#69E772;">quantising noise</mark>
- Hence, the original Analogue Data signal can <mark style="background:#69E772;">never</mark> truly be reproduced

Using PCM to encode voice data results in:
- A stream of 8-bit samples,
- Each sample is assigned an 8-bit value,
- Resulting in a Data Rate of 64kbps in Europe

![](https://i.imgur.com/dVco4cc.png)


### <mark style="background:#69E772;">Delta Modulation:</mark>

This technique involves the use of a <mark style="background:#69E772;">staircase function</mark>
- Here, the analogue signal is <mark style="background:#69E772;">approximated</mark> by a simple mathematical function
- At each sampling interval a positive or negative <mark style="background:#69E772;">quantisation step</mark> is added to the output

The result is a single binary digit for <mark style="background:#69E772;">each</mark> sample indicating a positive or negative slope in the original analogue signal

![](https://i.imgur.com/KHbBDq6.png)


### <mark style="background:#69E772;">Two Significant Parameters:</mark>

<mark style="background:#69E772;">Quantisation step delta (δ):</mark>
- Large delta <mark style="background:#69E772;">reduces</mark> <mark style="background:#69E772;">Slope Overload Noise</mark>
- Small delta <mark style="background:#69E772;">reduces</mark> <mark style="background:#69E772;">Quantisation Noise</mark>

<mark style="background:#69E772;">Sampling rate:</mark> Large rate <mark style="background:#69E772;">reduces</mark> noise but <mark style="background:#69E772;">increases</mark> data rate of output signal

<mark style="background:#69E772;">DM compared to PCM:</mark>
- DM is easier to implement
- PCM produces better SNR characteristics

### <mark style="background:#69E772;">Voice Data - Digital vs Analogue:</mark>

<mark style="background:#69E772;">Digital (PCM):</mark>
- Good voice reproduction with 256 quantisation levels i.e. 8-bit coding
- Required sampling rate of 8000 per second for 4000hz voice i.e. 64kbps voice channels
- 64kpbs voice channel requires approximately 32KHz. of BW

<mark style="background:#69E772;">Analogue (POTS):</mark>
- Voice channel requires approx. 4KHz. of BW

However, digital is still preferable to analogue for the following reasons

<mark style="background:#69E772;">Popularity increasing:</mark>
- Repeaters can be used with no additive noise
- Time-division multiplexing (TDM) can be used eliminating intermodulation noise which occurs with FDM
- Digital signalling allows use of digital switching techniques

### <mark style="background:#69E772;">Analogue Signals:</mark>

Analogue Data can be used to modulate an analogue signal

This is often used to:
- Obtain a more appropriate frequency for a particular transmission
- Allow a number of analogue signals to share a transmission medium (Frequency Division Multiplexing)

<mark style="background:#69E772;">Three Basic Techniques available:</mark>
- <mark style="background:#69E772;">Amplitude Modulation:</mark> Carrier amplitude varies in proportion to the amplitude of the analogue data
- <mark style="background:#69E772;">Frequency Modulation:</mark> Frequency deviation is proportional to the analogue data
- <mark style="background:#69E772;">Phase Modulation:</mark> Phase is proportional to the analogue data

# <mark style="background: #69E772;">08. Multiplexing</mark>
It is unlikely that two communicating devices will <mark style="background:#69E772;">utilise</mark> fully the capacity of a transmission link. For example, Fibre Optic cables have very high BW and hence can carry a lot of data; more data than would be required for most host-to-host interaction

This <mark style="background:#69E772;">spare</mark> capacity can be used by other communicating devices

The sharing of a data communications facility in the this way is called multiplexing

### <mark style="background:#69E772;">Basic Multiplexing Components:</mark>

![](https://i.imgur.com/92TWTlD.png)

### <mark style="background:#69E772;">Motivations for using multiplexing:</mark>

Multiplexing is commonly used in communications because:
- Communications equipment is expensive. Hence, the higher the data rate of a transmission system the lower the cost per Kbps.
- Many communicating devices use relatively modest data rates and so can be mixed together on a higher speed system.

### <mark style="background:#69E772;">Multiplexing Examples:</mark>

<mark style="background:#69E772;">Cable networks:</mark>
- Many communication services are provided on Cable networks such as TV, Broadband, IP Telephony, Radio etc. Each of these services are multiplexed onto the subscriber connection.

<mark style="background:#69E772;">Telecommunications networks:</mark>
- Fibre optical, coaxial cable, and microwave links are used between exchanges and towns/cities,
- Each communications link simultaneously carries many voice and data transmissions between multiple end devices/users.

### <mark style="background:#69E772;">Types of multiplexing:</mark>

There are two common Multiplexing techniques employed:
- <mark style="background:#69E772;">Frequency-division multiplexing</mark> (<mark style="background:#69E772;">FDM</mark>) is an <mark style="background:#69E772;">Analogue Transmission</mark> technique which produces an analogue signal from multiplexed analogue and/or digital signals <mark style="background:#69E772;">without</mark> regard to the data,
- <mark style="background:#69E772;">Time-division Multiplexing</mark> (<mark style="background:#69E772;">TDM</mark>) is a <mark style="background:#69E772;">Digital Transmission</mark> technique which produces a digital signal from multiplexed analogue and/or digital signals <mark style="background:#69E772;">with</mark> regard to the data.

### <mark style="background:#69E772;">Frequency Division Multiplexing:</mark>

Used when the useful BW of a transmission link exceeds the BW of individual signals.

Each signal is modulated onto a different <mark style="background:#69E772;">carrier frequency</mark> (known as a subcarrier).

The <mark style="background:#69E772;">carrier frequencies</mark> are combined to produce a <mark style="background:#69E772;">composite</mark> analogue signal (known as a <mark style="background:#69E772;">baseband signal</mark>).

The <mark style="background:#69E772;">baseband signal</mark> is analogue and is transmitted across a single transmission link.

The input <mark style="background:#69E772;">data</mark> may be <mark style="background:#69E772;">analogue</mark> or <mark style="background:#69E772;">digital</mark>.

The BW of the composite signal must be <mark style="background:#69E772;">greater</mark> than the sum of BWs of the individual input signals.

A <mark style="background:#69E772;">guard band</mark> must be inserted between the carrier frequencies to prevent <mark style="background:#69E772;">overlap</mark>

<mark style="background:#69E772;">FDM - Transmitter:</mark>

![](https://i.imgur.com/vNQT62a.png)


<mark style="background:#69E772;">FDM - Receiver:</mark>

![](https://i.imgur.com/ehC8ZTQ.png)

<mark style="background:#69E772;">FDM Example - Virgin TV services:</mark>

![](https://i.imgur.com/hhu2BwU.png)


### <mark style="background:#69E772;">Synchronous Time-Division Multiplexing:</mark>

This is the digital equivalent of FDM.

Here portions of each input signal are <mark style="background:#69E772;">interleaved</mark> in <mark style="background:#69E772;">time</mark> (as opposed to frequency) onto the transmission medium.

Incoming data carrying signals can be either <mark style="background:#69E772;">analogue</mark> (with encoded digital data) or <mark style="background:#69E772;">digital</mark>.

The interleaving can be at <mark style="background:#69E772;">bit</mark> level or in <mark style="background:#69E772;">blocks</mark> of bytes: This determines the size of the input <mark style="background:#69E772;">buffers</mark>

<mark style="background:#69E772;">TDM - Transmitter:</mark>

![](https://i.imgur.com/FZe0Dlw.png)


<mark style="background:#69E772;">TDM - Receiver:</mark>

![](https://i.imgur.com/337aM05.png)


Data are organised into <mark style="background:#69E772;">frames</mark>.

Frames contain a cycle of <mark style="background:#69E772;">time</mark> slots.

One or more <mark style="background:#69E772;">time</mark> slots within a <mark style="background:#69E772;">frame</mark> is dedicated to <mark style="background:#69E772;">one</mark> pair of data source devices.

The combination of <mark style="background:#69E772;">time slots</mark> across successive frames is called a <mark style="background:#69E772;">channel</mark>: Each pair of data source devices is allocated a <mark style="background:#69E772;">channel</mark> for their communication requirements.

The system is <mark style="background:#69E772;">synchronous</mark> because:
- Time slots are <mark style="background:#69E772;">pre-assigned</mark> to source devices,
- They are transmitted regardless of whether the source devices are sending data.

Frame <mark style="background:#69E772;">synchronisation</mark> is required:
- Achieved using a <mark style="background:#69E772;">separate channel</mark>,
- Known as <mark style="background:#69E772;">Added-digit Framing</mark>.

TDM is used as part of the public long-haul telecommunications system

# <mark style="background: #69E772;">09. Synchronous and Asynchronous Transmission</mark>
### <mark style="background:#69E772;">Two types of Data Transmission:</mark>

<mark style="background:#69E772;">Serial:</mark> one bit at a time,

<mark style="background:#69E772;">Parallel:</mark> more than one bit at a time on several channels, typically 8, 16 or 32 bits

This course is primarily concerned with <mark style="background:#69E772;">Serial</mark> data transmission

### <mark style="background:#69E772;">Data Communications Techniques:</mark>

Data is typically transmitted one bit at a time over a <mark style="background:#69E772;">channel</mark>

A high degree of co-operation is required between communicating devices

The timing (rate, duration and spacing) must be <mark style="background:#69E772;">identical</mark> for both <mark style="background:#69E772;">receiver</mark> and <mark style="background:#69E772;">transmitter</mark>

For example, if a Transmitter device is "clocking-out" bits at 1 Mbps to ensure successful communications

To successfully receive the data bits the <mark style="background:#69E772;">Receiver</mark> device must <mark style="background:#69E772;">sample</mark> the incoming bit stream <mark style="background:#69E772;">once</mark> every <mark style="background:#69E772;">bit interval</mark>:
- Consequently it must know the duration of <mark style="background:#69E772;">each</mark> bit
- For a 1mbps transmission the <mark style="background:#69E772;">bit interval</mark> (or <mark style="background:#69E772;">bit duration</mark>) is 1 millionth of a second

<mark style="background:#69E772;">Timing</mark> is achieved on both sides (i.e. at the receiver <mark style="background:#69E772;">and</mark> transmitter) using an internal electronic clock

To achieve successful communications, these clocks must sometimes be <mark style="background:#69E772;">synchronised</mark>

<mark style="background:#69E772;">Three Possibilities for achieving synchronisation:</mark>
- Using separate clock link - not viable for computer-to-computer communications as it's too expensive
- Ignore the potential synchronisation problems by sending very short bursts of data. This is called <mark style="background:#69E772;">Asynchronous</mark> transmission
- Embed clocking pulses within the data signal. This is called <mark style="background:#69E772;">Synchronous</mark> transmission, this <mark style="background:#69E772;">framing</mark> approach is more commonly used

### <mark style="background:#69E772;">Asynchronous Transmission and Timing problems:</mark>

![](https://i.imgur.com/45ZBGI3.png)


The <mark style="background:#69E772;">start</mark> and <mark style="background:#69E772;">stop</mark> bits determine where a character starts and ends

This function is called <mark style="background:#69E772;">framing</mark>

<mark style="background:#69E772;">Advantage:</mark> Simple and cheap. Typically used between keyboard and PC

<mark style="background:#69E772;">Disadvantage:</mark> The overhead is typically 20% i.e. 2 framing bits plus 8 data bits

### <mark style="background:#69E772;">Synchronous Transmission:</mark>

Here the data bits are transmitted in a large block of bits which has a particular structure: This structure is known as a <mark style="background:#69E772;">frame</mark>

The Receiver must be able to identify the start and end of a frame. This is achieved by using a special bit pattern for the <mark style="background:#69E772;">preamble</mark> (start of frame) and <mark style="background:#69E772;">postamble</mark> (end of frame)

Additional <mark style="background:#69E772;">control information</mark> is also sent within the frame to provide extra functionality.

### <mark style="background:#69E772;">Generic Synchronous Frame Structure:</mark>

In general, frames have a well-defined structure which is comprised of any number of distinct fields:
- A <mark style="background:#69E772;">preamble</mark> field, or <mark style="background:#69E772;">Opening Flag</mark>, at the start of the frame
- A <mark style="background:#69E772;">post-amble</mark> field, or Closing Flag, at the end of the frame
- <mark style="background:#69E772;">Data</mark> and <mark style="background:#69E772;">Control</mark> <mark style="background:#69E772;">Information</mark> fields in between
- The exact format of the frame depends upon the <mark style="background:#69E772;">data link protocol</mark> being used. Different structures will be examined later

![](https://i.imgur.com/xq7d5AM.png)

# <mark style="background: #69E772;">10. Data Link Flow Control:</mark>

So far we have explored the transmission of signals with encoded data over a <mark style="background:#69E772;">basic transmission link</mark>

For effective communications much more is needed to control and manage the exchange of <mark style="background:#69E772;">Data</mark>

A layer of control logic is required above the physical layer in each Source/Destination device:
- This logic is referred to as Data Link Control,
- When used, it transforms a basic Transmission link into a fully functioning <mark style="background:#69E772;">Data Communications Channel</mark>

### <mark style="background:#69E772;">Data Link Control:</mark>

This <mark style="background:#69E772;">logic</mark> is implemented as a set of <mark style="background:#69E772;">Rules</mark> which are well defined.

The definition of the logic/rules is known as a <mark style="background:#69E772;">Protocol</mark>

Protocols are <mark style="background:#69E772;">synonymous</mark> with data communications
- They are often referred to in texts on the subject,
- The first protocol to be explored is the <mark style="background:#69E772;">data link protocol</mark>

### <mark style="background:#69E772;">Data Link Control Requirements:</mark>

There are six basic requirements for effective Data Link Control as follows:

<mark style="background:#69E772;">Frame Synchronisation:</mark> Frames must be recognisable by the Receiver

<mark style="background:#69E772;">Flow Control:</mark> The Sender must <mark style="background:#69E772;">not</mark> overload the receiver

<mark style="background:#69E772;">Error Control:</mark> Errors should be detectable by the Receiver

<mark style="background:#69E772;">Addressing:</mark> For a multi-point configuration each station must be uniquely identifiable

<mark style="background:#69E772;">Control and Data on the Same Link:</mark> The receiver must not have to wait for control information to arrive before it can process a frame

<mark style="background:#69E772;">Link Management:</mark> Procedures for establishing and relinquishing the link must be adhered to

### <mark style="background:#69E772;">Flow Control:</mark>

Receiver and buffer stations each allocate a data <mark style="background:#69E772;">buffer</mark> of a fixed size
- Data Remains in the buffer until it has been processed by the receiving station,
- Consequently the buffers can fill to capacity

<mark style="background:#69E772;">Flow control</mark> enables the Receiving station to indicate to the Sending station that its buffers are full

There are <mark style="background:#69E772;">two flow control</mark> techniques to consider:
- <mark style="background:#69E772;">Stop-and-wait</mark>
- <mark style="background:#69E772;">Sliding Windows</mark>

### <mark style="background:#69E772;">Stop-and-wait Flow Control:</mark>

Here the Sending station transmits a frame:
- The Sending station must get an <mark style="background:#69E772;">acknowledgement</mark> (<mark style="background:#69E772;">ACK</mark>) from the Receiving station before transmitting the next frame,
- The Receiving station can control the flow of data by withholding <mark style="background:#69E772;">ACKs</mark>

This technique only allows for the transmission of a single frame in either direction i.e. Half-Duplex communications

![](https://i.imgur.com/42oF5jY.png)


### <mark style="background:#69E772;">Sliding Window Flow Control:</mark>

Here both stations use an <mark style="background:#69E772;">extended</mark> buffer size to hold multiple frame

The Sending and Receiving stations maintain a list of frames already sent/received

This technique allows for <mark style="background:#69E772;">more efficient link utilisation</mark>:
- The transmission link is effectively treated as a <mark style="background:#69E772;">pipeline</mark> that can be <mark style="background:#69E772;">filled</mark> with many frames in transmit <mark style="background:#69E772;">simultaneously</mark>

This technique allows multiple frames to be in either direction i.e. Full Duplex communications

![](https://i.imgur.com/F9gvrnS.png)


In the example, Stations <mark style="background:#69E772;">A</mark> and <mark style="background:#69E772;">B</mark> each <mark style="background:#69E772;">allocate</mark> buffer space for <mark style="background:#69E772;">W</mark> frames: I.E. Station B can accept W frames and Station A can send W frames without any acknowledgement being sent or received

Each frame contains a <mark style="background:#69E772;">sequence number</mark>

Station B sends <mark style="background:#69E772;">ACKs</mark> that include the sequence number of the <mark style="background:#69E772;">next</mark> frame expected: I.E. station B is prepared to receive <mark style="background:#69E772;">starting</mark> at the <mark style="background:#69E772;">sequence number</mark> indicated e.g. RR5

Multiple frames can be <mark style="background:#69E772;">ACK'd</mark> using a single <mark style="background:#69E772;">control message</mark>
- e.g. Receipt of ACK for frame <mark style="background:#69E772;">2</mark> (RR3) followed later by ACK for frame <mark style="background:#69E772;">5</mark> (RR6) implies acknowledgement of frames <mark style="background:#69E772;">3</mark> and <mark style="background:#69E772;">4</mark>


Station A maintains a list of frame numbers it is allowed to send

Station B maintains a list of frame numbers it is prepared to receive

These lists can be considered as <mark style="background:#69E772;">windows</mark>


To impose flow control, the Receiver can send a different control message:
- <mark style="background:#69E772;">Receiver Not Ready</mark> (<mark style="background:#69E772;">RNR</mark>)
- This acknowledges previous frames but stems the flow from the Sender e.g. RNR5 acknowledges all frames up to frame 4

To resume flow the Receiver sends a Receiver Ready (RR) message e.g. RR5 - recommence at frame 5


<mark style="background:#69E772;">Example Sliding Window:</mark>

![](https://i.imgur.com/DmKsU8t.png)


In the previous example the operation of Sliding Windows can be clearly seen:
- Frames 0-2 are transmitted
- Copies of these frames are held in memory on both the Sender (Tx) and the Receiver (Rx) station until an ACK is returned
- When the Rx sends the ACK it removes the frames from memory and the Sliding Window expands
- When the Tx receives the ACK it removes the frames from memory and the Sliding Window expands

### <mark style="background:#69E772;">Note on ACKs:</mark>

Here, an ACK is shown as a special message (RR3)

Both RR and RNR messages are positive ACKs. They are acknowledging that a successful transmission has occurred

Only one ACK is required for three frame. RR3 acknowledges all frame up to and including frame 2 i.e. 0, 1 and 2

This is one of the efficiencies of the technique. Recall that S-and-W required one ACK per transmission

This approach to sending one ACK for multiple frames allow for <mark style="background:#69E772;">Full Duplex</mark> communications: ACKs can be returned anytime i.e. after receipt of a single frame or multiple frames

This Full Duplex mode can be seen in the later transmission of Frames 3-6: Frame 3 has arrived and an ACK (RR4) is immediately returned. The ACK can be clearly seen in transit at the same time as Frames 4, 5 and 6 are arriving

The consequence of this is that Frame 3 is held in memory very briefly and then it is removed. This is too quick for it to be seen stored in memory

Frames 4, 5 and 6 arrive soon after Frame 3: these frames can be clearly seen stored in memory

<mark style="background:#69E772;">Question:</mark> Assuming Frames 4, 5 and 6 arrive without incident, what would the next positive ACK be?

<mark style="background:#69E772;">Answer:</mark> The next positive ACK could potentially be one of two messages depending on the status of the Rx buffers:
- If, upon receipt of Frame 6, the Rx buffers become full then it could be RNR7. This message would acknowledge receipt of all frames up to and including Frame 6 but it would also instruct the Tx to stop sending frames
- If, upon receipt of Frame 6, there is still space in the Rx buffers, then it would be RR7. Once again this message would acknowledge receipt of all frames up to and including Frame 6 but it would also permit the Tx to <mark style="background:#69E772;">continue</mark> sending frames

With the introduction of Full Duplex mode each station can be a Tx'er or Rx'er

Full Duplex mode allows for frames to be in transit between the stations <mark style="background:#69E772;">simultaneously</mark> and in <mark style="background:#69E772;">opposite</mark> directions. This includes <mark style="background:#69E772;">Data</mark> frames

With the capability to transmit Data frames in opposite directions, it is possible to introduce another efficiency.

ACKs don't have to be sent as separate frames


Instead, ACKs can be included in outgoing <mark style="background:#69E772;">Data</mark> frames
- i.e. Data Frames moving in one direction can carry ACKs in their Control Fields for Data Frames moving in the opposite direction
- This technique is known as piggybacking i.e. a <mark style="background:#69E772;">single</mark> frame can carry both <mark style="background:#69E772;">Data</mark> and <mark style="background:#69E772;">ACKs</mark>

Consequently, in Full Duplex mode each station must maintain <mark style="background:#69E772;">two</mark> sliding windows
- One for <mark style="background:#69E772;">Transmitted</mark> frames and one for <mark style="background:#69E772;">Received</mark> frames

### <mark style="background:#69E772;">Sliding Window Versus Stop-and-Wait Flow Control:</mark>

Sliding Windows is potentially <mark style="background:#69E772;">more</mark> efficient than Stop-and-wait in relation to <mark style="background:#69E772;">Link Utilisation</mark>:
- With Stop-and-Wait only <mark style="background:#69E772;">one</mark> frame can be in transit at any time i.e. Half-Duplex communications
- With Sliding Window the link is treated like a pipeline that can be filled with multiple frames
- This allows for simultaneous two-way communications i.e. Full Duplex communications

Sliding Windows uses a special message, RNR, to impose Flow Control:
- This RNR message is a positive ACK which allows the Tx to clear frames from its outgoing buffer
- Recall that Stop-and-Wait simply with-held the ACK. The Tx must hold onto the frame until the ACK arrives
# <mark style="background:#69E772;">11. Error Control:</mark>

The most common <mark style="background:#69E772;">error control</mark> techniques use some or all of these elements use some or all of these elements

Collectively, these <mark style="background:#69E772;">error control</mark> techniques are called <mark style="background:#69E772;">Automatic Repeat Requests</mark> (<mark style="background:#69E772;">ARQ</mark>):
- Stop-and-Wait ARQ
- Go-back-N ARQ
- Selective-reject ARQ

### <mark style="background:#69E772;">Stop-and-Wait ARQ:</mark>

This technique is an enhancement to the Stop-and-Wait Flow Control Technique:

Recall that the Tx transmits a frame and awaits and ACK before continuing

If the frame contains an error, the Receiver simply discards it and does not return an ACK

If the frame is not acknowledged after a time-out period the Transmitter simply retransmits the frame

<mark style="background:#69E772;">Problem:</mark>
- If ACK is sent but damaged in transit, the transmitter will resend the frame after time-out
- The Receiver will now get <mark style="background:#69E772;">two</mark> copies of the frame

![](https://i.imgur.com/RYyQ9Rs.png)


<mark style="background:#69E772;">Solution:</mark>
- Frames are alternatively numbered 1 or 0 and ACKs are correspondingly numbered 0 or 1

### <mark style="background:#69E772;">Go-back-N ARQ:</mark>

This technique is an enhancement to the Sliding Window Flow Control technique

Recall that the Tx can send a number of frames (up to some window size) <mark style="background:#69E772;">without</mark> having to receive some form of ACK from the Rx

In relation to the types of error (or non-error) conditions that can occur:
- Successful Transmission,
- Lost Data or Lost ACK frame
- Damaged Data Frame

If <mark style="background:#69E772;">NO</mark> errors occur i.e. frames arrive in sequence <mark style="background:#69E772;">and</mark> undamaged:
- The Receiver returns a positive ACK e.g. RR4 or RNR4, with the number of the next frame expected
- This ACK can be sent as an <mark style="background:#69E772;">explicit</mark> message in its own frame, or, it can be piggybacked onto an outgoing Data Frame (implicitly)
- The Transmitter continues to send Data Frames up to the agreed <mark style="background:#69E772;">window</mark> size

If <mark style="background:#69E772;">Errors</mark> there are two responses depending on the type of error:
- Lost Frames/Damaged Frames (Lost Frames are detected as <mark style="background:#69E772;">out-of-sequence</mark> frames)
- Lost ACKs

<mark style="background:#69E772;">For Lost Frames and Damaged Frames:</mark>
- They are treated the same
- The Receiver sends a <mark style="background:#69E772;">Reject</mark> (<mark style="background:#69E772;">REJ</mark>) message with the number of the next frame expected e.g. REJ 4.
- The Sending Station, upon receipt of this REJ message, retransmits <mark style="background:#69E772;">all</mark> frames starting at the number included in the message. This is regardless of whether subsequent frames have arrived intact -they are simply discarded

<mark style="background:#69E772;">For Lost ACKs:</mark>
- Here the transmitter station has not received any messages (positive or negative ACKs) from the receiver station
- Recall the use of a Timer for each frame that is transmitted. The timer has a part to play here

Depending on whether the timer for a frame expires, the transmitter can respond as follows:
- If a timer has <mark style="background:#69E772;">not</mark> expired it can continue to send more frames up to the <mark style="background:#69E772;">window</mark> size. This is not considered an error condition

If a <mark style="background:#69E772;">timer</mark> does expire, the transmitter immediately stops transmitting Data frames:
- It then sends a 'special' RR message with the <mark style="background:#69E772;">poll</mark> bit set
- This is considered a <mark style="background:#69E772;">command</mark> frame
- The Receiver <mark style="background:#69E772;">must</mark> respond with an RR of its own identifying the number of the next frame expected

### <mark style="background:#69E772;">Selective Reject ARQ:</mark>

This is very similar to the Go-back-N technique with the exception that the only frames retransmitted are:
- Transmitted frames for which a timer has expired i.e. a <mark style="background:#69E772;">Lost ACK</mark> or,
- Transmitted frames that were <mark style="background:#69E772;">lost</mark> or <mark style="background:#69E772;">damaged</mark>. The receiver uses a slightly different Negative ACK - it's called a <mark style="background:#69E772;">Selective Reject</mark> (SREJ) message
- The number of the frame to be re-transmitted is also included e.g. SREJ 5

This is considered more efficient than Go-Back-N as it minimises the amount of re-transmitted frames

However, this technique is also more complex than Go-Back-N as the Receiver station has to:
- Store frames received <mark style="background:#69E772;">after</mark> a Damaged frame has been rejected
- It has to re-sequence retransmitted frames as they arrive <mark style="background:#69E772;">out-of-sequence</mark>
- This requires more complex logic on both the Transmitter and Receiver stations

Hence, <mark style="background:#69E772;">Go-back-N</mark> ARQ is often preferred over <mark style="background:#69E772;">Selective Reject</mark> ARQ

### <mark style="background:#69E772;">Go-back-N and Selective-Reject ARQ:</mark>

![](https://i.imgur.com/Lqg02AH.png)


# <mark style="background: #69E772;">12. High Level Data Link Control:</mark>

#DataComms 
### <mark style="background:#69E772;">Data Link Control Requirements:</mark>

The first three of the <mark style="background:#69E772;">six</mark> Data Link Control requirements have been examined through an exploration of various techniques:
- <mark style="background: #69E772;">Frame Synchronisation</mark> (recall <mark style="background:#69E772;">Asynchronous/Synchronous</mark> communications),	
-  <mark style="background: #69E772;">Flow Control</mark> (recall <mark style="background:#69E772;">Stop-and-Wait</mark> and <mark style="background:#69E772;">Sliding Windows</mark> Flow Control),
- <mark style="background: #69E772;">Error Control</mark> (recall <mark style="background:#69E772;">Stop-and-Wait</mark>, <mark style="background:#69E772;">Go-back-N</mark> and <mark style="background:#69E772;">Selective Reject ARQ</mark>)
- <mark style="background: #69E772;">Addressing</mark>
- <mark style="background: #69E772;">Control and Data on same link</mark>
- <mark style="background: #69E772;">Link Management.</mark>

Recall the reason for using these techniques: To transform a <mark style="background:#69E772;">transmission link</mark> into a fully functioning, reliable and effective <mark style="background:#69E772;">data communications link</mark>.	

The remaining requirements can be considered using a real protocol that fulfils all of the requirements together namely, <mark style="background:#69E772;">High Level Data Link Control</mark> (<mark style="background:#69E772;">HDLC</mark>).

### <mark style="background:#69E772;">High-Level Data Link Control:</mark>

This is a very important Data Link Control Protocol. As well as being widely used, it also forms the basis for many other data link protocols such as <mark style="background: #69E772;">Point-to-Point Protocol over Ethernet (PPPoE)</mark> which is used by many ISPs and by Cisco

<mark style="background: #69E772;">The protocol defines the following:</mark>
- The role of each station attached to the link i.e. is there a Master-Slave or Peer-to-Peer relationship?
- The mode of data transfer i.e. can any station initiate a data transfer?
- The structure of the frame i.e. the location of each field
- The exchange of data during each phase of communication

<mark style="background:#69E772;">The protocol defines three types of station:</mark>⠀
- <mark style="background:#69E772;">Primary Station:</mark> Controls the operation of the link through the use of commands.
- <mark style="background:#69E772;">Secondary Station:</mark> Operates under the control of primary station. It responds to commands
- <mark style="background:#69E772;">Combined Station:</mark> combines features of both. It can send commands and responses

⠀
<mark style="background:#69E772;">Synchronous</mark> transmission is used, i.e. transmissions are in the form of <mark style="background:#69E772;">frames</mark>
⠀
A <mark style="background:#69E772;">frame</mark> is a block of data delineated by a special <mark style="background:#69E772;">flag</mark> character/sequence (01111110)
⠀
<mark style="background:#69E772;">Data</mark> and <mark style="background:#69E772;">Control</mark> frames have the same frame format with some minor differences in relation to the control fields
⠀
### <mark style="background:#69E772;">HDLC Frame Format:</mark>

![](https://i.imgur.com/L2h0rJQ.png)

⠀
### <mark style="background:#69E772;">HDLC - The Flag Fields:</mark>

All active stations scan incoming bit streams:
- Initially to determine "start of a frame"
- The station continues to scan the bits looking for the "end of the frame"


The same flag pattern may be used to signify end and start of two consecutive frames

The flag pattern (01111110) must not be allowed to occur inside frame

This is prevented by <mark style="background:#69E772;">bit stuffing</mark>


<mark style="background:#69E772;">Bit stuffing example:</mark>

![](https://i.imgur.com/gosf57d.png)

### <mark style="background:#69E772;">HDLC - The Address Field:</mark>

Used to identify the stations

Only relevant on a multi-point link (not on a point-to-point link) but it is always included.

Usually 8 bits long but can be extended.

### <mark style="background:#69E772;">HDLC - The Control Field:</mark>

There are three <mark style="background:#69E772;">types</mark> of frame and each has its own control field format:

<mark style="background:#69E772;">Information (I)</mark> frames carry <mark style="background:#69E772;">data</mark>. They can also carry piggybacked frame sequence numbers for Flow and Error Control.

<mark style="background:#69E772;">Supervisory (S)</mark> frames carry Flow and Error control data when not <mark style="background:#69E772;">piggybacked</mark>

<mark style="background: #69E772;">Unnumbered (U)</mark> frames provide link control functions such as set-up and disconnect

### <mark style="background: #69E772;">HDLC - The Information Field:</mark>

Present in I-frames.

This is where the data is stored

Its length is variable up to some predefined system specific limit

However, it must be a multiple of 8 bits

### <mark style="background:#69E772;">HDLC - The FCS Field:</mark>

<mark style="background: #69E772;">FCS - Frame Check Sequence</mark>

Used in <mark style="background:#69E772;">Error Detection</mark>:
- This is an <mark style="background:#69E772;">Error Detection</mark> code. It is calculated using all bit within the frame <mark style="background:#69E772;">excluding</mark> flags.
- Recalling Cyclic Redundancy Check (CRC)

Normally a 16-bit CRC technique is used
### <mark style="background:#69E772;">HDLC Commands/Resources:</mark>

![](https://i.imgur.com/4mc98IG.png)

### <mark style="background:#69E772;">HDLC Operation:</mark>

All HDLC interactions follow <mark style="background:#69E772;">three</mark> distinct phases of operation
- <mark style="background: #69E772;">Phase 1 - Initialisation:</mark> This is where the "link" is set-up prior to actual communications. Certain parameters are agreed by each station.
- <mark style="background: #69E772;">Phase 2 - Data Transfer:</mark> This is where <mark style="background:#69E772;">data</mark> is exchanged
- <mark style="background: #69E772;">Phase 3 - Termination/Disconnect:</mark> This is where the 'link' is decommissioned

### <mark style="background:#69E772;">Initialisation:</mark>

Either station may initialise the link by sending one of 6 <mark style="background:#69E772;">set</mark> <mark style="background:#69E772;">mode</mark> commands depending on the mode required

Most commonly used is SABM i.e. Set Asynchronous Balanced Mode. Used with two <mark style="background:#69E772;">combined</mark> stations.

The receiving station responds with an <mark style="background:#69E772;">Unnumbered Acknowledgement</mark> (UA) to accept or, <mark style="background:#69E772;">Disconnect Mode</mark> (DM) to reject the request

Only 'U' frames are used during this phase

### <mark style="background:#69E772;">Data Transfer:</mark>

After initialisation, data exchange takes place using I-frames. Recall that I-frames carry <mark style="background:#69E772;">Data</mark>.

Each I-frame also contains two sequence numbers:
- One relates to the outgoing i.e. <mark style="background:#69E772;">this</mark> frame number
- The other is <mark style="background:#69E772;">piggybacked</mark> ACK for a frame <mark style="background:#69E772;">received</mark> from the other side of the link i.e. the number of the next frame expected
- When <mark style="background:#69E772;">piggybacking</mark> is not being used, S-frames are used for flow and error control
- The first frame transmitted is always numbered zero.

### <mark style="background:#69E772;">Disconnect:</mark>

Either station can initiate the Disconnect Phase

This is achieved using a <mark style="background:#69E772;">U-frame</mark> containing the <mark style="background:#69E772;">DISC</mark> message

The remote station <mark style="background:#69E772;">must</mark> respond with a <mark style="background:#69E772;">U-frame</mark> containing the <mark style="background:#69E772;">UA</mark> message

### <mark style="background:#69E772;">HDLC Operation - Example:</mark>

![](https://i.imgur.com/77ua8Tg.png)

![](https://i.imgur.com/cYGM6XH.png)


# <mark style="background: #69E772;">13. Intro to LANs</mark>

# <mark style="background: #69E772;">13. Intro to LANs:</mark>

### <mark style="background:#69E772;">Local Area Networks:</mark>
 
These are private communications networks:

They are are used to interconnect the computing resources within an organisation

All devices attach to a shared transmission medium. They can provide data rates up to 1 Gbps

<mark style="background:#69E772;">The rationale for interconnecting devices:</mark>
- Proliferation of computing devices,
- Growth in Multimedia applications,
- Increase in client/server application

<mark style="background:#69E772;">LANs can be classified according to:</mark>
- Their topology e.g. ring, star, bus
- The type of transmission medium used e.g. ThickNet, Thinnet
- How they access the shared Tx medium (aka as Access Control) e.g. CSMA, Token
 
### <mark style="background:#69E772;">There are three broad types of LANs:</mark>

<mark style="background:#69E772;">PC LANs (aka Access Layer):</mark>
- Used to connect low-cost devices e.g. PCs, small server devices, etc
- Used in most organisations
- These LANs are cheap to implement and maintain, consequently their performance and speed is low
    
<mark style="background:#69E772;">Backend LANs (aka Core Layer):</mark>
- Used to connect high-cost devices e.g. Mainframes, Supercomputers, mass storage devices
- Mainly used for the bulk transfer of data
- Used in large organisations
- These LANs are costly to implement and maintain, consequently their performance and speed is high

<mark style="background:#69E772;">Backbone LANs (aka Distribution Layer):</mark>
- Used to provide connectivity between PC LANs and backend LANs

<mark style="background:#69E772;">The use of a single LAN is not desirable:</mark>
- <mark style="background:#69E772;">Reliability:</mark> If the single LAN develops a fault the effects can be devastating
- <mark style="background:#69E772;">Capacity:</mark> More devices connecting to LAN reduces its performance
- <mark style="background:#69E772;">Cost:</mark> Connecting low-cost PC devices using the same type of LAN used to connect High Cost server devices would be impractical

### <mark style="background:#69E772;">LAN topologies:</mark>

![](https://i.imgur.com/f9KYSM8.png)


There are three LAN topologies to consider: <mark style="background:#69E772;">Bus</mark>, <mark style="background:#69E772;">Ring</mark> and <mark style="background:#69E772;">Star</mark>.

### <mark style="background:#69E772;">Bus LAN characteristics:</mark>

A <mark style="background:#69E772;">linear</mark> transmission medium is used

Each station attaches to the bus using a tap

There are no closed loops

Transmissions travel in both directions i.e. <mark style="background:#69E772;">bi-directional</mark>, and can be seen by <mark style="background:#69E772;">every</mark> attached device

The bus is terminated by a <mark style="background:#69E772;">terminator</mark> device which removes the transmission signal.

Example of a bus LAN is an <mark style="background:#69E772;">ethernet</mark>

### <mark style="background:#69E772;">Ring LAN characteristics:</mark>

Consists of a set of interconnected <mark style="background:#69E772;">repeaters</mark> (using point to point links) in a <mark style="background:#69E772;">ring</mark> configuration

Repeaters receive data on one link and transmit them <mark style="background:#69E772;">bit-by-bit</mark> onto another link

These links are <mark style="background:#69E772;">uni-directional</mark>

Each station attaches at a <mark style="background:#69E772;">repeater</mark>

The transmission signal must be <mark style="background:#69E772;">physically</mark> removed from the network

Example of a ring LAN is the <mark style="background:#69E772;">IBM Token Ring</mark>

### <mark style="background:#69E772;">Star LAN characteristics:</mark>

Consists of a central <mark style="background:#69E772;">hub</mark> component of which there are two types:
- <mark style="background:#69E772;">Shared-medium</mark> hub
- <mark style="background:#69E772;">Switched-LAN</mark> hub

Each station is attached by two links (<mark style="background:#69E772;">transmit</mark> and <mark style="background:#69E772;">receive</mark>)

All transmissions travel via the Hub device

Example of a star LAN is an ATM
### <mark style="background:#69E772;">Common Characteristics of LANs:</mark>

Data is transmitted in small blocks known as <mark style="background:#69E772;">frames</mark>.

Each frame contains <mark style="background:#69E772;">Data</mark> plus <mark style="background:#69E772;">Control Information</mark> (similar to HDLC)

Stations must gain access to the shared medium transmission

Access must be provided on a fair and equitable basis i.e. there must be some controlling mechanism employed

# <mark style="background: #69E772;">14. Access Techniques</mark>
#DataComms 

### <mark style="background:#69E772;">Medium Access Control:</mark>

Gaining access to a LAN is a fundamental requirement for Data Transmission between stations.

<mark style="background: #69E772;">Access can be controlled either:</mark>
- <mark style="background:#69E772;">Centrally:</mark> Stations must obtain permission before accessing the transmission medium
- <mark style="background:#69E772;">Distributed:</mark> Access is controlled by stations acting <mark style="background:#69E772;">together</mark>

<mark style="background:#69E772;">Advantages of Centrally Controlled:</mark>
- The access logic required at each station is simple
- There is no co-ordination required between stations

<mark style="background:#69E772;">Disadvantages of Centrally Controlled:</mark>
- Single point of failure. If the controlling device develops a fault all stations are affected
- Potential <mark style="background:#69E772;">bottleneck</mark>. All "requests for access" must be sanctioned by a central device
- Distributed access will be discussed later

### <mark style="background:#69E772;">Three generalised access control techniques:</mark>

<mark style="background:#69E772;">Reservation (will not be covered):</mark>
- Medium is divided into <mark style="background:#69E772;">time</mark> slots
- Station wishing to send has to <mark style="background:#69E772;">reserve</mark> future slots
- Very suited to stream traffic i.e. <mark style="background:#69E772;">long</mark> and <mark style="background:#69E772;">continuous</mark> transmissions on an <mark style="background:#69E772;">irregular</mark> basis

<mark style="background:#69E772;">Round Robin:</mark>
- Each station takes a turn to transmit data
- Efficient only if stations have a lot of data to transmit on a <mark style="background:#69E772;">regular</mark> basis

<mark style="background:#69E772;">Contention:</mark>
- Continued.

### <mark style="background:#69E772;">MAC - Contention:</mark>

Each station contends for access when needed

The technique is <mark style="background:#69E772;">distributed</mark> by nature

Works on a <mark style="background:#69E772;">"First Come/First Served"</mark> basis and is easy to implement

Very suited to <mark style="background:#69E772;">bursty</mark> traffic i.e. short, sporadic transmissions

### <mark style="background:#69E772;">Ethernet's Contention Access Technique:</mark>

Ethernet - an example of a <mark style="background:#69E772;">Bus/Star</mark> <mark style="background:#69E772;">LAN</mark>

It employs a Contention MAC technique known as a "<mark style="background: #69E772;">Carrier Sense Multiple Access with Collision Detection </mark>(<mark style="background:#69E772;">CSMA</mark>/<mark style="background:#69E772;">CD</mark>)"

It is <mark style="background:#69E772;">random</mark> and requires each station to contend for access to the shared transmission medium

The most commonly used MAC technique for <mark style="background:#69E772;">bus</mark> and <mark style="background:#69E772;">star</mark> <mark style="background:#69E772;">LANs</mark>

Defined under IEEE802.3 standard

### <mark style="background:#69E772;">CSMA - Basic Operation:</mark>

Steps followed by a station when it wishes to transmit Data frames:
- The station listens to the medium for activity (known as carrier sense)
- If the medium is clear of traffic the station begins transmission immediately
- If the medium is in use, the station waits a random period of time before it attempts to transmit the Data frame.

![](https://i.imgur.com/qNG2EVv.png)


In normal operation, transmitting stations can send multiple frames and would expect ACKs in the return direction: Recall ARQ techniques: Go-Back-N and Selective Reject.

The problem with this access technique:

It is possible for two or more stations to attempt transmit at approximately the same time.

This will lead to a <mark style="background:#69E772;">collision</mark> i.e. a <mark style="background:#69E772;">garbled</mark> transmission. Recall what happens when <mark style="background:#69E772;">digital</mark> signals meet

![](https://i.imgur.com/RkvPZLz.png)


<mark style="background:#69E772;">Collisions</mark> are an example of frames "going missing":
- Recall scenarios outlined in discussions on Go-Back-N and Selective Reject
- Collisions can lead to "out-of-sequence" frames and/or "missing" RR messages

Recall in the ARQ techniques that a transmitting station:
- Sets a timer for each frame transmission
- Expects an ACK from the destination station
- Takes action after a <mark style="background:#69E772;">timeout</mark> period using command-responses (Poll/Final bit)

### <mark style="background:#69E772;">CSMA Characteristics:</mark>

CSMA results in <mark style="background:#69E772;">poor</mark> <mark style="background:#69E772;">utilisation</mark> of the link

The medium remains <mark style="background:#69E772;">unusable</mark> for the time taken to clear the collision

The <mark style="background:#69E772;">transmitting</mark> station is reliant upon the non-return of an acknowledgement to detect a problem

To counteract this inefficiency CSMA was extended to include <mark style="background:#69E772;">collision detection</mark>

### <mark style="background:#69E772;">CSMA/CD - Basic Operation:</mark>

As before, the station listens to the medium before attempting to transmit

<mark style="background:#69E772;">During</mark> transmission the station <mark style="background:#69E772;">continues</mark> to <mark style="background:#69E772;">listen</mark> to the medium for a <mark style="background:#69E772;">collision</mark>, known as <mark style="background:#69E772;">Collision Detection</mark>:
- If present, the station ceases transmission immediately
- The station then transmits a brief jamming signal to inform all other stations of collision
- The station waits a random amount of time (delta) before attempting to retransmit
- Additional collisions are dealt with using a <mark style="background:#69E772;">binary exponential backoff</mark>

### <mark style="background:#69E772;">CSMA versus CSMA/CD:</mark>

<mark style="background:#69E772;">Without</mark> the use of CSMA/CD collisions would <mark style="background:#69E772;">not</mark> be detected

If the affected frame was a data frame, then the Rx'er would likely interpret the next frame <mark style="background:#69E772;">as</mark> an out-of-sequence frame and would return a REJ message

If the collided frame was a returning ACK, the Tx'er would not receive an RR message for an outstanding frame.

Recall: Its timer would expire and it would have to send an RR message with the Poll bit set

Consequently the overall time to send multiple frames would be extended as the communicating station would have to rely on <mark style="background:#69E772;">Timers</mark> and <mark style="background:#69E772;">REJ</mark> messages to recover from collisions

<mark style="background:#69E772;">With</mark> Collision Detection collisions <mark style="background:#69E772;">would</mark> be detected

The Tx'ing station would stop transmitting the frame and would wait a random period before attempting to re-transmit. The Rx'er should eventually receive the frame

Collision Detection, in part, addresses some of the issues normally addressed with error control, namely "lost" frames. The Tx'er does not have to rely on returning ACKs/NACKs

Consequently the overall time to send multiple frames would be reduced as the Tx'er would only have to wait for the collision to disappear from the segment in order to re-transmit the frame

### <mark style="background:#69E772;">CSMA Characteristics:</mark>

The use of CSMA/CD is beneficial:
- By reducing the "down-time" of the LAN segment, "Link-Utilisation" is improved
- The time to deliver multiple frames is improved

However, <mark style="background:#69E772;">frame-size</mark> (length) is critical
- Short frames prevent <mark style="background:#69E772;">collision</mark> detection
- Frames have to be a minimum length
- Consequently the MAC frame format includes a special field called <mark style="background:#69E772;">Pad</mark>: Extra octets ("random data") can be added to the frame

### <mark style="background:#69E772;">802.3 MAC Frame Format:</mark>

   ![](https://i.imgur.com/OdQkgFs.png)


### <mark style="background:#69E772;">Ring LANs:</mark>

Consists of a number of stations, each of which is connected to a <mark style="background:#69E772;">repeater</mark>

These in turn are connected to two other repeaters by <mark style="background:#69E772;">unidirectional</mark> transmission links to form a ring

Data is transferred <mark style="background:#69E772;">bit-by-bit</mark> around the ring from one repeater to the next

The repeaters <mark style="background:#69E772;">regenerate</mark> and <mark style="background:#69E772;">retransmit</mark> <mark style="background:#69E772;">each</mark> bit

![](https://i.imgur.com/x74Znjd.png)


### <mark style="background:#69E772;">Ring LANs - Repeater functionality:</mark>

<mark style="background:#69E772;">Frame Insertion:</mark> Frames (with addresses) are placed onto the Tx medium by the repeater

<mark style="background:#69E772;">Frame reception:</mark> As a frame passes through a repeater the address field is copied to the station. If the station recognises the address, the entire frame is copied

<mark style="background:#69E772;">Frame Removal:</mark> A repeater can remove a frame by not repeating it to the next link. Either the <mark style="background:#69E772;">addressed repeater</mark> can remove the data or, the <mark style="background:#69E772;">transmitting station</mark> can remove it (after one round trip)

### <mark style="background:#69E772;">Example Access Technique - Token Ring:</mark>

The most commonly used MAC technique for ring LANs is IBM Token Ring. This is a round robin technique and is defined under the IEEE802.5 standard

Token Ring uses a small frame, called a Token:
- The token circulates around the <mark style="background:#69E772;">ring</mark> indefinitely
- A station wishing to transmit must <mark style="background:#69E772;">seize</mark> the token and remove it from the LAN.

The token is then transformed into a <mark style="background:#69E772;">start-of-frame</mark> field for a <mark style="background:#69E772;">data frame</mark>

More fields are added to construct a data frame.

The token is effectively removed from the ring and replaced by a <mark style="background:#69E772;">Data</mark> <mark style="background:#69E772;">Frame</mark>

When the frame returns to the <mark style="background:#69E772;">transmitting</mark> station it removes the <mark style="background:#69E772;">frame</mark> from the ring and inserts a <mark style="background:#69E772;">new</mark> token

### <mark style="background:#69E772;">802.5 MAC Frame Format:</mark>

   ![](https://i.imgur.com/Q7kyju0.png)

### <mark style="background:#69E772;">Token Ring Operation:</mark>

![](https://i.imgur.com/OSgCDJV.png)


<mark style="background:#69E772;">Token Ring Advantages:</mark>
- Access is efficient and fair under heavy traffic loads

<mark style="background:#69E772;">Token Ring Disadvantages:</mark>
- Access can be inefficient under <mark style="background:#69E772;">light</mark> traffic loads. A station must wait for a token before transmitting
- There is a requirement for <mark style="background:#69E772;">token maintenance</mark>
- Tokens can be lost or duplicated
- One station is assigned responsibility for token maintenance

### <mark style="background:#69E772;">Star LANs:</mark>

Uses a central component known as a <mark style="background:#69E772;">hub</mark>

Two types of hub:
- Shared-medium hub
- Switched LAN hub

<mark style="background:#69E772;">Shared Medium hub (hub-star LAN):</mark>

Transmission from any station is repeated to <mark style="background:#69E772;">all</mark> stations

Only <mark style="background:#69E772;">one</mark> station can transmit at any one time. This is the same behaviour as a Bus Lan

Hence this type of <mark style="background:#69E772;">star</mark> LAN is also known as a <mark style="background:#69E772;">star-shaped bus</mark> (as opposed to a <mark style="background:#69E772;">simple bus</mark> LAN)

Advantages of <mark style="background:#69E772;">star-shaped</mark> bus LAN: Can use existing building wiring

![](https://i.imgur.com/0zbFokW.png)


<mark style="background:#69E772;">Switched LAN hub (Switched-star LAN):</mark>

Acts as a switch i.e. incoming frame is only passed to the addressed station

Frames from <mark style="background:#69E772;">other</mark> stations can be switched simultaneously

<mark style="background:#69E772;">Greater</mark> performance can be achieved with a <mark style="background:#69E772;">switched LAN</mark> hub <mark style="background:#69E772;">over</mark> a shared-medium hub

![](https://i.imgur.com/duECb6H.png)


Switched-LANs provides improved performance because there is <mark style="background: #69E772;">no contention</mark>

Multiple simultaneous communications between pairs of stations can be facilitated

![](https://i.imgur.com/RIfzayB.png)


### <mark style="background:#69E772;">Wireless LAN:</mark>

The specification for wireless LANs is called IEEE 802.11.

This specification defines two types of architecture:
- The Basic Service Set (BSS), and,
- The Extended Service Set (ESS).

<mark style="background:#69E772;">BSS Wireless LAN:</mark>

The BSS typically comprises a number of mobile stations and a central <mark style="background:#69E772;">base</mark> station known as an <mark style="background:#69E772;">Access Point (AP)</mark>

![](https://i.imgur.com/ohCAt64.png)

### <mark style="background:#69E772;">ESS Wireless LAN:</mark>

The ESS typically comprises two or more BSSs with APs.

The APs are usually connected via a <mark style="background:#69E772;">distribution network</mark> (typically a wired LAN).

Like BSSs, ESSs define two types of stations:
- Stationary stations which usually connect via the wired LAN. These stations include the APs.
- Mobile stations. Some of these stations can only communicate within a single BSS, others between BSSs and yet others between ESSs.

![](https://i.imgur.com/eL6x4zW.png)


### <mark style="background:#69E772;">Wireless LAN Access Technique:</mark>

The access technique employed on a wireless LAN is CSMA/CA (Collision Avoidance)

This is similar to CSMA/CD as follows:
- Before a station can transmit a frame it must detect activity on the shared medium (in this case the air interface).
- Timers and Back-off periods are used in the event that the medium is in use.

As with wired Bus LANs collisions can occur.

### <mark style="background:#69E772;">Collision Detection on a WLAN:</mark>

Collision Detection (CD) within a Wired LAN relies on a transmitting station being able to detect a collision:
- This is not always the case with a Wireless LAN.
- Due to distances between stations not all transmissions are visible to all stations as per the “Hidden Station Problem”.

<mark style="background:#69E772;">Hidden Station Problem:</mark>

![](https://i.imgur.com/1ib77HE.png)


<mark style="background:#69E772;">Collision Avoidance on WLAN:</mark>

The approach to dealing with collisions on a WLAN is to avoid collisions in the first instance.

The technique is known as Collision Avoidance:
- This technique uses fixed timers and a message exchange technique.
- When used with CSMA the technique is called CSMA/CA

<mark style="background:#69E772;">CSMA/CA:</mark>

Message exchange technique uses two messages:
- <mark style="background:#69E772;">Ready To Send</mark> (<mark style="background:#69E772;">RTS</mark>) and <mark style="background:#69E772;">Clear To Send</mark> (<mark style="background:#69E772;">CTS</mark>).

The timers used are called:
- <mark style="background:#69E772;">Short Inter-Frame Space</mark> (<mark style="background:#69E772;">SIFS</mark>) and <mark style="background:#69E772;">Distributed Inter-Frame Space</mark> (<mark style="background:#69E772;">DIFS</mark>) and,
- <mark style="background:#69E772;">Network Allocation Vector</mark> (<mark style="background:#69E772;">NAV</mark>).

![](https://i.imgur.com/Yn92q94.png)

# <mark style="background: #69E772;">15. Hardware MAC Addressing</mark>

#DataComms 

### <mark style="background:#69E772;">Hardware Addressing:</mark>

LAN technologies facilitate sharing of information between <mark style="background:#69E772;">all</mark> locally connected stations

Direct communication between specific pairs of stations is achieved using an <mark style="background:#69E772;">addressing scheme</mark>

Each station is assigned a <mark style="background:#69E772;">UNIQUE</mark> address called a <mark style="background:#69E772;">Hardware Address</mark> or a <mark style="background:#69E772;">MAC Address</mark>

An example of an Ethernet MAC address is: <mark style="background:#69E772;">00:40:05:1c:0e:9f</mark>

Ethernet MAC addresses are 48-bit long and are usually represented in Hex format; 12 Hex digits, each digit representing 4 bits

### <mark style="background:#69E772;">Hardware Addressing in Frames:</mark>

The header within each transmitted frame contains the addresses of the sender and receiver

This allows the LAN interface card (<mark style="background:#69E772;">Network Interface Card</mark> aka <mark style="background:#69E772;">NIC</mark>) to filter out frames without conferring with the CPU:

The NIC only interrupts the CPU when it has data specific to the station

All other frames are discarded

### <mark style="background:#69E772;">The Network Interface Card (NIC):</mark>

![](https://i.imgur.com/ax8yxeU.png)


### <mark style="background:#69E772;">Hardware Addressing Allocation:</mark>

Different addressing schemes are employed on different LAN topologies.

Each station’s address must be unique on the LAN to which it connects.

Address allocation falls into three categories:
- <mark style="background:#69E772;">Static:</mark> The h/w manufacturer sets the address
- <mark style="background:#69E772;">Dynamic:</mark> Stations sets their address at boot-up
- <mark style="background:#69E772;">Configurable:</mark> The admin sets the address

### <mark style="background:#69E772;">Types of Communication:</mark>

There are three types of communication possible on a LAN:
- <mark style="background:#69E772;">Unicast:</mark> This is station-to-station communication.
- <mark style="background:#69E772;">Broadcast:</mark> This is station-to-ALL stations communications.
- <mark style="background:#69E772;">Multicast:</mark> This is station-to-SOME station communications.

Each type of communication requires its own address.

Unicast communication requires the use of unique MAC addresses. All NICs are configured with a unique MAC address.

Broadcast communication requires one address to be recognised by all stations: All NICs are configured to recognised the broadcast address of all ones (FF:FF:FF:FF:FF:FF)

Multicast communications require one address to be recognised by some stations.


# <mark style="background: #69E772;">16. Extending LANs:</mark>

#DataComms 
### <mark style="background:#69E772;">Extending the reach of LANs:</mark>

Where there is a need to <mark style="background:#69E772;">extend</mark> or <mark style="background:#69E772;">interconnect</mark> LANs <mark style="background:#69E772;">three</mark> devices can be used:

<mark style="background:#69E772;">Repeaters:</mark>
- Used to interconnect identical LANs i.e. LANs using the <mark style="background:#69E772;">same</mark> MAC protocols (e.g. conforming to IEEE 802.3 or 802.5 etc.).
- Repeaters do <mark style="background:#69E772;">not</mark> process frames.

<mark style="background:#69E772;">Bridges:</mark>
- Used to interconnect LANs that use <mark style="background:#69E772;">similar</mark> or <mark style="background:#69E772;">different</mark> MAC protocols (e.g. IEEE 802.3 and/or 802.5 etc.).
- Bridges <mark style="background:#69E772;">do</mark> process frames.
	
<mark style="background:#69E772;">Routers:</mark>
- Similar to bridges but with extra functionality i.e. used to interconnect <mark style="background:#69E772;">different</mark> LAN technologies. To be examined later under the topic <mark style="background:#69E772;">Internetworking</mark>

### <mark style="background:#69E772;">Repeaters:</mark>

Repeaters are used to overcome the distance limitation of LANs:

Recall that transmission signals attenuate over distance.

The length of a LAN segment is restricted to address attenuation e.g. a 10Base5 LAN has a length restriction of 500m.

When there is a need to interconnect stations beyond this distance, a <mark style="background:#69E772;">Repeater</mark> can be used.

A Repeater connects <mark style="background:#69E772;">segments</mark> of a LAN: It does <mark style="background:#69E772;">not</mark> connect two LANs i.e. unique addressing is still required.

<mark style="background:#69E772;">Basic functionality:</mark>
- Repeaters regenerate attenuated bits. For each bit received a fresh signal is reproduced.
- Repeaters forward every frame without filtering.

<mark style="background:#69E772;">Repeater Implementation:</mark>

![](https://i.imgur.com/Ol6Dc1R.png)

### <mark style="background:#69E772;">Bridges:</mark>

Bridges facilitate the interconnection of <mark style="background:#69E772;">small</mark> LANs to create <mark style="background:#69E772;">one</mark> large LAN: This is preferable to creating a single large LAN.

<mark style="background:#69E772;">Advantages of using small interconnected LANs:</mark>

<mark style="background:#69E772;">Reliability:</mark> The effects of a fault can be contained and restricted to only a few stations.

<mark style="background:#69E772;">Performance:</mark> Smaller LANs provide better performance to <mark style="background:#69E772;">locally</mark> attached devices. This ties in with the <mark style="background:#69E772;">Principal of Locality of Reference</mark>:

The <mark style="background:#69E772;">majority</mark> of traffic is often between <mark style="background:#69E772;">locally</mark> connected stations

<mark style="background:#69E772;">Security:</mark> With some LAN topologies such as Bus and Wireless LANs <mark style="background:#69E772;">all</mark> stations can potentially see <mark style="background:#69E772;">all</mark> frames. The use of a Bridge facilitates the <mark style="background:#69E772;">physical</mark> isolation of high security traffic <mark style="background:#69E772;">and</mark> users with special security access.

<mark style="background:#69E772;">Geography:</mark> It facilitates extending a LAN to isolated clusters of stations using long distance communications links e.g. microwave links, satellite links etc.

Bridges can interconnect more than 2 LANs.

### <mark style="background:#69E772;">Bridge Implementation:</mark>

![](https://i.imgur.com/QmOWmQT.png)

### <mark style="background:#69E772;">Functions of a bridge:</mark>

Basic Bridges only understand one frame format e.g. 802.3, 805.5 etc. These are sometimes called MAC Relay Bridges.

<mark style="background:#69E772;">Store and Forward Functionality:</mark>

Operating in <mark style="background:#69E772;">promiscuous</mark> mode a Bridge reads all frames transmitted on one LAN.

It <mark style="background:#69E772;">retransmits</mark> frames to an outgoing port to which another LAN is connected only if the destination station is on that LAN.

The <mark style="background:#69E772;">retransmission</mark> is done <mark style="background:#69E772;">without modification</mark> to the frame i.e. <mark style="background:#69E772;">bit-by-bit</mark>.

This function is performed in <mark style="background:#69E772;">both</mark> directions.


<mark style="background:#69E772;">Routing and Addressing:</mark>

Not all frames are copied. Only those relevant to a particular LAN segment are copied. This implies a routing capability.

The use of a bridge does not affect how stations communicate with each other:

Unique MAC addresses are used for routing frames between stations connected to the same bridged network.

A routing strategy is used to decide which frames are forwarded onto another LAN.

There are two routing strategies to consider:
- Fixed routing.
- Address Learning

### <mark style="background:#69E772;">Fixed Routing Strategy:</mark>

<mark style="background:#69E772;">Fixed routing:</mark>

For each pair of source-destination station a route is created in a routing table stored on the bridge.

Based on the destination address in a received MAC frame the bridge performs a lookup of the routing table to determine if the frame is to be forwarded.

<mark style="background:#69E772;">Advantages/Disadvantages of fixed routing:</mark>

Simplicity. Requires minimal processing overhead. However, this can become very complicated if multiple bridges are used.

Requires a lot of manual intervention when more stations/bridges are added or removed.

<mark style="background:#69E772;">Example Bridge Routing Table:</mark>

![](https://i.imgur.com/xQYbowe.png)


### <mark style="background:#69E772;">Address Learning Routing Strategy:</mark>

<mark style="background:#69E772;">Address Learning</mark> is an alternative approach to routing. Here the Bridge can <mark style="background:#69E772;">learn</mark> the location of each station <mark style="background:#69E772;">automatically</mark> because:
- Each incoming MAC frame contains a <mark style="background:#69E772;">source address</mark> field.
- Each LAN attaches to one <mark style="background:#69E772;">port</mark> only.

Using both of these identifiers the bridge constructs <mark style="background:#69E772;">a routing table</mark> automatically i.e. without manual intervention

<mark style="background:#69E772;">Address learning starts at boot-up time:</mark>

Initially the routing table is empty.

As MAC frames arrive on any of the incoming ports the Bridge constructs the routing table using the source MAC address/source port information.

After a period of time known as the <mark style="background:#69E772;">steady-state</mark> period the table is complete: <mark style="background:#69E772;">Frame filtering</mark> can commence in earnest.

<mark style="background:#69E772;">Address Learning Process:</mark>

![](https://i.imgur.com/8wXqOQB.png)

### <mark style="background:#69E772;">Address Learning Routing Strategy:</mark>

Bridges that use an address learning strategy are known as <mark style="background:#69E772;">Transparent Bridges</mark>:

Stations connected to the LAN are unaware of the existence of the bridge.

A problem with Transparent Bridges is <mark style="background:#69E772;">Looping</mark>:
- Arises from the use of <mark style="background:#69E772;">redundant bridges</mark>,
- Redundant bridges are often used for reliability in the event that one bridge fails; another bridge can take over.

Redundant bridges can create loops within the network as follows

![](https://i.imgur.com/C0q83ir.png)


### <mark style="background:#69E772;">Overcoming Bridging Loops:</mark>

Graph theory is used to create a loop-free bridge network:

A <mark style="background:#69E772;">Spanning Tree</mark> is a graph in which there is no loop.

To create a <mark style="background:#69E772;">Spanning Tree</mark> the network is represented as a graph:
- Here the graph <mark style="background:#69E772;">nodes</mark> represent the bridges and the LANs to which they connect,
- The connecting <mark style="background:#69E772;">arcs</mark> represent the connections between a LAN(s) and a bridge(s),
- Each arc is a assigned a <mark style="background:#69E772;">cost metric</mark> (‘1’ in the direction of a bridge to a LAN and, ‘0’ for the opposite direction)

An example bridged network:

![](https://i.imgur.com/3PEGQ8C.png)

Finding the Spanning Tree involves three steps:
- Identify the <mark style="background:#69E772;">Root Bridge</mark>. The bridge with the lowest value ID (usually the Bridge serial number) is designated the Root bridge,
- Find the <mark style="background:#69E772;">shortest path</mark> from the Root Bridge to every other bridge and LAN in the network,
- Eliminate redundant routes. The routes with the shortest paths become the spanning tree.

All bridge ports in the spanning tree are marked as <mark style="background:#69E772;">forwarding ports</mark>:

All other ports are marked as <mark style="background:#69E772;">blocking ports</mark>.

### <mark style="background:#69E772;">Finding the Shortest Path:</mark>

![](https://i.imgur.com/A38BueT.png)


### <mark style="background:#69E772;">A loop-free Bridged Network:</mark>

![](https://i.imgur.com/DttnjDc.png)

![](https://i.imgur.com/QRxjjeh.png)

### <mark style="background:#69E772;">Advantages of using Bridges:</mark>

<mark style="background:#69E772;">Parallelism:</mark>
- Not every frame arriving at the bridge is copied to another LAN:
- This allows for two pairs of stations to communicate simultaneously provided each pair is on a separate LAN and separated by a bridge.

<mark style="background:#69E772;">Optimised performance:</mark>
- Stations that are likely to communicate with each other frequently can be moved to the same LAN to ensure adherence to the Principal of Locality of Reference.
- Collision Domains are smaller, reducing the likelihood of collisions occurring

<mark style="background:#69E772;">Optimised performance and Parallelism:</mark>
![](https://i.imgur.com/4VKqfL1.png)


Without bridging each station perceives the speed of the LAN as:

(LAN Data Rate) / (number of stations).

This is significantly improved with bridging.

### <mark style="background:#69E772;">Collision Domains are reduced in size:</mark>

![](https://i.imgur.com/9i8QjAH.png)


<mark style="background:#69E772;">With</mark> bridging the size of the collision domain is reduced and contention is therefore reduced.

### <mark style="background:#69E772;">Summary of Bridges:</mark>

Used to extend LANs creating small interconnected LANs rather than a single large LAN.

Can connect LANs with similar <mark style="background:#69E772;">or</mark> different MAC protocols.

Contains <mark style="background:#69E772;">Routing</mark> functionality to <mark style="background:#69E772;">filter</mark> frames:
- This facilitates parallelism which in turn improves performance of each connected LAN
- Also, collisions are not copied between LANs which reduces the Collision Domain and improves contention ratio.

Contains <mark style="background:#69E772;">Store</mark> and <mark style="background:#69E772;">Forward</mark> functionality:
- Facilitates connecting fast, busy LANs to slow LANs.


# <mark style="background: #69E772;">17. Intro to Internets:</mark>
#DataComms 
### <mark style="background:#69E772;">Problems with LAN technologies:</mark>

From previous discussions on LANs there are a variety of <mark style="background:#69E772;">networking</mark> technologies available to facilitate communications between host computers:

For any given LAN implementation, host computers can only communicate with other hosts attached to the <mark style="background:#69E772;">same</mark> networking technology.

It is not unreasonable to assume that many organisations may employ a variety of <mark style="background:#69E772;">technologies</mark>

This is usually for historical reasons due to mergers and take-overs etc.

Historically this can lead to the creation of <mark style="background:#69E772;">islands</mark> of networks within organisations:

Difference in frame formats, Electrical characteristics (voltages, wiring types, etc.) and Addressing Schemes prevented <mark style="background:#69E772;">direct</mark> communications between hosts connected to different LAN technologies

Today, there is a need to facilitate communication between any two hosts regardless of the type of LAN they attach to

This is similar to telephone systems which facilitate communication between any two telephones. For example between a mobile phone and a fixed-line phone

This is known as universal service and is a fundamental concept within networking

### <mark style="background:#69E772;">Universal Service:</mark>

With <mark style="background:#69E772;">Universal Service</mark>: A user on any host in any part of an organisation can send messages or data to any other user without any knowledge of the underlying networking technology.

Whilst highly desirable <mark style="background:#69E772;">universal service</mark> can be difficult to achieve due to incompatibilities between network technologies.

The provision of <mark style="background:#69E772;">Universal Service</mark> for host computers requires addressing the problems associated with <mark style="background:#69E772;">heterogeneous</mark> (multiple) network technologies.

The introduction of <mark style="background:#69E772;">Internetworking</mark> technology is the solution.

### <mark style="background:#69E772;">Universal Service through Internetworking:</mark>

<mark style="background:#69E772;">Internetworking introduces a new hardware component and new software :</mark>

Additional hardware is needed to provide a physical interconnection between LANs for the purpose of routing traffic:
- This hardware needs a physical connection to each LAN using the correct NIC.
- Only then can it route and deliver traffic between LANs.

<mark style="background:#69E772;">Additional software is also required to:</mark>

Address the <mark style="background:#69E772;">lack of</mark> uniqueness when using MAC addresses,

Address the <mark style="background:#69E772;">lack of</mark> summary routing when using MAC addresses,

Introduce a single, unique <mark style="background:#69E772;">“framing”</mark> structure/format understood by all hosts.

The result is a system of connected physical networks known as an <mark style="background:#69E772;">internetwork</mark> or <mark style="background:#69E772;">internet</mark> as shown in the next slide.

There is no restriction on the size of an <mark style="background:#69E772;">internet</mark>. However, there are reliability, efficiency and performance issues to consider when designing and/or attaching to an internet

<mark style="background:#69E772;">An example of a small internet:</mark>

![](https://i.imgur.com/4xDbPVW.png)


<mark style="background:#69E772;">An example of a larger internet:</mark>

![](https://i.imgur.com/QlxHL9t.png)

### <mark style="background:#69E772;">The Hardware components - Routers:</mark>

The hardware component is called a <mark style="background:#69E772;">Router</mark>.

It is a special purpose computer used for <mark style="background:#69E772;">interconnecting</mark> networks:

It is like any host computer in that it contains: a CPU, RAM, I/O interfaces (Network Interface Cards) etc.

Whilst the previous diagram shows a router connecting only two networks; in practise a single router can connect many LANs.

Also, many organisations use <mark style="background:#69E772;">multiple</mark> routers to maximise performance and to allow for <mark style="background:#69E772;">redundancy</mark>.

To provide <mark style="background:#69E772;">universal service</mark> the routers must physically pass data between the LANs

### <mark style="background:#69E772;">The Software Component - Internet Protocol (IP):</mark>

As already discussed, passing data directly between different <mark style="background:#69E772;">LANs</mark> technologies is impossible due to differing <mark style="background:#69E772;">frame formats</mark> and <mark style="background:#69E772;">addressing schemes</mark>.

Internet <mark style="background:#69E772;">protocol software</mark> addresses these issues by:

Introducing a <mark style="background:#69E772;">single</mark> globally-unique addressing scheme:

This single scheme hides the underlying <mark style="background:#69E772;">multiplicity</mark> of physical addressing schemes (recall static, dynamic and configurable MAC addresses) employed on each LAN.

Introducing a <mark style="background:#69E772;">single</mark> “framing” structure called a “Packet/Datagram” that is understood by <mark style="background:#69E772;">all</mark> host computers.

<mark style="background:#69E772;">The IP Datagram/Packet:</mark>

![](https://i.imgur.com/GCFErEZ.png)


<mark style="background:#69E772;">IP Datagram and the Internet:</mark>

![](https://i.imgur.com/xli1dgA.png)

<mark style="background:#69E772;">Internetworking technology - Providing Universal Service for Host Computers:</mark>

The routers combined with the internet protocol software makes universal access possible.

However, internets are really an abstraction

No such network exists in reality, consequently they are often called virtual networks.

We will now examine the concepts behind interworking.

Firstly, we will look at the globally unique addressing scheme design especially for interworks.

Secondly, we will look at the role played by the router in delivering data across different network technologies.

# <mark style="background: #69E772;">18. IP Classful Addressing</mark>
#DataComms 


An <mark style="background: #69E772;">internet</mark> must operate like any other network:
- It must allow hosts to send and receive data to each other
- To facilitate this some type of <mark style="background: #69E772;">addressing scheme</mark> is
- required
- i.e. all hosts require a <mark style="background: #69E772;">unique</mark> address

So <mark style="background: #69E772;">addressing</mark> is a <mark style="background: #69E772;">critical</mark> component of the <mark style="background: #69E772;">internet abstraction</mark>

The <mark style="background: #69E772;">Internet Protocol </mark>(<mark style="background: #69E772;">IP</mark>) defines such an addressing scheme

IP addressing is <mark style="background: #69E772;">independent</mark> of the underlying physical addressing scheme

### <mark style="background: #69E772;">A multi-node internet:</mark>
    
![](https://i.imgur.com/xv2h2N6.png)
 
### <mark style="background: #69E772;">IP Address Hierarchy:</mark>

Each host/router <mark style="background: #69E772;">interface</mark> is assigned a <mark style="background: #69E772;">unique</mark> 32-bit <mark style="background: #69E772;">IP address</mark>

This address is used in packets that are sent across an internet

Each IP address consists of two parts: a <mark style="background: #69E772;">prefix</mark> and a <mark style="background: #69E772;">suffix</mark>

Each physical network is assigned a <mark style="background: #69E772;">unique network number</mark> which forms the <mark style="background: #69E772;">network prefix</mark> part of a host’s IP address.

It uniquely identifies the physical network to which the host is attached

The <mark style="background: #69E772;">host suffix</mark> uniquely identifies the host on that network.

<mark style="background: #69E772;">Network numbers/prefixes</mark> are assigned <mark style="background: #69E772;">globally</mark>, <mark style="background: #69E772;">host</mark> suffixes are assigned <mark style="background: #69E772;">locally</mark>
    
### <mark style="background: #69E772;">Dotted Decimal Notation:</mark>

Representing IP addresses in 32-bit binary form is only suitable for computers.

A human-friendly version of IP addresses is known as <mark style="background: #69E772;">dotted-decimal notation</mark>.

Here each <mark style="background: #69E772;">octet</mark> of the IP address is represented as a decimal value separated by a dot ‘.’
- Examples include: 129.52.6.0, 128.10.2.3 and 128.128.255.0
- Each decimal value represents 8-bits,
- Consequently, the range of decimal numbers extends from 0 - 255

 
### <mark style="background: #69E772;">IP Address Hierarchy:</mark>

The IP addressing scheme must accommodate large <mark style="background: #69E772;">and</mark> small internets:

This was originally achieved using classful <mark style="background: #69E772;">IP addressing</mark>

Classful Addressing was the first attempt to organise the IP address space

### <mark style="background: #69E772;">Original Classful IP addressing:</mark>

- Here the IP address space was divided into <mark style="background: #69E772;">five</mark> classes:
- Each class had different size <mark style="background: #69E772;">prefix</mark> and <mark style="background: #69E772;">suffix</mark> portions to accommodate large and small networks.
- The first four bits identify the <mark style="background: #69E772;">class</mark> to which the address belongs (see next slide).
- <mark style="background: #69E772;">Classes A, B and C</mark> are known as the <mark style="background: #69E772;">primary classes</mark> because they are used for <mark style="background: #69E772;">host addressing</mark>.
- Class D addresses are used for <mark style="background: #69E772;">multicasting</mark>
- Class E was reserved for future use

### <mark style="background: #69E772;">Classful IP Addressing Scheme:</mark>

![](https://i.imgur.com/NUXm2Q0.png)

Note the different sizes of the <mark style="background: #69E772;">prefix</mark> and <mark style="background: #69E772;">suffix</mark> portions for each class:

For Class A addresses the first octet is the <mark style="background: #69E772;">network prefix</mark> and the last three octets are the <mark style="background: #69E772;">host suffix</mark>.

Notice also the split between <mark style="background: #69E772;">network prefix</mark> and <mark style="background: #69E772;">host suffix</mark> for Classes B and C

![](https://i.imgur.com/kOf7yq7.png)

### <mark style="background: #69E772;">Routing of IP Packets:</mark>

Q: Why is the separation of prefix and suffix important?

A: Routers are responsible for directing datagrams/packets onto their final destination.
- This is called <mark style="background: #69E772;">routing</mark>.
- The router needs to look at the address to make a decision about where to route a packet.
- This is similar to the Post Office delivering letters

### <mark style="background: #69E772;">Routing of "Letters":</mark>

Letters are routed through <mark style="background: #69E772;">National</mark> and <mark style="background: #69E772;">Local</mark> sorting offices.

National Sorting Offices tend to be far away from the destination.

They only need to examine the County/Town to route the letter towards a sorting office closest to the destination

The Local Sorting Office closest to the destination examines the Street Name and House Number to make the final delivery.

This Post Office analogy is similar to the way Routers route incoming IP packets.

### <mark style="background: #69E772;">Back to routing of "Packets":</mark>

Routers far away from the Destination router can be considered <mark style="background: #69E772;">National</mark> Sorting Offices:

They only need to examine <mark style="background: #69E772;">network prefixes</mark> (similar to <mark style="background: #69E772;">County/Town</mark>) in an attempt to route the packet towards the final destination router.

The Router closest to the destination station can be considered a <mark style="background: #69E772;">Local Sorting</mark> Office

They examine the entire destination IP address including the <mark style="background: #69E772;">host suffix</mark>

### <mark style="background: #69E772;">Routing of IP Packets using Classful Addressing:</mark>

Classful IP addresses are <mark style="background: #69E772;">self-identifying</mark> as the <mark style="background: #69E772;">network prefix</mark> portion of an IP address can be computed from the address itself:

The first four bits will determine the class and hence the <mark style="background: #69E772;">network prefix</mark>.

Refer to the next slide to see how the bits relate to the classes.

This makes it easy for <mark style="background: #69E772;">“far away”</mark> routers to route packets towards the destination router

Whilst dotted-decimal notation represents IP addressing in a simple form it does hide the first four bits:

Instead, we humans have to rely on range values to determine the Class of the address:
- For Class A addresses the first octet is in the range 0-127,
- For Class B addresses the range is 128-191, and,
- For Class C addresses the range is 193-223


### <mark style="background: #69E772;">Classful IP address values:</mark>

![](https://i.imgur.com/PWxKt7b.png)
    
### <mark style="background: #69E772;">Routing of IP Packets using Classful Addressing</mark>

Whilst <mark style="background: #69E772;">dotted-decimal notation</mark> represents OP addressing in simple form it does hide the first four bits

Instead, we humans have to rely on range values to determine the four classes of the address
* For Class A addresses the <mark style="background: #69E772;">first</mark> octet is in the range 0-127,
* For Class B addresses the range is 128-191, and,
* For Class C addresses the range is 193-223.


### <mark style="background: #69E772;">Classful Addressing Example:</mark>

![](https://i.imgur.com/s3IBbhw.png)

### <mark style="background: #69E772;"> Subnet and Classless IP Addressing:</mark>

A problem with <mark style="background: #69E772;">Classful addressing</mark> is that it results in an <mark style="background: #69E772;">unequal</mark> division of the <mark style="background: #69E772;">IP address space</mark>.

As the global Internet has grown, the use of <mark style="background: #69E772;">classful addressing</mark> has become problematic:
* The IP address space is being exhausted,
* Many addresses remain unused,
* Refer to examples in class.
	
Two new addressing methods are used to overcome this: <mark style="background: #69E772;">subnet addressing</mark> and <mark style="background: #69E772;">classless addressing</mark>

Here the division between the prefix and suffix portions can occur on any bit boundary: e.g. a 20-bit <mark style="background: #69E772;">network prefix</mark> + 12-bit <mark style="background: #69E772;">host suffix</mark> is possible.

To facilitate Classless Addressing, an additional piece of information is defined with each address block: Known as an <mark style="background: #69E772;">address mask</mark> or <mark style="background: #69E772;">subnet mask</mark>.

<mark style="background: #69E772;">Masks</mark> are 32-bit values that facilitate the extraction of the <mark style="background: #69E772;">network prefix</mark> from any given IP address:
* They are comprised of a contiguous sequence (unbroken sequence) of 1 bits followed by a contiguous sequence of 0 bits.
* They can be represented in dotted-decimal notation just like IP addresses.


### <mark style="background: #69E772;">Example Classless IP Addressing Allocation:</mark>

![](https://i.imgur.com/7rm5oyG.png)

![](https://i.imgur.com/AO2A5Ub.png)

Note the <mark style="background: #69E772;">address mask</mark> or <mark style="background: #69E772;">subnet mask</mark> for the 192.4.10.0/24 network.

The <mark style="background: #69E772;">/XX </mark>(‘slash’ XX) is another way to represent masks:

<mark style="background: #69E772;">/24</mark> means that the mask is comprised of 24 ONE bits followed by 8 (32-24) ZERO bits:

This notation is known as Classless Inter-Domain Routing (CIDR): 
* It is a human-friendly way of representing <mark style="background: #69E772;">address masks</mark>
* In <mark style="background: #69E772;">dotted-decimal notation</mark>, this mask can be represented as: <mark style="background: #69E772;">255.255.255.0</mark>
* The first three octets are all ONEs, the last octet is all ZEROs.


### <mark style="background: #69E772;">Using Address Masks to route packets:</mark>

Following on from the previous discussion on routing.

Recall that for any given destination IP address, the router must determine the <mark style="background: #69E772;">network prefix</mark> portion:
* The router uses the <mark style="background: #69E772;">network prefix</mark> to query its <mark style="background: #69E772;">routing table</mark>.

With Classless addressing, routers use the <mark style="background: #69E772;">Mask</mark> (aka: <mark style="background: #69E772;">network masks</mark>, <mark style="background: #69E772;">subnet masks</mark>) to extract the <mark style="background: #69E772;">network prefix</mark> portion from a destination IP address:
- Recall that with <mark style="background: #69E772;">classful address</mark>, the router simply examined the first four bits of the address to determine the class.

For an incoming packet with a destination IP address, D, the router tests the following condition: <mark style="background: #69E772;">A = = (D&&M)</mark>

<mark style="background: #69E772;">Where:</mark>
* <mark style="background: #69E772;">A</mark> is the IP address (network number) of networks that the router knows about,
* <mark style="background: #69E772;">M</mark> is the mask associated with the network, and,
* <mark style="background: #69E772;">D</mark> represents a destination IP address that the router needs to make a routing decision.

### <mark style="background: #69E772;">Address Masks:</mark>

For example, consider the following:
* A = 11000000 00000100 00001010 00000000
* D = 11000000 00000100 00001010 00000011
* M = 11111111 11111111 11111111 00000000
	
The mask, <mark style="background: #69E772;">M</mark>, is ‘applied’ to the Destination IP address <mark style="background: #69E772;">D</mark> i.e. D && M
- The <mark style="background: #69E772;">AND</mark> operation effectively zeros out the last eight bits of <mark style="background: #69E772;">D</mark>.

The result is then compared to the <mark style="background: #69E772;">A</mark> address.

If they match, then the Destination IP address, <mark style="background: #69E772;">D</mark> is said to <mark style="background: #69E772;">belong</mark> to the network, <mark style="background: #69E772;">A</mark>:
- The packet containing the Destination IP address, D, is then <mark style="background: #69E772;">routed</mark> towards network <mark style="background: #69E772;">A</mark>,
* The packet is routed to the address indicated by the <mark style="background: #69E772;">Next Hop</mark> field in the routing table (refer to next slide).

Otherwise, the <mark style="background: #69E772;">next</mark> entry in the routing table will be tried using the above approach.

### <mark style="background: #69E772;">Example IP Routing Table using Classless Addressing:</mark>

![](https://i.imgur.com/g3UUoty.png)
	
### <mark style="background: #69E772;">Classless Addressing and the IP Address Space:</mark>

<mark style="background: #69E772;">Classless addressing</mark> makes more efficient use of the IP address space.

Consider an example of a single <mark style="background: #69E772;">class B prefix</mark> (16-bit prefix): 128.211.0.0
* With <mark style="background: #69E772;">classful</mark> addressing this Class B prefix can only be used to identify a <mark style="background: #69E772;">single</mark> network with approx. 65K host addresses.
* With <mark style="background: #69E772;">classless addressing</mark>, this Class B prefix can be considered as having a 16-bit mask:
	* In dotted-decimal notation: 255.255.0.0
	* In CIDR notation: /16
	
Using <mark style="background: #69E772;">classless addressing</mark>, there are multiple approaches to dividing this large address block into smaller blocks.

### <mark style="background: #69E772;">Classless Addressing VS. IP Address Space:</mark>

Larger value address masks (e.g. /17, /18, /19 etc.) can be used to partition the Class B address block into smaller address blocks (known as <mark style="background: #69E772;">subnets</mark>)

For example, two customers could be allocated subnet address blocks with /28 masks (/28 > /16): 128.211.0.16/28 and, 128.211.0.32/28

Although both subnets have the same mask size (28 bits), the network prefixes differ and are <mark style="background: #69E772;">unique</mark>.

In addition, most of the original /16 address space is still available for allocation to other customers.

### <mark style="background: #69E772;">Basic Subnetting:</mark>

Subnetting allows for the creation of <mark style="background: #69E772;">multiple</mark> logical networks from a single address block.
* Subnets are created by taking one, or more, of the <mark style="background: #69E772;">host</mark> bits from the original address block and using them as <mark style="background: #69E772;">network</mark> bits in the smaller subnet blocks:
* This is achieved by increasing the mask of the original large address block. For example, from <mark style="background: #69E772;">/16 </mark>to <mark style="background: #69E772;">/20</mark>
* The more <mark style="background: #69E772;">host bits</mark> from the original large address block that are used, the more subnets can be defined.

For each additional host bit <mark style="background: #69E772;">taken</mark>, the number of subnetworks available is doubled:
* For example, with <mark style="background: #69E772;">one</mark> host bit taken, two subnets can be defined. With two host bits taken, four subnets are created etc.
* However, with each host bit taken, fewer host addresses are available for each of the subnets.

For example, if <mark style="background: #69E772;">n-bits</mark> are taken from the original host portion:
* The number of <mark style="background: #69E772;">subnets</mark> created is: <mark style="background: #69E772;">2^n</mark>
* The total number of addresses per subnet is <mark style="background: #69E772;">2^m</mark> (<mark style="background: #69E772;">m</mark> = the number of host bits remaining)
* The number of <mark style="background: #69E772;">usable</mark> host addresses: <mark style="background: #69E772;">2^m – 2</mark>;
* The first address in the block is used to identify the <mark style="background: #69E772;">network</mark>, The last address in the block is the <mark style="background: #69E772;">Broadcast Address</mark>

<mark style="background: #69E772;">Basic Subnetting Example:</mark>

Given address block:192.168.1.0/24, divide this network into 2 subnets:

Looking at the original address block:
* /24 means 8 hosts bits i.e. 28 = 256, Addresses
* Of these 256 addresses, 254 are usable for host addresses
* i.e. 28 – 2 = 254.
	
![](https://i.imgur.com/3J7t4xN.png)

<mark style="background: #69E772;">Basic Subnetting:</mark>
	
To divide this network into 2 subnets, <mark style="background: #69E772;">one</mark> bit is taken from the original host portion:

This extends the original mask (255.255.255.0) by one bit as follows:
* 11111111.1111111.1111111.10000000
* In dotted-decimal notation (DDN): <mark style="background: #69E772;">255.255.255.128</mark>
* In CIDR notation: <mark style="background: #69E772;">/25</mark>

Note: <mark style="background: #69E772;">X</mark> below represents the single host bit taken from the host portion of original address block to be used in the network prefix.

![](https://i.imgur.com/NeQhtZA.png)

![](https://i.imgur.com/nS5LYQs.png)

Taking 1 bit from the original host portion creates 2 subnets, each with the same extended subnet mask: <mark style="background: #69E772;">255.255.255.128</mark> or <mark style="background: #69E772;">/25</mark>

For each new sub-net, there are: <mark style="background: #69E772;">7 Host Bits</mark>, i.e. 2<sup>7</sup> = 128 addresses, of which 126 are usable host addresses.

![](https://i.imgur.com/IiCvnwe.png)

The single host bit taken from the original host portion gives: <mark style="background: #69E772;">2^1 = 2</mark> Subnets:
* Leaving <mark style="background: #69E772;">7</mark> bits for the host portion i.e. so <mark style="background: #69E772;">2^7 =128</mark> addresses per subnet,
* With the network and broadcast addresses removed this leaves <mark style="background: #69E772;">2^7 – 2 = 126 usable host addresses</mark> on each subnet
* The <mark style="background: #69E772;">Address Table</mark> needs to be completed:
* The <mark style="background: #69E772;">Magic Number</mark> approach is one way to determine the addresses in each subnet.


### <mark style="background: #69E772;">Basic Subnetting Using Magic Numbers (The Magic Number approach):</mark>

Determine the mask for each new subnet.

In the above example the mask is determined to be: 255.255.255.128

Looking from left-to-right along the new mask, seek the last octet that is non-zero <mark style="background: #69E772;">and</mark> less than or equal to 255.
* In this case, the fourth octet matches this criterion.
* Subtract this octet from 256 as follows:
* 256 – 128 = 128 which is <mark style="background: #69E772;">The Magic Number</mark>

The <mark style="background: #69E772;">Magic Number (MN)</mark> is used to determine the starting network address for <mark style="background: #69E772;">each</mark> of the Subnets:
* To determine network address of the <mark style="background: #69E772;">next</mark> subnet, simply add the MN to the previous network address, taking care to add the MN to the octet from which it was derived.
* In this example, the network address of the <mark style="background: #69E772;">first</mark> subnet is the first address in the original address block: 192.168.1.0
* As the MN (128) was found in the fourth octet, the MN is added to the fourth octet: 192.168.1.0, to give the network address of the <mark style="background: #69E772;">next</mark> subnet: 192.168.1.128

With the <mark style="background: #69E772;">Magic Number</mark> approach, the Address Table is easy to complete as follows

![](https://i.imgur.com/tEN6k1F.png)


<mark style="background: #69E772;">Subnets in Use:</mark>

![](https://i.imgur.com/GTKJ1rW.png)


### <mark style="background: #69E772;">Basic Subnetting:</mark>

Given an address block of 192.168.1.0 /24, we wish to divide this network into 4 subnets:
* Determine the power of 2 to provide 4 networks:
* i.e. <mark style="background: #69E772;">2^? = 4</mark> (Note the number of subnets will be a power of 2)
* Hence <mark style="background: #69E772;">two</mark> bits are required to be taken from the original host portion.
* This leaves <mark style="background: #69E772;">6 bits</mark> remaining for host addresses.

Having calculated the number of host bits required for each subnet, the mask can be determined as follows:

The new Subnet mask is: 11111111.1111111.11111111.11000000
* In DDN: 255.255.255.192
* In CIDR notation: /26

Using the <mark style="background: #69E772;">Magic Number</mark> approach to determine the addresses in each subnet.

With a Mask for each subnet of: 255.255.255.192
* Looking from left-to-right along the new mask, seek the last octet that is non-zero <mark style="background: #69E772;">and</mark> less than or equal to 255.
* In this case, the fourth octet matches this criterion. Subtract this octet from 256 as follows: 256 – 192 = 64 which is The Magic Number

The Address Table can be completed as follows:

![](https://i.imgur.com/2svQZCC.png)

See how the <mark style="background: #69E772;">MN</mark> (64) is used to determine the <mark style="background: #69E772;">network address</mark> for each subnet.

Note: the MN was derived from the fourth octet. Consequently, it is added to this octet in the previous subnet’s network address.

### <mark style="background: #69E772;">Subnetting a Class B Network:</mark>

Given an address block of <mark style="background: #69E772;">172.25.0.0 /16</mark>, we wish to divide this network into 11 subnets with each subnet catering for 3000 hosts:
* Determine the power of 2 to provide for 3000 hosts:
* i.e. <mark style="background: #69E772;">2? = 3000</mark>
* 2^12 is sufficient (i.e. 211 = 2048, 2 12 = 4096)
* This requires four bits to be borrowed from the second octet.
* Leaving <mark style="background: #69E772;">12 bits</mark> for host addresses.

The new Subnet mask is:
* 11111111.1111111.11110000.00000000
* In DDN: <mark style="background: #69E772;">255.255.240.0</mark>
* In CIDR notation: <mark style="background: #69E772;">/20</mark>
	
Using the <mark style="background: #69E772;">Magic Number</mark> approach to determine the addresses in each subnet.

With a Mask for each subnet of: 255.255.240.0
* Looking from left-to-right along the new mask, seek the last octet that is non-zero <mark style="background: #69E772;">and</mark> less than or equal to 255.
* In this case, the third octet matches this criterion.
* Subtract this octet from 256 as follows: 256 – 240 = 16 which is <mark style="background: #69E772;">The Magic Number</mark>

The Address Table can be completed as follows:

![](https://i.imgur.com/Fyl7zNN.png)
 
### <mark style="background: #69E772;">Basic Subnetting:</mark>

![](https://i.imgur.com/Npkpm8K.png)

See how the <mark style="background: #69E772;">MN</mark> (16) is used to determine the <mark style="background: #69E772;">network address</mark> for each subnet. 

Note: the MN was derived in the third octet. Consequently, it is added to this octet in the previous subnet’s network address.

### <mark style="background: #69E772;">Special IP Addresses:</mark>

IP defines a set of special address forms that are reserved and should never be assigned to hosts

These include:
* <mark style="background: #69E772;">Directed Broadcast Address:</mark> This is defined for <mark style="background: #69E772;">each</mark> physical network. A <mark style="background: #69E772;">suffix</mark> of all 1 bits is added to the network prefix
* <mark style="background: #69E772;">Limited Broadcast Address.</mark> Here an <mark style="background: #69E772;">address</mark> consisting of all 1 bits will allow a broadcast on “a single wire”
* <mark style="background: #69E772;">This Computer Address.</mark> An IP address consisting of all zeros refers to <mark style="background: #69E772;">this computer</mark>. Used by hosts at <mark style="background: #69E772;">boot-up</mark> to obtain its IP address
* <mark style="background: #69E772;">Loopback Address:</mark> This has a network prefix 127/8; the host suffix is irrelevant but is usually set to 1 i.e. 127.0.0.1


### <mark style="background: #69E772;">Routers and Multi-Homed Hosts:</mark>

Routers <mark style="background: #69E772;">and</mark> multi-homed host computers are assigned two or more IP addresses because: 
* They have connections to multiple physical networks
* Each IP address prefix specifies <mark style="background: #69E772;">only one</mark> physical network.

A fundamental principle of the IP addressing scheme:
“An IP address does not identify a specific computer. Instead, each IP address identifies a connection between a computer and a network. A computer with multiple network connections, e.g. a router, requires one IP address for each connection.”

<mark style="background: #69E772;">A router addressing example:</mark>
![](https://i.imgur.com/5szfNDr.png)


### <mark style="background: #69E772;">An example Classless Address Allocation:</mark>

An organisation with an address block 17.12.40.0/26 has to divide this block for three separate networks requiring 32, 16 and 16 addresses.

Firstly the size of the subnet masks for each sub-network needs to be calculated as follows:
* 32 addresses requires a mask of 27 i.e. 2 32-27 = 32
* 16 addresses requires a mask of 28 i.e. 2 32-28 = 16
 

An example configuration for this organisation would be:

![](https://i.imgur.com/LbrbpdS.png)


### <mark style="background: #69E772;">Another example of Classless Address Allocation:</mark>

An ISP is allocated an address block 190.100.0.0/16.

There are two groups of customers that need to be allocated addresses as follows:

Group 1 - This group consists of 64 customers each requiring 256 addresses.

Group 2 - This group consists of 128 customers each requiring 128 addresses.

To be completed in class.

### <mark style="background: #69E772;">Example IP Routing Table:</mark>

![](https://i.imgur.com/VzY92OK.png)

Note the network numbers and the connections to the routers.

![](https://i.imgur.com/haubOLS.png)

# <mark style="background: #69E772;">19. Protocol Hierarchies:</mark>

#DataComms 

Computer networks are generally comprised of numerous pieces of hardware and software

Recall the previous attempt to "model" how these components interconnect and interact with each other

![](https://i.imgur.com/pERkopl.png)

Whilst this horizontal model is useful when looking at hardware components, the reality is that it does not explain everything.

From previous discussions on: <mark style="background: #69E772;">Data Link Control, LANs technologies, Internetworking </mark> etc. much of the functionality required to provide communications between host machines is not necessarily provided on a single hardware component as suggested by the previous slide

The purpose of each layer is to provide <mark style="background: #69E772;">one</mark> component of  the overall solution to the <mark style="background: #69E772;">“Communications Problem”</mark> such  as “frame reception/transmission” etc.

These layers of software can exist on: separate hardware components and/or hosts or, in some instances multiple layers can exist on a single hardware component and/or hosts

This concept is not dissimilar to the approach used  for software development:
* Objects or libraries are used to perform specific operations.
* Importantly the object/library function keeps details of its internal state and algorithms hidden from the main program.
 
The same approach is used for network protocol software:
* Each layer of software provides one part of the solution such  as: frame transmission/reception or, transmitting one/zeros  onto a wire/wireless transmission medium etc.
	
With networking software, the layers of protocol  software are organised into a Stack:
* Each layer sits between other layers as shown in the next slide.
* Each layer is said to offer services to higher layers and to use the services offered by the lower layers.
	
<mark style="background: #69E772;">The ISO OSI Reference Model:</mark>
	
![](https://i.imgur.com/xOEOvAv.png)
	
### <mark style="background: #69E772;">Protocol Hierarchies - Terminology:</mark>
	
<mark style="background: #69E772;">Protocol/Protocol Entity:</mark> A software module that performs one sub-task such as: frame transmission/reception etc.

<mark style="background: #69E772;">Protocol suites/stack:</mark> A number of such software modules that work together to perform all of the tasks required to enable two hosts communicate.

<mark style="background: #69E772;">Protocol Architectures/Model:</mark> A model by which we can categorise or view the different protocol layers.

The following slide provides an analogy to the Communications Problem:
* How can two CEOs communicate with each other effectively and efficiently?

![](https://i.imgur.com/SheCkhL.png)

### <mark style="background: #69E772;">The OSI ISO Reference (7 layer model):</mark>
	
Communications between computer hosts presents the same challenges.

The OSI model deals with connecting <mark style="background: #69E772;">open</mark> systems: i.e. systems that are <mark style="background: #69E772;">open</mark> for communication with <mark style="background: #69E772;">other</mark> systems  regardless of who built them or how they were manufactured.

The principles that were applied to arrive at the seven layers are as follows: 
* Each layer was created when a different <mark style="background: #69E772;">level of abstraction</mark> was required.
* Each layer performs one well-defined function with each function chosen carefully to facilitate the development of <mark style="background: #69E772;">standardised protocols</mark>.
* The number of layers chosen was sufficient enough to ensure that distinct functions were not <mark style="background: #69E772;">lumped</mark> together to become unwieldy.

The layers of software work together in unison to provide overall solutions to the problems of communicating between host computers across complex networks.

<mark style="background: #69E772;">Information</mark> flows across each of the interfaces (boundaries) between the layers:
* These boundaries were carefully defined to <mark style="background: #69E772;">minimise</mark> information flow across the interfaces.
* The following slides discuss the functionality of each layer of protocol software. This functionality should be recognisable from previous discussions.

![](https://i.imgur.com/5Q1NfEh.png)

### <mark style="background: #69E772;">The 7 layer Model: Layer-by-layer:</mark>
	
<mark style="background: #69E772;">The Physical Layer (Layer 1):</mark> 
* Concerned with  transmitting <mark style="background: #69E772;">raw</mark> bits over a <mark style="background: #69E772;">communication channel</mark>:
* Its purpose is to ensure that the transmission of binary 1s and 0s adheres to what is appropriate for the transmission medium and what is expected by the <mark style="background: #69E772;">receiver</mark>.

* Primarily it deals with matters such as: What voltage levels are used? What frequencies are used? How long does it take to transmit a bit (Bit Duration)? etc. 

* There are certain design issues to address such as: the <mark style="background: #69E772;">mechanical</mark> and <mark style="background: #69E772;">electrical</mark> design of the plugs and sockets, <mark style="background: #69E772;">timing interfaces</mark>, the physical <mark style="background: #69E772;">transmission medium</mark> etc
	
<mark style="background: #69E772;">The Data Link Layer (Layer 2):</mark>

* Concerned with the successful transmission of data across an individual link.
* Its purpose is to transforms a <mark style="background: #69E772;">raw</mark> transmission facility into a <mark style="background: #69E772;">data communications channel</mark> that <mark style="background: #69E772;">appears</mark> free of transmission errors.
* Primarily it deals with matters such as the transmission/reception of <mark style="background: #69E772;">data frames</mark>. 
* There are certain design issues to address such as: the creation of localised unique addressing, the creation of a unique framing structure, flow control, error control, controlling access to a <mark style="background: #69E772;">shared</mark> channel etc.

<mark style="background: #69E772;">The Network Layer (Layer 3):</mark>
	
* Concerned with the successful delivery of data between hosts across complex network infrastructures:
* Its purpose is to control the operation of the <mark style="background: #69E772;">sub-networks</mark> to achieve host-to-host delivery.
* Primarily it deals with matters such as the routing of <mark style="background: #69E772;">packets</mark> from the <mark style="background: #69E772;">source</mark> station towards the <mark style="background: #69E772;">destination</mark> station across sub-nets etc. 
* There are certain design issues to address such as: the creation a globally unique address space, the creation of a globally unique framing structure.
* Essentially this layer is responsible for managing data communications across interconnected <mark style="background: #69E772;">heterogeneous</mark> networks.

<mark style="background: #69E772;">The Transport Layer (Layer 4):</mark>
*  This is a key layer. 
* It is a true <mark style="background: #69E772;">end-to-end</mark> layer responsible for the reliable delivery of data between <mark style="background: #69E772;">processes</mark> on end-host machines i.e. process-to-process delivery:
* Its purpose is to provide a reliable data transport service to applications.
* Primarily it deals with interfacing with applications for the purpose of exchanging data between applications across a network.
* There are certain design issues to address such as: multiplexing data streams from/to remote applications, data loss, network latency etc.
	
### <mark style="background: #69E772;">Data Flows:</mark>

The layers work together to provide the complete functionality required to facilitate communications between two remotely connected host machines regardless of how they connect to the internet.

The following slide shows how data flows between the layers (up-and-down):

Note that sometimes it is necessary to break up the data to meet some size restrictions associated with some lower layer protocol software. Recall use of <mark style="background: #69E772;">Fragmentation</mark> at the Network layer.

### <mark style="background: #69E772;">Encapsulation and Information flow between the layers of an end-host:</mark>

![](https://i.imgur.com/eHEJhd6.png)

### <mark style="background: #69E772;">Data Flows:</mark>

* Some of the layers are also implemented on intermediary networking devices such as Routers:
* This is because the functionality associated with these layers is needed for a particular purpose such as: frame reception / transmission, packet routing etc.
* The following slide shows how the complete set of layers are implemented on the end-hosts as well as on the intermediary networking devices.
	
### <mark style="background: #69E772;">The ISO Reference Model - Layers 1-3 V Layers 4-7:</mark>
	
![](https://i.imgur.com/fyIKdRl.png)

### <mark style="background: #69E772;">Repeater Implementation:</mark>

![](https://i.imgur.com/JtDYsa8.png)

![](https://i.imgur.com/uFlXdDg.png)

# <mark style="background: #69E772;">20. IP Delivery</mark>

#DataComms 

### <mark style="background: #69E772;">Format of Internet Packets:</mark>

The IP software defines its own internet  packet format known as an <mark style="background: #69E772;">IP datagram</mark>.

It is a <mark style="background: #69E772;">universal</mark>, <mark style="background: #69E772;">virtual</mark> packet which has a  particular format/structure which is very different to that of a hardware frame.

It can carry a <mark style="background: #69E772;">single</mark> octet of data or multiple octets up to a maximum of <mark style="background: #69E772;">64K</mark> octets (including the header)

### <mark style="background: #69E772;">The IP Datagram Header Format:</mark>

![](https://i.imgur.com/V4kL3nN.png)


### <mark style="background: #69E772;">Forwarding an IP Datagram:</mark>

Recall that a router makes its routing decision based on 
the <mark style="background: #69E772;">destination IP address</mark>.

Routing information is stored in a <mark style="background: #69E772;">routing table</mark>.

This table must be <mark style="background: #69E772;">initialised</mark> on boot-up and updated if the  topology changes

The next three slides show example <mark style="background: #69E772;">Routing Tables</mark>:
- The first slide recalls a high-level <mark style="background: #69E772;">Routing Table</mark> from previous discussions,
- The second and third slides shows a <mark style="background: #69E772;">Routing Table</mark> from a real router

### <mark style="background: #69E772;">Example IP Routing Table:</mark>

![](https://i.imgur.com/a6wotZM.png)

![](https://i.imgur.com/eL67zJQ.png)

Note the network numbers and the connections to the 
routers.
The Routing Table router 1 (R1) is shown on the next slide

![](https://i.imgur.com/UBN7g5L.png)

### <mark style="background: #69E772;">IP Encapsulation:</mark>

The <mark style="background: #69E772;">physical network</mark> does not understand  the datagram format.

Instead the datagram is placed in the <mark style="background: #69E772;">data 
area</mark> of a <mark style="background: #69E772;">hardware frame</mark>.

This is known as <mark style="background: #69E772;">encapsulation</mark>

![](https://i.imgur.com/nlQNrlY.png)

This process is applied on each leg of the transmission path.

The <mark style="background: #69E772;">datagram</mark> is stored in memory without the additional <mark style="background: #69E772;">frame header</mark> information.

The size of the <mark style="background: #69E772;">frame header</mark> may vary as it traverses different network technologies.

### <mark style="background: #69E772;">Encapsulation at work:</mark>

![](https://i.imgur.com/dONu4zB.png)

# <mark style="background: #69E772;">21. IP Address Resolution:</mark>

#DataComms 
### <mark style="background: #69E772;">Binding Protocol Addresses</mark>

IP protocol software works with IP addresses when 
forwarding <mark style="background: #69E772;">packets</mark>:

The outcome of the routing process is the IP address of the <mark style="background: #69E772;">Next Hop</mark>.

The <mark style="background: #69E772;">Next Hop</mark> can be another router or, it can be the 
destination host residing on a <mark style="background: #69E772;">directly connected</mark> LAN.

Refer to examples given in class. 

Recall that IP addresses cannot be used when forwarding <mark style="background: #69E772;">frames</mark> across a <mark style="background: #69E772;">physical network</mark>: Only MAC addresses are relevant for this task.

Therefore the <mark style="background: #69E772;">Next Hop</mark> IP address must be translated to 
an equivalent <mark style="background: #69E772;">hardware/MAC</mark> address before the frame 
can be transmitted: This translation is known as <mark style="background: #69E772;">Address Resolution</mark>.

Once translated, the IP address is said to be resolved.

Address resolution is <mark style="background: #69E772;">local</mark> to a network.

Any host connected to a LAN can only resolve the IP 
addresses of other stations/routers connected to the 
same LAN:

Hosts A, B and router R1 can resolve each others IP 
addresses but, neither hosts A nor B can resolve Hosts C, 
D, E, F or router R2s’ IP addresses.

![](https://i.imgur.com/O8122e5.png)

### <mark style="background: #69E772;">Address Resolution Techniques:</mark>

The algorithm used to translate a protocol address into a hardware address depends upon the protocol and hardware addressing schemes in use.

However, there are three categories of address resolution algorithms as follows:
- Table lookup
- Closed-form computation
- Message exchange

### <mark style="background: #69E772;">Address Resolution with Table Lookup:</mark>

Here an array is used to store information about 
address bindings.

The main advantages of the table lookup approach 
are:
- It can be used to store arbitrary address bindings. 
- A protocol address can be mapped to an arbitrary hardware address .
- It is straightforward and easy to program.

![](https://i.imgur.com/yNdXZUR.png)

### <mark style="background: #69E772;">Address Resolution with Closed-Form Computation:</mark>

For <mark style="background: #69E772;">configurable MAC addressing</mark> it is possible to choose addresses that make <mark style="background: #69E772;">closed-form address resolution</mark> possible.

A <mark style="background: #69E772;">resolver</mark> computes the MAC address from the IP address using a mathematical function.

If the relationship is simplistic, the computation requires only a few arithmetic operations (e.g. a single Boolean
AND operation):

``hardware_address = ip_address AND Oxff``

Closed-form computation can be very efficient because both the <mark style="background: #69E772;">hardware</mark> and <mark style="background: #69E772;">IP addresses</mark> can be changed
