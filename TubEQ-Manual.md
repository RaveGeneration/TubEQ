# TubEQ User Manual

[![Rave Generation](https://img.shields.io/badge/Rave%20Generation-Audio%20Software-purple)](https://ravegeneration.io)
[![Version](https://img.shields.io/badge/Version-1.0.9-blue)]()
[![Platform](https://img.shields.io/badge/Platform-VST3%20%7C%20AU-green)]()

## Table of Contents

1. [Introduction](#1-introduction)
2. [Key Features](#2-key-features)
3. [Quick Start](#3-quick-start)
4. [User Interface](#4-user-interface)
   - [4.1 Low Frequency Section (Pultec EQP-1A)](#41-low-frequency-section-pultec-eqp-1a)
   - [4.2 Mid/High Frequency Section (Maag EQ4M)](#42-midhigh-frequency-section-maag-eq4m)
   - [4.3 Tube Section (12AX7)](#43-tube-section-12ax7)
   - [4.4 Output Section](#44-output-section)
   - [4.5 Additional Controls](#45-additional-controls)
5. [Signal Flow & Processing](#5-signal-flow--processing)
6. [The Legendary Hardware](#6-the-legendary-hardware)
7. [Tips & Tricks](#7-tips--tricks)
8. [Installation & Troubleshooting](#8-installation--troubleshooting)

---

## 1. Introduction

**TubEQ** is an authentic analog equalizer plugin that combines the musical character of two legendary EQs in a single, powerful processor. This unique hybrid design features:

- The warm, surgical low-end of the iconic **Pultec EQP-1A** (modeled using Wave Digital Filters)
- The modern clarity and presence of the **Maag EQ4M** mid/high frequency bands (using State Variable Filters)
- The harmonic richness of the **12AX7 tube** from the original Pultec amplifier stage
- Precision brickwall lowpass filter at 24.5kHz

From the studio-defining low-end warmth heard on countless classic recordings to the crystal-clear "Air" that makes modern productions sparkle, TubEQ delivers the authentic analog sound and character that shaped music history.

## 2. Key Features

- **Authentic Pultec EQP-1A low-end modeling** - Wave Digital Filter implementation of the legendary passive tube EQ circuit
- **Maag EQ4M-inspired mid/high bands** - Musical frequency points (160Hz, 650Hz, 2.5kHz) plus sweepable Air Band
- **12AX7 tube character modeling** - Authentic modeling from the original Pultec EQP-1A amplifier stage
- **The legendary "Pultec Trick"** - Simultaneous boost and cut at low frequencies
- **Interactive EQ bands** - Analog-style frequency interaction and natural phase relationships
- **Progressive gain compensation** - Intelligent level management
- **Brickwall filter** - Precision 24.5kHz lowpass prevents aliasing
- **Auto makeup gain** - Intelligent automatic level compensation

## 3. Quick Start

1. Insert TubEQ on your desired track or mix bus
2. Enable the effect using the **"Effect In"** switch
3. **Start with the Low frequency section:**
   - Select frequency band (30Hz/60Hz/100Hz)
   - Try the "Pultec Trick" for enhanced weight
4. **Shape the midrange and highs:**
   - Use 160Hz for body control
   - Use 650Hz for vocal presence and punch
   - Use 2.5kHz for definition and bite
   - Add Air Band for open, sparkling highs
5. Add tube character with **Tube Input** and **Tube Level** controls
6. Set **Output** level to match bypassed signal or creative preference

## 4. User Interface

### 4.1 Low Frequency Section (Pultec EQP-1A)

The low frequency section faithfully recreates the legendary Pultec EQP-1A using Wave Digital Filter modeling.

| **Control** | **Range** | **Description** |
|-------------|-----------|-----------------|
| **LF Boost** | `0-10` | Low frequency boost amount with authentic Pultec curve scaling |
| **LF Atten** | `0-10` | Low frequency attenuation - enables the famous "Pultec Trick" |
| **LF Band** | `30Hz/60Hz/100Hz` | Frequency selection switch for both boost and attenuation |

#### The Famous "Pultec Trick"
> The original Pultec EQP-1A allows simultaneous boost and attenuation because the circuits operate at slightly different frequencies. This creates a unique sound where you can add low-end weight while removing muddiness.

**Frequency characteristics:**
- **30Hz** - Deep sub-bass, adds fundamental weight to kick drums and bass
- **60Hz** - Classic low-end warmth, excellent for adding body to thin sources
- **100Hz** - Upper bass region, great for adding warmth without excessive sub content

### 4.2 Mid/High Frequency Section (Maag EQ4M)

The mid and high frequency bands are inspired by the legendary Maag EQ4M, featuring musical frequency points with smooth, continuous gain control.

| **Control** | **Range** | **Description** |
|-------------|-----------|-----------------|
| **160 Hz** | `±5` | Low-mid frequency band for warmth and body control |
| **650 Hz** | `±5` | Mid frequency band for vocal presence and clarity |
| **2.5 kHz** | `±5` | Presence band for definition and attack |
| **Air Gain** | `0-10` | Boost amount for the Air Band with progressive curve |
| **Air Band** | `off/2.5kHz/5kHz/10kHz/15kHz/20kHz/40kHz` | Selects the Air Band frequency |

**Frequency characteristics:**
- **160Hz** - Low-mid control for warmth, body, and muddiness reduction
- **650Hz** - Critical for vocal intelligibility and mix presence
- **2.5kHz** - Upper-mid presence for clarity and definition
- **Air Band** - Legendary high-frequency enhancement that defines modern production

### 4.3 Tube Section (12AX7)

The tube section models the 12AX7 (ECC83) tube from the original Pultec EQP-1A amplifier stage.

| **Control** | **Range** | **Description** |
|-------------|-----------|-----------------|
| **Tube In** | `0-1` | Input drive level into the tube stage |
| **Tube Level** | `0-1` | Amount of tube character processing applied |

**Tube modeling characteristics:**
- **Harmonic coloration** - Subtle even and odd harmonics that contribute to the "Pultec sound"
- **Tonal character** - Natural tube response that adds warmth and musicality
- **Headroom behavior** - Authentic response when approaching the +21 dBm maximum output
- **Tube warmth** - The characteristic smoothness and musical quality of the 12AX7

### 4.4 Output Section

| **Control** | **Range** | **Description** |
|-------------|-----------|-----------------|
| **Output** | `±12dB` | Final output level control with progressive gain compensation |
| **Auto Gain** | `off/on` | Automatic level compensation based on EQ settings |
| **Effect In** | `off/on` | Master bypass switch |

### 4.5 Additional Controls

#### Keyboard Shortcuts
- **Shift + Drag** - Precise knob movements
- **Right Click** - Reset knob to default
- **Alt/Option + Click** - Reset knob (alternative)
- **Double Click** - Direct value entry

#### Menu Bar Options
- **Undo/Redo** - Easily correct or reapply changes
- **GUI Opacity** - Adjust transparency (0-100%)
- **Resize** - Scale interface (70-200%)
- **Preset Menu** - Browse, load, save, and manage presets

## 5. Signal Flow & Processing

### Complete Signal Path
```
Input → Pultec Low EQ (WDF) → Maag Mid/High EQ (SVF) → 12AX7 Tube Character
      → Brickwall Lowpass Filter (24.5kHz) → Output Level → Output
```

### Detailed Processing Chain

#### Pultec Low Frequency Processing (Wave Digital Filter)
- Authentic inductor-capacitor network modeling
- Passive EQ behavior with tube makeup gain
- Supports simultaneous boost/cut ("Pultec Trick")
- Frequency-dependent impedance interactions

#### Maag Mid/High Frequency Processing (State Variable Filter)
- **160Hz** - Bandpass processing for warmth and body control
- **650Hz** - Bandpass processing for vocal presence and clarity
- **2.5kHz** - High shelf processing for presence control
- **Air Band** - Selectable high-frequency enhancement

#### 12AX7 Tube Character (from Pultec EQP-1A)
- Models the amplifier stage tube from the original Pultec hardware
- Subtle harmonic coloration and tonal enhancement
- Natural tube warmth and musical character
- Authentic headroom behavior matching +21 dBm specifications

#### Brickwall Lowpass Filter
- 12dB/octave rolloff at 24.5kHz
- Prevents aliasing while preserving musical content
- Maintains phase coherence in the audio band

## 6. The Legendary Hardware

### Pultec EQP-1A (1951-present)
The Pultec Program Equalizer, designed by Eugene Shenk and Ollie Summerland, revolutionized audio processing with its passive inductor-capacitor networks and tube makeup gain. The famous "Pultec Trick" became a studio standard technique heard on countless classic recordings.

### Maag EQ4M (1999-present)
Designed by Cliff Maag Jr., the EQ4M introduced the legendary "Air Band®" that set a new standard for high-frequency enhancement. Used by top engineers like Dave Pensado and Dylan Dresdow, the EQ4M's musical frequency points created the signature sound heard on hits by Madonna, Justin Timberlake, and countless others.

### 12AX7 Tube (ECC83) in the Pultec EQP-1A
The 12AX7 is part of the amplifier stage in the original Pultec EQP-1A, working alongside the 12AU7 (ECC82) and 6X4 rectifier. While not designed as a tube saturator, the 12AX7 contributes subtle harmonic coloration and tonal character that gives the Pultec its distinctive musical warmth.

## 7. Tips & Tricks

### The Pultec Trick
```
1. Start with LF Boost at 3-5 for weight
2. Add LF Atten at 2-4 to remove muddiness
3. Result: Enhanced low-end with improved clarity
```
> Perfect for kick drums, bass, and full mixes

### Frequency Selection Guide

| **Frequency** | **Best For** |
|---------------|--------------|
| **30Hz** | Deep content - kick drums, bass, full mixes |
| **60Hz** | Most versatile - works on most sources |
| **100Hz** | Upper bass warmth without excessive sub content |

### Vocal Processing
- **160Hz** - Cut to reduce muddiness, boost for warmth
- **650Hz** - Boost for intelligibility and presence
- **2.5kHz** - Boost for definition, cut to reduce harshness
- **Air Band** - Try 10kHz or 20kHz for open, detailed sound

### Air Band Selection
| **Frequency** | **Character** |
|---------------|---------------|
| **2.5kHz** | Aggressive presence for cutting through mixes |
| **5kHz** | Balanced enhancement, versatile for most sources |
| **10kHz** | Classic character, smooth and musical |
| **15kHz** | Balanced between 10kHz and 20kHz |
| **20kHz** | Very smooth, adds "air" without harshness |
| **40kHz** | Ultra-smooth, subtle enhancement |

### Tube Character Settings
| **Style** | **Tube In** | **Tube Level** |
|-----------|-------------|----------------|
| **Subtle** | `0.3-0.5` | `0.2-0.4` |
| **Classic** | `0.5-0.7` | `0.4-0.6` |
| **Enhanced** | `0.7-1.0` | `0.6-1.0` |

### Auto Gain Usage
- **Enable** for consistent levels while dialing in EQ settings
- **Disable** for creative level changes or parallel processing

### Genre Applications

| **Genre** | **Recommended Settings** |
|-----------|--------------------------|
| **Electronic** | Pultec for drums/bass, Air Band 10-20kHz, moderate tube |
| **Rock/Pop** | Pultec trick on rhythm section, 650Hz for vocals, 20kHz Air |
| **Hip-Hop/R&B** | Strong low-end, 650Hz for vocal clarity |
| **Jazz/Acoustic** | Gentle enhancement, higher Air Band frequencies (20-40kHz) |

## 8. Installation & Troubleshooting

### System Requirements

| **Component** | **Minimum** | **Recommended** |
|---------------|-------------|-----------------|
| **OS** | macOS 10.13+ / Windows 10+ | Latest OS version |
| **Processor** | Intel Core i5 or equivalent | Intel Core i7 or better |
| **RAM** | 4 GB | 8 GB or more |
| **Formats** | VST3, AU (macOS) | - |

### Installation Process
1. Run the installer and follow on-screen instructions
2. Restart your DAW after installation
3. Locate "TubEQ" in your plugin list under "Rave Generation"

### Troubleshooting

| **Issue** | **Solution** |
|-----------|--------------|
| **Plugin not appearing** | Ensure plugin path is correct in your DAW settings |
| **Activation issues** | Check internet connection and license key accuracy |
| **Performance issues** | Increase buffer size or freeze other tracks |
| **No sound** | Check "Effect In" switch is enabled |

---

## Support & Resources

**TubEQ** by **Rave Generation** combines the legendary analog character of the Pultec EQP-1A and Maag EQ4M with authentic 12AX7 tube character. Experience the authentic analog sound that shaped music history, now with the convenience and precision of modern digital control.

📧 **Support**: support@ravegeneration.io  
🌐 **Website**: [ravegeneration.io](https://ravegeneration.io)  
📚 **More Resources**: Updates, preset packs, and tutorials available online

---

*© 2025 Rave Generation Audio Software. All rights reserved.*
