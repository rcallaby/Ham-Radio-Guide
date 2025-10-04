# Antennas and Feedline

## Antenna Types

Antennas are critical components in amateur radio systems, converting electrical signals into radio waves and vice versa. The following describes common types relevant to ham radio licensing study: dipole, vertical, Yagi, and ground plane. These are often used on HF, VHF, and UHF bands.

| Antenna Type | Description | Common Uses in Ham Radio | Key Characteristics |
|--------------|-------------|---------------------------|---------------------|
| Dipole | A balanced antenna consisting of two equal-length conductive elements (halves) extending from a center feed point, typically made of wire. It is fed at the center, where the feedline connects. Multi-band versions allow operation on multiple frequencies by adjusting lengths or using traps. | HF bands for long-distance communication; simple to build for beginners. Often used as a reference antenna due to its predictable performance. | Resonant at half-wavelength; horizontal or inverted-V configurations; impedance around 72 ohms in free space; low cost and easy to deploy. |
| Vertical | A monopole antenna, typically a quarter-wavelength long, mounted perpendicular to the ground. It relies on a ground plane or radials for efficient operation. Vertical antennas are omnidirectional in the horizontal plane. They can be base-fed or center-fed, and multi-band versions use loading coils or traps. | Ground-wave communications on HF; VHF/UHF for mobile or base stations. Effective for local coverage where low-angle radiation is needed. | Omnidirectional azimuth pattern; requires good ground system to minimize losses; polarization is vertical; common for AM broadcast equivalents in ham setups. |
| Yagi | A directional antenna (also called Yagi-Uda) with a driven element, reflector(s), and director(s) arranged in parallel on a boom. It focuses energy in one direction for increased gain. Elements are typically metal rods; designs can include 2-4 elements for portable use, like on 6 meters. | VHF/UHF for point-to-point links, satellite work, or weak-signal modes like moonbounce. HF versions for DXing. | High directivity with front-to-back ratio; gain increases with more elements; beamwidth narrows; requires rotation for aiming; patterns vary with height above ground. |
| Ground Plane | A quarter-wavelength vertical monopole with radial elements (usually 3-4) forming an artificial ground plane at the base. Radials are typically sloped or horizontal. It simulates a full dipole by using the radials to reflect signals. Common with 4 radials for balanced performance. | VHF/UHF base stations; 2-meter repeaters or simplex. Portable setups due to simplicity. | Omnidirectional; low-angle radiation; impedance around 35-50 ohms; easy to build; performance improves with more radials (e.g., 120 for optimal HF verticals). |

These types are modeled using software that assumes straight-wire elements, common in amateur designs. Compliance with RF exposure guidelines often involves evaluating patterns for dipoles, ground planes, and Yagis.

#### Polarization

Polarization refers to the orientation of the electric field vector in a radio wave. It affects signal strength due to mismatch losses between transmitting and receiving antennas.

- **Horizontal Polarization**: The electric field is parallel to the ground. Common for HF dipoles or Yagis mounted horizontally. Provides better performance for skywave propagation but can suffer from ground reflections. Loop antennas like the hourglass design offer horizontal polarization with gain.
- **Vertical Polarization**: The electric field is perpendicular to the ground. Ideal for ground-wave and line-of-sight VHF communications, such as to repeaters. Vertical antennas or ground planes use this to minimize path loss. Broadcast stations prefer vertical for omnidirectional coverage.
- **Circular Polarization**: The electric field rotates as the wave propagates (right-hand or left-hand). Used in satellite communications to reduce fading from rotation. Turnstile antennas or crossed Yagis achieve this; switching polarization improves signal capture. WWV's 25 MHz signal uses circular polarization.

Mismatch between polarizations can cause up to 20 dB loss; cross-polarization (e.g., horizontal to vertical) results in significant fading. For ARISS (Amateur Radio on the International Space Station), circular polarization minimizes dropouts.

#### Gain vs. Directivity

Antenna gain and directivity are related but distinct metrics describing how an antenna focuses energy.

- **Directivity**: Measures how much an antenna concentrates radiation in a preferred direction compared to an isotropic radiator (uniform in all directions). It is a ratio, often in dB, ignoring losses. Higher directivity correlates with narrower beamwidth and more focused power. Directivity is the ideal focusing capability without real-world inefficiencies.
- **Gain**: Combines directivity with antenna efficiency (accounting for losses like resistance or mismatch). Gain = Directivity × Efficiency. Expressed in dBi (relative to isotropic) or dBd (relative to dipole). For efficient ham antennas, gain ≈ directivity. A 7 dB gain antenna with 10 W input yields about 50 W effective radiated power (ERP).

In ham radio, gain describes the ratio of input power to output radiation in a direction, while directivity is spherical. Most amateur antennas are efficient, making the terms nearly interchangeable, except for lossy designs.

#### Radiation Patterns

Radiation patterns depict how an antenna distributes energy in space, shown as plots of field strength vs. angle. They include elevation (vertical plane) and azimuth (horizontal plane) views.

