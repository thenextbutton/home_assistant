Here are example payloads of data sent from the Plex server


* [Movie Play](#movie-play)
* [Movie Pause](#movie-pause)
* [Movie Resume](#movie-resume)
* [Movie Scrobble](#movie-scrobble)
* [Movie Stop](#movie-stop)
* [Episode Play](#episode-play)
* [Episode Pause](#episode-pause)
* [Episode Resume](#episode-resume)
* [Episode Scrobble](#episode-scrobble)
* [Episode Stop](#episode-stop)
* [Track Play](#track-play)
* [Track Pause](#track-pause)
* [Track Resume](#track-resume)
* [Track Scrobble](#track-scrobble)
* [Track Stop](#track-stop)
* [Item Added Movie](#item-added-movie)
* [Item Added Show](#item-added-show)
* [Item Added Episode](#item-added-episode)
* [Item Added Artist](#item-added-artist)
* [Item Added Album](#item-added-album)
* [Movie Rate](#movie-rate)
* * [Star Ratings](#star-ratings)
* [Collection Rate](#collection-rate)
* * [Star Ratings](#star-ratings)
* [Album Rate](#album-rate)
* * [Star Ratings](#star-ratings)
* [Artist Rate](#artist-rate)
* * [Star Ratings](#star-ratings)
* [Track Rate](#track-rate)
* * [Star Ratings](#star-ratings)
* [Season Rate](#season-rate)
* * [Star Ratings](#star-ratings)
* [Episode Rate](#episode-rate)
* * [Star Ratings](#star-ratings)
* [Admin Database Backup](#admin-database-backup)
* [Admin Database Corrupted](#admin-database-corrupted)
* [NEW Device](#new-device)
* [Playback Started](#playback-started)


---

## Movie Play
##### Movie starts playing.
```yaml

```
## Movie Pause
##### Movie playback pauses.
```yaml

```
## Movie Resume
##### Movie playback resumes.
```yaml

```
## Movie Scrobble
##### Movie is viewed (played past the 90% mark).
```yaml

```
## Movie Stop
##### Movie playback stops.
```yaml

```
## Episode Play
##### TV Episode starts playing.
```yaml

```
## Episode Pause
##### TV Episode playback pauses.
```yaml

```
## Episode Resume
##### TV Episode playback resumes.
```yaml

```
## Episode Scrobble
##### TV Episode is viewed (played past the 90% mark).
```yaml

```
## Episode Stop
##### TV Episode playback stops.
```yaml

```
## Track Play
##### Music Track starts playing.
```yaml

```
## Track Pause
##### Music Track playback pauses.
```yaml

```
## Track Resume
##### Music Track playback resumes.
```yaml

```
## Track Scrobble
##### Music Track is played (played past the 90% mark).
```yaml

```
## Track Stop
##### Music Track playback stops.
```yaml

```
## Item Added Movie

```yaml

```
## Item Added Show

```yaml

```
## Item Added Episode

```yaml

```
## Item Added Artist

```yaml

```
## Item Added Album

```yaml

```
## Movie Rate
##### Movie is rated.
```yaml

```
## Collection Rate
##### A Collection is rated.
```yaml

```
## Album Rate
##### Album is rated.
```yaml

```
## Artist Rate
##### Artist is rated.
```yaml

```
## Track Rate
##### Music Track is rated.
```yaml

```
## Season Rate
##### TV Season is rated.
```yaml

```
## Episode Rate
##### TV Episode is rated.
```yaml

```
## Admin Database Backup
##### A database backup is completed successfully via Scheduled Tasks.
```yaml

```
## Admin Database Corrupted
##### Corruption is detected in the server database.
```yaml

```
## New Device
```yaml

```
## Playback Started
##### Playback is started by a shared user for the server.
```yaml

```

## Star Ratings

☆☆☆☆☆<br>
0 Stars / {payload.rating} = -1

½☆☆☆☆<br>
½ Star / {payload.rating} = 1

★☆☆☆☆<br>
1 Star / {payload.rating} = 2

★½☆☆☆<br>
1½ Stars / {payload.rating} = 3

★★☆☆☆<br>
2 Stars / {payload.rating} = 4

★★½☆☆<br>
2½ Stars / {payload.rating} = 5

★★★☆☆<br>
3 Stars / {payload.rating} = 6

★★★½☆<br>
3½ Stars / {payload.rating} = 7

★★★★☆<br>
4 Stars / {payload.rating} = 8

★★★★½<br>
4½ Stars / {payload.rating} = 9

★★★★★<br>
5 Stars / {payload.rating} = 10
