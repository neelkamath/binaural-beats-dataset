# Binaural Beats Dataset

The [`src/tracks`](src/tracks) directory contains the binaural beats in MP3 format. Solfeggio tracks are fifteen minutes long, and the rest are one minute long.

[`src/data.json`](src/data.json) contains metadata on binaural beats (frequencies are measured in Hz). It contains four keys: `delta`, `theta`, `alpha`, `beta`, and `gamma`, each having the following structure.

|Key|Optional|Data type|Explanation|Example|
|---|---|---|---|---|
|`minFrequency`|No|`number`|Starting frequency|`0.5`|
|`maxFrequency`|No|`number`|Ending frequency|`4`|
|`pureRanges`|No|`array`|Metadata on the subranges of pure binaural beats|`[{"frequency": 0.9, "effects": ["Euphoric feeling"], "name": "0.9 Hz Delta.mp3"}]`|
|`solfeggioRanges`|Yes|`array`|Metadata on the subranges of binaural beats mixed with solfeggio|`{"binauralBeatFrequency": 12, "solfeggioFrequency": 396, "effects": ["Designed to ease you into a state of mental awareness"], "name": "12 Hz Alpha 396 Hz Solfeggio.mp3"}`|
|`isochronicRanges`|Yes|`array`|Metadata on the subranges of binaural beats mixed with isochronic pulses|`{"frequency": 10, "effects": ["More intense meditation"], "name": "10 Hz Alpha + Isochronic Pulses.mp3"}`|
|`explanation`|No|`string`|What this range of binaural beats do|`"Delta brainwaves are considered the most relaxing brainwave frequency range."`|
|`benefits`|No|`string`|Positive effects of this brainwave|`"Having high amounts of self-control"`|

`pureRanges` has the following structure.

|Key|Optional|Data type|Explanation|Example|
|---|---|---|---|---|
|`frequency`|No|`number`|Frequency|`0.9`|
|`effects`|Yes|`array` of `string`s|Effects of hearing this track|`["Euphoric feeling"]`|
|`name`|No|`string`|Name of the track present in the `tracks` subdirectory|`"0.9 Hz Delta.mp3"`|

`solfeggioRanges` has the following structure.

|Key|Optional|Data type|Explanation|Example|
|---|---|---|---|---|
|`binauralBeatFrequency`|No|`number`|Binaural beats' frequency|`3`|
|`solfeggioFrequency`|No|`number`|Solfeggio's frequency|`741`|
|`effects`|No|`array` of `string`s|Effects of hearing this track|`["Deep state of relaxation"]`|
|`name`|No|`string`|Name of the track present in the `tracks` subdirectory|`"3 Hz Delta 741 Hz Solfeggio.mp3"`|

`isochronicRanges` has the following structure.

|Key|Optional|Data type|Explanation|Example|
|---|---|---|---|---|
|`frequency`|No|`number`|Frequency|`4`|
|`effects`|Yes|`array` of `string`s|Effects of hearing this track|`["More intense meditation"]`|
|`name`|No|`string`|Name of the track present in the `tracks` subdirectory|`"4 Hz Delta + Isochronic Pulses.mp3"`|

## Credits

- [FulLengthBinaurals](https://www.youtube.com/user/FulLengthBinaurals/featured)
- [Greenred Productions - Relaxing Music](https://www.youtube.com/channel/UC1bjWVLp2aaJmPcNbi9OOsw)
- [WaveSource](https://www.youtube.com/channel/UCpYoHJQBehUorTJhbOVqYcQ)
- [DeepWave Meditation](https://www.youtube.com/channel/UCC7jJKR5hleaXDrADBkpG9A)
- [Binaural Beats Online](http://www.binauralbeatsonline.com)

## License

This project is under the [MIT License](LICENSE).