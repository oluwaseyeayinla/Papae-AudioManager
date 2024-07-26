
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)![.Net](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)![Unity](https://img.shields.io/badge/Unity-100000?style=for-the-badge&logo=unity&logoColor=white)

# Papae-AudioManager
![AudioManager - Papae2D.AudioEngine](https://github.com/oluwaseyeayinla/oluwaseyeayinla.github.io/blob/master/papae/audio_manager/promotional_images/860-x-389.jpg)

**AudioManager** is a free unity library for audio. It provides a simple way for programmers to manage and control your 2D game’s background music and sound effects.


## Features
- An audio manager component in inspector view 
- Persistent singleton component with one line calls from code
- 3 background music transition effects (Swift, Linear Fade & Cross Fade)
- Control of all sound effects in game without tags
- Integration with AudioMixerGroups
- Built-in sound pool for looping or repeating sound effects
- Playlist for loading audio assets from resource folder or url


## Installation
Import the Papae-AudioManager.unitypackage or just copy the AudioManager.cs script anywhere inside Assets folder and you are ready to go


## Usage
1.  Drag and drop the **AudioManager.prefab** gameobject anywhere in the scene or hierarchy, edit any properties visible in the Inspector then call any API related function or attribute from code

2.  Or attach or add the **AudioManager** component to an empty game object in the scene, and call any API related function or attribute from code

3.  Or just fire or call any API related function or attribute from code

Note that you have to import the namespace **Papae.UnitySDK.Managers** to use the AudioManager in script


### Fade out the current music and fade in the next music within 4 seconds
```c#
AudioManager.Instance.PlayBGM(sound_clip, MusicTransition.LinearFade, 4f);
```

### Play a sound clip for the duration of 10 seconds
```c#
AudioManager.Instance.PlaySFX(sound_clip, 10f);
```

### Loop or repeat a sound at a particular world location 5 times
```c#
AudioManager.Instance.RepeatSFX(clip, world_location, 5);
```

### Load an audio clip from the resources folder and save to the playlist
```c#
AudioManager.Instance.LoadClip(resources_path, true);
```

### Play a sound clip from the playlist once
```c#
AudioManager.Instance.PlayOneShot(AudioManager.Instance.GetClipFromPlaylist(“clip_name”));
```

### Play a single instance of a sound clip forever until external stop
```c#
AudioManager.Instance.RepeatSFX(clip, -1, true);
```
> [!Note] 
You can also use the PlaySFX to loop a sound forever. Just pass the `float.PositiveInfinity` as the duration parameter.


### Load a wave audio file from a specified url path but don’t add to playlist
```c#
AudioManager.Instance.LoadClip(url_string, AudioType.WAV, false, callback);
```


Read the [API Reference](https://oluwaseyeayinla.github.io/papae/audio_manager/api_reference/html/annotated.html) for more information.


## Author

[@oluwaseyeayinla](https://github.com/oluwaseyeayinla) 


[![Ko-fi Badge](https://flat.badgen.net/badge/Buy%20me%20a%20coffee/Ko-fi/FF5E5B?icon=buymeacoffee)](https://ko-fi.com/oluwaseyeayinla)

[![Ko-fi Badge](https://flat.badgen.net/badge/Buy%20me%20a%20coffee/Revolut/191C1F?icon=buymeacoffee)](https://revolut.me/oluwaseyeayinla)



## Current Version
Version 1.3.1

## License
MIT License. Copyright 2016 Oluwaseye Ayinla.
