# Binaural Beats Dataset

This dataset lists tracks along with their metadata for the binaural beats for the five brainwaves. It is not exhaustive, but should be complete enough for most use cases, since it contains binaural beats mixed with isochronic pulses and solfeggios as well. You can use this dataset by downloading a [release](https://github.com/neelkamath/binaural-beats-dataset/releases).

## Documentation

The [`src/tracks`](src/tracks) directory contains the binaural beats in aac format. Solfeggio tracks are fifteen minutes long. Pure and isochronic tracks are one second long. The following conventions are used to name tracks, where `<WAVE>` is the brainwave, `<FREQUENCY>` is the track's frequency, and `<SOLFEGGIO_FREQUENCY>` is the solfeggio's frequency.

|Type|Format|Example|
|---|---|---|
|Pure|`<WAVE>_<FREQUENCY>.aac`|`Alpha_8_Hz.aac`|
|Isochronic|`<WAVE>_<FREQUENCY>_Isochronic_Pulses.aac`|`Alpha_10_Hz_Isochronic_Pulses.aac`|
|Solfeggio|`<WAVE>_<FREQUENCY>_Solfeggio_<SOLFEGGIO_FREQUENCY>.aac`|`Alpha_12_Hz_Solfeggio_396_Hz.aac`|

[`src/data.json`](src/data.json) contains metadata on binaural beats (frequencies are measured in Hz). It contains five keys representing the five brainwaves: `alpha`, `beta`, `delta`, `gamma`, and `theta`, each having the following structure.

|Key|Optional|Data type|Explanation|Example|
|---|---|---|---|---|
|`minFrequency`|No|`number`|Starting frequency|`0.5`|
|`maxFrequency`|No|`number`|Ending frequency|`4`|
|`pure`|No|`array`|Metadata on pure binaural beats|`[{"frequency": 0.9, "effects": ["Euphoric feeling"], "name": "Delta_0.9_Hz.aac"}]`|
|`solfeggio`|Yes|`array`|Metadata on the binaural beats mixed with solfeggio|`{"binauralBeatFrequency": 12, "solfeggioFrequency": 396, "effects": ["Designed to ease you into a state of mental awareness"], "name": "Alpha_12_Hz_Solfeggio_396_Hz.aac"}`|
|`isochronic`|Yes|`array`|Metadata on binaural beats mixed with isochronic pulses|`{"frequency": 10, "effects": ["More intense meditation"], "name": "Alpha_10_Hz_Isochronic_Pulses.aac"}`|
|`explanation`|No|`string`|What this range of binaural beats do|`"Delta brainwaves are considered the most relaxing brainwave frequency range."`|
|`benefits`|No|`array` of `string`s|Positive effects of this brainwave|`["Having high amounts of self-control"]`|

The structures of `pure`, `isochronic`, and `solfeggio` are described below.

|Key|Structures|Optional|Data type|Explanation|Example|
|---|---|---|---|---|---|
|`frequency`|`pure`, `isochronic`|No|`number`|Frequency|`0.9`|
|`binauralBeatFrequency`|`solfeggio`|No|`number`|Binaural beats' frequency|`3`|
|`solfeggioFrequency`|`solfeggio`|No|`number`|Solfeggio's frequency|`741`|
|`effects`|`pure`, `isochronic`, `solfeggio`|Yes|`array` of `string`s|Effects of hearing this track|`["Euphoric feeling"]`|
|`name`|`pure`, `isochronic`, `solfeggio`|No|`string`|Name of the track present in the `tracks` subdirectory|`"Delta_0.9_Hz.aac"`|
|`duration`|`pure`, `isochronic`, `solfeggio`|No|`number`|Track's duration in seconds|`5`|

## Credits

- [FulLengthBinaurals](https://www.youtube.com/user/FulLengthBinaurals/featured)
- [Eric Bartel](https://www.youtube.com/channel/UC98_050r8lMxngxurJgU1gA)
- [WaveSource](https://www.youtube.com/channel/UCpYoHJQBehUorTJhbOVqYcQ)
- [DeepWave Meditation](https://www.youtube.com/channel/UCC7jJKR5hleaXDrADBkpG9A)
- [Binaural Beats Online](http://www.binauralbeatsonline.com)

## License

This project is under the [MIT License](LICENSE).