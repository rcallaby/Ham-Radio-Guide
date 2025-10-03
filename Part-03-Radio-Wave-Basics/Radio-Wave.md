# Radio Wave Basics & Propagation

This section dives into the fundamentals of how radio waves work and travel, which is crucial for understanding why your signals can reach across town or around the world. We'll break it down step by step in a student-friendly way, using simple explanations, analogies, and examples. Think of radio waves like ripples in a pond—they spread out from your antenna (the stone you throw) but can bounce, bend, or get blocked depending on the environment. I'll cover each topic in the outline comprehensively, drawing from reliable sources like the American Radio Relay League (ARRL) to ensure accuracy. By the end, you'll have the key concepts, formulas, and real-world applications you need to know for your license exam and practical operating.

### Radio Wave Properties

Radio waves are a type of electromagnetic radiation, just like visible light or X-rays, but with much longer wavelengths. They travel at the speed of light (about 300,000 kilometers per second or 186,000 miles per second in a vacuum) and carry energy from your transmitter to a receiver. Key properties include:

- **Amplitude**: This is the "height" or strength of the wave, which determines how much power it carries. Higher amplitude means a stronger signal, but it can fade due to distance or obstacles.
- **Frequency and Wavelength**: These are interconnected (more on them below). Frequency tells how fast the wave oscillates, while wavelength is the physical distance between wave peaks.
- **Polarization**: Waves can be vertically or horizontally polarized, depending on your antenna orientation. This affects how well signals are received—mismatched polarization can weaken them.
- **Behavior in Space**: Radio waves can:
  - **Reflect** off surfaces like buildings or the ground (like light bouncing off a mirror).
  - **Refract** (bend) when passing through different mediums, such as atmospheric layers.
  - **Diffract** around obstacles, allowing signals to "bend" slightly over hills.
  - **Absorb** energy from materials like trees or rain, causing signal loss.
  - **Interfere** with each other, creating stronger or weaker spots.

In ham radio, these properties explain why signals weaken over distance (path loss) or why certain frequencies work better in different conditions. For example, lower frequencies penetrate obstacles better but need larger antennas. Electromagnetic waves are characterized by their frequency, wavelength, and field strength, which influence how they propagate.

What you need to know: Radio waves are transverse waves (they oscillate perpendicular to their direction of travel). They're non-ionizing (safe at ham power levels) but follow inverse square law—signal strength drops with the square of distance. For your license, remember that all radio waves travel at the same speed, but their interaction with the environment varies by frequency.

#### Frequency

Frequency is the number of complete wave cycles per second, measured in Hertz (Hz). In ham radio, we deal with kilohertz (kHz = 1,000 Hz), megahertz (MHz = 1,000,000 Hz), and gigahertz (GHz = 1,000,000,000 Hz).

- **Ham Bands by Frequency**:
  - **HF (High Frequency)**: 3–30 MHz (e.g., 20m band at 14 MHz for worldwide contacts).
  - **VHF (Very High Frequency)**: 30–300 MHz (e.g., 2m band at 144–148 MHz for local repeaters).
  - **UHF (Ultra High Frequency)**: 300–3,000 MHz (e.g., 70cm band at 430–450 MHz for handheld radios).

Higher frequencies mean shorter wavelengths and more directional signals, but they're more easily blocked. Lower frequencies travel farther via skywave but require bigger antennas. The FCC assigns specific frequency bands to amateurs to avoid interference—stay within them!

Key formula: Frequency (f) relates to wavelength (λ) by the speed of light (c): c = f × λ (or f = c / λ). Use c ≈ 300,000,000 m/s for calculations. Example: For 14 MHz (20m band), f = 14,000,000 Hz, so λ = 300,000,000 / 14,000,000 ≈ 21.4 meters—hence the "20m" band name.

What you need to know: Frequency determines propagation mode (e.g., HF for long-distance, VHF for local). Exams often ask about band limits, like "What frequency is in the 6m band?" (50–54 MHz). Ionization affects higher frequencies less, allowing them to pass through the atmosphere more easily.

#### Wavelength

Wavelength (λ) is the distance between two identical points on a wave (e.g., peak to peak), measured in meters. It's inversely related to frequency: Higher frequency = shorter wavelength.

- **Why It Matters in Ham Radio**: Antenna size is based on wavelength. A basic dipole antenna is λ/2 long (half-wavelength). For example, on the 80m band (3.5 MHz), λ ≈ 85.7m, so a half-wave dipole is about 42.85m—big! On 2m (144 MHz), λ ≈ 2m, so half-wave is 1m—portable.
- **Calculation**: λ (in meters) = 300 / f (in MHz). This is a handy shortcut since c ≈ 300 million m/s. Example: For 7 MHz (40m band), λ = 300 / 7 ≈ 42.86m.

Bands are often named by wavelength (e.g., 10m band = 28–29.7 MHz). Shorter wavelengths (higher freq) are more line-of-sight, while longer ones bend better. (Note: The standard equation is c = f × λ, so λ = c / f.)

What you need to know: Understand conversions between frequency and wavelength for antenna design and propagation. Exams test this with questions like "What's the approximate wavelength for 52 MHz?" (300/52 ≈ 5.77m, so 6m band).

#### Line-of-Sight vs. Skywave

Propagation is how radio waves travel from transmitter to receiver. Two main modes for hams:

- **Line-of-Sight (LOS) Propagation**: Waves travel in a straight line, like shining a flashlight. Limited by Earth's curvature—the radio horizon is farther than visual due to slight bending (about 1.4 times optical horizon). Formula for horizon distance (d in miles): d ≈ √(2 × antenna height in feet). Example: Two 100ft antennas? Each has ~14 miles horizon, total ~28 miles (plus some over-horizon due to diffraction).
  - Best for VHF/UHF: Signals don't bend much, so need clear path. Obstructions like mountains block them.
  - Ground-wave extension: Low frequencies hug the ground a bit farther.

