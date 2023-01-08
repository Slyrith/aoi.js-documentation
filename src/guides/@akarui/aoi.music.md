---
title: akarui/aoi.music
description: How to integrate aoi.music into your Discord Bot with ease.
id: akarui/aoi.music
---

### Installation

**node.js 16.9.0 or newer is required.**

```bash
npm install @akarui/aoi.music
```

## Example

```javascript
const aoijs = require("aoi.js");
const { AoiVoice } = require("@akarui/aoi.music");

const bot = new aoijs.AoiClient({
    token: "Discord Bot Token",
    prefix: "Discord Bot Prefix",
    intents: ["MessageContent", "Guilds", "GuildMessages", "GuildVoiceStates"],
});

//Events
bot.onMessage();

//Command Example (ping)
bot.command({
    name: "ping",
    code: `Pong! $pingms`,
});

const voice = new AoiVoice(bot, {
    searchOptions: {
        soundcloudClientId: "Sound Cloud Id",
        youtubegl: "US",
    },
    requestOptions: {
        offsetTimeout: 0,
        soundcloudLikeTrackLimit: 200,
    },
});
```

## All Available Options

<details>
<summary>Voice#devOptions</summary>

```typescript
devOptions?: {
        debug: boolean;
    };
```

</details>
<details>
<summary>Voice#searchOptions</summary>

```typescript
    searchOptions?: {
        soundcloudClientId?: string;
        youtubeCookie?: string;
        youtubeAuth?: PathLike;
        youtubegl?: string;
        youtubeClient?: "WEB" | "ANDROID" | "YTMUSIC";
    };
```

</details>
<details>
<summary>Voice#requestOptions</summary>

```typescript
    requestOptions?: {
        offsetTimeout?: number;
        soundcloudLikeTrackLimit?: number;
        youtubePlaylistLimit?: number;
        spotifyPlaylistLimit?: number;
    };
```

</details>

## Functions
<!-- $joinVc -->
<details>
<summary>$joinVc</summary>
<table>
  <tr>
    <th>Usage</th>
    <td style="display:flex;flex-direction: row;justify-content:flex-start;align-items: flex-start;width:100%;">$joinVc[<details><summary>voice/stage id</summary>Voice/Stage Channel ID</details>;<details><summary>selfDeaf?</summary>Whether the bot should deafen itself (default: yes)</details>;<details><summary>selfMute?</summary>Whether the bot should mute itself (default: no)</details>;<details><summary>speaker?</summary>Whether the bot should be speaker on stage channel (default: yes)</details>;<details><summary>debug?</summary>Whether to enable debug mode (default: no)</details>]</td>
  </tr>
  <tr>
    <th>Example</th>
    <td>$joinVc || $joinVc[$voiceId]</td>
  </tr>
</table>
</details>

<!-- $leaveVc -->
<details>
<summary>$leaveVc</summary>
<table>
  <tr>
    <th>Usage</th>
    <td style="display:flex;">$leaveVc[
        <details>
    <summary>guildId?</summary>
    Guild ID
    </details>
    ]</td>
  </tr>
  <tr>
    <th>Example</th>
    <td>$leaveVc || $leaveVc[$guildId]</td>
  </tr>
</table>
</details>

<!-- $playTrack -->
<details>
<summary>$playTrack</summary>
<table>
  <tr>
    <th>Usage</th>
    <td style="display:flex;">$playTrack[
        <details>
    <summary>query</summary>
    Search query
    </details>;
    <details>
    <summary>type</summary>
    Platform type (youtube, soundcloud, spotify, localfile, url)
    </details>
    ]</td>
  </tr>
  <tr>
    <th>Example</th>
    <td>$playTrack[https://www.youtube.com/watch?v=dQw4w9WgXcQ;youtube]</td>
  </tr>
</table>
</details>

<!-- $queue -->
<details>
<summary>$queue</summary>
<table>
  <tr>
    <th>Usage</th>
    <td style="display:flex;">$queue[
        <details>
    <summary>page?</summary>
    Page number (default: 1)
    </details>;
    <details>
    <summary>limit?</summary>
    Limit of tracks per page (default: 10)
    </details>;
    <details>
    <summary>format?</summary>
    Format of the queue (default: `{number}) {title} | {requester.user.tag}`)
    </details>
    ]</td>
  </tr>
  <tr>
    <th>Example</th>
    <td>$queue || $queue[1;10;{number}) {title} | {requester.user.tag}]</td>
  </tr>
</table>
</details>

<!-- $autoPlay -->
<details>
<summary>$autoPlay</summary>
<table>
  <tr>
    <th>Usage</th>
    <td style="display:flex;">$autoPlay[
        <details>
    <summary>type?</summary>
    Type of autoplay (relative, youtube, soundcloud, spotify, none) (default: relative)
    </details>
    ]</td>
  </tr>
  <tr>
    <th>Example</th>
    <td>$autoPlay || $autoplay[relative]</td>
  </tr>
</table>
</details>

<!-- $addFilter -->

<details>
<summary>$addFilter</summary>
<table>
  <tr>
    <th>Usage</th>
    <td style="display:flex;">$addFilter[
        <details>
    <summary>filter</summary>
    JSON format of FFmpeg audio filters
    </details>
    ]</td>
  </tr>
  <tr>
    <th>Example</th>
    <td>$addFilter[{ "asetrate" : 52000 , "aresample" : 48000 }]</td>
  </tr>
