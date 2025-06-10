 ,Here are example payloads of what are sent from the Jellyfin server when webhooks are received when using the required [template](https://github.com/thenextbutton/home_assistant/blob/main/blueprints/jellyfin_webhook_handler_v2/webhook_template.handlebars)

---



* [Authentication Success](#authentication-success)
* [Authentication Failure](#authentication-failure)
* [User Created](#user-created)
* [User Deleted](#user-deleted)
* [User Password Changed](#user-password-changed)
* [User Locked Out](#user-locked-out)
* [Movie Item Added](#movie-item-added)
* [Movie Item Deleted](#movie-item-deleted)
* [TV Show Season Item Added](#tv-show-season-item-added)
* [TV Show Season Item Deleted](#tv-show-season-item-deleted)
* [TV Show Series Item Added](#tv-show-series-item-added)
* [TV Show Series Item Deleted](#tv-show-series-item-deleted)
* [TV Show Episode Item Added](#tv-show-episode-item-added)
* [TV Show Episode Item Deleted](#tv-show-episode-item-deleted)
* [Music Album Item Added](#music-album-item-added)
* [Music Album Item Deleted](#music-album-item-deleted)
* [Music Audio Item Added](#music-audio-item-added)
* [Music Audio Item Deleted](#music-audio-item-deleted)
* [Movie Playback Start](#movie-playback-start)
* [Movie Playback Progress](#movie-playback-progress)
* [Movie Playback Stop](#movie-playback-stop)
* [TV Show Episode Playback Start](#tv-show-episode-playback-start)
* [TV Show Episode Playback Progress](#tv-show-episode-playback-progress)
* [TV Show Episode Playback Stop](#tv-show-episode-playback-stop)
* [Music Playback Start](#music-playback-start)
* [Music Playback Progress](#music-playback-progress)
* [Music Playback Stop](#music-playback-stop)
* [Jinja Examples](#jinja-examples)

---

## Authentication Success

```yaml
payload:
  notification_type: AuthenticationSuccess
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
```

## Authentication Failure

```yaml
payload:
  notification_type: AuthenticationFailure
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
```
## User Created
```yaml

payload:
  notification_type: UserCreated
  user_name: test_account
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  event_type: user_created
  user_id: my_user_id
  last_login_date: '2025-06-07T09:32:57.8725574Z'
  last_activity_date: '0001-01-01T00:00:00.0000000'
```
## User Deleted
```yaml

payload:
  notification_type: UserDeleted
  user_name: test_account
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  event_type: user_deleted
  user_id: my_user_id
  last_login_date: '2025-06-07T09:42:12.2474129Z'
  last_activity_date: '0001-01-01T00:00:00.0000000'
```
## User Password Changed
```yaml

payload:
  notification_type: UserPasswordChanged
  user_name: test_account
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  event_type: user_password_changed
  user_id: my_user_id
  last_login_date: '2025-06-07T09:32:58.0512112Z'
  last_activity_date: '0001-01-01T00:00:00.0000000'
```
## User Locked Out
```yaml

payload:
  notification_type: UserLockedOut
  user_name: test_account
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  event_type: user_locked_out
  user_id: my_user_id
  last_login_date: '2025-06-07T09:40:54.5662233Z'
  last_activity_date: '0001-01-01T00:00:00.0000000'
```
## Movie Item Added
```yaml

payload:
  notification_type: ItemAdded
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: f89e3c5d-6233-e82a-a952-10bc172ded22
  item_type: Movie
  item_name: Auntie Edna
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/f89e3c5d-6233-e82a-a952-10bc172ded22/Images/Primary
  year: '2018'
  overview: >-
    Taking place during the events of Incredibles 2, Edna Mode babysits
    Jack-Jack.
  genres: Animation, Comedy, Family, Science Fiction
```
## Movie Item Deleted
```yaml

payload:
  notification_type: ItemDeleted
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: f89e3c5d-6233-e82a-a952-10bc172ded22
  item_type: Movie
  item_name: Auntie Edna
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/f89e3c5d-6233-e82a-a952-10bc172ded22/Images/Primary
  year: '2018'
  overview: >-
    Taking place during the events of Incredibles 2, Edna Mode babysits
    Jack-Jack.
  genres: Animation, Comedy, Family, Science Fiction
```
## TV Show Season Item Added
```yaml

payload:
  notification_type: ItemAdded
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 1044e35a-9517-8aba-5e93-fb40da383ae1
  item_type: Season
  item_name: Season 2
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/1044e35a-9517-8aba-5e93-fb40da383ae1/Images/Primary
  series_name: 'Star Trek: Strange New Worlds'
  series_id: 611b03a7-dcdc-2968-10a6-23b8954c2046
  season_number: '2'
  season_number_00: '02'
  overview: >-
    In season two, the crew of the U.S.S. Enterprise, under the command of
    Captain Christopher Pike, confronts increasingly dangerous stakes, explores
    uncharted territories and encounters new life and civilizations. The crew
    will also embark on personal journeys that will continue to test their
    resolve and redefine their destinies. Facing friends and enemies both new
    and familiar, their adventures will unfold in surprising ways never seen
    before.
  year: '2022'
```
## TV Show Season Item Deleted
```yaml

payload:
  notification_type: ItemDeleted
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 1044e35a-9517-8aba-5e93-fb40da383ae1
  item_type: Season
  item_name: Season 2
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/1044e35a-9517-8aba-5e93-fb40da383ae1/Images/Primary
  series_name: 'Star Trek: Strange New Worlds'
  series_id: 611b03a7-dcdc-2968-10a6-23b8954c2046
  season_number: '2'
  season_number_00: '02'
  overview: >-
    In season two, the crew of the U.S.S. Enterprise, under the command of
    Captain Christopher Pike, confronts increasingly dangerous stakes, explores
    uncharted territories and encounters new life and civilizations. The crew
    will also embark on personal journeys that will continue to test their
    resolve and redefine their destinies. Facing friends and enemies both new
    and familiar, their adventures will unfold in surprising ways never seen
    before.
  year: '2022'
```
## TV Show Series Item Added
```yaml

payload:
  notification_type: ItemAdded
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 611b03a7-dcdc-2968-10a6-23b8954c2046
  item_type: Series
  item_name: 'Star Trek: Strange New Worlds'
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/611b03a7-dcdc-2968-10a6-23b8954c2046/Images/Primary
  overview: >-
    Follow Captain Christopher Pike, Science Officer Spock and Number One in the
    years before Captain Kirk boarded the U.S.S. Enterprise, as they explore new
    worlds around the galaxy.
  year: '2022'
```
## TV Show Series Item Deleted
```yaml

payload:
  notification_type: ItemDeleted
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 611b03a7-dcdc-2968-10a6-23b8954c2046
  item_type: Series
  item_name: 'Star Trek: Strange New Worlds'
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/611b03a7-dcdc-2968-10a6-23b8954c2046/Images/Primary
  overview: >-
    Follow Captain Christopher Pike, Science Officer Spock and Number One in the
    years before Captain Kirk boarded the U.S.S. Enterprise, as they explore new
    worlds around the galaxy.
  year: '2022'
```
## TV Show Episode Item Added
```yaml

payload:
  notification_type: ItemAdded
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: e0c97f36-7e2d-fda5-9cad-1f769bb1fac8
  item_type: Episode
  item_name: All Those Who Wander
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/e0c97f36-7e2d-fda5-9cad-1f769bb1fac8/Images/Primary
  series_name: 'Star Trek: Strange New Worlds'
  season_number: '1'
  season_number_00: '01'
  episode_number: '9'
  episode_number_00: '09'
  episode_year: '2022'
  overview: >-
    The U.S.S. Enterprise crew comes face-to-face with their demons – and
    scary monsters too – when their landing party is stranded on a barren
    planet with a ravenous enemy.
  genres: Action, Adventure, Sci-Fi
  series_id: 611b03a7-dcdc-2968-10a6-23b8954c2046
```
## TV Show Episode Item Deleted
```yaml

payload:
  notification_type: ItemDeleted
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: e0c97f36-7e2d-fda5-9cad-1f769bb1fac8
  item_type: Episode
  item_name: All Those Who Wander
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/e0c97f36-7e2d-fda5-9cad-1f769bb1fac8/Images/Primary
  series_name: 'Star Trek: Strange New Worlds'
  season_number: '1'
  season_number_00: '01'
  episode_number: '9'
  episode_number_00: '09'
  episode_year: '2022'
  overview: >-
    The U.S.S. Enterprise crew comes face-to-face with their demons – and
    scary monsters too – when their landing party is stranded on a barren
    planet with a ravenous enemy.
  genres: Action, Adventure, Sci-Fi
  series_id: 611b03a7-dcdc-2968-10a6-23b8954c2046
```
## Music Album Item Added
```yaml

payload:
  notification_type: ItemAdded
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 6191fa08-75dc-c02d-25b2-02abef618fa9
  item_type: MusicAlbum
  item_name: Greatest Hits
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/6191fa08-75dc-c02d-25b2-02abef618fa9/Images/Primary
  album: ''
  artist: Bob Seger & the Silver Bullet Band
  genres: Rock
  year: '1994'
  runtime_ticks: '37598665299'
  runtime: '01:02:39'
```
## Music Album Item Deleted
```yaml

payload:
  notification_type: ItemDeleted
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 6191fa08-75dc-c02d-25b2-02abef618fa9
  item_type: MusicAlbum
  item_name: Greatest Hits
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/6191fa08-75dc-c02d-25b2-02abef618fa9/Images/Primary
  album: ''
  artist: Bob Seger & the Silver Bullet Band
  genres: Rock
  year: '1994'
  runtime_ticks: '37598665299'
  runtime: '01:02:39'
```
## Music Audio Item Added
```yaml

payload:
  notification_type: ItemAdded
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 55a9a512-7114-adbd-22e7-97019d3f7d47
  item_type: Audio
  item_name: The Fire Inside
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/55a9a512-7114-adbd-22e7-97019d3f7d47/Images/Primary
  album: Greatest Hits
  artist: Bob Seger & the Silver Bullet Band
  genres: Rock
  year: '1994'
```
## Music Audio Item Deleted
```yaml

payload:
  notification_type: ItemDeleted
  user_name: ''
  device_name: ''
  device_id: ''
  client_name: ''
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: a9f485e7-f679-a083-e519-e70a66d3bea9
  item_type: Audio
  item_name: Hollywood Nights
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/a9f485e7-f679-a083-e519-e70a66d3bea9/Images/Primary
  album: Greatest Hits
  artist: Bob Seger & the Silver Bullet Band
  genres: Rock
  year: '1994'
```
## Movie Playback Start
```yaml

payload:
  notification_type: PlaybackStart
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: f14f3e48-e868-df8e-9b1e-86f04e5eb0c0
  item_type: Movie
  item_name: The Adventures of André and Wally B.
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/f14f3e48-e868-df8e-9b1e-86f04e5eb0c0/Images/Primary
  year: '1984'
  overview: >-
    There's nothing like a restful nap in a pleasant wooded valley. But when
    André awakens and is greeted by a pesky yellow-and-black striped insect
    with a nasty stinger, he ends up taking a quick (and painful) hike.
  genres: Family, Animation, Comedy
  event_type: playback_start
  runtime_ticks: '1231780000'
  play_method: DirectPlay
  is_paused: 'False'
```
## Movie Playback Progress
```yaml

payload:
  notification_type: PlaybackProgress
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: f14f3e48-e868-df8e-9b1e-86f04e5eb0c0
  item_type: Movie
  item_name: The Adventures of Andr&#233; and Wally B.
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/f14f3e48-e868-df8e-9b1e-86f04e5eb0c0/Images/Primary
  year: '1984'
  overview: >-
    There's nothing like a restful nap in a pleasant wooded valley. But when
    Andr&#233; awakens and is greeted by a pesky yellow-and-black striped insect
    with a nasty stinger, he ends up taking a quick (and painful) hike.
  genres: Family, Animation, Comedy
  event_type: playback_progress
  playback_position_ticks: '532820000'
  runtime_ticks: '1231780000'
  is_paused: 'False'
  play_method: DirectPlay
```
## Movie Playback Stop
```yaml

payload:
  notification_type: PlaybackStop
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: f14f3e48-e868-df8e-9b1e-86f04e5eb0c0
  item_type: Movie
  item_name: The Adventures of André and Wally B.
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/f14f3e48-e868-df8e-9b1e-86f04e5eb0c0/Images/Primary
  year: '1984'
  overview: >-
    There's nothing like a restful nap in a pleasant wooded valley. But when
    André awakens and is greeted by a pesky yellow-and-black striped insect
    with a nasty stinger, he ends up taking a quick (and painful) hike.
  genres: Family, Animation, Comedy
  event_type: playback_stop
  played_to_completion: 'False'
  playback_position_ticks: '35250000'
  runtime_ticks: '1231780000'
  play_method: ''
  is_paused: 'False'
```
## TV Show Episode Playback Start
```yaml

payload:
  notification_type: PlaybackStart
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 14072a95-20c9-c1af-49ab-13dda856613b
  item_type: Episode
  item_name: Uno
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/14072a95-20c9-c1af-49ab-13dda856613b/Images/Primary
  series_name: Better Call Saul
  season_number: '1'
  season_number_00: '01'
  episode_number: '1'
  episode_number_00: '01'
  episode_year: '2015'
  overview: >-
    Jimmy works his magic in the courtroom. Unexpected inspiration leads him to
    an unconventional pursuit of potential clients.
  genres: Crime, Drama
  series_id: 16c6001b-e2a4-0f2a-72d2-3bcedcdc6add
  event_type: playback_start
  runtime_ticks: '31852030000'
  play_method: DirectPlay
  is_paused: 'False'
```
## TV Show Episode Playback Progress
```yaml

payload:
  notification_type: PlaybackProgress
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 14072a95-20c9-c1af-49ab-13dda856613b
  item_type: Episode
  item_name: Uno
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/14072a95-20c9-c1af-49ab-13dda856613b/Images/Primary
  series_name: Better Call Saul
  season_number: '1'
  season_number_00: '01'
  episode_number: '1'
  episode_number_00: '01'
  episode_year: '2015'
  overview: >-
    Jimmy works his magic in the courtroom. Unexpected inspiration leads him to
    an unconventional pursuit of potential clients.
  genres: Crime, Drama
  series_id: 16c6001b-e2a4-0f2a-72d2-3bcedcdc6add
  event_type: playback_progress
  playback_position_ticks: '14932600000'
  runtime_ticks: '31852030000'
  is_paused: 'False'
  play_method: DirectPlay
```
## TV Show Episode Playback Stop
```yaml

payload:
  notification_type: PlaybackStop
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 14072a95-20c9-c1af-49ab-13dda856613b
  item_type: Episode
  item_name: Uno
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/14072a95-20c9-c1af-49ab-13dda856613b/Images/Primary
  series_name: Better Call Saul
  season_number: '1'
  season_number_00: '01'
  episode_number: '1'
  episode_number_00: '01'
  episode_year: '2015'
  overview: >-
    Jimmy works his magic in the courtroom. Unexpected inspiration leads him to
    an unconventional pursuit of potential clients.
  genres: Crime, Drama
  series_id: 16c6001b-e2a4-0f2a-72d2-3bcedcdc6add
  event_type: playback_stop
  played_to_completion: 'False'
  playback_position_ticks: '29810000'
  runtime_ticks: '31852030000'
  play_method: ''
  is_paused: 'False'
```
## Music Playback Start
```yaml

payload:
  notification_type: PlaybackStart
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 2648c078-2a6c-fb48-f873-b2f7cdcf968f
  item_type: Audio
  item_name: Mr. Brownstone
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/2648c078-2a6c-fb48-f873-b2f7cdcf968f/Images/Primary
  album: Appetite for Destruction
  artist: Guns N’ Roses
  genres: Hard Rock
  year: '1987'
  event_type: playback_start
  playback_position_ticks: '0'
  runtime_ticks: '2288933330'
  play_method: DirectPlay
  is_paused: 'False'
```
## Music Playback Progress
```yaml

payload:
  notification_type: PlaybackProgress
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 2648c078-2a6c-fb48-f873-b2f7cdcf968f
  item_type: Audio
  item_name: Mr. Brownstone
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/2648c078-2a6c-fb48-f873-b2f7cdcf968f/Images/Primary
  album: Appetite for Destruction
  artist: Guns N&#8217; Roses
  genres: Hard Rock
  year: '1987'
  event_type: playback_progress
  playback_position_ticks: '1136410000'
  runtime_ticks: '2288933330'
  is_paused: 'False'
  play_method: DirectPlay
```
## Music Playback Stop
```yaml

payload:
  notification_type: PlaybackStop
  user_name: my_username
  device_name: my_funky_player_name
  device_id: >-
    my_funky_player_id
  client_name: Jellyfin Media Player
  server_name: my_funky_server_name
  server_id: my_funky_server_id
  server_version: 10.10.7
  item_id: 2648c078-2a6c-fb48-f873-b2f7cdcf968f
  item_type: Audio
  item_name: Mr. Brownstone
  thumbnail_url: >-
    http://10.0.1.101:8096/Items/2648c078-2a6c-fb48-f873-b2f7cdcf968f/Images/Primary
  album: Appetite for Destruction
  artist: Guns N’ Roses
  genres: Hard Rock
  year: '1987'
  event_type: playback_stop
  played_to_completion: 'False'
  playback_position_ticks: '21120000'
  runtime_ticks: '2288933330'
  play_method: ''
  is_paused: 'False'
```
## Jinja Examples

#### Movie:
`{{ payload.user_name }}` is now watching `{{ payload.item_name }}` which was released in `{{ payload.year }}`
<br>my_username is now watching The Adventures of André and Wally B. which was released in 1984

#### TV Show:
`{{ payload.series_name }}` Season `{{ payload.season_number_00 }}` Episode `{{ payload.episode_number_00 }}` is currently playing on `{{ payload.device_name }}`
<br>Better Call Saul Season 01 Episode 01 is currently playing on my_funky_player_name

#### Music:
`{{ payload.user_name }}` is listening to `{{ payload.item_name }}` by `{{ payload.artist }}`
<br>my_username is listening to Hollywood Nights by Bob Seger & the Silver Bullet Band
