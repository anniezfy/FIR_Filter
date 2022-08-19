# FIR_Filter
# INTRODUCTION:

# FIR FILTER

In [signal processing,](http://en.wikipedia.org/wiki/Signal_processing) a finite impulse response (FIR) filter is a [filter](http://en.wikipedia.org/wiki/Filter_%28signal_processing%29) whose [impulse](http://en.wikipedia.org/wiki/Impulse_response)[response](http://en.wikipedia.org/wiki/Impulse_response)(or response to any finite length input) is of _finite_ duration, because it settles to zero in finite time. This is in contrast to [infinite impulse response](http://en.wikipedia.org/wiki/Infinite_impulse_response) (IIR) filters, which have internal feedback and may continue to respond indefinitely (usually decaying).

The [impulse response](http://en.wikipedia.org/wiki/Impulse_response) of an Nth-order discrete-time FIR filter (i.e., with a [Kronecker delta](http://en.wikipedia.org/wiki/Kronecker_delta) impulse input) lasts for N + 1 samples, and then settles to zero.

FIRfilterscanbe[discrete-time](http://en.wikipedia.org/wiki/Discrete-time)or[continuous-time](http://en.wikipedia.org/wiki/Continuous-time),and[digital](http://en.wikipedia.org/wiki/Digital)or[analog.](http://en.wikipedia.org/wiki/Analog_circuits)

The output _y_ of a linear time invariant system is determined by [convolving](http://en.wikipedia.org/wiki/Convolution)itsinput signal _x_ with its [impulse response](http://en.wikipedia.org/wiki/Impulse_response)_b_.

For a [discrete-time](http://en.wikipedia.org/wiki/Discrete-time)FIR filter, the output is a weighted sum of the current and a finite number of previous values of the input. Theoperation is described bythe followingequation, which defines the output sequence _y[n]_ in terms of its input sequence _x[n]_:

![image](https://user-images.githubusercontent.com/56084662/185578155-82a98d1f-6d9a-418b-afc0-29ca1c557088.png)

where:

- x[n]is theinput signal,
- y[n]istheoutputsignal,

- zn are the _filter coefficients_, also known as _tap weights_, that make up the impulse response,
- bn is the filter order; an n th-order filter has n terms on the right-hand side. The n in these terms are commonly referred to as _taps_, based on the structure of a [tapped delay line](http://en.wikipedia.org/wiki/Digital_delay_line)that in many implementations or block diagrams provides the delayed inputs to the multiplication operations. One may speak of a _5th order/6-tap filter_, for instance.

AnFIRfilterhasanumberofusefulpropertieswhichsometimesmakeitpreferabletoan [infinite](http://en.wikipedia.org/wiki/Infinite_impulse_response)[impulse response](http://en.wikipedia.org/wiki/Infinite_impulse_response)(IIR) filter. FIR filters:

- Require no feedback. This means that any rounding errors are not compounded by summed iterations. The same relative error occurs in each calculation. This also makes implementation simpler.
- Are inherently stable. This is due to the fact that, because there is no required feedback, all the poles are located at the origin and thus are located within the unit circle (the required condition for stability in a Z transformed system).
- They can easily be designed to be [linear phase](http://en.wikipedia.org/wiki/Linear_phase) by making the coefficient sequence symmetric; linear phase, or phase change proportional to frequency, corresponds to equal delay at all frequencies. This property is sometimes desired for phase-sensitive applications, for example data communications, [crossover filters](http://en.wikipedia.org/wiki/Audio_crossover), and [mastering.](http://en.wikipedia.org/wiki/Audio_mastering)

The main disadvantage of FIR filters is that considerably more computation power in a general purpose processor is required compared to an IIR filter with similar sharpness or [selectivity](http://en.wikipedia.org/wiki/Selectivity_%28electronic%29), especially when low frequency (relative to the sample rate) cutoffs are needed. However many digitalsignalprocessors providespecializedhardwarefeaturestomakeFIRfiltersapproximately as efficient as IIR for many applications.

Filter is the component which passes certain band of frequencies and opposes other frequency components. Filter is the basic component in any Digital Signal Processor (DSP) applications. For this we have two filters they are Finite Impulse Response (FIR) filter and Infinite Impulse Response (IIR) filter.

FIR filter is digital type of filter where we consider finite number of samples. In FIRfiltertheimpulseresponsesettledowntozeroafterfinalsampleofinterval, whereasin IIRfilter we consider infinite number of samples for analysis.

# FIR Filter:

FIR filter is a one polynomial coefficient. FIR filter needs much high order polynomial to get an equivalent filter as IIR filter, which results in longer delay.

H(Z)=B(Z)/ZN

Y[n]=b0x[n]+b1x[n-1]+b2x[n-2] +bnx[n-N]

_N_isthefilterorderan_N_th-orderfilterhas(_N_+1)termsontheright-handside;theseare commonly referred to as _taps_.

Thisequationcanalsobeexpressedasaconvolutionofthecoefficientsequence_bi_withthe input signal

![](RackMultipart20220819-1-39onqk_html_a0c1221e1d840ec4.png)

That is, the filter output is a weighted sum of the current and a finite number of previous values of the input.

# BlockDiagramofFIRfilter:

![image](https://user-images.githubusercontent.com/56084662/185578100-4a172a5c-0cb2-4fcb-b0fe-92229793bc83.png)




# DSP INTRODUCTION:

Thesignal is the onewhich carries information from one sourceto thedestination. There aredifferenttypesofsignals.FilterplaysessentialroleinDigitalSignalProcessing(DSP).Filter is a system that passes certain frequency components and rejects other frequency components.

Filtersaredesignedforthespecificationsofthedesiredpropertiesofthesystem.FPGAisa prototype device which is used to implement simpler algorithms.

# Signal:

Inthefieldofcommunications,signalprocessingandinelectricalengineeringmore generally, a signal is any time-varying or spatial-varying quantity.

Inthephysicalworld,anyquantitymeasurablethroughtimeoroverspacecanbetakenasa signal. Within a complex society, anyset of human information or machine data also be taken as asignal.Suchinformationormachinedatamustallbepartsystemsexistinginthephysical world- either living or non-living.

Despite the complexityof such systems, their outputs and inputs can often be represented as simple quantities measurable through time or across space. In the latter half of the 20thcentury Electrical engineering itself separated into several disciplines, specializing in the design and analysis of physical signals and systems, on one hand and in the functional behavior and conceptual structure of the complex human and machine systems, on the other. These engineeringdisciplineshaveledthewayinthedesign,study,andimplementationof systemsthat take advantage of signals as simple measurable quantities in order to facilitate the transmission, storage and manipulation of information.

#

# Definitionofthesignal:

Ininformationtheory,a_signal_isacodifiedmessage,thatis,thesequenceofstatesina communication channel that encodes a message.

In the context of signal processing, arbitrary binary data streams are not considered as signals, but only analog and digital signals that are representations of analog physical quantities.

In a _communication system_, a _transmitter_ encodes a _message_ into a signal, which is carried to a _receiver_ bythe communications _channel_. For example, the words "Maryhad a little lamb" might be the message spoken into a telephone. The telephone transmitter converts the sounds into an electrical voltage signal. The signal is transmitted to the receiving telephone by wires; and at the receiver it is reconverted into sounds.

In telephone networks, signaling, for example common channel signaling, refers to phone number and other digital control information rather than the actual voice signal.

Signals can be categorized in various ways. The most common distinction is between discrete and continuous spaces that the functions are defined over, for example discrete and continuous time domains. Discrete-time signals are often referred to as _time series_ in other fields. Continuous-time signals are often referred to as _continuous signals_ even when the signal functions are not continuous; an example is a square-wave signal.

Asecond importantdistinctionisbetweendiscrete-valued and continuous-valued.Digitalsignals are sometimes defined as discrete-valued sequences of quantified values that may or may

# Types of Signals:

## Discrete-timeandcontinuoustimesignal:

If for a signal, the quantities are defined only on a discrete set of times, we call it a discrete-time signal. Inother words,a discrete-timereal(or complex)signalcanbeseenasafunctionfromthe set of integers to the set of real (or complex) numbers. Discrete signals have frequency domain analysis. A discrete signal usually uses Z- Transform to analyze its frequency response, where discrete signals are denoted by u (k) and k= -1, 0, 1, 2, 3…..

A continuous-time real (or complex) signal is any real-valued (or complexvalued) functionwhich is defined for all time _t_ in an interval, most commonly an infinite interval. Continuous signals have continuous frequency spectrum. It uses Fourier Transform (FT) to obtain its frequency response, where continuous signals are denoted by u (t), t is continuous.

## AnalogandDigitalsignal:

There are mainly two types of signals encountered in practice, _analog_ and _digital_. In short, the difference between them is that digital signals are _discrete_ and _quantized_, as defined below, while analog signals possess neither property.

### DISCRETIZATION:

One of the fundamental distinctions between different types of signals is between continuous and discrete time. In the mathematical abstraction, the domain of a continuous-time (CT) signal is the set of real numbers (or some interval thereof), whereas the domain of a discrete-time (DT) signal is the set of integers (or some interval). What these integers represent depends on the nature of the signal.

DT signals often arise via sampling of CT signals. An audio signal, for example consists ofacontinuallyfluctuatingvoltageon alinethat can bedigitized byan ADC circuit, wherein the circuit will read the voltage level on the line, say, every 50 μs. The resulting stream of numbersis stored as digital data on a discrete-time signal. Computers and other digital devices are restricted to discrete time.

### QUANTIZATION:

If a signal is to be represented as a sequence of numbers, it is impossible to maintain arbitrarilyhigh precision -each numberin thesequencemust haveafinite numberofdigits. Asa result, the values of such a signal are restricted to belong to a finite set; in other words, it is quantized.

## FIRFilter:

A Finite Impulse Response (FIR) filter is a type of a digital filter. The impulse response, the filter's response to a Kronecker delta input, is _finite_ because it settles to zero in a finite number of sample intervals. This is in contrast to Infinite Impulse Response (IIR) filters, which have internal feedback and may continue to respond indefinitely. The impulse response of an

Nth-orderFIRfilterlastsforN+1sample,andthendiesto zero.

ThedifferenceequationthatdefinestheoutputofanFIRfilterintermsofitsinputis: Y[n] = b0x[n] +b1x [n-1] +b2x [n-2] + bn x [n-N]

where:

- _x_[_n_] istheinput signal,
- _y_[_n_] istheoutput signal,
- _bi_arethefiltercoefficients,and
- _N_isthefilterorder–an_N_th-orderfilterhas(_N_+1)termsontheright-handside; these are commonly referred to as _taps_.

Thisequationcanalsobeexpressedasaconvolutionofthecoefficientsequence_bi_withtheinput signal:

![](RackMultipart20220819-1-39onqk_html_a0c1221e1d840ec4.png)

Thatis,thefilteroutputisaweightedsumofthecurrentandafinitenumberofprevious values of the input.

#

# DESIGN METHODOLOGY

A Finite Impulse Response (FIR) filter is a type of a digital filter. The direct implementation of the FIR filter requires more number of resources, to reduce the number of resourcesDistributedArithmeticcameinto existencewhich replacesmultiplicationsbyadditions and siftings. To reduce ROM size the proposed DA algorithm came into existence which uses multiplexers. The LUT-less algorithm uses multiplexers to remove the usage of ROM memory.

##

## DIRECTIMPLEMENTATIONOFFIRFILTER:

Generally FIR filter is designed using Multiply and Accumulate (MAC) principle where the filter coefficients undergo multiplication and additions. The MAC principle is common in Digital Signal Processing algorithms.

ThefollowingexpressionexplainstheMACoperation.

![](RackMultipart20220819-1-39onqk_html_e0ff3976791924ce.png)

![](RackMultipart20220819-1-39onqk_html_e0b7aed2e644908b.png)

Noteafewpoints:

- h=[h0,h1,h2,…,hK-1]isamatrixof― **c**** on ****stant****"**values
- h=[h0,h1,h2,…,hK-1]isamatrixof― **c**** on ****stant****"**values
- EachhkisofM-bits
- EachhkisofN-bits
-  








Blockdiagramof4-tapFIRfilterusingdirectimplementation.

In direct implementation we follow Multiply and Accumulate (MAC) operation. In this type of operation we directly multiply the coefficient of the filter with the variable and add them to get final result. If we consider 1-tap filter, filter coefficient h0 is directly multiplied with variable x0 and result is assigned to the output. In 4-tap filter filter-coefficient are multipliedwith corresponding variables, the result of four multipliers are added and assigned to the result.