</table>
</details>

<details> 
<summary>$setFilter</summary> 
This function overwrites all filter with provided filter 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$setFilter[ 
        <details> 
    <summary>filter</summary> 
    the JSON format of filter to be used 
    </details> 
    ]</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$setFilter[{ "asetrate" : 52000 , "aresample" : 48000 }]</td> 
  </tr> 
</table> 
</details><details> 
<summary>$removeFilter</summary> 
This function removes provided filter 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$removeFilter[ 
        <details> 
    <summary>filter</summary> 
    the JSON format of filter to be removed 
    </details> 
    ]</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$removeFilter[{ "asetrate" : 52000 , "aresample" : 48000 }]</td> 
  </tr> 
</table> 
</details><details> 
<summary>$resetFilter</summary> 
This function removes all filter 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$resetFilter</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$resetFilter</td> 
  </tr> 
</table> 
</details><details> 
<summary>$getFilter</summary> 
This function returns the current filter 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$getFilter</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$getFilter</td> 
  </tr> 
</table> 
</details><details> 
<summary>$volume</summary> 
This function sets/gets the volume of the audio 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$volume[ 
        <details> 
    <summary>volume</summary> 
    the volume to be set 
    </details> 
    ]</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$volume || $volume[50]</td> 
  </tr> 
</table> 
</details><details> 
<summary>$seek</summary> 
This function seeks the audio to the provided time 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$seek[ 
        <details> 
    <summary>time</summary> 
    the time to seek to 
    </details> 
    ]</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$seek[10s]</td> 
  </tr> 
</table> 
</details><details> 
<summary>$getCurrentTrackDuration</summary> 
This function returns the duration of the current track 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$getCurrentTrackDuration</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$getCurrentTrackDuration</td> 
  </tr> 
</table> 
</details><details> 
<summary>$hasPlayer</summary> 
This function returns true if the player is connected 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$hasPlayer</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$hasPlayer</td> 
  </tr> 
</table> 
</details><details> 
<summary>$loopMode</summary> 
This function sets/gets the loop mode of the player 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$loopMode[ 
        <details> 
    <summary>mode</summary> 
    the loop mode to be set (song, queue, none) 
    </details> 
    ]</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$loopMode[queue]</td> 
  </tr> 
</table> 
</details><details> 
<summary>$clearQueue</summary> 
This function clears the queue 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$clearQueue</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$clearQueue</td> 
  </tr> 
</table> 
</details><details> 
<summary>$pauseTrack</summary> 
This function pauses the current track 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$pauseTrack</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$pauseTrack</td> 
  </tr> 
</table> 
</details><details> 
<summary>$resumeTrack</summary> 
This function resumes the current track 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$resumeTrack</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$resumeTrack</td> 
  </tr> 
</table> 
</details><details> 
<summary>$stopTrack</summary> 
This function stops the current track 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$stopTrack</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$stopTrack</td> 
  </tr> 
</table> 
</details><details> 
<summary>$skipTrack</summary> 
This function skips the current track 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$skipTrack</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$skipTrack</td> 
  </tr> 
</table> 
</details><details> 
<summary>$skipTo</summary> 
This function skips to the provided track 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$skipTo[ 
        <details> 
    <summary>track</summary> 
    the track to skip to 
    </details> 
    ]</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$skipTo[5]</td> 
  </tr> 
</table> 
</details><details> 
<summary>$playPreviousTrack</summary> 
This function plays the previous track 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$playPreviousTrack</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$playPreviousTrack</td> 
  </tr> 
</table> 
</details><details> 
<summary>$queueLength</summary> 
This function returns the length of the queue 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$queueLength</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$queueLength</td> 
  </tr> 
</table> 
</details><details> 
<summary>$voicePing</summary> 
This function returns the ping of the voice connection 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$voicePing[ 
        <details> 
    <summary>type</summary> 
    the type of ping to be returned (ws, udp) 
    </details> 
    ]</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$voicePing || $voicePing[ws]</td> 
  </tr> 
</table> 
</details><details> 
<summary>$playerStatus</summary> 
This function returns the status of the player 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$playerStatus</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$playerStatus</td> 
  </tr> 
</table> 
</details><details> 
<summary>$shuffleQueue</summary> 
This function shuffles the queue 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$shuffleQueue</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$shuffleQueue</td> 
  </tr> 
</table> 
</details><details> 
<summary>$unshuffleQueue</summary> 
This function unshuffles the queue 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$unshuffleQueue</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$unshuffleQueue</td> 
  </tr> 
</table> 
</details><details> 
<summary>$songInfo</summary> 
This function returns the info of the song 
<table> 
  <tr> 
    <th>Usage</th> 
    <td style="display:flex;">$songInfo[ 
        <details> 
    <summary>type</summary> 
    the type of info to be returned (title, url, thumbnail, duration, user.{option here} ,author,authorURL etc.) 
    </details><details> 
    <summary>position</summary> 
    the position of the song in the queue (default: current song) 
    </details> 
    ]</td> 
  </tr> 
  <tr> 
    <th>Example</th> 
    <td>$songInfo</td> 
  </tr> 
</table> 
</details> 
