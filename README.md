# Beat-Sync-VFX
MTRX3700 Assignment 2: Beat-Sync VFX

## Git Setup Instructions

1. **Clone the repository to your local**

   * Use a path with no spaces.

2. **Create a new Quartus project**

   * Use the *New Project Wizard*.
   * Set the repository as the project path.
   * Pick a project name.
   * Select the DE2 board (Cyclone IV, EP4CE115F29C7).
   * Add pin assignments

3. **Add Verilog files**

   * In Quartus: `Project → Add/Remove Files in Project`.
   * Add all `.v` files.

4. **Commit and push code**

   * Use `git add .`, `git commit`, and `git push` in the terminal.
   * Only push *working* code.
   * The `.gitignore` ensures Quartus build files aren’t committed.

5. **Done**

   * Everyone’s local Quartus build will regenerate its own files.

---

Frequency selective beat detection
- - Must use an FFT and Spectral Flux
- - Must detect beat events distinctly for different frequencies 
- - Must use an adaptive threshold
- - Must general to unseen songs
- BPM displayed on 7-segment display
- - Must be calculated using autocorrelation
- SNR estimates on 7-segment display 
- - Must be A-weighted and measured in dB
- BRAM image display
- - Must be 12-bit colour (i.e. 3x4-bit RGB)
- 2 selectable pixel-wise filters
- 2 selectable convolution filters
- - Must use 5x5 kernals
- Use "beat" events to modify the filters in real time (changing intensities and kernals)
- - Each frequency of beat event should modify the band-selective mapping differently
- Use BPM to modify filters 


- Plan and model all DSP algorithms used with Python (e.g. Jupyter Notebook).
- Modular Verilog/SystemVerilog with testbenches for key units and evidence of timing analysis
- Resource-aware implementation (efficient BRAM use, pipelined 1-pixel/cycle
convolution, DSP block use).


## Project structure

## Format
top level
- modules
- - submodules

## Top Level

## Microphone module
Configures the microphone and starts outputting streaming sample data

### Submodules
- mic_load
- - Reads the WM8731 LJ Data Stream's left channel and generates the mic sample_data
- set_audio_encoder
- - configures the WM8731 audio codec chip through i2c_master
- i2c_master
- - Acts as a master device for writing to the WM8731 audio codec chip

## Beat Detections Module 
Frequency selective beat detection
- - Must use an FFT and Spectral Flux
- - Must detect beat events distinctly for different frequencies 
- - Must use an adaptive threshold
- - Must general to unseen songs

## Tempo Calculator Module
- BPM displayed on 7-segment display
- - Must be calculated using autocorrelation

## SNR Calculator Module
- SNR estimates on 7-segment display 
- - Must be A-weighted and measured in dB

## Display (work in progress...)
- BRAM image display
- - Must be 12-bit colour (i.e. 3x4-bit RGB)
- 2 selectable pixel-wise filters
- 2 selectable convolution filters
- - Must use 5x5 kernals
- Use "beat" events to modify the filters in real time (changing intensities and kernals)
- - Each frequency of beat event should modify the band-selective mapping differently
- Use BPM to modify filters 

## TBC...


