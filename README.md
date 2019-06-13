# Binaural Beats Dataset

This dataset lists tracks along with their metadata for the binaural beats for the five brainwaves. It is not exhaustive, but should be complete enough for most use cases, since it contains binaural beats mixed with solfeggio and isochronic pulses as well.

## Documentation

The [`src/tracks`](src/tracks) directory contains the binaural beats in MP3 format. Solfeggio tracks are fifteen minutes long, and the rest are one minute long. Track names are guaranteed to be valid HTML `id`s. The following conventions are used to name tracks, where `<WAVE>` is the brainwave, `<FREQUENCY>` is the track's frequency, and `<SOLFEGGIO_FREQUENCY>` is the solfeggio's frequency.
- Pure: `<WAVE>_<FREQUENCY>.mp3` (e.g., `Alpha_8_Hz.mp3`)
- Isochronic: `<WAVE>_<FREQUENCY>_Isochronic_Pulses.mp3` (e.g., `Alpha_10_Hz_Isochronic_Pulses.mp3`)
- Solfeggio: `<WAVE>_<FREQUENCY>_Solfeggio_<SOLFEGGIO_FREQUENCY>.mp3` (e.g., `Alpha_12_Hz_Solfeggio_396_Hz.mp3`)

[`src/data.json`](src/data.json) contains metadata on binaural beats (frequencies are measured in Hz). It contains five keys representing the five brainwaves: `alpha`, `beta`, `delta`, `gamma`, and `theta`, each having the following structure.

|Key|Optional|Data type|Explanation|Example|
|---|---|---|---|---|
|`minFrequency`|No|`number`|Starting frequency|`0.5`|
|`maxFrequency`|No|`number`|Ending frequency|`4`|
|`pure`|No|`array`|Metadata on pure binaural beats|`[{"frequency": 0.9, "effects": ["Euphoric feeling"], "name": "Delta_0.9_Hz.mp3"}]`|
|`solfeggio`|Yes|`array`|Metadata on the binaural beats mixed with solfeggio|`{"binauralBeatFrequency": 12, "solfeggioFrequency": 396, "effects": ["Designed to ease you into a state of mental awareness"], "name": "Alpha_12_Hz_Solfeggio_396_Hz.mp3"}`|
|`isochronic`|Yes|`array`|Metadata on binaural beats mixed with isochronic pulses|`{"frequency": 10, "effects": ["More intense meditation"], "name": "Alpha_10_Hz_Isochronic_Pulses.mp3"}`|
|`explanation`|No|`string`|What this range of binaural beats do|`"Delta brainwaves are considered the most relaxing brainwave frequency range."`|
|`benefits`|No|`array` of `string`s|Positive effects of this brainwave|`["Having high amounts of self-control"]`|

`pure` and `isochronic` have the following structure.

|Key|Optional|Data type|Explanation|Example|
|---|---|---|---|---|
|`frequency`|No|`number`|Frequency|`0.9`|
|`effects`|Yes|`array` of `string`s|Effects of hearing this track|`["Euphoric feeling"]`|
|`name`|No|`string`|Name of the track present in the `tracks` subdirectory|`"Delta_0.9_Hz.mp3"`|

`solfeggio` has the following structure.

|Key|Optional|Data type|Explanation|Example|
|---|---|---|---|---|
|`binauralBeatFrequency`|No|`number`|Binaural beats' frequency|`3`|
|`solfeggioFrequency`|No|`number`|Solfeggio's frequency|`741`|
|`effects`|No|`array` of `string`s|Effects of hearing this track|`["Deep state of relaxation"]`|
|`name`|No|`string`|Name of the track present in the `tracks` subdirectory|`"Delta_3_Hz_Solfeggio_741_Hz.mp3"`|

## Credits

- [FulLengthBinaurals](https://www.youtube.com/user/FulLengthBinaurals/featured)
- [Greenred Productions - Relaxing Music](https://www.youtube.com/channel/UC1bjWVLp2aaJmPcNbi9OOsw)
- [WaveSource](https://www.youtube.com/channel/UCpYoHJQBehUorTJhbOVqYcQ)
- [DeepWave Meditation](https://www.youtube.com/channel/UCC7jJKR5hleaXDrADBkpG9A)
- [Binaural Beats Online](http://www.binauralbeatsonline.com)

## License

This project is under the [MIT License](LICENSE).