- **Skywave Propagation**: Waves bounce off the ionosphere (upper atmosphere) like skipping a stone on water, allowing global reach. Mainly for HF (3–30 MHz). The ionosphere refracts (bends) waves back to Earth, creating "skips" of 1,000+ miles per hop. Multiple hops = worldwide DX (distant contacts).
  - Depends on frequency, time of day, and solar activity. Higher frequencies may punch through without bending.
  - vs. LOS: Skywave has much greater range but is unpredictable; LOS is reliable but short-range.

What you need to know: LOS for local chats (e.g., 2m simplex); skywave for international QSOs (e.g., 20m). Factors like solar flares can enhance or disrupt skywave. NVIS (Near Vertical Incidence Skywave) is a special skywave for regional coverage (200–500 miles) using high-angle antennas.

#### Ionospheric Layers

The ionosphere (50–600 miles up) is ionized by solar UV radiation, creating charged layers that refract radio waves. Layers vary by height, density, and time:

- **D Layer (37–56 miles)**: Lowest, absorbs low-frequency HF signals during daytime (causes fade on 80m/160m). Disappears at night, allowing better propagation.
- **E Layer (56–93 miles)**: Reflects medium HF (up to 10 MHz daytime). Good for short skips (300–1,500 miles). Sporadic E (Es) clouds cause sudden VHF openings.
- **F Layer (93–310 miles)**: Splits into F1 (daytime, 93–124 miles) and F2 (highest, main for long-distance HF). F2 refracts up to 30 MHz, enabling global skips. Merges at night.

Critical concepts:
- **Maximum Usable Frequency (MUF)**: Highest frequency that reflects back (depends on ionization). Above MUF, waves escape to space.
- **Lowest Usable Frequency (LUF)**: Below this, too much absorption.
- Solar cycle (11 years) boosts ionization, improving HF skywave.

What you need to know: Daytime: D absorbs, E/F reflect higher freq. Night: D gone, F lower for longer skips. Exams cover how layers affect bands (e.g., 10m opens during high solar activity).

#### Simple VHF/UHF Propagation Considerations

VHF (30–300 MHz) and UHF (300–3,000 MHz) are mostly line-of-sight, but not strictly—signals can extend via:

- **Knife-Edge Diffraction**: Bends over sharp obstacles like mountain ridges.
- **Tropospheric Scatter**: Weak signals bounce off air particles for 100–300 miles.
- **Auroral Reflection**: Northern lights reflect VHF for polar paths.
- **Meteor Scatter**: Burning meteors ionize trails, bouncing signals briefly (use WSJT modes).
- **Earth-Moon-Earth (EME)**: Bounce off the moon for global VHF/UHF (needs big antennas).
- **Repeaters**: Extend range via hilltop stations.

Antenna height is key—higher = farther LOS. Urban areas cause multipath (echoes from buildings). Rain/snow scatters UHF more. VHF contests exploit rare openings.

What you need to know: VHF/UHF for FM voice, digital modes like APRS. Power and antenna gain compensate for losses. Unlike HF, no reliable skywave—focus on terrain.

#### Tropospheric Ducting Basics

The troposphere (0–10 miles up) can "duct" VHF/UHF signals far beyond LOS when temperature inversions occur (warm air over cold, often near coasts or mornings).

- **How It Works**: Waves get trapped in a "duct" like light in fiber optics, traveling 100–1,000+ miles with low loss. Caused by weather fronts, high pressure.
- **When/Where**: Common in summer, over water. Enhances 2m/70cm DX.
- **Detection**: Listen for distant repeaters or use beacons.

What you need to know: Not daily, but exciting for contests. Differs from ionospheric—tropospheric is weather-based, lower altitude.

#### Lab: Use Online Propagation Tools to Plan a Contact; Mapping Line-of-Sight for Local Sites

Hands-on time! These exercises build skills for real operating.

1. **Planning a Contact with Propagation Tools**:
   - **VOACAP (voacap.com/hf)**: Free HF tool. Input your location (lat/long), friend's location, time, band, power, antennas. It predicts reliability (e.g., 80% chance on 20m at 1800 UTC). Adjust for solar data (SSN). Great for skywave planning.
   - **Radio Mobile Online (radiomobileonline.pe1mew.nl)**: For VHF/UHF/HF. Upload terrain data, simulate coverage. Predicts signal strength for a path.
   - **HF Propagation Map (hf.dxview.org)**: Real-time band openings based on spots.
   - Steps: Choose a friend 1,000 miles away. Use VOACAP to find best HF band/time. Log predicted vs. actual contact.

2. **Mapping Line-of-Sight for Local Sites**:
   - **SCADACore RF Line-of-Sight (scadacore.com/tools/rf-path/rf-line-of-sight)**: Input two locations/heights. Plots profile showing if path is clear (green) or blocked (red). Accounts for Earth curvature.
   - **SPLAT! (qsl.net/kd2bd/splat.html)**: Advanced for paths/maps. Download, input coords, generates topographic views.
   - Steps: Pick local hill/repeater. Enter your home coords (use Google Maps for lat/long) and heights (e.g., 20ft antenna). Map if you can reach 50 miles. Test with a real simplex contact.

Tips: Use free tools first. Record results in a logbook. This preps you for exams (e.g., T3B questions on propagation) and fun DXing! If tools show poor propagation, try another band/time.