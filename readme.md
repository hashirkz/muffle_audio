# about
audio / music muffler/fuzzifier for     
- \*.mp3  
- \*.wav  
- \*.ogg  

## installation
```bash
git clone "https://github.com/hashirkz/muffle_audio"
cd muffle_audio
./setup.sh
```

### options  
| rec | flag             | description                                                         |
| --- | ---------------- | ------------------------------------------------------------------- |
| !   | -f \| --file     | filename to muffle                                                  |
| !   | -r \| --read_dir | directory to muffle all audio files                                 |
| ?   | -d \| --dest     | destination file/directory name if filename ***must end with .mp3** |


### conf.yml
feel free to play around with these values to see what works best for you  

hz      : butterworth lowpass filter cutoff frequency 
roll    : strength of lowpass filter
tones   : non time stretching pitching **tones < 0 pitch down** 
rate    : slowing factor rate < 1 slows

### ex. usage
```bash
>> python3 -m __muffle__.app -r "audios" -d "muffled"

2023-12-30 01:59:43,431|INFO           |reading: fuzzywave_A faint signal.mp3
2023-12-30 01:59:43,431|INFO           |writing: fuzzywave_A faint signal.mp3
2023-12-30 01:59:50,859|INFO           |reading: fuzzywave_a l e x - zelda's lullaby (slowed).mp3
2023-12-30 01:59:50,860|INFO           |writing: fuzzywave_a l e x - zelda's lullaby (slowed).mp3
2023-12-30 02:00:03,949|INFO           |reading: fuzzywave_MISOGI - Clairvoyant Slowed Down.mp3
2023-12-30 02:00:03,949|INFO           |writing: fuzzywave_MISOGI - Clairvoyant Slowed Down.mp3
2023-12-30 02:00:22,382|INFO           |reading: fuzzywave_OMORI OST - 004 Spaces In - Between.mp3
2023-12-30 02:00:22,382|INFO           |writing: fuzzywave_OMORI OST - 004 Spaces In - Between.mp3
2023-12-30 02:00:25,925|INFO           |reading: lovefool_miku_looped.mp3
2023-12-30 02:00:25,925|INFO           |writing: lovefool_miku_looped.mp3
2023-12-30 02:00:38,322|INFO           |reading: okay_poorstacy.mp3
2023-12-30 02:00:38,323|INFO           |writing: okay_poorstacy.mp3
```