- Patterns vary by antenna type: Dipoles have figure-8 azimuth patterns; verticals/ground planes are omnidirectional. Yagis show lobes with front-to-back ratios.
- Height affects patterns: For dipoles or Yagis, elevation patterns change with electrical height above ground (e.g., 1/4 or 1/2 wavelength). Higher heights (70+ feet) improve low-angle radiation for DX.
- Loops show mixed polarization; small loops have weaker broadside radiation. Directive antennas like Yagis have predictable patterns with fewer side lobes.
- RF safety considers patterns for exposure calculations. Antennas radiate due to accelerating charges creating fields.

Modeling software uses elevation angles (0° horizon to 90° zenith) for patterns.

#### Simple Antenna Tuning and Matching

Tuning adjusts an antenna to resonance (purely resistive impedance) at a desired frequency; matching ensures efficient power transfer from transmitter to antenna (typically 50 ohms).

- **Tuning Methods**: Shorten/lengthen elements for resonance. Use an analyzer to measure resistance and reactance separately. For dipoles, trim wire ends.
- **Matching Networks**: L-network (inductor and capacitor) for simple impedance transformation. Gamma match borrows reactance. Antenna tuners (transmatch) vary inductance/capacitance; manual versions note settings per band.
- Process: Measure at antenna for accuracy; tuners at shack compensate but increase losses. SWR indicates match quality.

#### Feedline Losses

Feedlines (transmission lines) carry signals between radio and antenna; losses reduce power due to resistance, dielectric absorption, and radiation.

- Common Types: Coaxial cable (coax) is most used; open-wire (ladder line) has lower loss but requires baluns.
- Loss Factors: Increases with frequency, length, and SWR mismatch (reflected power travels extra distance). 3 dB loss halves power; 6 dB quarters it.
- VHF/UHF Impact: Significant; calculate for ERP in RF exposure. High SWR exacerbates losses.
- Mitigation: Use low-loss coax (e.g., RG-213 vs. RG-58); minimize length; match impedance.

| Loss Example | Description |
|--------------|-------------|
| 3 dB in Feedline | 50% power lost to antenna. |
| High-End Coax (2 dB/100 ft at UHF) | Better than cheap coax; varies by type. |

#### SWR Measurement and Practical Tolerances

Standing Wave Ratio (SWR or VSWR) measures impedance match between transmitter, feedline, and antenna. It compares forward and reflected power; perfect match is 1:1.

- **Measurement Tools**:
  - **SWR Meter**: Basic device inserted in line; measures forward/reflected power during transmission. Set to forward, calibrate, then switch to reflected for ratio. Place near antenna for accuracy.
  - **Antenna Analyzer**: Advanced; sweeps frequencies without transmitting high power. Measures resistance, reactance, and SWR directly; better for tuning. NanoVNA shows graphs.
- **Practical Tolerances**: Aim for <2:1; 1.5:1 or lower ideal. >3:1 risks transmitter damage. Resonance ≠ perfect SWR; good SWR indicates match, not efficiency. "Perfect" 1:1 is mythical; tolerances vary by radio (most handle 2:1). Measure at feedpoint for best accuracy; shack readings differ due to line losses.

### Lab: Build and Test a 2-Meter Dipole or 1/4λ Ground Plane; Measure SWR with an Antenna Analyzer or SWR Meter

This hands-on lab reinforces concepts by building and testing a simple VHF antenna for the 2-meter band (144-148 MHz). Center frequency: 146 MHz. Wavelength λ = 300/f (MHz) ≈ 2 meters; 1/4λ ≈ 0.5 meters (19.5 inches). Use low power (5-10 W) for testing.

#### Option 1: Build and Test a 2-Meter Dipole
- **Materials**: 6-7 ft PVC pipe (1" diameter), two 38" aluminum tape strips (or wire), SO-239 connector, RG-58 coax, solder/iron, tape measure, wire cutters.
- **Steps**:
  1. Cut two elements: Each 19-20" (1/4λ, trim for tuning). For vertical mount, connect one to coax center, other to shield.
  2. Attach to PVC: Align elements straight on pipe; solder to connector at center. Use RG-58 for feedline.
  3. Mount vertically for omnidirectional use; horizontal for directional.
- **Testing**: Connect to HT or transceiver. Use SWR meter/analyzer at feedpoint. Transmit low power; adjust length for lowest SWR at 146 MHz (aim <1.5:1). Fan dipole variant for dual-band (2m/70cm).

#### Option 2: Build and Test a 1/4λ Ground Plane
- **Materials**: SO-239 connector, 19.5" wire/rod for vertical element, four 20" radials (coat hangers/wire), solder/iron, pliers.
- **Steps**:
  1. Solder vertical element to SO-239 center pin.
  2. Attach radials to mounting holes/flange; bend at 45° downward for 50-ohm match (no coil needed).
  3. Mount elevated (e.g., mast); connect coax.
- **Testing**: Use analyzer for sweep or SWR meter during TX. Trim elements/radials for resonance; expect omnidirectional pattern. High elevation improves performance over 5/8λ designs.

**Safety Notes**: Ground shack for safety; avoid high power until tuned. Test in open area; record SWR vs. frequency.