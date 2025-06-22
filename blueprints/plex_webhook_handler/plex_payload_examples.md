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
payload:
  event: media.stop
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: movie
    ratingKey: '73'
    key: /library/metadata/73
    guid: plex://movie/5e833bb566500c0041d29af9
    slug: nobody-2021
    studio: 87North Productions
    type: movie
    title: Nobody
    librarySectionTitle: Films
    librarySectionID: 6
    librarySectionKey: /library/sections/6
    contentRating: R
    summary: >-
      Hutch Mansell, a suburban dad, overlooked husband, nothing neighbor — a
      "nobody." When two thieves break into his home one night, Hutch's unknown
      long-simmering rage is ignited and propels him on a brutal path that will
      uncover dark secrets he fought to leave behind.
    rating: 8.4
    audienceRating: 9.4
    userRating: 10
    lastRatedAt: 1745785982
    year: 2021
    tagline: Never underestimate a nobody.
    thumb: /library/metadata/73/thumb/1749091611
    art: /library/metadata/73/art/1749091611
    duration: 5460000
    originallyAvailableAt: '2021-03-18'
    addedAt: 1733008519
    updatedAt: 1749091611
    audienceRatingImage: rottentomatoes://image.rating.upright
    chapterSource: media
    primaryExtraKey: /library/metadata/82
    ratingImage: rottentomatoes://image.rating.ripe
    Image:
      - alt: Nobody
        type: coverPoster
        url: /library/metadata/73/thumb/1749091611
      - alt: Nobody
        type: background
        url: /library/metadata/73/art/1749091611
      - alt: Nobody
        type: clearLogo
        url: /library/metadata/73/clearLogo/1749091611
    UltraBlurColors:
      topLeft: 4f1a17
      topRight: 913b3a
      bottomRight: 8d4633
      bottomLeft: 8d3839
    Genre:
      - id: 50944
        filter: genre=50944
        tag: 4k HDR
        count: 48
      - id: 50946
        filter: genre=50946
        tag: Dolby Atmos
        count: 38
      - id: 50945
        filter: genre=50945
        tag: Dolby Vision
        count: 21
      - id: 19
        filter: genre=19
        tag: Thriller
        count: 86
      - id: 21
        filter: genre=21
        tag: Action
        count: 230
      - id: 20
        filter: genre=20
        tag: Crime
        count: 49
      - id: 17
        filter: genre=17
        tag: Drama
        count: 128
    Country:
      - id: 87
        filter: country=87
        tag: United States of America
        count: 470
    Guid:
      - id: imdb://tt7888964
      - id: tmdb://615457
      - id: tvdb://133393
    Rating:
      - image: imdb://image.rating
        value: 7.4
        type: audience
        count: 501
      - image: rottentomatoes://image.rating.ripe
        value: 8.4
        type: critic
        count: 330
      - image: rottentomatoes://image.rating.upright
        value: 9.4
        type: audience
        count: 411
      - image: themoviedb://image.rating
        value: 7.9
        type: audience
        count: 508
    Director:
      - id: 3266
        filter: director=3266
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
    Writer:
      - id: 3267
        filter: writer=3267
        tag: Derek Kolstad
        tagKey: 5d776a8afb0d55001f54921f
        count: 4
        thumb: >-
          https://metadata-static.plex.tv/5/people/5c97a829e3651739f2971e4e2898682c.jpg
    Role:
      - id: 3268
        filter: actor=3268
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        count: 2
        role: Hutch Mansell
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3269
        filter: actor=3269
        tag: Aleksey Serebryakov
        tagKey: 5d77682b151a60001f24b98c
        role: Yulian Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b743f3f7a75e1b5bd937e2060753837.jpg
      - id: 3270
        filter: actor=3270
        tag: Connie Nielsen
        tagKey: 5d7768267228e5001f1dcdb5
        count: 4
        role: Becca Mansell
        thumb: >-
          https://metadata-static.plex.tv/3/people/328b075ecee9e20d7e22e95a72596edb.jpg
      - id: 3271
        filter: actor=3271
        tag: Christopher Lloyd
        tagKey: 5d7768244de0ee001fcc80bb
        count: 6
        role: David Mansell
        thumb: >-
          https://metadata-static.plex.tv/c/people/c2d2c2ab21e34db5837877ca386d43c3.jpg
      - id: 3272
        filter: actor=3272
        tag: Michael Ironside
        tagKey: 5d7768268718ba001e311c35
        count: 3
        role: Eddie Williams
        thumb: >-
          https://metadata-static.plex.tv/5/people/562560faf349fed1531898b075cfdf54.jpg
      - id: 3273
        filter: actor=3273
        tag: Colin Salmon
        tagKey: 5d776826880197001ec906c3
        role: The Barber
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05fd85a41289fbd0375c013fbb6593f.jpg
      - id: 3274
        filter: actor=3274
        tag: RZA
        tagKey: 5d77682985719b001f3a132f
        role: Harry Mansell
        thumb: >-
          https://metadata-static.plex.tv/9/people/97914947f71b47e35f9e0e708f6b6054.jpg
      - id: 3275
        filter: actor=3275
        tag: Billy MacLellan
        tagKey: 5d7768355af944001f1f9ddb
        role: Charlie Williams
        thumb: >-
          https://metadata-static.plex.tv/7/people/793801223b142f24e8455525db4f98b0.jpg
      - id: 3276
        filter: actor=3276
        tag: Araya Mengesha
        tagKey: 5d77687633f255001e8571ca
        role: Pavel
        thumb: >-
          https://metadata-static.plex.tv/0/people/0c5cf3bf1ba0fc04f5dfbfe7787419cd.jpg
      - id: 3277
        filter: actor=3277
        tag: Gage Munroe
        tagKey: 5d776843961905001eb96d28
        role: Brady Mansell
        thumb: >-
          https://metadata-static.plex.tv/0/people/07bdd3e7b5c9bf0151f67c6e986e546c.jpg
      - id: 3278
        filter: actor=3278
        tag: Paisley Cadorath
        tagKey: 5e166be52d4d84003e4bede2
        role: Sammy Mansell
        thumb: >-
          https://metadata-static.plex.tv/4/people/46fce2ea69eca54daeb8ef48e4fb788c.jpg
      - id: 3279
        filter: actor=3279
        tag: Aleksandr Pal
        tagKey: 5d776a28fb0d55001f53c11f
        role: Teddy Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/4/people/418db25e4856946a298e70440778a26a.jpg
      - id: 3280
        filter: actor=3280
        tag: Humberly González
        tagKey: 5d776c7cad5437001f7bf60d
        role: Lupita Martin
        thumb: >-
          https://metadata-static.plex.tv/9/people/9e0cf7073f9849cb8c6a17157c0cb1df.jpg
      - id: 3281
        filter: actor=3281
        tag: Edsson Morales
        tagKey: 5d776870eb5d26001f1eb87d
        role: Luis Martin
        thumb: >-
          https://metadata-static.plex.tv/2/people/270e11868a651c1f64e076871a0ebe09.jpg
      - id: 3282
        filter: actor=3282
        tag: J.P. Manoux
        tagKey: 5d776827103a2d001f56467f
        count: 3
        role: Pentagon Darren
        thumb: >-
          https://metadata-static.plex.tv/4/people/48d515df07e7954ad7bd291acba622d2.jpg
      - id: 3283
        filter: actor=3283
        tag: Adrian McLean
        tagKey: 5d776f5bad5437001f80fbb5
        role: Joey
        thumb: >-
          https://metadata-static.plex.tv/7/people/78e72df33a9979c71f376c23639ff4dd.jpg
      - id: 3284
        filter: actor=3284
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        role: Hitman Anatoly
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
      - id: 3285
        filter: actor=3285
        tag: Sergey Shnurov
        tagKey: 5d7768466f4521001ea9f873
        role: Hitman Valentin
        thumb: >-
          https://metadata-static.plex.tv/f/people/f78b732363a4c27c39078cf9dee79277.jpg
      - id: 3286
        filter: actor=3286
        tag: Joanne Rodriguez
        tagKey: 5d7768342ec6b5001f6bbd05
        role: Bus Driver Donna
        thumb: >-
          https://metadata-static.plex.tv/9/people/9cccffdd78a83dd849a4a41f7199f169.jpg
      - id: 3287
        filter: actor=3287
        tag: Stephanie Sy
        tagKey: 5d776d3d96b655001fe438e4
        role: Realtor
        thumb: https://metadata-static.plex.tv/people/5d776d3d96b655001fe438e4.jpg
      - id: 3288
        filter: actor=3288
        tag: Dan Rizzuto
        tagKey: 5d9f35b0b0262f001f6ec2de
        count: 2
        role: Gunman
      - id: 3289
        filter: actor=3289
        tag: Ruslan Rusin
        tagKey: 5d776d267a53e9001e752a5e
        role: Gunman
      - id: 3290
        filter: actor=3290
        tag: Vladimir Levkovsky
        tagKey: 60b90595f28049002d7ec8e2
        role: Gunman
      - id: 3291
        filter: actor=3291
        tag: Dan Skene
        tagKey: 5d77683c4de0ee001fccce80
        count: 2
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/9/people/9a3aae3a0a9c552d8c9dd651d6244f89.jpg
      - id: 3292
        filter: actor=3292
        tag: BJ Verot
        tagKey: 5d776ca79ab5440021519486
        role: Gunman
        thumb: https://metadata-static.plex.tv/people/5d776ca79ab5440021519486.jpg
      - id: 3293
        filter: actor=3293
        tag: Dylan Rampulla
        tagKey: 5e1647cd46aceb003cee8a84
        role: Gunman
      - id: 3294
        filter: actor=3294
        tag: Margaryta Soldatova
        tagKey: 5d776de696b655001fe5645f
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/2/people/2ef47acd293dd4e81ef6607c47af18aa.jpg
      - id: 3295
        filter: actor=3295
        tag: Megan Best
        tagKey: 5e166be52d4d84003e4bedde
        role: Woman on Bus
        thumb: >-
          https://metadata-static.plex.tv/d/people/d4ca27f2b660ae1fc76c8806b9b5a720.jpg
      - id: 3296
        filter: actor=3296
        tag: Darya Charusha
        tagKey: 5d7768bb374a5b001fece978
        role: Beta
        thumb: >-
          https://metadata-static.plex.tv/c/people/c503be6f3a83d9a3692d6c392679eb8e.jpg
      - id: 3297
        filter: actor=3297
        tag: Neil Davison
        tagKey: 5d9f3581adeb7a0021ce25ab
        role: Albert
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d1606a3ec7f8c775346b666d48aed59.jpg
      - id: 3298
        filter: actor=3298
        tag: Paul Essiembre
        tagKey: 5d77684f6f4521001eaa0e2c
        role: Jim the Neighbor
        thumb: >-
          https://metadata-static.plex.tv/1/people/143679603a8a9033feb9815d6a8eca29.jpg
      - id: 3299
        filter: actor=3299
        tag: Adam Hurtig
        tagKey: 5d7769e27a53e9001e6f36b4
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/c/people/cf6adb15c4d5a5ccd1dbe93fd684e807.jpg
      - id: 3300
        filter: actor=3300
        tag: Gabriel Daniels
        tagKey: 5d77689efb0d55001f5158ad
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/7/people/764cf91ca84fd8e24d10682acda85510.jpg
      - id: 3301
        filter: actor=3301
        tag: Kristen Harris
        tagKey: 5d7769ebfb0d55001f534779
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/8/people/8b82bda4aa071a57092c5e0bd82765e6.jpg
      - id: 3302
        filter: actor=3302
        tag: Erik Athavale
        tagKey: 5d776ab59ab54400215027c9
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/b/people/b0f12073fb6fa6f25213256a4493ebde.jpg
      - id: 3303
        filter: actor=3303
        tag: Tom Soares
        tagKey: 5f4059d8a4f07a00421717aa
        role: Alan Breiseth
      - id: 3304
        filter: actor=3304
        tag: Neven Pajkic
        tagKey: 5d7768256f4521001ea989ba
        role: Big Brute
        thumb: https://metadata-static.plex.tv/people/5d7768256f4521001ea989ba.jpg
      - id: 3305
        filter: actor=3305
        tag: Stephen Eric McIntyre
        tagKey: 5d776831151a60001f24d011
        role: Veteran
        thumb: >-
          https://metadata-static.plex.tv/5/people/556a233e543d87d4d3d1a2dc2630b4bb.jpg
      - id: 3306
        filter: actor=3306
        tag: Rick Dobran
        tagKey: 5d77684261141d001fb171ab
        count: 2
        role: Tattoo Shop Owner
        thumb: >-
          https://metadata-static.plex.tv/3/people/313b89fef7dd52cd49d6c78d0c1cb7e2.jpg
      - id: 3307
        filter: actor=3307
        tag: Richard Thomas
        tagKey: 64c10b5fdcb9af3bd1eee9e7
        role: Security Guard (Obshak Basement)
      - id: 3308
        filter: actor=3308
        tag: Alan Wh Wong
        tagKey: 66981d0bdcafced077160d19
        role: Doctor
      - id: 3309
        filter: actor=3309
        tag: Sharon Bajer
        tagKey: 5d776838151a60001f24e8fe
        role: Receptionist
        thumb: https://metadata-static.plex.tv/people/5d776838151a60001f24e8fe.jpg
      - id: 3310
        filter: actor=3310
        tag: Yulia Guzhva
        tagKey: 60b90596526b16002d6b1d25
        role: Karaoke Singer
      - id: 3311
        filter: actor=3311
        tag: Boris Gulyarin
        tagKey: 5d776d267a53e9001e752a57
        role: Mob Boss
        thumb: https://metadata-static.plex.tv/people/5d776d267a53e9001e752a57.jpg
      - id: 3312
        filter: actor=3312
        tag: Alex Nikolaychuk
        tagKey: 64c10b5f5b2d39db72ea18b4
        role: Mob Boss
      - id: 3313
        filter: actor=3313
        tag: Volodymyr Yamnenko
        tagKey: 5d776a5196b655001fdeac0c
        role: Mob Boss
        thumb: >-
          https://metadata-static.plex.tv/e/people/e00c1e06d5bd36b8afef7abadb3397a7.jpg
      - id: 3314
        filter: actor=3314
        tag: Meaghan Ann De Werrenne-Walle
        tagKey: 60b905965f7d3f002cb034d1
        role: Waitress (Karaoke Club)
      - id: 3315
        filter: actor=3315
        tag: Eugene Baffoe
        tagKey: 5ec419e0f8a5e90040cfaadb
        role: Barber's Guard
        thumb: >-
          https://metadata-static.plex.tv/0/people/08f07e73e74d04362ff80af43e27af9a.jpg
      - id: 3316
        filter: actor=3316
        tag: Daniel Bernhardt
        tagKey: 5d776828a091de001f2e6428
        count: 4
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/8/people/894ce74954806b4f55fac059f5af9bd9.jpg
      - id: 3317
        filter: actor=3317
        tag: Alain Moussi
        tagKey: 5d776b5096b655001fe0c5ab
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/5/people/5de5e70da005d9bcd84ee387ccd06079.jpg
      - id: 3318
        filter: actor=3318
        tag: Stéphane Julien
        tagKey: 5d776ac796b655001fdf93cc
        count: 2
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/c/people/c5501403d440b91a3c0d86cfe283523b.jpg
      - id: 3319
        filter: actor=3319
        tag: Robert Heinamaki
        tagKey: 60b90596b6a3c2002cb5df92
        role: Body Builder
      - id: 3320
        filter: actor=3320
        tag: Brent Alarie
        tagKey: 60b90596526b16002d6b1d27
        role: Tattoo Parlor
      - id: 66738
        filter: actor=66738
        tag: Tyrell Witherspoon
        tagKey: 6837cbc422219f2940060d8a
        role: Dancer
      - id: 3322
        filter: actor=3322
        tag: Frederick Allen
        tagKey: 5e166be52d4d84003e4bede0
        role: Russian Mafia Member (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/7/people/7904579927adae5ff33b8149870c5cf4.jpg
      - id: 3323
        filter: actor=3323
        tag: Destini Boldt
        tagKey: 64b018cffa119025f00aa26c
        role: Club Patron (uncredited)
    Producer:
      - id: 3324
        filter: producer=3324
        tag: David Leitch
        tagKey: 5d776828151a60001f24ae96
        count: 3
        thumb: >-
          https://metadata-static.plex.tv/4/people/4d935845dd16ac700054162203566edd.jpg
      - id: 3325
        filter: producer=3325
        tag: Kelly McCormick
        tagKey: 5d776b49fb0d55001f5629d7
        count: 2
        thumb: >-
          https://metadata-static.plex.tv/0/people/09afce317f35900bdcd7518664795277.jpg
      - id: 3326
        filter: producer=3326
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3327
        filter: producer=3327
        tag: Marc Provissiero
        tagKey: 5d776bb747dd6e001f6e242d
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b65cf07ae7032dd37dfe24ff0b00870.jpg
      - id: 66739
        filter: producer=66739
        tag: Braden Aftergood
        tagKey: 6839e0351aa1f166b353d040
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d5f88c6dbff24ede9bd423ea2fc0b95.jpg
    Field:
      - locked: true
        name: thumb
      - locked: true
        name: genre
```
## Movie Pause
##### Movie playback pauses.
```yaml
payload:
  event: media.resume
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: movie
    ratingKey: '73'
    key: /library/metadata/73
    guid: plex://movie/5e833bb566500c0041d29af9
    slug: nobody-2021
    studio: 87North Productions
    type: movie
    title: Nobody
    librarySectionTitle: Films
    librarySectionID: 6
    librarySectionKey: /library/sections/6
    contentRating: R
    summary: >-
      Hutch Mansell, a suburban dad, overlooked husband, nothing neighbor — a
      "nobody." When two thieves break into his home one night, Hutch's unknown
      long-simmering rage is ignited and propels him on a brutal path that will
      uncover dark secrets he fought to leave behind.
    rating: 8.4
    audienceRating: 9.4
    userRating: 10
    lastRatedAt: 1745785982
    year: 2021
    tagline: Never underestimate a nobody.
    thumb: /library/metadata/73/thumb/1749091611
    art: /library/metadata/73/art/1749091611
    duration: 5460000
    originallyAvailableAt: '2021-03-18'
    addedAt: 1733008519
    updatedAt: 1749091611
    audienceRatingImage: rottentomatoes://image.rating.upright
    chapterSource: media
    primaryExtraKey: /library/metadata/82
    ratingImage: rottentomatoes://image.rating.ripe
    Image:
      - alt: Nobody
        type: coverPoster
        url: /library/metadata/73/thumb/1749091611
      - alt: Nobody
        type: background
        url: /library/metadata/73/art/1749091611
      - alt: Nobody
        type: clearLogo
        url: /library/metadata/73/clearLogo/1749091611
    UltraBlurColors:
      topLeft: 4f1a17
      topRight: 913b3a
      bottomRight: 8d4633
      bottomLeft: 8d3839
    Genre:
      - id: 50944
        filter: genre=50944
        tag: 4k HDR
        count: 48
      - id: 50946
        filter: genre=50946
        tag: Dolby Atmos
        count: 38
      - id: 50945
        filter: genre=50945
        tag: Dolby Vision
        count: 21
      - id: 19
        filter: genre=19
        tag: Thriller
        count: 86
      - id: 21
        filter: genre=21
        tag: Action
        count: 230
      - id: 20
        filter: genre=20
        tag: Crime
        count: 49
      - id: 17
        filter: genre=17
        tag: Drama
        count: 128
    Country:
      - id: 87
        filter: country=87
        tag: United States of America
        count: 470
    Guid:
      - id: imdb://tt7888964
      - id: tmdb://615457
      - id: tvdb://133393
    Rating:
      - image: imdb://image.rating
        value: 7.4
        type: audience
        count: 501
      - image: rottentomatoes://image.rating.ripe
        value: 8.4
        type: critic
        count: 330
      - image: rottentomatoes://image.rating.upright
        value: 9.4
        type: audience
        count: 411
      - image: themoviedb://image.rating
        value: 7.9
        type: audience
        count: 508
    Director:
      - id: 3266
        filter: director=3266
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
    Writer:
      - id: 3267
        filter: writer=3267
        tag: Derek Kolstad
        tagKey: 5d776a8afb0d55001f54921f
        count: 4
        thumb: >-
          https://metadata-static.plex.tv/5/people/5c97a829e3651739f2971e4e2898682c.jpg
    Role:
      - id: 3268
        filter: actor=3268
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        count: 2
        role: Hutch Mansell
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3269
        filter: actor=3269
        tag: Aleksey Serebryakov
        tagKey: 5d77682b151a60001f24b98c
        role: Yulian Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b743f3f7a75e1b5bd937e2060753837.jpg
      - id: 3270
        filter: actor=3270
        tag: Connie Nielsen
        tagKey: 5d7768267228e5001f1dcdb5
        count: 4
        role: Becca Mansell
        thumb: >-
          https://metadata-static.plex.tv/3/people/328b075ecee9e20d7e22e95a72596edb.jpg
      - id: 3271
        filter: actor=3271
        tag: Christopher Lloyd
        tagKey: 5d7768244de0ee001fcc80bb
        count: 6
        role: David Mansell
        thumb: >-
          https://metadata-static.plex.tv/c/people/c2d2c2ab21e34db5837877ca386d43c3.jpg
      - id: 3272
        filter: actor=3272
        tag: Michael Ironside
        tagKey: 5d7768268718ba001e311c35
        count: 3
        role: Eddie Williams
        thumb: >-
          https://metadata-static.plex.tv/5/people/562560faf349fed1531898b075cfdf54.jpg
      - id: 3273
        filter: actor=3273
        tag: Colin Salmon
        tagKey: 5d776826880197001ec906c3
        role: The Barber
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05fd85a41289fbd0375c013fbb6593f.jpg
      - id: 3274
        filter: actor=3274
        tag: RZA
        tagKey: 5d77682985719b001f3a132f
        role: Harry Mansell
        thumb: >-
          https://metadata-static.plex.tv/9/people/97914947f71b47e35f9e0e708f6b6054.jpg
      - id: 3275
        filter: actor=3275
        tag: Billy MacLellan
        tagKey: 5d7768355af944001f1f9ddb
        role: Charlie Williams
        thumb: >-
          https://metadata-static.plex.tv/7/people/793801223b142f24e8455525db4f98b0.jpg
      - id: 3276
        filter: actor=3276
        tag: Araya Mengesha
        tagKey: 5d77687633f255001e8571ca
        role: Pavel
        thumb: >-
          https://metadata-static.plex.tv/0/people/0c5cf3bf1ba0fc04f5dfbfe7787419cd.jpg
      - id: 3277
        filter: actor=3277
        tag: Gage Munroe
        tagKey: 5d776843961905001eb96d28
        role: Brady Mansell
        thumb: >-
          https://metadata-static.plex.tv/0/people/07bdd3e7b5c9bf0151f67c6e986e546c.jpg
      - id: 3278
        filter: actor=3278
        tag: Paisley Cadorath
        tagKey: 5e166be52d4d84003e4bede2
        role: Sammy Mansell
        thumb: >-
          https://metadata-static.plex.tv/4/people/46fce2ea69eca54daeb8ef48e4fb788c.jpg
      - id: 3279
        filter: actor=3279
        tag: Aleksandr Pal
        tagKey: 5d776a28fb0d55001f53c11f
        role: Teddy Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/4/people/418db25e4856946a298e70440778a26a.jpg
      - id: 3280
        filter: actor=3280
        tag: Humberly González
        tagKey: 5d776c7cad5437001f7bf60d
        role: Lupita Martin
        thumb: >-
          https://metadata-static.plex.tv/9/people/9e0cf7073f9849cb8c6a17157c0cb1df.jpg
      - id: 3281
        filter: actor=3281
        tag: Edsson Morales
        tagKey: 5d776870eb5d26001f1eb87d
        role: Luis Martin
        thumb: >-
          https://metadata-static.plex.tv/2/people/270e11868a651c1f64e076871a0ebe09.jpg
      - id: 3282
        filter: actor=3282
        tag: J.P. Manoux
        tagKey: 5d776827103a2d001f56467f
        count: 3
        role: Pentagon Darren
        thumb: >-
          https://metadata-static.plex.tv/4/people/48d515df07e7954ad7bd291acba622d2.jpg
      - id: 3283
        filter: actor=3283
        tag: Adrian McLean
        tagKey: 5d776f5bad5437001f80fbb5
        role: Joey
        thumb: >-
          https://metadata-static.plex.tv/7/people/78e72df33a9979c71f376c23639ff4dd.jpg
      - id: 3284
        filter: actor=3284
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        role: Hitman Anatoly
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
      - id: 3285
        filter: actor=3285
        tag: Sergey Shnurov
        tagKey: 5d7768466f4521001ea9f873
        role: Hitman Valentin
        thumb: >-
          https://metadata-static.plex.tv/f/people/f78b732363a4c27c39078cf9dee79277.jpg
      - id: 3286
        filter: actor=3286
        tag: Joanne Rodriguez
        tagKey: 5d7768342ec6b5001f6bbd05
        role: Bus Driver Donna
        thumb: >-
          https://metadata-static.plex.tv/9/people/9cccffdd78a83dd849a4a41f7199f169.jpg
      - id: 3287
        filter: actor=3287
        tag: Stephanie Sy
        tagKey: 5d776d3d96b655001fe438e4
        role: Realtor
        thumb: https://metadata-static.plex.tv/people/5d776d3d96b655001fe438e4.jpg
      - id: 3288
        filter: actor=3288
        tag: Dan Rizzuto
        tagKey: 5d9f35b0b0262f001f6ec2de
        count: 2
        role: Gunman
      - id: 3289
        filter: actor=3289
        tag: Ruslan Rusin
        tagKey: 5d776d267a53e9001e752a5e
        role: Gunman
      - id: 3290
        filter: actor=3290
        tag: Vladimir Levkovsky
        tagKey: 60b90595f28049002d7ec8e2
        role: Gunman
      - id: 3291
        filter: actor=3291
        tag: Dan Skene
        tagKey: 5d77683c4de0ee001fccce80
        count: 2
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/9/people/9a3aae3a0a9c552d8c9dd651d6244f89.jpg
      - id: 3292
        filter: actor=3292
        tag: BJ Verot
        tagKey: 5d776ca79ab5440021519486
        role: Gunman
        thumb: https://metadata-static.plex.tv/people/5d776ca79ab5440021519486.jpg
      - id: 3293
        filter: actor=3293
        tag: Dylan Rampulla
        tagKey: 5e1647cd46aceb003cee8a84
        role: Gunman
      - id: 3294
        filter: actor=3294
        tag: Margaryta Soldatova
        tagKey: 5d776de696b655001fe5645f
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/2/people/2ef47acd293dd4e81ef6607c47af18aa.jpg
      - id: 3295
        filter: actor=3295
        tag: Megan Best
        tagKey: 5e166be52d4d84003e4bedde
        role: Woman on Bus
        thumb: >-
          https://metadata-static.plex.tv/d/people/d4ca27f2b660ae1fc76c8806b9b5a720.jpg
      - id: 3296
        filter: actor=3296
        tag: Darya Charusha
        tagKey: 5d7768bb374a5b001fece978
        role: Beta
        thumb: >-
          https://metadata-static.plex.tv/c/people/c503be6f3a83d9a3692d6c392679eb8e.jpg
      - id: 3297
        filter: actor=3297
        tag: Neil Davison
        tagKey: 5d9f3581adeb7a0021ce25ab
        role: Albert
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d1606a3ec7f8c775346b666d48aed59.jpg
      - id: 3298
        filter: actor=3298
        tag: Paul Essiembre
        tagKey: 5d77684f6f4521001eaa0e2c
        role: Jim the Neighbor
        thumb: >-
          https://metadata-static.plex.tv/1/people/143679603a8a9033feb9815d6a8eca29.jpg
      - id: 3299
        filter: actor=3299
        tag: Adam Hurtig
        tagKey: 5d7769e27a53e9001e6f36b4
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/c/people/cf6adb15c4d5a5ccd1dbe93fd684e807.jpg
      - id: 3300
        filter: actor=3300
        tag: Gabriel Daniels
        tagKey: 5d77689efb0d55001f5158ad
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/7/people/764cf91ca84fd8e24d10682acda85510.jpg
      - id: 3301
        filter: actor=3301
        tag: Kristen Harris
        tagKey: 5d7769ebfb0d55001f534779
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/8/people/8b82bda4aa071a57092c5e0bd82765e6.jpg
      - id: 3302
        filter: actor=3302
        tag: Erik Athavale
        tagKey: 5d776ab59ab54400215027c9
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/b/people/b0f12073fb6fa6f25213256a4493ebde.jpg
      - id: 3303
        filter: actor=3303
        tag: Tom Soares
        tagKey: 5f4059d8a4f07a00421717aa
        role: Alan Breiseth
      - id: 3304
        filter: actor=3304
        tag: Neven Pajkic
        tagKey: 5d7768256f4521001ea989ba
        role: Big Brute
        thumb: https://metadata-static.plex.tv/people/5d7768256f4521001ea989ba.jpg
      - id: 3305
        filter: actor=3305
        tag: Stephen Eric McIntyre
        tagKey: 5d776831151a60001f24d011
        role: Veteran
        thumb: >-
          https://metadata-static.plex.tv/5/people/556a233e543d87d4d3d1a2dc2630b4bb.jpg
      - id: 3306
        filter: actor=3306
        tag: Rick Dobran
        tagKey: 5d77684261141d001fb171ab
        count: 2
        role: Tattoo Shop Owner
        thumb: >-
          https://metadata-static.plex.tv/3/people/313b89fef7dd52cd49d6c78d0c1cb7e2.jpg
      - id: 3307
        filter: actor=3307
        tag: Richard Thomas
        tagKey: 64c10b5fdcb9af3bd1eee9e7
        role: Security Guard (Obshak Basement)
      - id: 3308
        filter: actor=3308
        tag: Alan Wh Wong
        tagKey: 66981d0bdcafced077160d19
        role: Doctor
      - id: 3309
        filter: actor=3309
        tag: Sharon Bajer
        tagKey: 5d776838151a60001f24e8fe
        role: Receptionist
        thumb: https://metadata-static.plex.tv/people/5d776838151a60001f24e8fe.jpg
      - id: 3310
        filter: actor=3310
        tag: Yulia Guzhva
        tagKey: 60b90596526b16002d6b1d25
        role: Karaoke Singer
      - id: 3311
        filter: actor=3311
        tag: Boris Gulyarin
        tagKey: 5d776d267a53e9001e752a57
        role: Mob Boss
        thumb: https://metadata-static.plex.tv/people/5d776d267a53e9001e752a57.jpg
      - id: 3312
        filter: actor=3312
        tag: Alex Nikolaychuk
        tagKey: 64c10b5f5b2d39db72ea18b4
        role: Mob Boss
      - id: 3313
        filter: actor=3313
        tag: Volodymyr Yamnenko
        tagKey: 5d776a5196b655001fdeac0c
        role: Mob Boss
        thumb: >-
          https://metadata-static.plex.tv/e/people/e00c1e06d5bd36b8afef7abadb3397a7.jpg
      - id: 3314
        filter: actor=3314
        tag: Meaghan Ann De Werrenne-Walle
        tagKey: 60b905965f7d3f002cb034d1
        role: Waitress (Karaoke Club)
      - id: 3315
        filter: actor=3315
        tag: Eugene Baffoe
        tagKey: 5ec419e0f8a5e90040cfaadb
        role: Barber's Guard
        thumb: >-
          https://metadata-static.plex.tv/0/people/08f07e73e74d04362ff80af43e27af9a.jpg
      - id: 3316
        filter: actor=3316
        tag: Daniel Bernhardt
        tagKey: 5d776828a091de001f2e6428
        count: 4
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/8/people/894ce74954806b4f55fac059f5af9bd9.jpg
      - id: 3317
        filter: actor=3317
        tag: Alain Moussi
        tagKey: 5d776b5096b655001fe0c5ab
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/5/people/5de5e70da005d9bcd84ee387ccd06079.jpg
      - id: 3318
        filter: actor=3318
        tag: Stéphane Julien
        tagKey: 5d776ac796b655001fdf93cc
        count: 2
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/c/people/c5501403d440b91a3c0d86cfe283523b.jpg
      - id: 3319
        filter: actor=3319
        tag: Robert Heinamaki
        tagKey: 60b90596b6a3c2002cb5df92
        role: Body Builder
      - id: 3320
        filter: actor=3320
        tag: Brent Alarie
        tagKey: 60b90596526b16002d6b1d27
        role: Tattoo Parlor
      - id: 66738
        filter: actor=66738
        tag: Tyrell Witherspoon
        tagKey: 6837cbc422219f2940060d8a
        role: Dancer
      - id: 3322
        filter: actor=3322
        tag: Frederick Allen
        tagKey: 5e166be52d4d84003e4bede0
        role: Russian Mafia Member (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/7/people/7904579927adae5ff33b8149870c5cf4.jpg
      - id: 3323
        filter: actor=3323
        tag: Destini Boldt
        tagKey: 64b018cffa119025f00aa26c
        role: Club Patron (uncredited)
    Producer:
      - id: 3324
        filter: producer=3324
        tag: David Leitch
        tagKey: 5d776828151a60001f24ae96
        count: 3
        thumb: >-
          https://metadata-static.plex.tv/4/people/4d935845dd16ac700054162203566edd.jpg
      - id: 3325
        filter: producer=3325
        tag: Kelly McCormick
        tagKey: 5d776b49fb0d55001f5629d7
        count: 2
        thumb: >-
          https://metadata-static.plex.tv/0/people/09afce317f35900bdcd7518664795277.jpg
      - id: 3326
        filter: producer=3326
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3327
        filter: producer=3327
        tag: Marc Provissiero
        tagKey: 5d776bb747dd6e001f6e242d
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b65cf07ae7032dd37dfe24ff0b00870.jpg
      - id: 66739
        filter: producer=66739
        tag: Braden Aftergood
        tagKey: 6839e0351aa1f166b353d040
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d5f88c6dbff24ede9bd423ea2fc0b95.jpg
    Field:
      - locked: true
        name: thumb
      - locked: true
        name: genre
```
## Movie Resume
##### Movie playback resumes.
```yaml
payload:
  event: media.pause
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: movie
    ratingKey: '73'
    key: /library/metadata/73
    guid: plex://movie/5e833bb566500c0041d29af9
    slug: nobody-2021
    studio: 87North Productions
    type: movie
    title: Nobody
    librarySectionTitle: Films
    librarySectionID: 6
    librarySectionKey: /library/sections/6
    contentRating: R
    summary: >-
      Hutch Mansell, a suburban dad, overlooked husband, nothing neighbor — a
      "nobody." When two thieves break into his home one night, Hutch's unknown
      long-simmering rage is ignited and propels him on a brutal path that will
      uncover dark secrets he fought to leave behind.
    rating: 8.4
    audienceRating: 9.4
    userRating: 10
    lastRatedAt: 1745785982
    year: 2021
    tagline: Never underestimate a nobody.
    thumb: /library/metadata/73/thumb/1749091611
    art: /library/metadata/73/art/1749091611
    duration: 5460000
    originallyAvailableAt: '2021-03-18'
    addedAt: 1733008519
    updatedAt: 1749091611
    audienceRatingImage: rottentomatoes://image.rating.upright
    chapterSource: media
    primaryExtraKey: /library/metadata/82
    ratingImage: rottentomatoes://image.rating.ripe
    Image:
      - alt: Nobody
        type: coverPoster
        url: /library/metadata/73/thumb/1749091611
      - alt: Nobody
        type: background
        url: /library/metadata/73/art/1749091611
      - alt: Nobody
        type: clearLogo
        url: /library/metadata/73/clearLogo/1749091611
    UltraBlurColors:
      topLeft: 4f1a17
      topRight: 913b3a
      bottomRight: 8d4633
      bottomLeft: 8d3839
    Genre:
      - id: 50944
        filter: genre=50944
        tag: 4k HDR
        count: 48
      - id: 50946
        filter: genre=50946
        tag: Dolby Atmos
        count: 38
      - id: 50945
        filter: genre=50945
        tag: Dolby Vision
        count: 21
      - id: 19
        filter: genre=19
        tag: Thriller
        count: 86
      - id: 21
        filter: genre=21
        tag: Action
        count: 230
      - id: 20
        filter: genre=20
        tag: Crime
        count: 49
      - id: 17
        filter: genre=17
        tag: Drama
        count: 128
    Country:
      - id: 87
        filter: country=87
        tag: United States of America
        count: 470
    Guid:
      - id: imdb://tt7888964
      - id: tmdb://615457
      - id: tvdb://133393
    Rating:
      - image: imdb://image.rating
        value: 7.4
        type: audience
        count: 501
      - image: rottentomatoes://image.rating.ripe
        value: 8.4
        type: critic
        count: 330
      - image: rottentomatoes://image.rating.upright
        value: 9.4
        type: audience
        count: 411
      - image: themoviedb://image.rating
        value: 7.9
        type: audience
        count: 508
    Director:
      - id: 3266
        filter: director=3266
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
    Writer:
      - id: 3267
        filter: writer=3267
        tag: Derek Kolstad
        tagKey: 5d776a8afb0d55001f54921f
        count: 4
        thumb: >-
          https://metadata-static.plex.tv/5/people/5c97a829e3651739f2971e4e2898682c.jpg
    Role:
      - id: 3268
        filter: actor=3268
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        count: 2
        role: Hutch Mansell
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3269
        filter: actor=3269
        tag: Aleksey Serebryakov
        tagKey: 5d77682b151a60001f24b98c
        role: Yulian Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b743f3f7a75e1b5bd937e2060753837.jpg
      - id: 3270
        filter: actor=3270
        tag: Connie Nielsen
        tagKey: 5d7768267228e5001f1dcdb5
        count: 4
        role: Becca Mansell
        thumb: >-
          https://metadata-static.plex.tv/3/people/328b075ecee9e20d7e22e95a72596edb.jpg
      - id: 3271
        filter: actor=3271
        tag: Christopher Lloyd
        tagKey: 5d7768244de0ee001fcc80bb
        count: 6
        role: David Mansell
        thumb: >-
          https://metadata-static.plex.tv/c/people/c2d2c2ab21e34db5837877ca386d43c3.jpg
      - id: 3272
        filter: actor=3272
        tag: Michael Ironside
        tagKey: 5d7768268718ba001e311c35
        count: 3
        role: Eddie Williams
        thumb: >-
          https://metadata-static.plex.tv/5/people/562560faf349fed1531898b075cfdf54.jpg
      - id: 3273
        filter: actor=3273
        tag: Colin Salmon
        tagKey: 5d776826880197001ec906c3
        role: The Barber
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05fd85a41289fbd0375c013fbb6593f.jpg
      - id: 3274
        filter: actor=3274
        tag: RZA
        tagKey: 5d77682985719b001f3a132f
        role: Harry Mansell
        thumb: >-
          https://metadata-static.plex.tv/9/people/97914947f71b47e35f9e0e708f6b6054.jpg
      - id: 3275
        filter: actor=3275
        tag: Billy MacLellan
        tagKey: 5d7768355af944001f1f9ddb
        role: Charlie Williams
        thumb: >-
          https://metadata-static.plex.tv/7/people/793801223b142f24e8455525db4f98b0.jpg
      - id: 3276
        filter: actor=3276
        tag: Araya Mengesha
        tagKey: 5d77687633f255001e8571ca
        role: Pavel
        thumb: >-
          https://metadata-static.plex.tv/0/people/0c5cf3bf1ba0fc04f5dfbfe7787419cd.jpg
      - id: 3277
        filter: actor=3277
        tag: Gage Munroe
        tagKey: 5d776843961905001eb96d28
        role: Brady Mansell
        thumb: >-
          https://metadata-static.plex.tv/0/people/07bdd3e7b5c9bf0151f67c6e986e546c.jpg
      - id: 3278
        filter: actor=3278
        tag: Paisley Cadorath
        tagKey: 5e166be52d4d84003e4bede2
        role: Sammy Mansell
        thumb: >-
          https://metadata-static.plex.tv/4/people/46fce2ea69eca54daeb8ef48e4fb788c.jpg
      - id: 3279
        filter: actor=3279
        tag: Aleksandr Pal
        tagKey: 5d776a28fb0d55001f53c11f
        role: Teddy Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/4/people/418db25e4856946a298e70440778a26a.jpg
      - id: 3280
        filter: actor=3280
        tag: Humberly González
        tagKey: 5d776c7cad5437001f7bf60d
        role: Lupita Martin
        thumb: >-
          https://metadata-static.plex.tv/9/people/9e0cf7073f9849cb8c6a17157c0cb1df.jpg
      - id: 3281
        filter: actor=3281
        tag: Edsson Morales
        tagKey: 5d776870eb5d26001f1eb87d
        role: Luis Martin
        thumb: >-
          https://metadata-static.plex.tv/2/people/270e11868a651c1f64e076871a0ebe09.jpg
      - id: 3282
        filter: actor=3282
        tag: J.P. Manoux
        tagKey: 5d776827103a2d001f56467f
        count: 3
        role: Pentagon Darren
        thumb: >-
          https://metadata-static.plex.tv/4/people/48d515df07e7954ad7bd291acba622d2.jpg
      - id: 3283
        filter: actor=3283
        tag: Adrian McLean
        tagKey: 5d776f5bad5437001f80fbb5
        role: Joey
        thumb: >-
          https://metadata-static.plex.tv/7/people/78e72df33a9979c71f376c23639ff4dd.jpg
      - id: 3284
        filter: actor=3284
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        role: Hitman Anatoly
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
      - id: 3285
        filter: actor=3285
        tag: Sergey Shnurov
        tagKey: 5d7768466f4521001ea9f873
        role: Hitman Valentin
        thumb: >-
          https://metadata-static.plex.tv/f/people/f78b732363a4c27c39078cf9dee79277.jpg
      - id: 3286
        filter: actor=3286
        tag: Joanne Rodriguez
        tagKey: 5d7768342ec6b5001f6bbd05
        role: Bus Driver Donna
        thumb: >-
          https://metadata-static.plex.tv/9/people/9cccffdd78a83dd849a4a41f7199f169.jpg
      - id: 3287
        filter: actor=3287
        tag: Stephanie Sy
        tagKey: 5d776d3d96b655001fe438e4
        role: Realtor
        thumb: https://metadata-static.plex.tv/people/5d776d3d96b655001fe438e4.jpg
      - id: 3288
        filter: actor=3288
        tag: Dan Rizzuto
        tagKey: 5d9f35b0b0262f001f6ec2de
        count: 2
        role: Gunman
      - id: 3289
        filter: actor=3289
        tag: Ruslan Rusin
        tagKey: 5d776d267a53e9001e752a5e
        role: Gunman
      - id: 3290
        filter: actor=3290
        tag: Vladimir Levkovsky
        tagKey: 60b90595f28049002d7ec8e2
        role: Gunman
      - id: 3291
        filter: actor=3291
        tag: Dan Skene
        tagKey: 5d77683c4de0ee001fccce80
        count: 2
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/9/people/9a3aae3a0a9c552d8c9dd651d6244f89.jpg
      - id: 3292
        filter: actor=3292
        tag: BJ Verot
        tagKey: 5d776ca79ab5440021519486
        role: Gunman
        thumb: https://metadata-static.plex.tv/people/5d776ca79ab5440021519486.jpg
      - id: 3293
        filter: actor=3293
        tag: Dylan Rampulla
        tagKey: 5e1647cd46aceb003cee8a84
        role: Gunman
      - id: 3294
        filter: actor=3294
        tag: Margaryta Soldatova
        tagKey: 5d776de696b655001fe5645f
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/2/people/2ef47acd293dd4e81ef6607c47af18aa.jpg
      - id: 3295
        filter: actor=3295
        tag: Megan Best
        tagKey: 5e166be52d4d84003e4bedde
        role: Woman on Bus
        thumb: >-
          https://metadata-static.plex.tv/d/people/d4ca27f2b660ae1fc76c8806b9b5a720.jpg
      - id: 3296
        filter: actor=3296
        tag: Darya Charusha
        tagKey: 5d7768bb374a5b001fece978
        role: Beta
        thumb: >-
          https://metadata-static.plex.tv/c/people/c503be6f3a83d9a3692d6c392679eb8e.jpg
      - id: 3297
        filter: actor=3297
        tag: Neil Davison
        tagKey: 5d9f3581adeb7a0021ce25ab
        role: Albert
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d1606a3ec7f8c775346b666d48aed59.jpg
      - id: 3298
        filter: actor=3298
        tag: Paul Essiembre
        tagKey: 5d77684f6f4521001eaa0e2c
        role: Jim the Neighbor
        thumb: >-
          https://metadata-static.plex.tv/1/people/143679603a8a9033feb9815d6a8eca29.jpg
      - id: 3299
        filter: actor=3299
        tag: Adam Hurtig
        tagKey: 5d7769e27a53e9001e6f36b4
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/c/people/cf6adb15c4d5a5ccd1dbe93fd684e807.jpg
      - id: 3300
        filter: actor=3300
        tag: Gabriel Daniels
        tagKey: 5d77689efb0d55001f5158ad
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/7/people/764cf91ca84fd8e24d10682acda85510.jpg
      - id: 3301
        filter: actor=3301
        tag: Kristen Harris
        tagKey: 5d7769ebfb0d55001f534779
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/8/people/8b82bda4aa071a57092c5e0bd82765e6.jpg
      - id: 3302
        filter: actor=3302
        tag: Erik Athavale
        tagKey: 5d776ab59ab54400215027c9
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/b/people/b0f12073fb6fa6f25213256a4493ebde.jpg
      - id: 3303
        filter: actor=3303
        tag: Tom Soares
        tagKey: 5f4059d8a4f07a00421717aa
        role: Alan Breiseth
      - id: 3304
        filter: actor=3304
        tag: Neven Pajkic
        tagKey: 5d7768256f4521001ea989ba
        role: Big Brute
        thumb: https://metadata-static.plex.tv/people/5d7768256f4521001ea989ba.jpg
      - id: 3305
        filter: actor=3305
        tag: Stephen Eric McIntyre
        tagKey: 5d776831151a60001f24d011
        role: Veteran
        thumb: >-
          https://metadata-static.plex.tv/5/people/556a233e543d87d4d3d1a2dc2630b4bb.jpg
      - id: 3306
        filter: actor=3306
        tag: Rick Dobran
        tagKey: 5d77684261141d001fb171ab
        count: 2
        role: Tattoo Shop Owner
        thumb: >-
          https://metadata-static.plex.tv/3/people/313b89fef7dd52cd49d6c78d0c1cb7e2.jpg
      - id: 3307
        filter: actor=3307
        tag: Richard Thomas
        tagKey: 64c10b5fdcb9af3bd1eee9e7
        role: Security Guard (Obshak Basement)
      - id: 3308
        filter: actor=3308
        tag: Alan Wh Wong
        tagKey: 66981d0bdcafced077160d19
        role: Doctor
      - id: 3309
        filter: actor=3309
        tag: Sharon Bajer
        tagKey: 5d776838151a60001f24e8fe
        role: Receptionist
        thumb: https://metadata-static.plex.tv/people/5d776838151a60001f24e8fe.jpg
      - id: 3310
        filter: actor=3310
        tag: Yulia Guzhva
        tagKey: 60b90596526b16002d6b1d25
        role: Karaoke Singer
      - id: 3311
        filter: actor=3311
        tag: Boris Gulyarin
        tagKey: 5d776d267a53e9001e752a57
        role: Mob Boss
        thumb: https://metadata-static.plex.tv/people/5d776d267a53e9001e752a57.jpg
      - id: 3312
        filter: actor=3312
        tag: Alex Nikolaychuk
        tagKey: 64c10b5f5b2d39db72ea18b4
        role: Mob Boss
      - id: 3313
        filter: actor=3313
        tag: Volodymyr Yamnenko
        tagKey: 5d776a5196b655001fdeac0c
        role: Mob Boss
        thumb: >-
          https://metadata-static.plex.tv/e/people/e00c1e06d5bd36b8afef7abadb3397a7.jpg
      - id: 3314
        filter: actor=3314
        tag: Meaghan Ann De Werrenne-Walle
        tagKey: 60b905965f7d3f002cb034d1
        role: Waitress (Karaoke Club)
      - id: 3315
        filter: actor=3315
        tag: Eugene Baffoe
        tagKey: 5ec419e0f8a5e90040cfaadb
        role: Barber's Guard
        thumb: >-
          https://metadata-static.plex.tv/0/people/08f07e73e74d04362ff80af43e27af9a.jpg
      - id: 3316
        filter: actor=3316
        tag: Daniel Bernhardt
        tagKey: 5d776828a091de001f2e6428
        count: 4
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/8/people/894ce74954806b4f55fac059f5af9bd9.jpg
      - id: 3317
        filter: actor=3317
        tag: Alain Moussi
        tagKey: 5d776b5096b655001fe0c5ab
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/5/people/5de5e70da005d9bcd84ee387ccd06079.jpg
      - id: 3318
        filter: actor=3318
        tag: Stéphane Julien
        tagKey: 5d776ac796b655001fdf93cc
        count: 2
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/c/people/c5501403d440b91a3c0d86cfe283523b.jpg
      - id: 3319
        filter: actor=3319
        tag: Robert Heinamaki
        tagKey: 60b90596b6a3c2002cb5df92
        role: Body Builder
      - id: 3320
        filter: actor=3320
        tag: Brent Alarie
        tagKey: 60b90596526b16002d6b1d27
        role: Tattoo Parlor
      - id: 66738
        filter: actor=66738
        tag: Tyrell Witherspoon
        tagKey: 6837cbc422219f2940060d8a
        role: Dancer
      - id: 3322
        filter: actor=3322
        tag: Frederick Allen
        tagKey: 5e166be52d4d84003e4bede0
        role: Russian Mafia Member (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/7/people/7904579927adae5ff33b8149870c5cf4.jpg
      - id: 3323
        filter: actor=3323
        tag: Destini Boldt
        tagKey: 64b018cffa119025f00aa26c
        role: Club Patron (uncredited)
    Producer:
      - id: 3324
        filter: producer=3324
        tag: David Leitch
        tagKey: 5d776828151a60001f24ae96
        count: 3
        thumb: >-
          https://metadata-static.plex.tv/4/people/4d935845dd16ac700054162203566edd.jpg
      - id: 3325
        filter: producer=3325
        tag: Kelly McCormick
        tagKey: 5d776b49fb0d55001f5629d7
        count: 2
        thumb: >-
          https://metadata-static.plex.tv/0/people/09afce317f35900bdcd7518664795277.jpg
      - id: 3326
        filter: producer=3326
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3327
        filter: producer=3327
        tag: Marc Provissiero
        tagKey: 5d776bb747dd6e001f6e242d
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b65cf07ae7032dd37dfe24ff0b00870.jpg
      - id: 66739
        filter: producer=66739
        tag: Braden Aftergood
        tagKey: 6839e0351aa1f166b353d040
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d5f88c6dbff24ede9bd423ea2fc0b95.jpg
    Field:
      - locked: true
        name: thumb
      - locked: true
        name: genre
```
## Movie Scrobble
##### Movie is viewed (played past the 90% mark).
```yaml
payload:
  event: media.scrobble
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: movie
    ratingKey: '73'
    key: /library/metadata/73
    guid: plex://movie/5e833bb566500c0041d29af9
    slug: nobody-2021
    studio: 87North Productions
    type: movie
    title: Nobody
    librarySectionTitle: Films
    librarySectionID: 6
    librarySectionKey: /library/sections/6
    contentRating: R
    summary: >-
      Hutch Mansell, a suburban dad, overlooked husband, nothing neighbor — a
      "nobody." When two thieves break into his home one night, Hutch's unknown
      long-simmering rage is ignited and propels him on a brutal path that will
      uncover dark secrets he fought to leave behind.
    rating: 8.4
    audienceRating: 9.4
    userRating: 9
    viewCount: 1
    skipCount: 1
    lastViewedAt: 1749683081
    lastRatedAt: 1749682611
    year: 2021
    tagline: Never underestimate a nobody.
    thumb: /library/metadata/73/thumb/1749091611
    art: /library/metadata/73/art/1749091611
    duration: 5460000
    originallyAvailableAt: '2021-03-18'
    addedAt: 1733008519
    updatedAt: 1749091611
    audienceRatingImage: rottentomatoes://image.rating.upright
    chapterSource: media
    primaryExtraKey: /library/metadata/82
    ratingImage: rottentomatoes://image.rating.ripe
    Image:
      - alt: Nobody
        type: coverPoster
        url: /library/metadata/73/thumb/1749091611
      - alt: Nobody
        type: background
        url: /library/metadata/73/art/1749091611
      - alt: Nobody
        type: clearLogo
        url: /library/metadata/73/clearLogo/1749091611
    UltraBlurColors:
      topLeft: 4f1a17
      topRight: 913b3a
      bottomRight: 8d4633
      bottomLeft: 8d3839
    Genre:
      - id: 50944
        filter: genre=50944
        tag: 4k HDR
        count: 48
      - id: 50946
        filter: genre=50946
        tag: Dolby Atmos
        count: 38
      - id: 50945
        filter: genre=50945
        tag: Dolby Vision
        count: 21
      - id: 19
        filter: genre=19
        tag: Thriller
        count: 86
      - id: 21
        filter: genre=21
        tag: Action
        count: 230
      - id: 20
        filter: genre=20
        tag: Crime
        count: 49
      - id: 17
        filter: genre=17
        tag: Drama
        count: 128
    Country:
      - id: 87
        filter: country=87
        tag: United States of America
        count: 470
    Guid:
      - id: imdb://tt7888964
      - id: tmdb://615457
      - id: tvdb://133393
    Rating:
      - image: imdb://image.rating
        value: 7.4
        type: audience
        count: 501
      - image: rottentomatoes://image.rating.ripe
        value: 8.4
        type: critic
        count: 330
      - image: rottentomatoes://image.rating.upright
        value: 9.4
        type: audience
        count: 411
      - image: themoviedb://image.rating
        value: 7.9
        type: audience
        count: 508
    Director:
      - id: 3266
        filter: director=3266
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
    Writer:
      - id: 3267
        filter: writer=3267
        tag: Derek Kolstad
        tagKey: 5d776a8afb0d55001f54921f
        count: 4
        thumb: >-
          https://metadata-static.plex.tv/5/people/5c97a829e3651739f2971e4e2898682c.jpg
    Role:
      - id: 3268
        filter: actor=3268
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        count: 2
        role: Hutch Mansell
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3269
        filter: actor=3269
        tag: Aleksey Serebryakov
        tagKey: 5d77682b151a60001f24b98c
        role: Yulian Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b743f3f7a75e1b5bd937e2060753837.jpg
      - id: 3270
        filter: actor=3270
        tag: Connie Nielsen
        tagKey: 5d7768267228e5001f1dcdb5
        count: 4
        role: Becca Mansell
        thumb: >-
          https://metadata-static.plex.tv/3/people/328b075ecee9e20d7e22e95a72596edb.jpg
      - id: 3271
        filter: actor=3271
        tag: Christopher Lloyd
        tagKey: 5d7768244de0ee001fcc80bb
        count: 6
        role: David Mansell
        thumb: >-
          https://metadata-static.plex.tv/c/people/c2d2c2ab21e34db5837877ca386d43c3.jpg
      - id: 3272
        filter: actor=3272
        tag: Michael Ironside
        tagKey: 5d7768268718ba001e311c35
        count: 3
        role: Eddie Williams
        thumb: >-
          https://metadata-static.plex.tv/5/people/562560faf349fed1531898b075cfdf54.jpg
      - id: 3273
        filter: actor=3273
        tag: Colin Salmon
        tagKey: 5d776826880197001ec906c3
        role: The Barber
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05fd85a41289fbd0375c013fbb6593f.jpg
      - id: 3274
        filter: actor=3274
        tag: RZA
        tagKey: 5d77682985719b001f3a132f
        role: Harry Mansell
        thumb: >-
          https://metadata-static.plex.tv/9/people/97914947f71b47e35f9e0e708f6b6054.jpg
      - id: 3275
        filter: actor=3275
        tag: Billy MacLellan
        tagKey: 5d7768355af944001f1f9ddb
        role: Charlie Williams
        thumb: >-
          https://metadata-static.plex.tv/7/people/793801223b142f24e8455525db4f98b0.jpg
      - id: 3276
        filter: actor=3276
        tag: Araya Mengesha
        tagKey: 5d77687633f255001e8571ca
        role: Pavel
        thumb: >-
          https://metadata-static.plex.tv/0/people/0c5cf3bf1ba0fc04f5dfbfe7787419cd.jpg
      - id: 3277
        filter: actor=3277
        tag: Gage Munroe
        tagKey: 5d776843961905001eb96d28
        role: Brady Mansell
        thumb: >-
          https://metadata-static.plex.tv/0/people/07bdd3e7b5c9bf0151f67c6e986e546c.jpg
      - id: 3278
        filter: actor=3278
        tag: Paisley Cadorath
        tagKey: 5e166be52d4d84003e4bede2
        role: Sammy Mansell
        thumb: >-
          https://metadata-static.plex.tv/4/people/46fce2ea69eca54daeb8ef48e4fb788c.jpg
      - id: 3279
        filter: actor=3279
        tag: Aleksandr Pal
        tagKey: 5d776a28fb0d55001f53c11f
        role: Teddy Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/4/people/418db25e4856946a298e70440778a26a.jpg
      - id: 3280
        filter: actor=3280
        tag: Humberly González
        tagKey: 5d776c7cad5437001f7bf60d
        role: Lupita Martin
        thumb: >-
          https://metadata-static.plex.tv/9/people/9e0cf7073f9849cb8c6a17157c0cb1df.jpg
      - id: 3281
        filter: actor=3281
        tag: Edsson Morales
        tagKey: 5d776870eb5d26001f1eb87d
        role: Luis Martin
        thumb: >-
          https://metadata-static.plex.tv/2/people/270e11868a651c1f64e076871a0ebe09.jpg
      - id: 3282
        filter: actor=3282
        tag: J.P. Manoux
        tagKey: 5d776827103a2d001f56467f
        count: 3
        role: Pentagon Darren
        thumb: >-
          https://metadata-static.plex.tv/4/people/48d515df07e7954ad7bd291acba622d2.jpg
      - id: 3283
        filter: actor=3283
        tag: Adrian McLean
        tagKey: 5d776f5bad5437001f80fbb5
        role: Joey
        thumb: >-
          https://metadata-static.plex.tv/7/people/78e72df33a9979c71f376c23639ff4dd.jpg
      - id: 3284
        filter: actor=3284
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        role: Hitman Anatoly
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
      - id: 3285
        filter: actor=3285
        tag: Sergey Shnurov
        tagKey: 5d7768466f4521001ea9f873
        role: Hitman Valentin
        thumb: >-
          https://metadata-static.plex.tv/f/people/f78b732363a4c27c39078cf9dee79277.jpg
      - id: 3286
        filter: actor=3286
        tag: Joanne Rodriguez
        tagKey: 5d7768342ec6b5001f6bbd05
        role: Bus Driver Donna
        thumb: >-
          https://metadata-static.plex.tv/9/people/9cccffdd78a83dd849a4a41f7199f169.jpg
      - id: 3287
        filter: actor=3287
        tag: Stephanie Sy
        tagKey: 5d776d3d96b655001fe438e4
        role: Realtor
        thumb: https://metadata-static.plex.tv/people/5d776d3d96b655001fe438e4.jpg
      - id: 3288
        filter: actor=3288
        tag: Dan Rizzuto
        tagKey: 5d9f35b0b0262f001f6ec2de
        count: 2
        role: Gunman
      - id: 3289
        filter: actor=3289
        tag: Ruslan Rusin
        tagKey: 5d776d267a53e9001e752a5e
        role: Gunman
      - id: 3290
        filter: actor=3290
        tag: Vladimir Levkovsky
        tagKey: 60b90595f28049002d7ec8e2
        role: Gunman
      - id: 3291
        filter: actor=3291
        tag: Dan Skene
        tagKey: 5d77683c4de0ee001fccce80
        count: 2
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/9/people/9a3aae3a0a9c552d8c9dd651d6244f89.jpg
      - id: 3292
        filter: actor=3292
        tag: BJ Verot
        tagKey: 5d776ca79ab5440021519486
        role: Gunman
        thumb: https://metadata-static.plex.tv/people/5d776ca79ab5440021519486.jpg
      - id: 3293
        filter: actor=3293
        tag: Dylan Rampulla
        tagKey: 5e1647cd46aceb003cee8a84
        role: Gunman
      - id: 3294
        filter: actor=3294
        tag: Margaryta Soldatova
        tagKey: 5d776de696b655001fe5645f
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/2/people/2ef47acd293dd4e81ef6607c47af18aa.jpg
      - id: 3295
        filter: actor=3295
        tag: Megan Best
        tagKey: 5e166be52d4d84003e4bedde
        role: Woman on Bus
        thumb: >-
          https://metadata-static.plex.tv/d/people/d4ca27f2b660ae1fc76c8806b9b5a720.jpg
      - id: 3296
        filter: actor=3296
        tag: Darya Charusha
        tagKey: 5d7768bb374a5b001fece978
        role: Beta
        thumb: >-
          https://metadata-static.plex.tv/c/people/c503be6f3a83d9a3692d6c392679eb8e.jpg
      - id: 3297
        filter: actor=3297
        tag: Neil Davison
        tagKey: 5d9f3581adeb7a0021ce25ab
        role: Albert
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d1606a3ec7f8c775346b666d48aed59.jpg
      - id: 3298
        filter: actor=3298
        tag: Paul Essiembre
        tagKey: 5d77684f6f4521001eaa0e2c
        role: Jim the Neighbor
        thumb: >-
          https://metadata-static.plex.tv/1/people/143679603a8a9033feb9815d6a8eca29.jpg
      - id: 3299
        filter: actor=3299
        tag: Adam Hurtig
        tagKey: 5d7769e27a53e9001e6f36b4
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/c/people/cf6adb15c4d5a5ccd1dbe93fd684e807.jpg
      - id: 3300
        filter: actor=3300
        tag: Gabriel Daniels
        tagKey: 5d77689efb0d55001f5158ad
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/7/people/764cf91ca84fd8e24d10682acda85510.jpg
      - id: 3301
        filter: actor=3301
        tag: Kristen Harris
        tagKey: 5d7769ebfb0d55001f534779
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/8/people/8b82bda4aa071a57092c5e0bd82765e6.jpg
      - id: 3302
        filter: actor=3302
        tag: Erik Athavale
        tagKey: 5d776ab59ab54400215027c9
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/b/people/b0f12073fb6fa6f25213256a4493ebde.jpg
      - id: 3303
        filter: actor=3303
        tag: Tom Soares
        tagKey: 5f4059d8a4f07a00421717aa
        role: Alan Breiseth
      - id: 3304
        filter: actor=3304
        tag: Neven Pajkic
        tagKey: 5d7768256f4521001ea989ba
        role: Big Brute
        thumb: https://metadata-static.plex.tv/people/5d7768256f4521001ea989ba.jpg
      - id: 3305
        filter: actor=3305
        tag: Stephen Eric McIntyre
        tagKey: 5d776831151a60001f24d011
        role: Veteran
        thumb: >-
          https://metadata-static.plex.tv/5/people/556a233e543d87d4d3d1a2dc2630b4bb.jpg
      - id: 3306
        filter: actor=3306
        tag: Rick Dobran
        tagKey: 5d77684261141d001fb171ab
        count: 2
        role: Tattoo Shop Owner
        thumb: >-
          https://metadata-static.plex.tv/3/people/313b89fef7dd52cd49d6c78d0c1cb7e2.jpg
      - id: 3307
        filter: actor=3307
        tag: Richard Thomas
        tagKey: 64c10b5fdcb9af3bd1eee9e7
        role: Security Guard (Obshak Basement)
      - id: 3308
        filter: actor=3308
        tag: Alan Wh Wong
        tagKey: 66981d0bdcafced077160d19
        role: Doctor
      - id: 3309
        filter: actor=3309
        tag: Sharon Bajer
        tagKey: 5d776838151a60001f24e8fe
        role: Receptionist
        thumb: https://metadata-static.plex.tv/people/5d776838151a60001f24e8fe.jpg
      - id: 3310
        filter: actor=3310
        tag: Yulia Guzhva
        tagKey: 60b90596526b16002d6b1d25
        role: Karaoke Singer
      - id: 3311
        filter: actor=3311
        tag: Boris Gulyarin
        tagKey: 5d776d267a53e9001e752a57
        role: Mob Boss
        thumb: https://metadata-static.plex.tv/people/5d776d267a53e9001e752a57.jpg
      - id: 3312
        filter: actor=3312
        tag: Alex Nikolaychuk
        tagKey: 64c10b5f5b2d39db72ea18b4
        role: Mob Boss
      - id: 3313
        filter: actor=3313
        tag: Volodymyr Yamnenko
        tagKey: 5d776a5196b655001fdeac0c
        role: Mob Boss
        thumb: >-
          https://metadata-static.plex.tv/e/people/e00c1e06d5bd36b8afef7abadb3397a7.jpg
      - id: 3314
        filter: actor=3314
        tag: Meaghan Ann De Werrenne-Walle
        tagKey: 60b905965f7d3f002cb034d1
        role: Waitress (Karaoke Club)
      - id: 3315
        filter: actor=3315
        tag: Eugene Baffoe
        tagKey: 5ec419e0f8a5e90040cfaadb
        role: Barber's Guard
        thumb: >-
          https://metadata-static.plex.tv/0/people/08f07e73e74d04362ff80af43e27af9a.jpg
      - id: 3316
        filter: actor=3316
        tag: Daniel Bernhardt
        tagKey: 5d776828a091de001f2e6428
        count: 4
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/8/people/894ce74954806b4f55fac059f5af9bd9.jpg
      - id: 3317
        filter: actor=3317
        tag: Alain Moussi
        tagKey: 5d776b5096b655001fe0c5ab
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/5/people/5de5e70da005d9bcd84ee387ccd06079.jpg
      - id: 3318
        filter: actor=3318
        tag: Stéphane Julien
        tagKey: 5d776ac796b655001fdf93cc
        count: 2
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/c/people/c5501403d440b91a3c0d86cfe283523b.jpg
      - id: 3319
        filter: actor=3319
        tag: Robert Heinamaki
        tagKey: 60b90596b6a3c2002cb5df92
        role: Body Builder
      - id: 3320
        filter: actor=3320
        tag: Brent Alarie
        tagKey: 60b90596526b16002d6b1d27
        role: Tattoo Parlor
      - id: 66738
        filter: actor=66738
        tag: Tyrell Witherspoon
        tagKey: 6837cbc422219f2940060d8a
        role: Dancer
      - id: 3322
        filter: actor=3322
        tag: Frederick Allen
        tagKey: 5e166be52d4d84003e4bede0
        role: Russian Mafia Member (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/7/people/7904579927adae5ff33b8149870c5cf4.jpg
      - id: 3323
        filter: actor=3323
        tag: Destini Boldt
        tagKey: 64b018cffa119025f00aa26c
        role: Club Patron (uncredited)
    Producer:
      - id: 3324
        filter: producer=3324
        tag: David Leitch
        tagKey: 5d776828151a60001f24ae96
        count: 3
        thumb: >-
          https://metadata-static.plex.tv/4/people/4d935845dd16ac700054162203566edd.jpg
      - id: 3325
        filter: producer=3325
        tag: Kelly McCormick
        tagKey: 5d776b49fb0d55001f5629d7
        count: 2
        thumb: >-
          https://metadata-static.plex.tv/0/people/09afce317f35900bdcd7518664795277.jpg
      - id: 3326
        filter: producer=3326
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3327
        filter: producer=3327
        tag: Marc Provissiero
        tagKey: 5d776bb747dd6e001f6e242d
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b65cf07ae7032dd37dfe24ff0b00870.jpg
      - id: 66739
        filter: producer=66739
        tag: Braden Aftergood
        tagKey: 6839e0351aa1f166b353d040
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d5f88c6dbff24ede9bd423ea2fc0b95.jpg
    Field:
      - locked: true
        name: thumb
      - locked: true
        name: genre
```
## Movie Stop
##### Movie playback stops.
```yaml
payload:
  event: media.play
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: movie
    ratingKey: '73'
    key: /library/metadata/73
    guid: plex://movie/5e833bb566500c0041d29af9
    slug: nobody-2021
    studio: 87North Productions
    type: movie
    title: Nobody
    librarySectionTitle: Films
    librarySectionID: 6
    librarySectionKey: /library/sections/6
    contentRating: R
    summary: >-
      Hutch Mansell, a suburban dad, overlooked husband, nothing neighbor — a
      "nobody." When two thieves break into his home one night, Hutch's unknown
      long-simmering rage is ignited and propels him on a brutal path that will
      uncover dark secrets he fought to leave behind.
    rating: 8.4
    audienceRating: 9.4
    userRating: 10
    lastRatedAt: 1745785982
    year: 2021
    tagline: Never underestimate a nobody.
    thumb: /library/metadata/73/thumb/1749091611
    art: /library/metadata/73/art/1749091611
    duration: 5460000
    originallyAvailableAt: '2021-03-18'
    addedAt: 1733008519
    updatedAt: 1749091611
    audienceRatingImage: rottentomatoes://image.rating.upright
    chapterSource: media
    primaryExtraKey: /library/metadata/82
    ratingImage: rottentomatoes://image.rating.ripe
    Image:
      - alt: Nobody
        type: coverPoster
        url: /library/metadata/73/thumb/1749091611
      - alt: Nobody
        type: background
        url: /library/metadata/73/art/1749091611
      - alt: Nobody
        type: clearLogo
        url: /library/metadata/73/clearLogo/1749091611
    UltraBlurColors:
      topLeft: 4f1a17
      topRight: 913b3a
      bottomRight: 8d4633
      bottomLeft: 8d3839
    Genre:
      - id: 50944
        filter: genre=50944
        tag: 4k HDR
        count: 48
      - id: 50946
        filter: genre=50946
        tag: Dolby Atmos
        count: 38
      - id: 50945
        filter: genre=50945
        tag: Dolby Vision
        count: 21
      - id: 19
        filter: genre=19
        tag: Thriller
        count: 86
      - id: 21
        filter: genre=21
        tag: Action
        count: 230
      - id: 20
        filter: genre=20
        tag: Crime
        count: 49
      - id: 17
        filter: genre=17
        tag: Drama
        count: 128
    Country:
      - id: 87
        filter: country=87
        tag: United States of America
        count: 470
    Guid:
      - id: imdb://tt7888964
      - id: tmdb://615457
      - id: tvdb://133393
    Rating:
      - image: imdb://image.rating
        value: 7.4
        type: audience
        count: 501
      - image: rottentomatoes://image.rating.ripe
        value: 8.4
        type: critic
        count: 330
      - image: rottentomatoes://image.rating.upright
        value: 9.4
        type: audience
        count: 411
      - image: themoviedb://image.rating
        value: 7.9
        type: audience
        count: 508
    Director:
      - id: 3266
        filter: director=3266
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
    Writer:
      - id: 3267
        filter: writer=3267
        tag: Derek Kolstad
        tagKey: 5d776a8afb0d55001f54921f
        count: 4
        thumb: >-
          https://metadata-static.plex.tv/5/people/5c97a829e3651739f2971e4e2898682c.jpg
    Role:
      - id: 3268
        filter: actor=3268
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        count: 2
        role: Hutch Mansell
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3269
        filter: actor=3269
        tag: Aleksey Serebryakov
        tagKey: 5d77682b151a60001f24b98c
        role: Yulian Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b743f3f7a75e1b5bd937e2060753837.jpg
      - id: 3270
        filter: actor=3270
        tag: Connie Nielsen
        tagKey: 5d7768267228e5001f1dcdb5
        count: 4
        role: Becca Mansell
        thumb: >-
          https://metadata-static.plex.tv/3/people/328b075ecee9e20d7e22e95a72596edb.jpg
      - id: 3271
        filter: actor=3271
        tag: Christopher Lloyd
        tagKey: 5d7768244de0ee001fcc80bb
        count: 6
        role: David Mansell
        thumb: >-
          https://metadata-static.plex.tv/c/people/c2d2c2ab21e34db5837877ca386d43c3.jpg
      - id: 3272
        filter: actor=3272
        tag: Michael Ironside
        tagKey: 5d7768268718ba001e311c35
        count: 3
        role: Eddie Williams
        thumb: >-
          https://metadata-static.plex.tv/5/people/562560faf349fed1531898b075cfdf54.jpg
      - id: 3273
        filter: actor=3273
        tag: Colin Salmon
        tagKey: 5d776826880197001ec906c3
        role: The Barber
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05fd85a41289fbd0375c013fbb6593f.jpg
      - id: 3274
        filter: actor=3274
        tag: RZA
        tagKey: 5d77682985719b001f3a132f
        role: Harry Mansell
        thumb: >-
          https://metadata-static.plex.tv/9/people/97914947f71b47e35f9e0e708f6b6054.jpg
      - id: 3275
        filter: actor=3275
        tag: Billy MacLellan
        tagKey: 5d7768355af944001f1f9ddb
        role: Charlie Williams
        thumb: >-
          https://metadata-static.plex.tv/7/people/793801223b142f24e8455525db4f98b0.jpg
      - id: 3276
        filter: actor=3276
        tag: Araya Mengesha
        tagKey: 5d77687633f255001e8571ca
        role: Pavel
        thumb: >-
          https://metadata-static.plex.tv/0/people/0c5cf3bf1ba0fc04f5dfbfe7787419cd.jpg
      - id: 3277
        filter: actor=3277
        tag: Gage Munroe
        tagKey: 5d776843961905001eb96d28
        role: Brady Mansell
        thumb: >-
          https://metadata-static.plex.tv/0/people/07bdd3e7b5c9bf0151f67c6e986e546c.jpg
      - id: 3278
        filter: actor=3278
        tag: Paisley Cadorath
        tagKey: 5e166be52d4d84003e4bede2
        role: Sammy Mansell
        thumb: >-
          https://metadata-static.plex.tv/4/people/46fce2ea69eca54daeb8ef48e4fb788c.jpg
      - id: 3279
        filter: actor=3279
        tag: Aleksandr Pal
        tagKey: 5d776a28fb0d55001f53c11f
        role: Teddy Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/4/people/418db25e4856946a298e70440778a26a.jpg
      - id: 3280
        filter: actor=3280
        tag: Humberly González
        tagKey: 5d776c7cad5437001f7bf60d
        role: Lupita Martin
        thumb: >-
          https://metadata-static.plex.tv/9/people/9e0cf7073f9849cb8c6a17157c0cb1df.jpg
      - id: 3281
        filter: actor=3281
        tag: Edsson Morales
        tagKey: 5d776870eb5d26001f1eb87d
        role: Luis Martin
        thumb: >-
          https://metadata-static.plex.tv/2/people/270e11868a651c1f64e076871a0ebe09.jpg
      - id: 3282
        filter: actor=3282
        tag: J.P. Manoux
        tagKey: 5d776827103a2d001f56467f
        count: 3
        role: Pentagon Darren
        thumb: >-
          https://metadata-static.plex.tv/4/people/48d515df07e7954ad7bd291acba622d2.jpg
      - id: 3283
        filter: actor=3283
        tag: Adrian McLean
        tagKey: 5d776f5bad5437001f80fbb5
        role: Joey
        thumb: >-
          https://metadata-static.plex.tv/7/people/78e72df33a9979c71f376c23639ff4dd.jpg
      - id: 3284
        filter: actor=3284
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        role: Hitman Anatoly
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
      - id: 3285
        filter: actor=3285
        tag: Sergey Shnurov
        tagKey: 5d7768466f4521001ea9f873
        role: Hitman Valentin
        thumb: >-
          https://metadata-static.plex.tv/f/people/f78b732363a4c27c39078cf9dee79277.jpg
      - id: 3286
        filter: actor=3286
        tag: Joanne Rodriguez
        tagKey: 5d7768342ec6b5001f6bbd05
        role: Bus Driver Donna
        thumb: >-
          https://metadata-static.plex.tv/9/people/9cccffdd78a83dd849a4a41f7199f169.jpg
      - id: 3287
        filter: actor=3287
        tag: Stephanie Sy
        tagKey: 5d776d3d96b655001fe438e4
        role: Realtor
        thumb: https://metadata-static.plex.tv/people/5d776d3d96b655001fe438e4.jpg
      - id: 3288
        filter: actor=3288
        tag: Dan Rizzuto
        tagKey: 5d9f35b0b0262f001f6ec2de
        count: 2
        role: Gunman
      - id: 3289
        filter: actor=3289
        tag: Ruslan Rusin
        tagKey: 5d776d267a53e9001e752a5e
        role: Gunman
      - id: 3290
        filter: actor=3290
        tag: Vladimir Levkovsky
        tagKey: 60b90595f28049002d7ec8e2
        role: Gunman
      - id: 3291
        filter: actor=3291
        tag: Dan Skene
        tagKey: 5d77683c4de0ee001fccce80
        count: 2
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/9/people/9a3aae3a0a9c552d8c9dd651d6244f89.jpg
      - id: 3292
        filter: actor=3292
        tag: BJ Verot
        tagKey: 5d776ca79ab5440021519486
        role: Gunman
        thumb: https://metadata-static.plex.tv/people/5d776ca79ab5440021519486.jpg
      - id: 3293
        filter: actor=3293
        tag: Dylan Rampulla
        tagKey: 5e1647cd46aceb003cee8a84
        role: Gunman
      - id: 3294
        filter: actor=3294
        tag: Margaryta Soldatova
        tagKey: 5d776de696b655001fe5645f
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/2/people/2ef47acd293dd4e81ef6607c47af18aa.jpg
      - id: 3295
        filter: actor=3295
        tag: Megan Best
        tagKey: 5e166be52d4d84003e4bedde
        role: Woman on Bus
        thumb: >-
          https://metadata-static.plex.tv/d/people/d4ca27f2b660ae1fc76c8806b9b5a720.jpg
      - id: 3296
        filter: actor=3296
        tag: Darya Charusha
        tagKey: 5d7768bb374a5b001fece978
        role: Beta
        thumb: >-
          https://metadata-static.plex.tv/c/people/c503be6f3a83d9a3692d6c392679eb8e.jpg
      - id: 3297
        filter: actor=3297
        tag: Neil Davison
        tagKey: 5d9f3581adeb7a0021ce25ab
        role: Albert
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d1606a3ec7f8c775346b666d48aed59.jpg
      - id: 3298
        filter: actor=3298
        tag: Paul Essiembre
        tagKey: 5d77684f6f4521001eaa0e2c
        role: Jim the Neighbor
        thumb: >-
          https://metadata-static.plex.tv/1/people/143679603a8a9033feb9815d6a8eca29.jpg
      - id: 3299
        filter: actor=3299
        tag: Adam Hurtig
        tagKey: 5d7769e27a53e9001e6f36b4
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/c/people/cf6adb15c4d5a5ccd1dbe93fd684e807.jpg
      - id: 3300
        filter: actor=3300
        tag: Gabriel Daniels
        tagKey: 5d77689efb0d55001f5158ad
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/7/people/764cf91ca84fd8e24d10682acda85510.jpg
      - id: 3301
        filter: actor=3301
        tag: Kristen Harris
        tagKey: 5d7769ebfb0d55001f534779
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/8/people/8b82bda4aa071a57092c5e0bd82765e6.jpg
      - id: 3302
        filter: actor=3302
        tag: Erik Athavale
        tagKey: 5d776ab59ab54400215027c9
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/b/people/b0f12073fb6fa6f25213256a4493ebde.jpg
      - id: 3303
        filter: actor=3303
        tag: Tom Soares
        tagKey: 5f4059d8a4f07a00421717aa
        role: Alan Breiseth
      - id: 3304
        filter: actor=3304
        tag: Neven Pajkic
        tagKey: 5d7768256f4521001ea989ba
        role: Big Brute
        thumb: https://metadata-static.plex.tv/people/5d7768256f4521001ea989ba.jpg
      - id: 3305
        filter: actor=3305
        tag: Stephen Eric McIntyre
        tagKey: 5d776831151a60001f24d011
        role: Veteran
        thumb: >-
          https://metadata-static.plex.tv/5/people/556a233e543d87d4d3d1a2dc2630b4bb.jpg
      - id: 3306
        filter: actor=3306
        tag: Rick Dobran
        tagKey: 5d77684261141d001fb171ab
        count: 2
        role: Tattoo Shop Owner
        thumb: >-
          https://metadata-static.plex.tv/3/people/313b89fef7dd52cd49d6c78d0c1cb7e2.jpg
      - id: 3307
        filter: actor=3307
        tag: Richard Thomas
        tagKey: 64c10b5fdcb9af3bd1eee9e7
        role: Security Guard (Obshak Basement)
      - id: 3308
        filter: actor=3308
        tag: Alan Wh Wong
        tagKey: 66981d0bdcafced077160d19
        role: Doctor
      - id: 3309
        filter: actor=3309
        tag: Sharon Bajer
        tagKey: 5d776838151a60001f24e8fe
        role: Receptionist
        thumb: https://metadata-static.plex.tv/people/5d776838151a60001f24e8fe.jpg
      - id: 3310
        filter: actor=3310
        tag: Yulia Guzhva
        tagKey: 60b90596526b16002d6b1d25
        role: Karaoke Singer
      - id: 3311
        filter: actor=3311
        tag: Boris Gulyarin
        tagKey: 5d776d267a53e9001e752a57
        role: Mob Boss
        thumb: https://metadata-static.plex.tv/people/5d776d267a53e9001e752a57.jpg
      - id: 3312
        filter: actor=3312
        tag: Alex Nikolaychuk
        tagKey: 64c10b5f5b2d39db72ea18b4
        role: Mob Boss
      - id: 3313
        filter: actor=3313
        tag: Volodymyr Yamnenko
        tagKey: 5d776a5196b655001fdeac0c
        role: Mob Boss
        thumb: >-
          https://metadata-static.plex.tv/e/people/e00c1e06d5bd36b8afef7abadb3397a7.jpg
      - id: 3314
        filter: actor=3314
        tag: Meaghan Ann De Werrenne-Walle
        tagKey: 60b905965f7d3f002cb034d1
        role: Waitress (Karaoke Club)
      - id: 3315
        filter: actor=3315
        tag: Eugene Baffoe
        tagKey: 5ec419e0f8a5e90040cfaadb
        role: Barber's Guard
        thumb: >-
          https://metadata-static.plex.tv/0/people/08f07e73e74d04362ff80af43e27af9a.jpg
      - id: 3316
        filter: actor=3316
        tag: Daniel Bernhardt
        tagKey: 5d776828a091de001f2e6428
        count: 4
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/8/people/894ce74954806b4f55fac059f5af9bd9.jpg
      - id: 3317
        filter: actor=3317
        tag: Alain Moussi
        tagKey: 5d776b5096b655001fe0c5ab
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/5/people/5de5e70da005d9bcd84ee387ccd06079.jpg
      - id: 3318
        filter: actor=3318
        tag: Stéphane Julien
        tagKey: 5d776ac796b655001fdf93cc
        count: 2
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/c/people/c5501403d440b91a3c0d86cfe283523b.jpg
      - id: 3319
        filter: actor=3319
        tag: Robert Heinamaki
        tagKey: 60b90596b6a3c2002cb5df92
        role: Body Builder
      - id: 3320
        filter: actor=3320
        tag: Brent Alarie
        tagKey: 60b90596526b16002d6b1d27
        role: Tattoo Parlor
      - id: 66738
        filter: actor=66738
        tag: Tyrell Witherspoon
        tagKey: 6837cbc422219f2940060d8a
        role: Dancer
      - id: 3322
        filter: actor=3322
        tag: Frederick Allen
        tagKey: 5e166be52d4d84003e4bede0
        role: Russian Mafia Member (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/7/people/7904579927adae5ff33b8149870c5cf4.jpg
      - id: 3323
        filter: actor=3323
        tag: Destini Boldt
        tagKey: 64b018cffa119025f00aa26c
        role: Club Patron (uncredited)
    Producer:
      - id: 3324
        filter: producer=3324
        tag: David Leitch
        tagKey: 5d776828151a60001f24ae96
        count: 3
        thumb: >-
          https://metadata-static.plex.tv/4/people/4d935845dd16ac700054162203566edd.jpg
      - id: 3325
        filter: producer=3325
        tag: Kelly McCormick
        tagKey: 5d776b49fb0d55001f5629d7
        count: 2
        thumb: >-
          https://metadata-static.plex.tv/0/people/09afce317f35900bdcd7518664795277.jpg
      - id: 3326
        filter: producer=3326
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3327
        filter: producer=3327
        tag: Marc Provissiero
        tagKey: 5d776bb747dd6e001f6e242d
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b65cf07ae7032dd37dfe24ff0b00870.jpg
      - id: 66739
        filter: producer=66739
        tag: Braden Aftergood
        tagKey: 6839e0351aa1f166b353d040
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d5f88c6dbff24ede9bd423ea2fc0b95.jpg
    Field:
      - locked: true
        name: thumb
      - locked: true
        name: genre
```
## Episode Play
##### TV Episode starts playing.
```yaml
payload:
  event: media.play
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: show
    ratingKey: '1966'
    key: /library/metadata/1966
    parentRatingKey: '1965'
    grandparentRatingKey: '1964'
    guid: plex://episode/61e8260c263955a780cf92fd
    parentGuid: plex://season/602e7abd88e0a9002dfa0c65
    grandparentGuid: plex://show/5ec75ff037d69c0039b83267
    grandparentSlug: star-trek-strange-new-worlds
    type: episode
    title: Strange New Worlds
    grandparentKey: /library/metadata/1964
    parentKey: /library/metadata/1965
    librarySectionTitle: TV
    librarySectionID: 7
    librarySectionKey: /library/sections/7
    grandparentTitle: 'Star Trek: Strange New Worlds'
    parentTitle: Season 1
    contentRating: TV-PG
    summary: >-
      When one of Pike’s officers goes missing while on a secret mission for
      Starfleet, Pike has to come out of self-imposed exile. He must navigate
      how to rescue his officer, while struggling with what to do with the
      vision of the future he’s been given.
    index: 1
    parentIndex: 1
    audienceRating: 7.5
    skipCount: 1
    year: 2022
    thumb: /library/metadata/1966/thumb/1749085463
    art: /library/metadata/1964/art/1747275883
    parentThumb: /library/metadata/1965/thumb/1733009675
    grandparentThumb: /library/metadata/1964/thumb/1747275883
    grandparentArt: /library/metadata/1964/art/1747275883
    grandparentTheme: /library/metadata/1964/theme/1747275883
    duration: 3180000
    originallyAvailableAt: '2022-05-05'
    addedAt: 1733009522
    updatedAt: 1749085463
    audienceRatingImage: themoviedb://image.rating
    chapterSource: media
    Image:
      - alt: Strange New Worlds
        type: coverPoster
        url: /library/metadata/1964/thumb/1747275883
      - alt: Strange New Worlds
        type: snapshot
        url: /library/metadata/1966/thumb/1749085463
      - alt: Strange New Worlds
        type: background
        url: /library/metadata/1964/art/1747275883
      - alt: Strange New Worlds
        type: clearLogo
        url: /library/metadata/1964/clearLogo/1747275883
    UltraBlurColors:
      topLeft: 49210d
      topRight: 5d250c
      bottomRight: '924324'
      bottomLeft: 3c2809
    Guid:
      - id: imdb://tt12330364
      - id: tmdb://3455959
      - id: tvdb://8785342
    Rating:
      - image: imdb://image.rating
        value: 8.1
        type: audience
      - image: themoviedb://image.rating
        value: 7.5
        type: audience
    Director:
      - id: 31782
        filter: director=31782
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/4/people/4b551e483c0f6e124a2b41d672808386.jpg
    Writer:
      - id: 31783
        filter: writer=31783
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/f/people/f8f7fa7c7b9e0a80f0a8a1bfb20961d0.jpg
      - id: 14215
        filter: writer=14215
        tag: Alex Kurtzman
        tagKey: 5d77682a999c64001ec2d250
        thumb: >-
          https://metadata-static.plex.tv/f/people/fa310b367421ffe27bc11a758135d751.jpg
      - id: 31784
        filter: writer=31784
        tag: Jenny Lumet
        tagKey: 5d77691a47dd6e001f6c3406
        thumb: >-
          https://metadata-static.plex.tv/5/people/5453958cc06c3dfb343a7b1e4fc4061f.jpg
    Role:
      - id: 31517
        filter: actor=31517
        tag: Anson Mount
        tagKey: 5d776833eb5d26001f1e02a7
        role: Captain Christopher Pike
        thumb: >-
          https://metadata-static.plex.tv/2/people/28cbe22261c22769cc73b861c4e96117.jpg
      - id: 31518
        filter: actor=31518
        tag: Ethan Peck
        tagKey: 5d7768535af944001f1ff612
        role: Spock
        thumb: >-
          https://metadata-static.plex.tv/b/people/b95e1c83662a27139421110fcdae9875.jpg
      - id: 31519
        filter: actor=31519
        tag: Jess Bush
        tagKey: 5d7770a17a53e9001e7a7820
        role: Christine Chapel
        thumb: >-
          https://metadata-static.plex.tv/a/people/ab53153640df8c8ed77ad2a0fd7f84e0.jpg
      - id: 24567
        filter: actor=24567
        tag: Christina Chong
        tagKey: 5d77689c3ab0e7001f505b3a
        role: La'an Noonien-Singh
        thumb: >-
          https://metadata-static.plex.tv/0/people/02a6d83b818f342308c7eb6f88d8a7a0.jpg
      - id: 31520
        filter: actor=31520
        tag: Celia Rose Gooding
        tagKey: 5f3fcc8302101b0040ed14d7
        role: Nyota Uhura
        thumb: >-
          https://metadata-static.plex.tv/7/people/72d95a6b2b1cb8dd864c417a2c5c1fca.jpg
      - id: 31521
        filter: actor=31521
        tag: Melissa Navia
        tagKey: 5d7768b5308bca0020330942
        role: Erica Ortegas
        thumb: >-
          https://metadata-static.plex.tv/d/people/d0d6d99c83ee88e134eee8514fd8f8c8.jpg
      - id: 31522
        filter: actor=31522
        tag: Babs Olusanmokun
        tagKey: 5d77691551dd69001fe14a16
        role: Dr. Joseph M'Benga
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05c1cadfb147d2af5900bf0c730c1be.jpg
      - id: 5721
        filter: actor=5721
        tag: Rebecca Romijn
        tagKey: 5d7768283c3c2a001fbcb634
        role: Una Chin-Riley
        thumb: >-
          https://metadata-static.plex.tv/7/people/7c5a72847a551338d7cc9dd5ce29e168.jpg
      - id: 31523
        filter: actor=31523
        tag: Bruce Horak
        tagKey: 5f4009aa52f20000414ec84a
        role: Hemmer
        thumb: >-
          https://metadata-static.plex.tv/3/people/3fc2ed3209f1b41eed851f7968002cd8.jpg
      - id: 18013
        filter: actor=18013
        tag: Samantha Smith
        tagKey: 5d77682a2ec6b5001f6baa0d
        role: Eldredth Leader
        thumb: >-
          https://metadata-static.plex.tv/1/people/1f6f7c1f10d6144f0f6f2c248fbd37a8.jpg
      - id: 31536
        filter: actor=31536
        tag: Carla Bennett
        tagKey: 5f3fd28d03883a0040ac062e
        role: 'Palion Aide #2'
      - id: 31537
        filter: actor=31537
        tag: Peter Bou-Ghannam
        tagKey: 5f406ea5427eeb0041ee367f
        role: Palion Leader
        thumb: >-
          https://metadata-static.plex.tv/e/people/e1442a2dfe8442654806c2d6a7897a9d.jpg
      - id: 31538
        filter: actor=31538
        tag: Marienne Castro
        tagKey: 5f405c8ccae2c60042f7ac5f
        role: Shuttle Pilot
        thumb: >-
          https://metadata-static.plex.tv/0/people/07a4bbb1d2f99e444c9de59413530ceb.jpg
      - id: 31539
        filter: actor=31539
        tag: Bessie Cheng
        tagKey: 5f3fc306ce2564003f853ed9
        role: 'Eldredth Aide #2'
        thumb: >-
          https://metadata-static.plex.tv/5/people/54c80a73d51262aef9e3ab7a4c06ed6f.jpg
      - id: 31540
        filter: actor=31540
        tag: John Chou
        tagKey: 62753c184d3d1cb58e93d506
        role: 'Kiley Scientist #1'
      - id: 31541
        filter: actor=31541
        tag: Joseph Daly
        tagKey: 5f3ff78bfea1a1003f9b2369
        role: 'Eldredth Aide #1'
        thumb: >-
          https://metadata-static.plex.tv/5/people/53f78913242f64d56316ee75f341c1b2.jpg
      - id: 31542
        filter: actor=31542
        tag: Myles Dobson
        tagKey: 5d776a8f51dd69001fe250f1
        role: Vulcan Waiter
        thumb: https://metadata-static.plex.tv/people/5d776a8f51dd69001fe250f1.jpg
      - id: 31543
        filter: actor=31543
        tag: Chandra Galasso
        tagKey: 5d776b30594b2b001e6d24cd
        role: Lieutenant
        thumb: >-
          https://metadata-static.plex.tv/b/people/b88852fe91228e8f5e6c89bf8a5227b4.jpg
      - id: 31544
        filter: actor=31544
        tag: Jaimee Joe Gonzaga
        tagKey: 602d810722796e002dce6fd6
        role: 'Terminal Jockey #2'
      - id: 31545
        filter: actor=31545
        tag: Sandy Kerr
        tagKey: 5f3ff9e404a86500409ba8bd
        role: 'Starfleet Scientist #1'
      - id: 3378
        filter: actor=3378
        tag: Joel Lacoursiere
        tagKey: 5d776b32fb0d55001f55f89f
        role: 'Kiley Guard #1'
      - id: 31546
        filter: actor=31546
        tag: Dana Levenson
        tagKey: 629130c2ed685fc4708979bc
        role: Newscaster
      - id: 31547
        filter: actor=31547
        tag: Andrew Locke
        tagKey: 5f3fd0dd03883a0040abe2eb
        role: 'Terminal Jockey #1'
      - id: 31548
        filter: actor=31548
        tag: Etan Muskat
        tagKey: 5d77685f3ab0e7001f4ff787
        role: 'Starfleet Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/e/people/e5281dd2c6869adfc8c38b383f6ae3e8.jpg
      - id: 31549
        filter: actor=31549
        tag: Daniel Pagett
        tagKey: 5f4006d81ae710004102d3ae
        role: 'Kiley Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/a/people/a994871d39cc04fe6fda3de89130ab55.jpg
      - id: 31550
        filter: actor=31550
        tag: Rachel Sellan
        tagKey: 5d7768a0decfcd001f2ee614
        role: Woman in Elevator
        thumb: https://image.tmdb.org/t/p/original/1T4h8GPtXa2B3NWqzJ90whLZGvK.jpg
      - id: 31528
        filter: actor=31528
        tag: Adrian Holmes
        tagKey: 5d7768315af944001f1f8e5d
        role: Admiral Robert April
        thumb: >-
          https://metadata-static.plex.tv/8/people/847f9bd416bbeb7dfd1141508b9fce60.jpg
      - id: 31529
        filter: actor=31529
        tag: Gia Sandhu
        tagKey: 5d776b9fad5437001f7a51af
        role: T'Pring
        thumb: >-
          https://metadata-static.plex.tv/7/people/7134a5a24907c3624622f8eec68ea9b7.jpg
      - id: 31524
        filter: actor=31524
        tag: Dan Jeannotte
        tagKey: 5d7768726f4521001eaa76c0
        role: George Samuel 'Sam' Kirk
        thumb: >-
          https://metadata-static.plex.tv/0/people/061d8cd023a1a686ddbdf055cea91b5f.jpg
      - id: 31527
        filter: actor=31527
        tag: Melanie Scrofano
        tagKey: 5d77684b2e80df001ebe0e3a
        role: Captain Marie Batel
        thumb: >-
          https://metadata-static.plex.tv/c/people/cbc66df9d39f2ab6b5c35edba96721cc.jpg
      - id: 31525
        filter: actor=31525
        tag: Rong Fu
        tagKey: 5d776d9e47dd6e001f6f4b93
        role: Jenna Mitchell
        thumb: >-
          https://metadata-static.plex.tv/7/people/7593afaa022e743a3b7736dbe326a3e9.jpg
      - id: 31526
        filter: actor=31526
        tag: André Dae Kim
        tagKey: 5f401a4c03883a0040b2ae4b
        role: Chief Kyle
        thumb: >-
          https://metadata-static.plex.tv/7/people/77500e32058dbe3cea766035d600b250.jpg
      - id: 31594
        filter: actor=31594
        tag: David Kirby
        tagKey: 6308b629fbb5dda04b436928
        role: 'Palion Aide #1'
      - id: 31650
        filter: actor=31650
        tag: Jon Blair
        tagKey: 5f400f1e768fc70040549f43
        role: 'Kiley Guard #2'
    Producer:
      - id: 31789
        filter: producer=31789
        tag: Paul Gadd
        tagKey: 5e164048df4678003f524f3e
      - id: 31790
        filter: producer=31790
        tag: Andrea Raffaghello
        tagKey: 5d776cc7fb0d55001f5922a8
        thumb: >-
          https://metadata-static.plex.tv/0/people/0d1c2013efdbddf16d7ea172de7deb39.jpg

```
## Episode Pause
##### TV Episode playback pauses.
```yaml
payload:
  event: media.pause
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: show
    ratingKey: '1966'
    key: /library/metadata/1966
    parentRatingKey: '1965'
    grandparentRatingKey: '1964'
    guid: plex://episode/61e8260c263955a780cf92fd
    parentGuid: plex://season/602e7abd88e0a9002dfa0c65
    grandparentGuid: plex://show/5ec75ff037d69c0039b83267
    grandparentSlug: star-trek-strange-new-worlds
    type: episode
    title: Strange New Worlds
    grandparentKey: /library/metadata/1964
    parentKey: /library/metadata/1965
    librarySectionTitle: TV
    librarySectionID: 7
    librarySectionKey: /library/sections/7
    grandparentTitle: 'Star Trek: Strange New Worlds'
    parentTitle: Season 1
    contentRating: TV-PG
    summary: >-
      When one of Pike’s officers goes missing while on a secret mission for
      Starfleet, Pike has to come out of self-imposed exile. He must navigate
      how to rescue his officer, while struggling with what to do with the
      vision of the future he’s been given.
    index: 1
    parentIndex: 1
    audienceRating: 7.5
    skipCount: 1
    year: 2022
    thumb: /library/metadata/1966/thumb/1749085463
    art: /library/metadata/1964/art/1747275883
    parentThumb: /library/metadata/1965/thumb/1733009675
    grandparentThumb: /library/metadata/1964/thumb/1747275883
    grandparentArt: /library/metadata/1964/art/1747275883
    grandparentTheme: /library/metadata/1964/theme/1747275883
    duration: 3180000
    originallyAvailableAt: '2022-05-05'
    addedAt: 1733009522
    updatedAt: 1749085463
    audienceRatingImage: themoviedb://image.rating
    chapterSource: media
    Image:
      - alt: Strange New Worlds
        type: coverPoster
        url: /library/metadata/1964/thumb/1747275883
      - alt: Strange New Worlds
        type: snapshot
        url: /library/metadata/1966/thumb/1749085463
      - alt: Strange New Worlds
        type: background
        url: /library/metadata/1964/art/1747275883
      - alt: Strange New Worlds
        type: clearLogo
        url: /library/metadata/1964/clearLogo/1747275883
    UltraBlurColors:
      topLeft: 49210d
      topRight: 5d250c
      bottomRight: '924324'
      bottomLeft: 3c2809
    Guid:
      - id: imdb://tt12330364
      - id: tmdb://3455959
      - id: tvdb://8785342
    Rating:
      - image: imdb://image.rating
        value: 8.1
        type: audience
      - image: themoviedb://image.rating
        value: 7.5
        type: audience
    Director:
      - id: 31782
        filter: director=31782
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/4/people/4b551e483c0f6e124a2b41d672808386.jpg
    Writer:
      - id: 31783
        filter: writer=31783
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/f/people/f8f7fa7c7b9e0a80f0a8a1bfb20961d0.jpg
      - id: 14215
        filter: writer=14215
        tag: Alex Kurtzman
        tagKey: 5d77682a999c64001ec2d250
        thumb: >-
          https://metadata-static.plex.tv/f/people/fa310b367421ffe27bc11a758135d751.jpg
      - id: 31784
        filter: writer=31784
        tag: Jenny Lumet
        tagKey: 5d77691a47dd6e001f6c3406
        thumb: >-
          https://metadata-static.plex.tv/5/people/5453958cc06c3dfb343a7b1e4fc4061f.jpg
    Role:
      - id: 31517
        filter: actor=31517
        tag: Anson Mount
        tagKey: 5d776833eb5d26001f1e02a7
        role: Captain Christopher Pike
        thumb: >-
          https://metadata-static.plex.tv/2/people/28cbe22261c22769cc73b861c4e96117.jpg
      - id: 31518
        filter: actor=31518
        tag: Ethan Peck
        tagKey: 5d7768535af944001f1ff612
        role: Spock
        thumb: >-
          https://metadata-static.plex.tv/b/people/b95e1c83662a27139421110fcdae9875.jpg
      - id: 31519
        filter: actor=31519
        tag: Jess Bush
        tagKey: 5d7770a17a53e9001e7a7820
        role: Christine Chapel
        thumb: >-
          https://metadata-static.plex.tv/a/people/ab53153640df8c8ed77ad2a0fd7f84e0.jpg
      - id: 24567
        filter: actor=24567
        tag: Christina Chong
        tagKey: 5d77689c3ab0e7001f505b3a
        role: La'an Noonien-Singh
        thumb: >-
          https://metadata-static.plex.tv/0/people/02a6d83b818f342308c7eb6f88d8a7a0.jpg
      - id: 31520
        filter: actor=31520
        tag: Celia Rose Gooding
        tagKey: 5f3fcc8302101b0040ed14d7
        role: Nyota Uhura
        thumb: >-
          https://metadata-static.plex.tv/7/people/72d95a6b2b1cb8dd864c417a2c5c1fca.jpg
      - id: 31521
        filter: actor=31521
        tag: Melissa Navia
        tagKey: 5d7768b5308bca0020330942
        role: Erica Ortegas
        thumb: >-
          https://metadata-static.plex.tv/d/people/d0d6d99c83ee88e134eee8514fd8f8c8.jpg
      - id: 31522
        filter: actor=31522
        tag: Babs Olusanmokun
        tagKey: 5d77691551dd69001fe14a16
        role: Dr. Joseph M'Benga
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05c1cadfb147d2af5900bf0c730c1be.jpg
      - id: 5721
        filter: actor=5721
        tag: Rebecca Romijn
        tagKey: 5d7768283c3c2a001fbcb634
        role: Una Chin-Riley
        thumb: >-
          https://metadata-static.plex.tv/7/people/7c5a72847a551338d7cc9dd5ce29e168.jpg
      - id: 31523
        filter: actor=31523
        tag: Bruce Horak
        tagKey: 5f4009aa52f20000414ec84a
        role: Hemmer
        thumb: >-
          https://metadata-static.plex.tv/3/people/3fc2ed3209f1b41eed851f7968002cd8.jpg
      - id: 18013
        filter: actor=18013
        tag: Samantha Smith
        tagKey: 5d77682a2ec6b5001f6baa0d
        role: Eldredth Leader
        thumb: >-
          https://metadata-static.plex.tv/1/people/1f6f7c1f10d6144f0f6f2c248fbd37a8.jpg
      - id: 31536
        filter: actor=31536
        tag: Carla Bennett
        tagKey: 5f3fd28d03883a0040ac062e
        role: 'Palion Aide #2'
      - id: 31537
        filter: actor=31537
        tag: Peter Bou-Ghannam
        tagKey: 5f406ea5427eeb0041ee367f
        role: Palion Leader
        thumb: >-
          https://metadata-static.plex.tv/e/people/e1442a2dfe8442654806c2d6a7897a9d.jpg
      - id: 31538
        filter: actor=31538
        tag: Marienne Castro
        tagKey: 5f405c8ccae2c60042f7ac5f
        role: Shuttle Pilot
        thumb: >-
          https://metadata-static.plex.tv/0/people/07a4bbb1d2f99e444c9de59413530ceb.jpg
      - id: 31539
        filter: actor=31539
        tag: Bessie Cheng
        tagKey: 5f3fc306ce2564003f853ed9
        role: 'Eldredth Aide #2'
        thumb: >-
          https://metadata-static.plex.tv/5/people/54c80a73d51262aef9e3ab7a4c06ed6f.jpg
      - id: 31540
        filter: actor=31540
        tag: John Chou
        tagKey: 62753c184d3d1cb58e93d506
        role: 'Kiley Scientist #1'
      - id: 31541
        filter: actor=31541
        tag: Joseph Daly
        tagKey: 5f3ff78bfea1a1003f9b2369
        role: 'Eldredth Aide #1'
        thumb: >-
          https://metadata-static.plex.tv/5/people/53f78913242f64d56316ee75f341c1b2.jpg
      - id: 31542
        filter: actor=31542
        tag: Myles Dobson
        tagKey: 5d776a8f51dd69001fe250f1
        role: Vulcan Waiter
        thumb: https://metadata-static.plex.tv/people/5d776a8f51dd69001fe250f1.jpg
      - id: 31543
        filter: actor=31543
        tag: Chandra Galasso
        tagKey: 5d776b30594b2b001e6d24cd
        role: Lieutenant
        thumb: >-
          https://metadata-static.plex.tv/b/people/b88852fe91228e8f5e6c89bf8a5227b4.jpg
      - id: 31544
        filter: actor=31544
        tag: Jaimee Joe Gonzaga
        tagKey: 602d810722796e002dce6fd6
        role: 'Terminal Jockey #2'
      - id: 31545
        filter: actor=31545
        tag: Sandy Kerr
        tagKey: 5f3ff9e404a86500409ba8bd
        role: 'Starfleet Scientist #1'
      - id: 3378
        filter: actor=3378
        tag: Joel Lacoursiere
        tagKey: 5d776b32fb0d55001f55f89f
        role: 'Kiley Guard #1'
      - id: 31546
        filter: actor=31546
        tag: Dana Levenson
        tagKey: 629130c2ed685fc4708979bc
        role: Newscaster
      - id: 31547
        filter: actor=31547
        tag: Andrew Locke
        tagKey: 5f3fd0dd03883a0040abe2eb
        role: 'Terminal Jockey #1'
      - id: 31548
        filter: actor=31548
        tag: Etan Muskat
        tagKey: 5d77685f3ab0e7001f4ff787
        role: 'Starfleet Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/e/people/e5281dd2c6869adfc8c38b383f6ae3e8.jpg
      - id: 31549
        filter: actor=31549
        tag: Daniel Pagett
        tagKey: 5f4006d81ae710004102d3ae
        role: 'Kiley Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/a/people/a994871d39cc04fe6fda3de89130ab55.jpg
      - id: 31550
        filter: actor=31550
        tag: Rachel Sellan
        tagKey: 5d7768a0decfcd001f2ee614
        role: Woman in Elevator
        thumb: https://image.tmdb.org/t/p/original/1T4h8GPtXa2B3NWqzJ90whLZGvK.jpg
      - id: 31528
        filter: actor=31528
        tag: Adrian Holmes
        tagKey: 5d7768315af944001f1f8e5d
        role: Admiral Robert April
        thumb: >-
          https://metadata-static.plex.tv/8/people/847f9bd416bbeb7dfd1141508b9fce60.jpg
      - id: 31529
        filter: actor=31529
        tag: Gia Sandhu
        tagKey: 5d776b9fad5437001f7a51af
        role: T'Pring
        thumb: >-
          https://metadata-static.plex.tv/7/people/7134a5a24907c3624622f8eec68ea9b7.jpg
      - id: 31524
        filter: actor=31524
        tag: Dan Jeannotte
        tagKey: 5d7768726f4521001eaa76c0
        role: George Samuel 'Sam' Kirk
        thumb: >-
          https://metadata-static.plex.tv/0/people/061d8cd023a1a686ddbdf055cea91b5f.jpg
      - id: 31527
        filter: actor=31527
        tag: Melanie Scrofano
        tagKey: 5d77684b2e80df001ebe0e3a
        role: Captain Marie Batel
        thumb: >-
          https://metadata-static.plex.tv/c/people/cbc66df9d39f2ab6b5c35edba96721cc.jpg
      - id: 31525
        filter: actor=31525
        tag: Rong Fu
        tagKey: 5d776d9e47dd6e001f6f4b93
        role: Jenna Mitchell
        thumb: >-
          https://metadata-static.plex.tv/7/people/7593afaa022e743a3b7736dbe326a3e9.jpg
      - id: 31526
        filter: actor=31526
        tag: André Dae Kim
        tagKey: 5f401a4c03883a0040b2ae4b
        role: Chief Kyle
        thumb: >-
          https://metadata-static.plex.tv/7/people/77500e32058dbe3cea766035d600b250.jpg
      - id: 31594
        filter: actor=31594
        tag: David Kirby
        tagKey: 6308b629fbb5dda04b436928
        role: 'Palion Aide #1'
      - id: 31650
        filter: actor=31650
        tag: Jon Blairpayload:
  event: media.pause
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: show
    ratingKey: '1966'
    key: /library/metadata/1966
    parentRatingKey: '1965'
    grandparentRatingKey: '1964'
    guid: plex://episode/61e8260c263955a780cf92fd
    parentGuid: plex://season/602e7abd88e0a9002dfa0c65
    grandparentGuid: plex://show/5ec75ff037d69c0039b83267
    grandparentSlug: star-trek-strange-new-worlds
    type: episode
    title: Strange New Worlds
    grandparentKey: /library/metadata/1964
    parentKey: /library/metadata/1965
    librarySectionTitle: TV
    librarySectionID: 7
    librarySectionKey: /library/sections/7
    grandparentTitle: 'Star Trek: Strange New Worlds'
    parentTitle: Season 1
    contentRating: TV-PG
    summary: >-
      When one of Pike’s officers goes missing while on a secret mission for
      Starfleet, Pike has to come out of self-imposed exile. He must navigate
      how to rescue his officer, while struggling with what to do with the
      vision of the future he’s been given.
    index: 1
    parentIndex: 1
    audienceRating: 7.5
    skipCount: 1
    year: 2022
    thumb: /library/metadata/1966/thumb/1749085463
    art: /library/metadata/1964/art/1747275883
    parentThumb: /library/metadata/1965/thumb/1733009675
    grandparentThumb: /library/metadata/1964/thumb/1747275883
    grandparentArt: /library/metadata/1964/art/1747275883
    grandparentTheme: /library/metadata/1964/theme/1747275883
    duration: 3180000
    originallyAvailableAt: '2022-05-05'
    addedAt: 1733009522
    updatedAt: 1749085463
    audienceRatingImage: themoviedb://image.rating
    chapterSource: media
    Image:
      - alt: Strange New Worlds
        type: coverPoster
        url: /library/metadata/1964/thumb/1747275883
      - alt: Strange New Worlds
        type: snapshot
        url: /library/metadata/1966/thumb/1749085463
      - alt: Strange New Worlds
        type: background
        url: /library/metadata/1964/art/1747275883
      - alt: Strange New Worlds
        type: clearLogo
        url: /library/metadata/1964/clearLogo/1747275883
    UltraBlurColors:
      topLeft: 49210d
      topRight: 5d250c
      bottomRight: '924324'
      bottomLeft: 3c2809
    Guid:
      - id: imdb://tt12330364
      - id: tmdb://3455959
      - id: tvdb://8785342
    Rating:
      - image: imdb://image.rating
        value: 8.1
        type: audience
      - image: themoviedb://image.rating
        value: 7.5
        type: audience
    Director:
      - id: 31782
        filter: director=31782
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/4/people/4b551e483c0f6e124a2b41d672808386.jpg
    Writer:
      - id: 31783
        filter: writer=31783
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/f/people/f8f7fa7c7b9e0a80f0a8a1bfb20961d0.jpg
      - id: 14215
        filter: writer=14215
        tag: Alex Kurtzman
        tagKey: 5d77682a999c64001ec2d250
        thumb: >-
          https://metadata-static.plex.tv/f/people/fa310b367421ffe27bc11a758135d751.jpg
      - id: 31784
        filter: writer=31784
        tag: Jenny Lumet
        tagKey: 5d77691a47dd6e001f6c3406
        thumb: >-
          https://metadata-static.plex.tv/5/people/5453958cc06c3dfb343a7b1e4fc4061f.jpg
    Role:
      - id: 31517
        filter: actor=31517
        tag: Anson Mount
        tagKey: 5d776833eb5d26001f1e02a7
        role: Captain Christopher Pike
        thumb: >-
          https://metadata-static.plex.tv/2/people/28cbe22261c22769cc73b861c4e96117.jpg
      - id: 31518
        filter: actor=31518
        tag: Ethan Peck
        tagKey: 5d7768535af944001f1ff612
        role: Spock
        thumb: >-
          https://metadata-static.plex.tv/b/people/b95e1c83662a27139421110fcdae9875.jpg
      - id: 31519
        filter: actor=31519
        tag: Jess Bush
        tagKey: 5d7770a17a53e9001e7a7820
        role: Christine Chapel
        thumb: >-
          https://metadata-static.plex.tv/a/people/ab53153640df8c8ed77ad2a0fd7f84e0.jpg
      - id: 24567
        filter: actor=24567
        tag: Christina Chong
        tagKey: 5d77689c3ab0e7001f505b3a
        role: La'an Noonien-Singh
        thumb: >-
          https://metadata-static.plex.tv/0/people/02a6d83b818f342308c7eb6f88d8a7a0.jpg
      - id: 31520
        filter: actor=31520
        tag: Celia Rose Gooding
        tagKey: 5f3fcc8302101b0040ed14d7
        role: Nyota Uhura
        thumb: >-
          https://metadata-static.plex.tv/7/people/72d95a6b2b1cb8dd864c417a2c5c1fca.jpg
      - id: 31521
        filter: actor=31521
        tag: Melissa Navia
        tagKey: 5d7768b5308bca0020330942
        role: Erica Ortegas
        thumb: >-
          https://metadata-static.plex.tv/d/people/d0d6d99c83ee88e134eee8514fd8f8c8.jpg
      - id: 31522
        filter: actor=31522
        tag: Babs Olusanmokun
        tagKey: 5d77691551dd69001fe14a16
        role: Dr. Joseph M'Benga
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05c1cadfb147d2af5900bf0c730c1be.jpg
      - id: 5721
        filter: actor=5721
        tag: Rebecca Romijn
        tagKey: 5d7768283c3c2a001fbcb634
        role: Una Chin-Riley
        thumb: >-
          https://metadata-static.plex.tv/7/people/7c5a72847a551338d7cc9dd5ce29e168.jpg
      - id: 31523
        filter: actor=31523
        tag: Bruce Horak
        tagKey: 5f4009aa52f20000414ec84a
        role: Hemmer
        thumb: >-
          https://metadata-static.plex.tv/3/people/3fc2ed3209f1b41eed851f7968002cd8.jpg
      - id: 18013
        filter: actor=18013
        tag: Samantha Smith
        tagKey: 5d77682a2ec6b5001f6baa0d
        role: Eldredth Leader
        thumb: >-
          https://metadata-static.plex.tv/1/people/1f6f7c1f10d6144f0f6f2c248fbd37a8.jpg
      - id: 31536
        filter: actor=31536
        tag: Carla Bennett
        tagKey: 5f3fd28d03883a0040ac062e
        role: 'Palion Aide #2'
      - id: 31537
        filter: actor=31537
        tag: Peter Bou-Ghannam
        tagKey: 5f406ea5427eeb0041ee367f
        role: Palion Leader
        thumb: >-
          https://metadata-static.plex.tv/e/people/e1442a2dfe8442654806c2d6a7897a9d.jpg
      - id: 31538
        filter: actor=31538
        tag: Marienne Castro
        tagKey: 5f405c8ccae2c60042f7ac5f
        role: Shuttle Pilot
        thumb: >-
          https://metadata-static.plex.tv/0/people/07a4bbb1d2f99e444c9de59413530ceb.jpg
      - id: 31539
        filter: actor=31539
        tag: Bessie Cheng
        tagKey: 5f3fc306ce2564003f853ed9
        role: 'Eldredth Aide #2'
        thumb: >-
          https://metadata-static.plex.tv/5/people/54c80a73d51262aef9e3ab7a4c06ed6f.jpg
      - id: 31540
        filter: actor=31540
        tag: John Chou
        tagKey: 62753c184d3d1cb58e93d506
        role: 'Kiley Scientist #1'
      - id: 31541
        filter: actor=31541
        tag: Joseph Daly
        tagKey: 5f3ff78bfea1a1003f9b2369
        role: 'Eldredth Aide #1'
        thumb: >-
          https://metadata-static.plex.tv/5/people/53f78913242f64d56316ee75f341c1b2.jpg
      - id: 31542
        filter: actor=31542
        tag: Myles Dobson
        tagKey: 5d776a8f51dd69001fe250f1
        role: Vulcan Waiter
        thumb: https://metadata-static.plex.tv/people/5d776a8f51dd69001fe250f1.jpg
      - id: 31543
        filter: actor=31543
        tag: Chandra Galasso
        tagKey: 5d776b30594b2b001e6d24cd
        role: Lieutenant
        thumb: >-
          https://metadata-static.plex.tv/b/people/b88852fe91228e8f5e6c89bf8a5227b4.jpg
      - id: 31544
        filter: actor=31544
        tag: Jaimee Joe Gonzaga
        tagKey: 602d810722796e002dce6fd6
        role: 'Terminal Jockey #2'
      - id: 31545
        filter: actor=31545
        tag: Sandy Kerr
        tagKey: 5f3ff9e404a86500409ba8bd
        role: 'Starfleet Scientist #1'
      - id: 3378
        filter: actor=3378
        tag: Joel Lacoursiere
        tagKey: 5d776b32fb0d55001f55f89f
        role: 'Kiley Guard #1'
      - id: 31546
        filter: actor=31546
        tag: Dana Levenson
        tagKey: 629130c2ed685fc4708979bc
        role: Newscaster
      - id: 31547
        filter: actor=31547
        tag: Andrew Locke
        tagKey: 5f3fd0dd03883a0040abe2eb
        role: 'Terminal Jockey #1'
      - id: 31548
        filter: actor=31548
        tag: Etan Muskat
        tagKey: 5d77685f3ab0e7001f4ff787
        role: 'Starfleet Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/e/people/e5281dd2c6869adfc8c38b383f6ae3e8.jpg
      - id: 31549
        filter: actor=31549
        tag: Daniel Pagett
        tagKey: 5f4006d81ae710004102d3ae
        role: 'Kiley Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/a/people/a994871d39cc04fe6fda3de89130ab55.jpg
      - id: 31550
        filter: actor=31550
        tag: Rachel Sellan
        tagKey: 5d7768a0decfcd001f2ee614
        role: Woman in Elevator
        thumb: https://image.tmdb.org/t/p/original/1T4h8GPtXa2B3NWqzJ90whLZGvK.jpg
      - id: 31528
        filter: actor=31528
        tag: Adrian Holmes
        tagKey: 5d7768315af944001f1f8e5d
        role: Admiral Robert April
        thumb: >-
          https://metadata-static.plex.tv/8/people/847f9bd416bbeb7dfd1141508b9fce60.jpg
      - id: 31529
        filter: actor=31529
        tag: Gia Sandhu
        tagKey: 5d776b9fad5437001f7a51af
        role: T'Pring
        thumb: >-
          https://metadata-static.plex.tv/7/people/7134a5a24907c3624622f8eec68ea9b7.jpg
      - id: 31524
        filter: actor=31524
        tag: Dan Jeannotte
        tagKey: 5d7768726f4521001eaa76c0
        role: George Samuel 'Sam' Kirk
        thumb: >-
          https://metadata-static.plex.tv/0/people/061d8cd023a1a686ddbdf055cea91b5f.jpg
      - id: 31527
        filter: actor=31527
        tag: Melanie Scrofano
        tagKey: 5d77684b2e80df001ebe0e3a
        role: Captain Marie Batel
        thumb: >-
          https://metadata-static.plex.tv/c/people/cbc66df9d39f2ab6b5c35edba96721cc.jpg
      - id: 31525
        filter: actor=31525
        tag: Rong Fu
        tagKey: 5d776d9e47dd6e001f6f4b93
        role: Jenna Mitchell
        thumb: >-
          https://metadata-static.plex.tv/7/people/7593afaa022e743a3b7736dbe326a3e9.jpg
      - id: 31526
        filter: actor=31526
        tag: André Dae Kim
        tagKey: 5f401a4c03883a0040b2ae4b
        role: Chief Kyle
        thumb: >-
          https://metadata-static.plex.tv/7/people/77500e32058dbe3cea766035d600b250.jpg
      - id: 31594
        filter: actor=31594
        tag: David Kirby
        tagKey: 6308b629fbb5dda04b436928
        role: 'Palion Aide #1'
      - id: 31650
        filter: actor=31650
        tag: Jon Blair
        tagKey: 5f400f1e768fc70040549f43
        role: 'Kiley Guard #2'
    Producer:
      - id: 31789
        filter: producer=31789
        tag: Paul Gadd
        tagKey: 5e164048df4678003f524f3e
      - id: 31790
        filter: producer=31790
        tag: Andrea Raffaghello
        tagKey: 5d776cc7fb0d55001f5922a8
        thumb: >-
          https://metadata-static.plex.tv/0/people/0d1c2013efdbddf16d7ea172de7deb39.jpg

        tagKey: 5f400f1e768fc70040549f43
        role: 'Kiley Guard #2'
    Producer:
      - id: 31789
        filter: producer=31789
        tag: Paul Gadd
        tagKey: 5e164048df4678003f524f3e
      - id: 31790
        filter: producer=31790
        tag: Andrea Raffaghello
        tagKey: 5d776cc7fb0d55001f5922a8
        thumb: >-
          https://metadata-static.plex.tv/0/people/0d1c2013efdbddf16d7ea172de7deb39.jpg

```
## Episode Resume
##### TV Episode playback resumes.
```yaml
payload:
  event: media.resume
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: show
    ratingKey: '1966'
    key: /library/metadata/1966
    parentRatingKey: '1965'
    grandparentRatingKey: '1964'
    guid: plex://episode/61e8260c263955a780cf92fd
    parentGuid: plex://season/602e7abd88e0a9002dfa0c65
    grandparentGuid: plex://show/5ec75ff037d69c0039b83267
    grandparentSlug: star-trek-strange-new-worlds
    type: episode
    title: Strange New Worlds
    grandparentKey: /library/metadata/1964
    parentKey: /library/metadata/1965
    librarySectionTitle: TV
    librarySectionID: 7
    librarySectionKey: /library/sections/7
    grandparentTitle: 'Star Trek: Strange New Worlds'
    parentTitle: Season 1
    contentRating: TV-PG
    summary: >-
      When one of Pike’s officers goes missing while on a secret mission for
      Starfleet, Pike has to come out of self-imposed exile. He must navigate
      how to rescue his officer, while struggling with what to do with the
      vision of the future he’s been given.
    index: 1
    parentIndex: 1
    audienceRating: 7.5
    skipCount: 1
    year: 2022
    thumb: /library/metadata/1966/thumb/1749085463
    art: /library/metadata/1964/art/1747275883
    parentThumb: /library/metadata/1965/thumb/1733009675
    grandparentThumb: /library/metadata/1964/thumb/1747275883
    grandparentArt: /library/metadata/1964/art/1747275883
    grandparentTheme: /library/metadata/1964/theme/1747275883
    duration: 3180000
    originallyAvailableAt: '2022-05-05'
    addedAt: 1733009522
    updatedAt: 1749085463
    audienceRatingImage: themoviedb://image.rating
    chapterSource: media
    Image:
      - alt: Strange New Worlds
        type: coverPoster
        url: /library/metadata/1964/thumb/1747275883
      - alt: Strange New Worlds
        type: snapshot
        url: /library/metadata/1966/thumb/1749085463
      - alt: Strange New Worlds
        type: background
        url: /library/metadata/1964/art/1747275883
      - alt: Strange New Worlds
        type: clearLogo
        url: /library/metadata/1964/clearLogo/1747275883
    UltraBlurColors:
      topLeft: 49210d
      topRight: 5d250c
      bottomRight: '924324'
      bottomLeft: 3c2809
    Guid:
      - id: imdb://tt12330364
      - id: tmdb://3455959
      - id: tvdb://8785342
    Rating:
      - image: imdb://image.rating
        value: 8.1
        type: audience
      - image: themoviedb://image.rating
        value: 7.5
        type: audience
    Director:
      - id: 31782
        filter: director=31782
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/4/people/4b551e483c0f6e124a2b41d672808386.jpg
    Writer:
      - id: 31783
        filter: writer=31783
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/f/people/f8f7fa7c7b9e0a80f0a8a1bfb20961d0.jpg
      - id: 14215
        filter: writer=14215
        tag: Alex Kurtzman
        tagKey: 5d77682a999c64001ec2d250
        thumb: >-
          https://metadata-static.plex.tv/f/people/fa310b367421ffe27bc11a758135d751.jpg
      - id: 31784
        filter: writer=31784
        tag: Jenny Lumet
        tagKey: 5d77691a47dd6e001f6c3406
        thumb: >-
          https://metadata-static.plex.tv/5/people/5453958cc06c3dfb343a7b1e4fc4061f.jpg
    Role:
      - id: 31517
        filter: actor=31517
        tag: Anson Mount
        tagKey: 5d776833eb5d26001f1e02a7
        role: Captain Christopher Pike
        thumb: >-
          https://metadata-static.plex.tv/2/people/28cbe22261c22769cc73b861c4e96117.jpg
      - id: 31518
        filter: actor=31518
        tag: Ethan Peck
        tagKey: 5d7768535af944001f1ff612
        role: Spock
        thumb: >-
          https://metadata-static.plex.tv/b/people/b95e1c83662a27139421110fcdae9875.jpg
      - id: 31519
        filter: actor=31519
        tag: Jess Bush
        tagKey: 5d7770a17a53e9001e7a7820
        role: Christine Chapel
        thumb: >-
          https://metadata-static.plex.tv/a/people/ab53153640df8c8ed77ad2a0fd7f84e0.jpg
      - id: 24567
        filter: actor=24567
        tag: Christina Chong
        tagKey: 5d77689c3ab0e7001f505b3a
        role: La'an Noonien-Singh
        thumb: >-
          https://metadata-static.plex.tv/0/people/02a6d83b818f342308c7eb6f88d8a7a0.jpg
      - id: 31520
        filter: actor=31520
        tag: Celia Rose Gooding
        tagKey: 5f3fcc8302101b0040ed14d7
        role: Nyota Uhura
        thumb: >-
          https://metadata-static.plex.tv/7/people/72d95a6b2b1cb8dd864c417a2c5c1fca.jpg
      - id: 31521
        filter: actor=31521
        tag: Melissa Navia
        tagKey: 5d7768b5308bca0020330942
        role: Erica Ortegas
        thumb: >-
          https://metadata-static.plex.tv/d/people/d0d6d99c83ee88e134eee8514fd8f8c8.jpg
      - id: 31522
        filter: actor=31522
        tag: Babs Olusanmokun
        tagKey: 5d77691551dd69001fe14a16
        role: Dr. Joseph M'Benga
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05c1cadfb147d2af5900bf0c730c1be.jpg
      - id: 5721
        filter: actor=5721
        tag: Rebecca Romijn
        tagKey: 5d7768283c3c2a001fbcb634
        role: Una Chin-Riley
        thumb: >-
          https://metadata-static.plex.tv/7/people/7c5a72847a551338d7cc9dd5ce29e168.jpg
      - id: 31523
        filter: actor=31523
        tag: Bruce Horak
        tagKey: 5f4009aa52f20000414ec84a
        role: Hemmer
        thumb: >-
          https://metadata-static.plex.tv/3/people/3fc2ed3209f1b41eed851f7968002cd8.jpg
      - id: 18013
        filter: actor=18013
        tag: Samantha Smith
        tagKey: 5d77682a2ec6b5001f6baa0d
        role: Eldredth Leader
        thumb: >-
          https://metadata-static.plex.tv/1/people/1f6f7c1f10d6144f0f6f2c248fbd37a8.jpg
      - id: 31536
        filter: actor=31536
        tag: Carla Bennett
        tagKey: 5f3fd28d03883a0040ac062e
        role: 'Palion Aide #2'
      - id: 31537
        filter: actor=31537
        tag: Peter Bou-Ghannam
        tagKey: 5f406ea5427eeb0041ee367f
        role: Palion Leader
        thumb: >-
          https://metadata-static.plex.tv/e/people/e1442a2dfe8442654806c2d6a7897a9d.jpg
      - id: 31538
        filter: actor=31538
        tag: Marienne Castro
        tagKey: 5f405c8ccae2c60042f7ac5f
        role: Shuttle Pilot
        thumb: >-
          https://metadata-static.plex.tv/0/people/07a4bbb1d2f99e444c9de59413530ceb.jpg
      - id: 31539
        filter: actor=31539
        tag: Bessie Cheng
        tagKey: 5f3fc306ce2564003f853ed9
        role: 'Eldredth Aide #2'
        thumb: >-
          https://metadata-static.plex.tv/5/people/54c80a73d51262aef9e3ab7a4c06ed6f.jpg
      - id: 31540
        filter: actor=31540
        tag: John Chou
        tagKey: 62753c184d3d1cb58e93d506
        role: 'Kiley Scientist #1'
      - id: 31541
        filter: actor=31541
        tag: Joseph Daly
        tagKey: 5f3ff78bfea1a1003f9b2369
        role: 'Eldredth Aide #1'
        thumb: >-
          https://metadata-static.plex.tv/5/people/53f78913242f64d56316ee75f341c1b2.jpg
      - id: 31542
        filter: actor=31542
        tag: Myles Dobson
        tagKey: 5d776a8f51dd69001fe250f1
        role: Vulcan Waiter
        thumb: https://metadata-static.plex.tv/people/5d776a8f51dd69001fe250f1.jpg
      - id: 31543
        filter: actor=31543
        tag: Chandra Galasso
        tagKey: 5d776b30594b2b001e6d24cd
        role: Lieutenant
        thumb: >-
          https://metadata-static.plex.tv/b/people/b88852fe91228e8f5e6c89bf8a5227b4.jpg
      - id: 31544
        filter: actor=31544
        tag: Jaimee Joe Gonzaga
        tagKey: 602d810722796e002dce6fd6
        role: 'Terminal Jockey #2'
      - id: 31545
        filter: actor=31545
        tag: Sandy Kerr
        tagKey: 5f3ff9e404a86500409ba8bd
        role: 'Starfleet Scientist #1'
      - id: 3378
        filter: actor=3378
        tag: Joel Lacoursiere
        tagKey: 5d776b32fb0d55001f55f89f
        role: 'Kiley Guard #1'
      - id: 31546
        filter: actor=31546
        tag: Dana Levenson
        tagKey: 629130c2ed685fc4708979bc
        role: Newscaster
      - id: 31547
        filter: actor=31547
        tag: Andrew Locke
        tagKey: 5f3fd0dd03883a0040abe2eb
        role: 'Terminal Jockey #1'
      - id: 31548
        filter: actor=31548
        tag: Etan Muskat
        tagKey: 5d77685f3ab0e7001f4ff787
        role: 'Starfleet Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/e/people/e5281dd2c6869adfc8c38b383f6ae3e8.jpg
      - id: 31549
        filter: actor=31549
        tag: Daniel Pagett
        tagKey: 5f4006d81ae710004102d3ae
        role: 'Kiley Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/a/people/a994871d39cc04fe6fda3de89130ab55.jpg
      - id: 31550
        filter: actor=31550
        tag: Rachel Sellan
        tagKey: 5d7768a0decfcd001f2ee614
        role: Woman in Elevator
        thumb: https://image.tmdb.org/t/p/original/1T4h8GPtXa2B3NWqzJ90whLZGvK.jpg
      - id: 31528
        filter: actor=31528
        tag: Adrian Holmes
        tagKey: 5d7768315af944001f1f8e5d
        role: Admiral Robert April
        thumb: >-
          https://metadata-static.plex.tv/8/people/847f9bd416bbeb7dfd1141508b9fce60.jpg
      - id: 31529
        filter: actor=31529
        tag: Gia Sandhu
        tagKey: 5d776b9fad5437001f7a51af
        role: T'Pring
        thumb: >-
          https://metadata-static.plex.tv/7/people/7134a5a24907c3624622f8eec68ea9b7.jpg
      - id: 31524
        filter: actor=31524
        tag: Dan Jeannotte
        tagKey: 5d7768726f4521001eaa76c0
        role: George Samuel 'Sam' Kirk
        thumb: >-
          https://metadata-static.plex.tv/0/people/061d8cd023a1a686ddbdf055cea91b5f.jpg
      - id: 31527
        filter: actor=31527
        tag: Melanie Scrofano
        tagKey: 5d77684b2e80df001ebe0e3a
        role: Captain Marie Batel
        thumb: >-
          https://metadata-static.plex.tv/c/people/cbc66df9d39f2ab6b5c35edba96721cc.jpg
      - id: 31525
        filter: actor=31525
        tag: Rong Fu
        tagKey: 5d776d9e47dd6e001f6f4b93
        role: Jenna Mitchell
        thumb: >-
          https://metadata-static.plex.tv/7/people/7593afaa022e743a3b7736dbe326a3e9.jpg
      - id: 31526
        filter: actor=31526
        tag: André Dae Kim
        tagKey: 5f401a4c03883a0040b2ae4b
        role: Chief Kyle
        thumb: >-
          https://metadata-static.plex.tv/7/people/77500e32058dbe3cea766035d600b250.jpg
      - id: 31594
        filter: actor=31594
        tag: David Kirby
        tagKey: 6308b629fbb5dda04b436928
        role: 'Palion Aide #1'
      - id: 31650
        filter: actor=31650
        tag: Jon Blair
        tagKey: 5f400f1e768fc70040549f43
        role: 'Kiley Guard #2'
    Producer:
      - id: 31789
        filter: producer=31789
        tag: Paul Gadd
        tagKey: 5e164048df4678003f524f3e
      - id: 31790
        filter: producer=31790
        tag: Andrea Raffaghello
        tagKey: 5d776cc7fb0d55001f5922a8
        thumb: >-
          https://metadata-static.plex.tv/0/people/0d1c2013efdbddf16d7ea172de7deb39.jpg

```
## Episode Scrobble
##### TV Episode is viewed (played past the 90% mark).
```yaml
payload:
  event: media.scrobble
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/8ef2ec209a71d6c7/avatar?c=1749626128
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: show
    ratingKey: '1966'
    key: /library/metadata/1966
    parentRatingKey: '1965'
    grandparentRatingKey: '1964'
    guid: plex://episode/61e8260c263955a780cf92fd
    parentGuid: plex://season/602e7abd88e0a9002dfa0c65
    grandparentGuid: plex://show/5ec75ff037d69c0039b83267
    grandparentSlug: star-trek-strange-new-worlds
    type: episode
    title: Strange New Worlds
    grandparentKey: /library/metadata/1964
    parentKey: /library/metadata/1965
    librarySectionTitle: TV
    librarySectionID: 7
    librarySectionKey: /library/sections/7
    grandparentTitle: 'Star Trek: Strange New Worlds'
    parentTitle: Season 1
    contentRating: TV-PG
    summary: >-
      When one of Pike’s officers goes missing while on a secret mission for
      Starfleet, Pike has to come out of self-imposed exile. He must navigate
      how to rescue his officer, while struggling with what to do with the
      vision of the future he’s been given.
    index: 1
    parentIndex: 1
    audienceRating: 7.5
    viewCount: 1
    skipCount: 1
    lastViewedAt: 1749681329
    year: 2022
    thumb: /library/metadata/1966/thumb/1749085463
    art: /library/metadata/1964/art/1747275883
    parentThumb: /library/metadata/1965/thumb/1733009675
    grandparentThumb: /library/metadata/1964/thumb/1747275883
    grandparentArt: /library/metadata/1964/art/1747275883
    grandparentTheme: /library/metadata/1964/theme/1747275883
    duration: 3180000
    originallyAvailableAt: '2022-05-05'
    addedAt: 1733009522
    updatedAt: 1749085463
    audienceRatingImage: themoviedb://image.rating
    chapterSource: media
    Image:
      - alt: Strange New Worlds
        type: coverPoster
        url: /library/metadata/1964/thumb/1747275883
      - alt: Strange New Worlds
        type: snapshot
        url: /library/metadata/1966/thumb/1749085463
      - alt: Strange New Worlds
        type: background
        url: /library/metadata/1964/art/1747275883
      - alt: Strange New Worlds
        type: clearLogo
        url: /library/metadata/1964/clearLogo/1747275883
    UltraBlurColors:
      topLeft: 49210d
      topRight: 5d250c
      bottomRight: '924324'
      bottomLeft: 3c2809
    Guid:
      - id: imdb://tt12330364
      - id: tmdb://3455959
      - id: tvdb://8785342
    Rating:
      - image: imdb://image.rating
        value: 8.1
        type: audience
      - image: themoviedb://image.rating
        value: 7.5
        type: audience
    Director:
      - id: 31782
        filter: director=31782
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/4/people/4b551e483c0f6e124a2b41d672808386.jpg
    Writer:
      - id: 31783
        filter: writer=31783
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/f/people/f8f7fa7c7b9e0a80f0a8a1bfb20961d0.jpg
      - id: 14215
        filter: writer=14215
        tag: Alex Kurtzman
        tagKey: 5d77682a999c64001ec2d250
        thumb: >-
          https://metadata-static.plex.tv/f/people/fa310b367421ffe27bc11a758135d751.jpg
      - id: 31784
        filter: writer=31784
        tag: Jenny Lumet
        tagKey: 5d77691a47dd6e001f6c3406
        thumb: >-
          https://metadata-static.plex.tv/5/people/5453958cc06c3dfb343a7b1e4fc4061f.jpg
    Role:
      - id: 31517
        filter: actor=31517
        tag: Anson Mount
        tagKey: 5d776833eb5d26001f1e02a7
        role: Captain Christopher Pike
        thumb: >-
          https://metadata-static.plex.tv/2/people/28cbe22261c22769cc73b861c4e96117.jpg
      - id: 31518
        filter: actor=31518
        tag: Ethan Peck
        tagKey: 5d7768535af944001f1ff612
        role: Spock
        thumb: >-
          https://metadata-static.plex.tv/b/people/b95e1c83662a27139421110fcdae9875.jpg
      - id: 31519
        filter: actor=31519
        tag: Jess Bush
        tagKey: 5d7770a17a53e9001e7a7820
        role: Christine Chapel
        thumb: >-
          https://metadata-static.plex.tv/a/people/ab53153640df8c8ed77ad2a0fd7f84e0.jpg
      - id: 24567
        filter: actor=24567
        tag: Christina Chong
        tagKey: 5d77689c3ab0e7001f505b3a
        role: La'an Noonien-Singh
        thumb: >-
          https://metadata-static.plex.tv/0/people/02a6d83b818f342308c7eb6f88d8a7a0.jpg
      - id: 31520
        filter: actor=31520
        tag: Celia Rose Gooding
        tagKey: 5f3fcc8302101b0040ed14d7
        role: Nyota Uhura
        thumb: >-
          https://metadata-static.plex.tv/7/people/72d95a6b2b1cb8dd864c417a2c5c1fca.jpg
      - id: 31521
        filter: actor=31521
        tag: Melissa Navia
        tagKey: 5d7768b5308bca0020330942
        role: Erica Ortegas
        thumb: >-
          https://metadata-static.plex.tv/d/people/d0d6d99c83ee88e134eee8514fd8f8c8.jpg
      - id: 31522
        filter: actor=31522
        tag: Babs Olusanmokun
        tagKey: 5d77691551dd69001fe14a16
        role: Dr. Joseph M'Benga
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05c1cadfb147d2af5900bf0c730c1be.jpg
      - id: 5721
        filter: actor=5721
        tag: Rebecca Romijn
        tagKey: 5d7768283c3c2a001fbcb634
        role: Una Chin-Riley
        thumb: >-
          https://metadata-static.plex.tv/7/people/7c5a72847a551338d7cc9dd5ce29e168.jpg
      - id: 31523
        filter: actor=31523
        tag: Bruce Horak
        tagKey: 5f4009aa52f20000414ec84a
        role: Hemmer
        thumb: >-
          https://metadata-static.plex.tv/3/people/3fc2ed3209f1b41eed851f7968002cd8.jpg
      - id: 18013
        filter: actor=18013
        tag: Samantha Smith
        tagKey: 5d77682a2ec6b5001f6baa0d
        role: Eldredth Leader
        thumb: >-
          https://metadata-static.plex.tv/1/people/1f6f7c1f10d6144f0f6f2c248fbd37a8.jpg
      - id: 31536
        filter: actor=31536
        tag: Carla Bennett
        tagKey: 5f3fd28d03883a0040ac062e
        role: 'Palion Aide #2'
      - id: 31537
        filter: actor=31537
        tag: Peter Bou-Ghannam
        tagKey: 5f406ea5427eeb0041ee367f
        role: Palion Leader
        thumb: >-
          https://metadata-static.plex.tv/e/people/e1442a2dfe8442654806c2d6a7897a9d.jpg
      - id: 31538
        filter: actor=31538
        tag: Marienne Castro
        tagKey: 5f405c8ccae2c60042f7ac5f
        role: Shuttle Pilot
        thumb: >-
          https://metadata-static.plex.tv/0/people/07a4bbb1d2f99e444c9de59413530ceb.jpg
      - id: 31539
        filter: actor=31539
        tag: Bessie Cheng
        tagKey: 5f3fc306ce2564003f853ed9
        role: 'Eldredth Aide #2'
        thumb: >-
          https://metadata-static.plex.tv/5/people/54c80a73d51262aef9e3ab7a4c06ed6f.jpg
      - id: 31540
        filter: actor=31540
        tag: John Chou
        tagKey: 62753c184d3d1cb58e93d506
        role: 'Kiley Scientist #1'
      - id: 31541
        filter: actor=31541
        tag: Joseph Daly
        tagKey: 5f3ff78bfea1a1003f9b2369
        role: 'Eldredth Aide #1'
        thumb: >-
          https://metadata-static.plex.tv/5/people/53f78913242f64d56316ee75f341c1b2.jpg
      - id: 31542
        filter: actor=31542
        tag: Myles Dobson
        tagKey: 5d776a8f51dd69001fe250f1
        role: Vulcan Waiter
        thumb: https://metadata-static.plex.tv/people/5d776a8f51dd69001fe250f1.jpg
      - id: 31543
        filter: actor=31543
        tag: Chandra Galasso
        tagKey: 5d776b30594b2b001e6d24cd
        role: Lieutenant
        thumb: >-
          https://metadata-static.plex.tv/b/people/b88852fe91228e8f5e6c89bf8a5227b4.jpg
      - id: 31544
        filter: actor=31544
        tag: Jaimee Joe Gonzaga
        tagKey: 602d810722796e002dce6fd6
        role: 'Terminal Jockey #2'
      - id: 31545
        filter: actor=31545
        tag: Sandy Kerr
        tagKey: 5f3ff9e404a86500409ba8bd
        role: 'Starfleet Scientist #1'
      - id: 3378
        filter: actor=3378
        tag: Joel Lacoursiere
        tagKey: 5d776b32fb0d55001f55f89f
        role: 'Kiley Guard #1'
      - id: 31546
        filter: actor=31546
        tag: Dana Levenson
        tagKey: 629130c2ed685fc4708979bc
        role: Newscaster
      - id: 31547
        filter: actor=31547
        tag: Andrew Locke
        tagKey: 5f3fd0dd03883a0040abe2eb
        role: 'Terminal Jockey #1'
      - id: 31548
        filter: actor=31548
        tag: Etan Muskat
        tagKey: 5d77685f3ab0e7001f4ff787
        role: 'Starfleet Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/e/people/e5281dd2c6869adfc8c38b383f6ae3e8.jpg
      - id: 31549
        filter: actor=31549
        tag: Daniel Pagett
        tagKey: 5f4006d81ae710004102d3ae
        role: 'Kiley Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/a/people/a994871d39cc04fe6fda3de89130ab55.jpg
      - id: 31550
        filter: actor=31550
        tag: Rachel Sellan
        tagKey: 5d7768a0decfcd001f2ee614
        role: Woman in Elevator
        thumb: https://image.tmdb.org/t/p/original/1T4h8GPtXa2B3NWqzJ90whLZGvK.jpg
      - id: 31528
        filter: actor=31528
        tag: Adrian Holmes
        tagKey: 5d7768315af944001f1f8e5d
        role: Admiral Robert April
        thumb: >-
          https://metadata-static.plex.tv/8/people/847f9bd416bbeb7dfd1141508b9fce60.jpg
      - id: 31529
        filter: actor=31529
        tag: Gia Sandhu
        tagKey: 5d776b9fad5437001f7a51af
        role: T'Pring
        thumb: >-
          https://metadata-static.plex.tv/7/people/7134a5a24907c3624622f8eec68ea9b7.jpg
      - id: 31524
        filter: actor=31524
        tag: Dan Jeannotte
        tagKey: 5d7768726f4521001eaa76c0
        role: George Samuel 'Sam' Kirk
        thumb: >-
          https://metadata-static.plex.tv/0/people/061d8cd023a1a686ddbdf055cea91b5f.jpg
      - id: 31527
        filter: actor=31527
        tag: Melanie Scrofano
        tagKey: 5d77684b2e80df001ebe0e3a
        role: Captain Marie Batel
        thumb: >-
          https://metadata-static.plex.tv/c/people/cbc66df9d39f2ab6b5c35edba96721cc.jpg
      - id: 31525
        filter: actor=31525
        tag: Rong Fu
        tagKey: 5d776d9e47dd6e001f6f4b93
        role: Jenna Mitchell
        thumb: >-
          https://metadata-static.plex.tv/7/people/7593afaa022e743a3b7736dbe326a3e9.jpg
      - id: 31526
        filter: actor=31526
        tag: André Dae Kim
        tagKey: 5f401a4c03883a0040b2ae4b
        role: Chief Kyle
        thumb: >-
          https://metadata-static.plex.tv/7/people/77500e32058dbe3cea766035d600b250.jpg
      - id: 31594
        filter: actor=31594
        tag: David Kirby
        tagKey: 6308b629fbb5dda04b436928
        role: 'Palion Aide #1'
      - id: 31650
        filter: actor=31650
        tag: Jon Blair
        tagKey: 5f400f1e768fc70040549f43
        role: 'Kiley Guard #2'
    Producer:
      - id: 31789
        filter: producer=31789
        tag: Paul Gadd
        tagKey: 5e164048df4678003f524f3e
      - id: 31790
        filter: producer=31790
        tag: Andrea Raffaghello
        tagKey: 5d776cc7fb0d55001f5922a8
        thumb: >-
          https://metadata-static.plex.tv/0/people/0d1c2013efdbddf16d7ea172de7deb39.jpg

```
## Episode Stop
##### TV Episode playback stops.
```yaml
payload:
  event: media.stop
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: show
    ratingKey: '1966'
    key: /library/metadata/1966
    parentRatingKey: '1965'
    grandparentRatingKey: '1964'
    guid: plex://episode/61e8260c263955a780cf92fd
    parentGuid: plex://season/602e7abd88e0a9002dfa0c65
    grandparentGuid: plex://show/5ec75ff037d69c0039b83267
    grandparentSlug: star-trek-strange-new-worlds
    type: episode
    title: Strange New Worlds
    grandparentKey: /library/metadata/1964
    parentKey: /library/metadata/1965
    librarySectionTitle: TV
    librarySectionID: 7
    librarySectionKey: /library/sections/7
    grandparentTitle: 'Star Trek: Strange New Worlds'
    parentTitle: Season 1
    contentRating: TV-PG
    summary: >-
      When one of Pike’s officers goes missing while on a secret mission for
      Starfleet, Pike has to come out of self-imposed exile. He must navigate
      how to rescue his officer, while struggling with what to do with the
      vision of the future he’s been given.
    index: 1
    parentIndex: 1
    audienceRating: 7.5
    skipCount: 1
    year: 2022
    thumb: /library/metadata/1966/thumb/1749085463
    art: /library/metadata/1964/art/1747275883
    parentThumb: /library/metadata/1965/thumb/1733009675
    grandparentThumb: /library/metadata/1964/thumb/1747275883
    grandparentArt: /library/metadata/1964/art/1747275883
    grandparentTheme: /library/metadata/1964/theme/1747275883
    duration: 3180000
    originallyAvailableAt: '2022-05-05'
    addedAt: 1733009522
    updatedAt: 1749085463
    audienceRatingImage: themoviedb://image.rating
    chapterSource: media
    Image:
      - alt: Strange New Worlds
        type: coverPoster
        url: /library/metadata/1964/thumb/1747275883
      - alt: Strange New Worlds
        type: snapshot
        url: /library/metadata/1966/thumb/1749085463
      - alt: Strange New Worlds
        type: background
        url: /library/metadata/1964/art/1747275883
      - alt: Strange New Worlds
        type: clearLogo
        url: /library/metadata/1964/clearLogo/1747275883
    UltraBlurColors:
      topLeft: 49210d
      topRight: 5d250c
      bottomRight: '924324'
      bottomLeft: 3c2809
    Guid:
      - id: imdb://tt12330364
      - id: tmdb://3455959
      - id: tvdb://8785342
    Rating:
      - image: imdb://image.rating
        value: 8.1
        type: audience
      - image: themoviedb://image.rating
        value: 7.5
        type: audience
    Director:
      - id: 31782
        filter: director=31782
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/4/people/4b551e483c0f6e124a2b41d672808386.jpg
    Writer:
      - id: 31783
        filter: writer=31783
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/f/people/f8f7fa7c7b9e0a80f0a8a1bfb20961d0.jpg
      - id: 14215
        filter: writer=14215
        tag: Alex Kurtzman
        tagKey: 5d77682a999c64001ec2d250
        thumb: >-
          https://metadata-static.plex.tv/f/people/fa310b367421ffe27bc11a758135d751.jpg
      - id: 31784
        filter: writer=31784
        tag: Jenny Lumet
        tagKey: 5d77691a47dd6e001f6c3406
        thumb: >-
          https://metadata-static.plex.tv/5/people/5453958cc06c3dfb343a7b1e4fc4061f.jpg
    Role:
      - id: 31517
        filter: actor=31517
        tag: Anson Mount
        tagKey: 5d776833eb5d26001f1e02a7
        role: Captain Christopher Pike
        thumb: >-
          https://metadata-static.plex.tv/2/people/28cbe22261c22769cc73b861c4e96117.jpg
      - id: 31518
        filter: actor=31518
        tag: Ethan Peck
        tagKey: 5d7768535af944001f1ff612
        role: Spock
        thumb: >-
          https://metadata-static.plex.tv/b/people/b95e1c83662a27139421110fcdae9875.jpg
      - id: 31519
        filter: actor=31519
        tag: Jess Bush
        tagKey: 5d7770a17a53e9001e7a7820
        role: Christine Chapel
        thumb: >-
          https://metadata-static.plex.tv/a/people/ab53153640df8c8ed77ad2a0fd7f84e0.jpg
      - id: 24567
        filter: actor=24567
        tag: Christina Chong
        tagKey: 5d77689c3ab0e7001f505b3a
        role: La'an Noonien-Singh
        thumb: >-
          https://metadata-static.plex.tv/0/people/02a6d83b818f342308c7eb6f88d8a7a0.jpg
      - id: 31520
        filter: actor=31520
        tag: Celia Rose Gooding
        tagKey: 5f3fcc8302101b0040ed14d7
        role: Nyota Uhura
        thumb: >-
          https://metadata-static.plex.tv/7/people/72d95a6b2b1cb8dd864c417a2c5c1fca.jpg
      - id: 31521
        filter: actor=31521
        tag: Melissa Navia
        tagKey: 5d7768b5308bca0020330942
        role: Erica Ortegas
        thumb: >-
          https://metadata-static.plex.tv/d/people/d0d6d99c83ee88e134eee8514fd8f8c8.jpg
      - id: 31522
        filter: actor=31522
        tag: Babs Olusanmokun
        tagKey: 5d77691551dd69001fe14a16
        role: Dr. Joseph M'Benga
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05c1cadfb147d2af5900bf0c730c1be.jpg
      - id: 5721
        filter: actor=5721
        tag: Rebecca Romijn
        tagKey: 5d7768283c3c2a001fbcb634
        role: Una Chin-Riley
        thumb: >-
          https://metadata-static.plex.tv/7/people/7c5a72847a551338d7cc9dd5ce29e168.jpg
      - id: 31523
        filter: actor=31523
        tag: Bruce Horak
        tagKey: 5f4009aa52f20000414ec84a
        role: Hemmer
        thumb: >-
          https://metadata-static.plex.tv/3/people/3fc2ed3209f1b41eed851f7968002cd8.jpg
      - id: 18013
        filter: actor=18013
        tag: Samantha Smith
        tagKey: 5d77682a2ec6b5001f6baa0d
        role: Eldredth Leader
        thumb: >-
          https://metadata-static.plex.tv/1/people/1f6f7c1f10d6144f0f6f2c248fbd37a8.jpg
      - id: 31536
        filter: actor=31536
        tag: Carla Bennett
        tagKey: 5f3fd28d03883a0040ac062e
        role: 'Palion Aide #2'
      - id: 31537
        filter: actor=31537
        tag: Peter Bou-Ghannam
        tagKey: 5f406ea5427eeb0041ee367f
        role: Palion Leader
        thumb: >-
          https://metadata-static.plex.tv/e/people/e1442a2dfe8442654806c2d6a7897a9d.jpg
      - id: 31538
        filter: actor=31538
        tag: Marienne Castro
        tagKey: 5f405c8ccae2c60042f7ac5f
        role: Shuttle Pilot
        thumb: >-
          https://metadata-static.plex.tv/0/people/07a4bbb1d2f99e444c9de59413530ceb.jpg
      - id: 31539
        filter: actor=31539
        tag: Bessie Cheng
        tagKey: 5f3fc306ce2564003f853ed9
        role: 'Eldredth Aide #2'
        thumb: >-
          https://metadata-static.plex.tv/5/people/54c80a73d51262aef9e3ab7a4c06ed6f.jpg
      - id: 31540
        filter: actor=31540
        tag: John Chou
        tagKey: 62753c184d3d1cb58e93d506
        role: 'Kiley Scientist #1'
      - id: 31541
        filter: actor=31541
        tag: Joseph Daly
        tagKey: 5f3ff78bfea1a1003f9b2369
        role: 'Eldredth Aide #1'
        thumb: >-
          https://metadata-static.plex.tv/5/people/53f78913242f64d56316ee75f341c1b2.jpg
      - id: 31542
        filter: actor=31542
        tag: Myles Dobson
        tagKey: 5d776a8f51dd69001fe250f1
        role: Vulcan Waiter
        thumb: https://metadata-static.plex.tv/people/5d776a8f51dd69001fe250f1.jpg
      - id: 31543
        filter: actor=31543
        tag: Chandra Galasso
        tagKey: 5d776b30594b2b001e6d24cd
        role: Lieutenant
        thumb: >-
          https://metadata-static.plex.tv/b/people/b88852fe91228e8f5e6c89bf8a5227b4.jpg
      - id: 31544
        filter: actor=31544
        tag: Jaimee Joe Gonzaga
        tagKey: 602d810722796e002dce6fd6
        role: 'Terminal Jockey #2'
      - id: 31545
        filter: actor=31545
        tag: Sandy Kerr
        tagKey: 5f3ff9e404a86500409ba8bd
        role: 'Starfleet Scientist #1'
      - id: 3378
        filter: actor=3378
        tag: Joel Lacoursiere
        tagKey: 5d776b32fb0d55001f55f89f
        role: 'Kiley Guard #1'
      - id: 31546
        filter: actor=31546
        tag: Dana Levenson
        tagKey: 629130c2ed685fc4708979bc
        role: Newscaster
      - id: 31547
        filter: actor=31547
        tag: Andrew Locke
        tagKey: 5f3fd0dd03883a0040abe2eb
        role: 'Terminal Jockey #1'
      - id: 31548
        filter: actor=31548
        tag: Etan Muskat
        tagKey: 5d77685f3ab0e7001f4ff787
        role: 'Starfleet Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/e/people/e5281dd2c6869adfc8c38b383f6ae3e8.jpg
      - id: 31549
        filter: actor=31549
        tag: Daniel Pagett
        tagKey: 5f4006d81ae710004102d3ae
        role: 'Kiley Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/a/people/a994871d39cc04fe6fda3de89130ab55.jpg
      - id: 31550
        filter: actor=31550
        tag: Rachel Sellan
        tagKey: 5d7768a0decfcd001f2ee614
        role: Woman in Elevator
        thumb: https://image.tmdb.org/t/p/original/1T4h8GPtXa2B3NWqzJ90whLZGvK.jpg
      - id: 31528
        filter: actor=31528
        tag: Adrian Holmes
        tagKey: 5d7768315af944001f1f8e5d
        role: Admiral Robert April
        thumb: >-
          https://metadata-static.plex.tv/8/people/847f9bd416bbeb7dfd1141508b9fce60.jpg
      - id: 31529
        filter: actor=31529
        tag: Gia Sandhu
        tagKey: 5d776b9fad5437001f7a51af
        role: T'Pring
        thumb: >-
          https://metadata-static.plex.tv/7/people/7134a5a24907c3624622f8eec68ea9b7.jpg
      - id: 31524
        filter: actor=31524
        tag: Dan Jeannotte
        tagKey: 5d7768726f4521001eaa76c0
        role: George Samuel 'Sam' Kirk
        thumb: >-
          https://metadata-static.plex.tv/0/people/061d8cd023a1a686ddbdf055cea91b5f.jpg
      - id: 31527
        filter: actor=31527
        tag: Melanie Scrofano
        tagKey: 5d77684b2e80df001ebe0e3a
        role: Captain Marie Batel
        thumb: >-
          https://metadata-static.plex.tv/c/people/cbc66df9d39f2ab6b5c35edba96721cc.jpg
      - id: 31525
        filter: actor=31525
        tag: Rong Fu
        tagKey: 5d776d9e47dd6e001f6f4b93
        role: Jenna Mitchell
        thumb: >-
          https://metadata-static.plex.tv/7/people/7593afaa022e743a3b7736dbe326a3e9.jpg
      - id: 31526
        filter: actor=31526
        tag: André Dae Kim
        tagKey: 5f401a4c03883a0040b2ae4b
        role: Chief Kyle
        thumb: >-
          https://metadata-static.plex.tv/7/people/77500e32058dbe3cea766035d600b250.jpg
      - id: 31594
        filter: actor=31594
        tag: David Kirby
        tagKey: 6308b629fbb5dda04b436928
        role: 'Palion Aide #1'
      - id: 31650
        filter: actor=31650
        tag: Jon Blair
        tagKey: 5f400f1e768fc70040549f43
        role: 'Kiley Guard #2'
    Producer:
      - id: 31789
        filter: producer=31789
        tag: Paul Gadd
        tagKey: 5e164048df4678003f524f3e
      - id: 31790
        filter: producer=31790
        tag: Andrea Raffaghello
        tagKey: 5d776cc7fb0d55001f5922a8
        thumb: >-
          https://metadata-static.plex.tv/0/people/0d1c2013efdbddf16d7ea172de7deb39.jpg

```
## Track Play
##### Music Track starts playing.
```yaml
payload:
  event: media.play
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: artist
    ratingKey: '17955'
    key: /library/metadata/17955
    parentRatingKey: '17950'
    grandparentRatingKey: '17949'
    guid: plex://track/5d07cdb3403c640290f4d455
    parentGuid: plex://album/5d07c1e5403c6402908857d5
    grandparentGuid: plex://artist/5d07bc02403c6402904aa2a7
    parentStudio: Capitol Records
    type: track
    title: Hollywood Nights
    grandparentKey: /library/metadata/17949
    parentKey: /library/metadata/17950
    librarySectionTitle: Music
    librarySectionID: 8
    librarySectionKey: /library/sections/8
    grandparentTitle: Bob Seger & the Silver Bullet Band
    parentTitle: Greatest Hits
    summary: ''
    index: 5
    parentIndex: 1
    ratingCount: 33577
    userRating: 10
    viewCount: 11
    lastViewedAt: 1749541487
    lastRatedAt: 1749049902
    parentYear: 1994
    thumb: /library/metadata/17950/thumb/1747412353
    art: /library/metadata/17949/art/1749608188
    parentThumb: /library/metadata/17950/thumb/1747412353
    grandparentThumb: /library/metadata/17949/thumb/1749608188
    grandparentArt: /library/metadata/17949/art/1749608188
    addedAt: 1747412346
    updatedAt: 1748915428
    Image:
      - alt: Hollywood Nights
        type: coverPoster
        url: /library/metadata/17949/thumb/1749608188
      - alt: Hollywood Nights
        type: background
        url: /library/metadata/17949/art/1749608188
    Genre:
      - id: 38623
        filter: genre=38623
        tag: Pop/Rock
    Guid:
      - id: mbid://08f9ed5a-1c38-387d-9491-9cea9805a479
    Mood:
      - id: 39303
        filter: mood=39303
        tag: Earthy
      - id: 39107
        filter: mood=39107
        tag: Earnest
      - id: 38631
        filter: mood=38631
        tag: Passionate
      - id: 39696
        filter: mood=39696
        tag: Hungry
```
## Track Pause
##### Music Track playback pauses.
```yaml
payload:
  event: media.pause
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: artist
    ratingKey: '17955'
    key: /library/metadata/17955
    parentRatingKey: '17950'
    grandparentRatingKey: '17949'
    guid: plex://track/5d07cdb3403c640290f4d455
    parentGuid: plex://album/5d07c1e5403c6402908857d5
    grandparentGuid: plex://artist/5d07bc02403c6402904aa2a7
    parentStudio: Capitol Records
    type: track
    title: Hollywood Nights
    grandparentKey: /library/metadata/17949
    parentKey: /library/metadata/17950
    librarySectionTitle: Music
    librarySectionID: 8
    librarySectionKey: /library/sections/8
    grandparentTitle: Bob Seger & the Silver Bullet Band
    parentTitle: Greatest Hits
    summary: ''
    index: 5
    parentIndex: 1
    ratingCount: 33577
    userRating: 10
    viewCount: 11
    lastViewedAt: 1749541487
    lastRatedAt: 1749049902
    parentYear: 1994
    thumb: /library/metadata/17950/thumb/1747412353
    art: /library/metadata/17949/art/1749608188
    parentThumb: /library/metadata/17950/thumb/1747412353
    grandparentThumb: /library/metadata/17949/thumb/1749608188
    grandparentArt: /library/metadata/17949/art/1749608188
    addedAt: 1747412346
    updatedAt: 1748915428
    Image:
      - alt: Hollywood Nights
        type: coverPoster
        url: /library/metadata/17949/thumb/1749608188
      - alt: Hollywood Nights
        type: background
        url: /library/metadata/17949/art/1749608188
    Genre:
      - id: 38623
        filter: genre=38623
        tag: Pop/Rock
    Guid:
      - id: mbid://08f9ed5a-1c38-387d-9491-9cea9805a479
    Mood:
      - id: 39303
        filter: mood=39303
        tag: Earthy
      - id: 39107
        filter: mood=39107
        tag: Earnest
      - id: 38631
        filter: mood=38631
        tag: Passionate
      - id: 39696
        filter: mood=39696
        tag: Hungry
```
## Track Resume
##### Music Track playback resumes.
```yaml
payload:
  event: media.resume
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: artist
    ratingKey: '17955'
    key: /library/metadata/17955
    parentRatingKey: '17950'
    grandparentRatingKey: '17949'
    guid: plex://track/5d07cdb3403c640290f4d455
    parentGuid: plex://album/5d07c1e5403c6402908857d5
    grandparentGuid: plex://artist/5d07bc02403c6402904aa2a7
    parentStudio: Capitol Records
    type: track
    title: Hollywood Nights
    grandparentKey: /library/metadata/17949
    parentKey: /library/metadata/17950
    librarySectionTitle: Music
    librarySectionID: 8
    librarySectionKey: /library/sections/8
    grandparentTitle: Bob Seger & the Silver Bullet Band
    parentTitle: Greatest Hits
    summary: ''
    index: 5
    parentIndex: 1
    ratingCount: 33577
    userRating: 10
    viewCount: 11
    lastViewedAt: 1749541487
    lastRatedAt: 1749049902
    parentYear: 1994
    thumb: /library/metadata/17950/thumb/1747412353
    art: /library/metadata/17949/art/1749608188
    parentThumb: /library/metadata/17950/thumb/1747412353
    grandparentThumb: /library/metadata/17949/thumb/1749608188
    grandparentArt: /library/metadata/17949/art/1749608188
    addedAt: 1747412346
    updatedAt: 1748915428
    Image:
      - alt: Hollywood Nights
        type: coverPoster
        url: /library/metadata/17949/thumb/1749608188
      - alt: Hollywood Nights
        type: background
        url: /library/metadata/17949/art/1749608188
    Genre:
      - id: 38623
        filter: genre=38623
        tag: Pop/Rock
    Guid:
      - id: mbid://08f9ed5a-1c38-387d-9491-9cea9805a479
    Mood:
      - id: 39303
        filter: mood=39303
        tag: Earthy
      - id: 39107
        filter: mood=39107
        tag: Earnest
      - id: 38631
        filter: mood=38631
        tag: Passionate
      - id: 39696
        filter: mood=39696
        tag: Hungry
```
## Track Scrobble
##### Music Track is played (played past the 90% mark).
```yaml
payload:
  event: media.scrobble
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/8ef2ec209a71d6c7/avatar?c=1749626128
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: artist
    ratingKey: '17955'
    key: /library/metadata/17955
    parentRatingKey: '17950'
    grandparentRatingKey: '17949'
    guid: plex://track/5d07cdb3403c640290f4d455
    parentGuid: plex://album/5d07c1e5403c6402908857d5
    grandparentGuid: plex://artist/5d07bc02403c6402904aa2a7
    parentStudio: Capitol Records
    type: track
    title: Hollywood Nights
    grandparentKey: /library/metadata/17949
    parentKey: /library/metadata/17950
    librarySectionTitle: Music
    librarySectionID: 8
    librarySectionKey: /library/sections/8
    grandparentTitle: Bob Seger & the Silver Bullet Band
    parentTitle: Greatest Hits
    summary: ''
    index: 5
    parentIndex: 1
    ratingCount: 33577
    userRating: 10
    viewCount: 12
    lastViewedAt: 1749681668
    lastRatedAt: 1749049902
    parentYear: 1994
    thumb: /library/metadata/17950/thumb/1747412353
    art: /library/metadata/17949/art/1749608188
    parentThumb: /library/metadata/17950/thumb/1747412353
    grandparentThumb: /library/metadata/17949/thumb/1749608188
    grandparentArt: /library/metadata/17949/art/1749608188
    addedAt: 1747412346
    updatedAt: 1748915428
    Image:
      - alt: Hollywood Nights
        type: coverPoster
        url: /library/metadata/17949/thumb/1749608188
      - alt: Hollywood Nights
        type: background
        url: /library/metadata/17949/art/1749608188
    Genre:
      - id: 38623
        filter: genre=38623
        tag: Pop/Rock
    Guid:
      - id: mbid://08f9ed5a-1c38-387d-9491-9cea9805a479
    Mood:
      - id: 39303
        filter: mood=39303
        tag: Earthy
      - id: 39107
        filter: mood=39107
        tag: Earnest
      - id: 38631
        filter: mood=38631
        tag: Passionate
      - id: 39696
        filter: mood=39696
        tag: Hungry
```
## Track Stop
##### Music Track playback stops.
```yaml
payload:
  event: media.stop
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: artist
    ratingKey: '17955'
    key: /library/metadata/17955
    parentRatingKey: '17950'
    grandparentRatingKey: '17949'
    guid: plex://track/5d07cdb3403c640290f4d455
    parentGuid: plex://album/5d07c1e5403c6402908857d5
    grandparentGuid: plex://artist/5d07bc02403c6402904aa2a7
    parentStudio: Capitol Records
    type: track
    title: Hollywood Nights
    grandparentKey: /library/metadata/17949
    parentKey: /library/metadata/17950
    librarySectionTitle: Music
    librarySectionID: 8
    librarySectionKey: /library/sections/8
    grandparentTitle: Bob Seger & the Silver Bullet Band
    parentTitle: Greatest Hits
    summary: ''
    index: 5
    parentIndex: 1
    ratingCount: 33577
    userRating: 10
    viewCount: 11
    lastViewedAt: 1749541487
    lastRatedAt: 1749049902
    parentYear: 1994
    thumb: /library/metadata/17950/thumb/1747412353
    art: /library/metadata/17949/art/1749608188
    parentThumb: /library/metadata/17950/thumb/1747412353
    grandparentThumb: /library/metadata/17949/thumb/1749608188
    grandparentArt: /library/metadata/17949/art/1749608188
    addedAt: 1747412346
    updatedAt: 1748915428
    Image:
      - alt: Hollywood Nights
        type: coverPoster
        url: /library/metadata/17949/thumb/1749608188
      - alt: Hollywood Nights
        type: background
        url: /library/metadata/17949/art/1749608188
    Genre:
      - id: 38623
        filter: genre=38623
        tag: Pop/Rock
    Guid:
      - id: mbid://08f9ed5a-1c38-387d-9491-9cea9805a479
    Mood:
      - id: 39303
        filter: mood=39303
        tag: Earthy
      - id: 39107
        filter: mood=39107
        tag: Earnest
      - id: 38631
        filter: mood=38631
        tag: Passionate
      - id: 39696
        filter: mood=39696
        tag: Hungry
```
## Item Added Movie

```yaml
payload:
  event: library.new
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Metadata:
    librarySectionType: movie
    ratingKey: '18152'
    key: /library/metadata/18152
    guid: plex://movie/5d776827eb5d26001f1ddabb
    slug: airplane
    studio: Paramount Pictures
    type: movie
    title: Airplane!
    librarySectionTitle: Films
    librarySectionID: 6
    librarySectionKey: /library/sections/6
    contentRating: PG
    summary: >-
      After the crew becomes sick with food poisoning, a neurotic ex-fighter
      pilot must safely land a commercial airplane full of passengers.
    rating: 9.7
    audienceRating: 8.9
    skipCount: 1
    year: 1980
    tagline: >-
      What's slower than a speeding bullet, and able to hit tall buildings at a
      single bound?
    thumb: /library/metadata/18152/thumb/1749770354
    art: /library/metadata/18152/art/1749770354
    duration: 5280000
    originallyAvailableAt: '1980-07-02'
    addedAt: 1749766735
    updatedAt: 1749770354
    audienceRatingImage: rottentomatoes://image.rating.upright
    chapterSource: media
    primaryExtraKey: /library/metadata/18153
    ratingImage: rottentomatoes://image.rating.ripe
    Image:
      - alt: Airplane!
        type: coverPoster
        url: /library/metadata/18152/thumb/1749770354
      - alt: Airplane!
        type: background
        url: /library/metadata/18152/art/1749770354
      - alt: Airplane!
        type: clearLogo
        url: /library/metadata/18152/clearLogo/1749770354
    UltraBlurColors:
      topLeft: 0c3149
      topRight: 1e5c7e
      bottomRight: 2d628a
      bottomLeft: 115c93
    Genre:
      - id: 126
        filter: genre=126
        tag: Comedy
        count: 262
    Country:
      - id: 87
        filter: country=87
        tag: United States of America
        count: 470
    Guid:
      - id: imdb://tt0080339
      - id: tmdb://813
      - id: tvdb://406
    Rating:
      - image: imdb://image.rating
        value: 7.7
        type: audience
        count: 501
      - image: rottentomatoes://image.rating.ripe
        value: 9.7
        type: critic
        count: 330
      - image: rottentomatoes://image.rating.upright
        value: 8.9
        type: audience
        count: 411
      - image: themoviedb://image.rating
        value: 7.3
        type: audience
        count: 508
    Director:
      - id: 22402
        filter: director=22402
        tag: Jim Abrahams
        tagKey: 5d776828eb5d26001f1ddb97
        thumb: >-
          https://metadata-static.plex.tv/7/people/7b17201fbeca9bfa2f3d3fbf6db5e753.jpg
      - id: 22400
        filter: director=22400
        tag: Jerry Zucker
        tagKey: 5d7768256f4521001ea98a0a
        thumb: >-
          https://metadata-static.plex.tv/f/people/f4e12ff72aba96844d66aeabb6e7d68e.jpg
      - id: 22401
        filter: director=22401
        tag: David Zucker
        tagKey: 5d776828eb5d26001f1ddb98
        thumb: https://image.tmdb.org/t/p/original/13iJccfZeC0X9WZgJnlI7ZphL7l.jpg
    Writer:
      - id: 22404
        filter: writer=22404
        tag: David Zucker
        tagKey: 5d776828eb5d26001f1ddb98
        thumb: https://image.tmdb.org/t/p/original/13iJccfZeC0X9WZgJnlI7ZphL7l.jpg
      - id: 22403
        filter: writer=22403
        tag: Jim Abrahams
        tagKey: 5d776828eb5d26001f1ddb97
        thumb: >-
          https://metadata-static.plex.tv/7/people/7b17201fbeca9bfa2f3d3fbf6db5e753.jpg
      - id: 22405
        filter: writer=22405
        tag: Jerry Zucker
        tagKey: 5d7768256f4521001ea98a0a
        thumb: >-
          https://metadata-static.plex.tv/f/people/f4e12ff72aba96844d66aeabb6e7d68e.jpg
    Role:
      - id: 22406
        filter: actor=22406
        tag: Robert Hays
        tagKey: 5d776828eb5d26001f1ddb9a
        role: Ted Striker
        thumb: >-
          https://metadata-static.plex.tv/0/people/0bac16e6db1cfead355c429a091b1f50.jpg
      - id: 22407
        filter: actor=22407
        tag: Julie Hagerty
        tagKey: 5d776828eb5d26001f1ddb9b
        role: Elaine Dickinson
        thumb: >-
          https://metadata-static.plex.tv/b/people/b71c8c523d9afc7e97bc44bae95e285e.jpg
      - id: 1725
        filter: actor=1725
        tag: Leslie Nielsen
        tagKey: 5d7768275af944001f1f6bad
        count: 2
        role: Dr. Rumack
        thumb: >-
          https://metadata-static.plex.tv/3/people/3359e49de055499bb1991c22bfb403a8.jpg
      - id: 22408
        filter: actor=22408
        tag: Kareem Abdul-Jabbar
        tagKey: 5d776828eb5d26001f1ddb9c
        role: Roger Murdock
        thumb: >-
          https://metadata-static.plex.tv/d/people/d6b0790d29b4f6c3519602a5d237c774.jpg
      - id: 22409
        filter: actor=22409
        tag: Lloyd Bridges
        tagKey: 5d776825151a60001f24a479
        role: Steve McCroskey
        thumb: >-
          https://metadata-static.plex.tv/3/people/3c27ffb2c44f48c53c64c91ce4a56da8.jpg
      - id: 18976
        filter: actor=18976
        tag: Peter Graves
        tagKey: 5d776827961905001eb914a6
        count: 2
        role: Capt. Clarence Oveur
        thumb: >-
          https://metadata-static.plex.tv/7/people/72ef3ad0e67326d595d1e9b141bd2bfe.jpg
      - id: 22410
        filter: actor=22410
        tag: Lorna Patterson
        tagKey: 5d776828eb5d26001f1ddb9d
        role: Randy
        thumb: >-
          https://metadata-static.plex.tv/d/people/de845f61bdd0b365c7a001e07a918db4.jpg
      - id: 22411
        filter: actor=22411
        tag: Robert Stack
        tagKey: 5d776826e6d55c002040aff5
        role: Captain Rex Kramer
        thumb: >-
          https://metadata-static.plex.tv/8/people/8ea3b1ef5316723a35fad296ee9ec020.jpg
      - id: 22412
        filter: actor=22412
        tag: Jim Abrahams
        tagKey: 5d776828eb5d26001f1ddb97
        role: 'Religious Zealot #6'
        thumb: >-
          https://metadata-static.plex.tv/7/people/7b17201fbeca9bfa2f3d3fbf6db5e753.jpg
      - id: 19286
        filter: actor=19286
        tag: Jonathan Banks
        tagKey: 5d776825999c64001ec2bf76
        count: 3
        role: Gunderson
        thumb: >-
          https://metadata-static.plex.tv/a/people/a7d5cb022aba167c6da8a92dfc88c55b.jpg
      - id: 22413
        filter: actor=22413
        tag: Stephen Stucker
        tagKey: 5d776828eb5d26001f1ddb9e
        role: Johnny Henshaw-Jacobs
        thumb: >-
          https://metadata-static.plex.tv/e/people/eb2e3a87da4470362f9e814a2aae4b9f.jpg
      - id: 22414
        filter: actor=22414
        tag: Frank Ashmore
        tagKey: 5d776828eb5d26001f1ddb9f
        role: Victor Basta
        thumb: https://metadata-static.plex.tv/people/5d776828eb5d26001f1ddb9f.jpg
      - id: 22415
        filter: actor=22415
        tag: Craig Berenson
        tagKey: 5d776828eb5d26001f1ddba0
        role: Paul Carey
        thumb: https://image.tmdb.org/t/p/original/dStEJ7OSMy7Tg4qlyAIuCfJ2J52.jpg
      - id: 22416
        filter: actor=22416
        tag: Barbara Billingsley
        tagKey: 5d776828eb5d26001f1ddba1
        role: Jive Lady
        thumb: >-
          https://metadata-static.plex.tv/8/people/840cd9c4eed166e5904466c9d1dec60c.jpg
      - id: 22417
        filter: actor=22417
        tag: Lee Bryant
        tagKey: 5d776828eb5d26001f1ddba2
        role: Mrs. Hammen
        thumb: https://metadata-static.plex.tv/people/5d776828eb5d26001f1ddba2.jpg
      - id: 22418
        filter: actor=22418
        tag: Joyce Bulifant
        tagKey: 5d776828eb5d26001f1ddba3
        role: Mrs. Davis
        thumb: >-
          https://metadata-static.plex.tv/6/people/66486971d0913d3377a423624dad33b4.jpg
      - id: 22419
        filter: actor=22419
        tag: Mae E. Campbell
        tagKey: 5d776828eb5d26001f1ddba4
        role: Security Lady
      - id: 22420
        filter: actor=22420
        tag: Ethel Merman
        tagKey: 5d776828eb5d26001f1ddba5
        role: Lieutenant Hurwitz
        thumb: >-
          https://metadata-static.plex.tv/f/people/f46ac9f546a104e4f6ea9ce6549df5c3.jpg
      - id: 22421
        filter: actor=22421
        tag: Jimmie Walker
        tagKey: 5d776828eb5d26001f1ddba6
        role: Windshield Wiper Man
        thumb: >-
          https://metadata-static.plex.tv/c/people/c923e00ba16f92703ed975ae08b5b0ed.jpg
      - id: 22422
        filter: actor=22422
        tag: Jill Whelan
        tagKey: 5d776828eb5d26001f1ddba7
        role: Lisa Davis
        thumb: >-
          https://metadata-static.plex.tv/8/people/80385da1d42066aaa23458821a3be481.jpg
      - id: 22423
        filter: actor=22423
        tag: Nora Meerbaum
        tagKey: 5d776828eb5d26001f1ddba9
        role: Cocaine Lady
        thumb: >-
          https://metadata-static.plex.tv/6/people/6066e28d1b55c8f4388ed2f44fbf0ee9.jpg
      - id: 20717
        filter: actor=20717
        tag: Kenneth Tobey
        tagKey: 5d776828eb5d26001f1ddbaa
        count: 2
        role: Air Controller Neubauer
        thumb: >-
          https://metadata-static.plex.tv/7/people/7b7b468577b1511f3a19771f009d92dc.jpg
      - id: 1194
        filter: actor=1194
        tag: James Hong
        tagKey: 5d7768245af944001f1f635e
        count: 3
        role: Japanese General
        thumb: >-
          https://metadata-static.plex.tv/8/people/8fe5cc1942a0836184be91251c6de0a9.jpg
      - id: 22424
        filter: actor=22424
        tag: Michelle Stacy
        tagKey: 5d776828eb5d26001f1ddbab
        role: Young Girl with Coffee
        thumb: >-
          https://metadata-static.plex.tv/f/people/f2e0b4c417396750dd5c03aa06884978.jpg
      - id: 22425
        filter: actor=22425
        tag: David Leisure
        tagKey: 5d77682b103a2d001f565823
        role: First Krishna
        thumb: >-
          https://metadata-static.plex.tv/8/people/83b83ef9071abed8dd38dbeaea98e316.jpg
      - id: 22426
        filter: actor=22426
        tag: Ann Nelson
        tagKey: 5d77682ee6d55c002040bd72
        role: Hanging Lady
        thumb: >-
          https://metadata-static.plex.tv/e/people/eb14fec940712d8fab68883b37ec0879.jpg
      - id: 10790
        filter: actor=10790
        tag: Al White
        tagKey: 5d77682b103a2d001f565829
        count: 2
        role: Second Jive Dude
        thumb: https://metadata-static.plex.tv/people/5d77682b103a2d001f565829.jpg
      - id: 4077
        filter: actor=4077
        tag: Nicholas Pryor
        tagKey: 5d7768288718ba001e31219a
        count: 2
        role: Mr. Hammen
        thumb: >-
          https://metadata-static.plex.tv/b/people/b0a9f1005211dbccf023d14222bc2278.jpg
      - id: 22427
        filter: actor=22427
        tag: Cyril O'Reilly
        tagKey: 5d77683f999c64001ec31486
        role: Soldier
        thumb: >-
          https://metadata-static.plex.tv/7/people/77d141e9ceb4ac2e070b6d72893f4a2b.jpg
      - id: 22428
        filter: actor=22428
        tag: Ted Chapman
        tagKey: 5d776c72f617c90020181a0b
        role: Airport Steward
      - id: 22429
        filter: actor=22429
        tag: Jesse Emmett
        tagKey: 5d7768dd47dd6e001f6bf958
        role: Man from India
      - id: 22430
        filter: actor=22430
        tag: Norman Alexander Gibbs
        tagKey: 5d77683854f42c001f8c4f80
        role: First Jive Dude
      - id: 22431
        filter: actor=22431
        tag: Amy Gibson
        tagKey: 5e1659d7cd0850003b7821c4
        role: Soldier's Girl
      - id: 22432
        filter: actor=22432
        tag: Marcy Goldman
        tagKey: 5d77686cfb0d55001f50fe8b
        role: Mrs. Geline
        thumb: >-
          https://metadata-static.plex.tv/d/people/dd0ce8ce5dd05c54b922b8de2b0c860f.jpg
      - id: 22433
        filter: actor=22433
        tag: Bob Gorman
        tagKey: 609d55fd479b83002c1967a1
        role: Striped Controller
      - id: 22434
        filter: actor=22434
        tag: Rossie Harris
        tagKey: 5d7768476f4521001ea9fa34
        role: Joey
      - id: 22435
        filter: actor=22435
        tag: Maurice Hill
        tagKey: 5d7768a27e5fa10020bf2ee9
        role: 'Reporter #3'
      - id: 22436
        filter: actor=22436
        tag: David Hollander
        tagKey: 5d7768747a53e9001e6cf30f
        role: Young Boy with Coffee
      - id: 22437
        filter: actor=22437
        tag: Howard Honig
        tagKey: 5d7768ab7a53e9001e6d5c5d
        role: Jack
      - id: 11209
        filter: actor=11209
        tag: Gregory Itzin
        tagKey: 5d77682a5af944001f1f778b
        count: 2
        role: 'Religious Zealot #1'
        thumb: >-
          https://metadata-static.plex.tv/f/people/fbd7973f474aac8e039b46227db83471.jpg
      - id: 22438
        filter: actor=22438
        tag: Howard Jarvis
        tagKey: 609d55fea57eac002d51c0e4
        role: Man in Taxi
      - id: 22439
        filter: actor=22439
        tag: Michael Laurence
        tagKey: 5d77685e33f255001e8541eb
        role: Newscaster
        thumb: >-
          https://metadata-static.plex.tv/f/people/fe5368c01b6bcafed2383894f7a02a71.jpg
      - id: 22440
        filter: actor=22440
        tag: Zachary Lewis
        tagKey: 63240928f26ffb4da8250a54
        role: 'Religious Zealot #3'
      - id: 22441
        filter: actor=22441
        tag: Barbara Mallory
        tagKey: 5d77698196b655001fdd08a7
        role: 'Religious Zealot #2'
      - id: 22442
        filter: actor=22442
        tag: Maureen McGovern
        tagKey: 5d77683f999c64001ec31580
        role: Nun
        thumb: >-
          https://metadata-static.plex.tv/8/people/8d3f5c21d76293030079cc576c6daa51.jpg
      - id: 22443
        filter: actor=22443
        tag: Mary Mercier
        tagKey: 5d7768b33ab0e7001f508422
        role: Shirley
      - id: 22444
        filter: actor=22444
        tag: Len Mooy
        tagKey: 609d55fef9c732002d9de25b
        role: 'Reporter #1'
      - id: 22445
        filter: actor=22445
        tag: Laura Nix
        tagKey: 609d55fefc2561002c98124e
        role: Mrs. Hurwitz
      - id: 22446
        filter: actor=22446
        tag: John O'Leary
        tagKey: 5d7768288718ba001e31211e
        role: 'Reporter #2'
        thumb: >-
          https://metadata-static.plex.tv/c/people/cdc031bf3085e790f4eb3c0a1072b258.jpg
      - id: 22447
        filter: actor=22447
        tag: Bill Porter
        tagKey: 609d55ff43cd6f002c7210f3
        role: Hospital Contortionist
      - id: 22448
        filter: actor=22448
        tag: Conrad E. Palmisano
        tagKey: 5d7768447228e5001f1e0cff
        role: 'Religious Zealot #4'
        thumb: https://metadata-static.plex.tv/people/5d7768447228e5001f1e0cff.jpg
      - id: 22449
        filter: actor=22449
        tag: Mallory Sandler
        tagKey: 5d776ef17a53e9001e7876e7
        role: L.A. Ticket Agent
      - id: 22450
        filter: actor=22450
        tag: Robert Starr
        tagKey: 5d77683854f42c001f8c4f33
        role: 'Religious Zealot #5'
        thumb: >-
          https://metadata-static.plex.tv/b/people/b6c3b1a3d28d8e6eda4261ab4b65ed08.jpg
      - id: 22451
        filter: actor=22451
        tag: Barbara Stuart
        tagKey: 5d7768618718ba001e31a58e
        role: Mrs. Kramer
        thumb: https://metadata-static.plex.tv/people/5d7768618718ba001e31a58e.jpg
      - id: 22452
        filter: actor=22452
        tag: Lee Terri
        tagKey: 5d77685933f255001e85373c
        role: Mrs. Oveur
      - id: 22453
        filter: actor=22453
        tag: William Tregoe
        tagKey: 5d7768cf23d5a3001f4f1ba3
        role: Jack Kirkpatrick
        thumb: >-
          https://metadata-static.plex.tv/4/people/4fcf08522e4e83b96c0b20b8c5ec6943.jpg
      - id: 22454
        filter: actor=22454
        tag: Hatsuo Uda
        tagKey: 5d776a8596b655001fdf0df6
        role: Japanese Newscaster
      - id: 22455
        filter: actor=22455
        tag: Herb Voland
        tagKey: 5d7768456f4521001ea9f3d0
        role: Air Controller Macias
        thumb: >-
          https://metadata-static.plex.tv/9/people/931b29f675769772c7d46773aecf3c28.jpg
      - id: 22456
        filter: actor=22456
        tag: John David Wilder
        tagKey: 5e16577a316a39003efa3eed
        role: Second Krishna
      - id: 22457
        filter: actor=22457
        tag: Windy
        tagKey: 609d55feafdd9b002ce95288
        role: Horse
      - id: 13399
        filter: actor=13399
        tag: Jason Wingreen
        tagKey: 5d77682a880197001ec918fb
        count: 3
        role: Dr. Brody
        thumb: >-
          https://metadata-static.plex.tv/f/people/f09011c8dc07391893debc5e57074506.jpg
      - id: 22458
        filter: actor=22458
        tag: Louise Yaffe
        tagKey: 5d7768606f4521001eaa42e6
        role: Mrs. Jaffe
      - id: 22459
        filter: actor=22459
        tag: Charlotte Zucker
        tagKey: 5d77682c880197001ec91ddf
        role: Make-up Lady
        thumb: https://image.tmdb.org/t/p/original/tiUqL5WuVvzMMFmxDTHkXWvF6o3.jpg
      - id: 22460
        filter: actor=22460
        tag: David Zucker
        tagKey: 5d776828eb5d26001f1ddb98
        role: 'Ground Crewman #2'
        thumb: https://image.tmdb.org/t/p/original/13iJccfZeC0X9WZgJnlI7ZphL7l.jpg
      - id: 22461
        filter: actor=22461
        tag: Jerry Zucker
        tagKey: 5d7768256f4521001ea98a0a
        role: 'Ground Crewman #1'
        thumb: >-
          https://metadata-static.plex.tv/f/people/f4e12ff72aba96844d66aeabb6e7d68e.jpg
      - id: 22462
        filter: actor=22462
        tag: Kitten Natividad
        tagKey: 5d776828eb5d26001f1ddba8
        role: Bouncy Topless Woman on Plane (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/d/people/d4eff2d756de0cca592e29e7659650ce.jpg
      - id: 22463
        filter: actor=22463
        tag: Larry Blake
        tagKey: 5dce6a5b8958c50020b56517
        role: Upside-Down Man (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/3/people/3f73d67a92864915f4850fc1ef468de1.jpg
      - id: 22464
        filter: actor=22464
        tag: Paula Moody
        tagKey: 5f3fb33d8642250042795b64
        role: Girl Scout In Bar (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/4/people/49fab1c783547fa4d429887bb25bbf98.jpg
      - id: 22465
        filter: actor=22465
        tag: Sandra Lee Gimpel
        tagKey: 5d7769fff617c90020167ade
        role: Girl Scout In Bar (uncredited)
        thumb: https://metadata-static.plex.tv/people/5d7769fff617c90020167ade.jpg
      - id: 22466
        filter: actor=22466
        tag: Henry Wills
        tagKey: 5d77682d2e80df001ebdd690
        role: Commuter on Baggage Carousel (uncredited)
        thumb: https://metadata-static.plex.tv/people/5d77682d2e80df001ebdd690.jpg
      - id: 22467
        filter: actor=22467
        tag: Joyce Mandel
        tagKey: 5d77683161141d001fb14b83
        role: Woman on Flight (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/6/people/6416c2ff958342bb51e99feae228d4af.jpg
      - id: 12426
        filter: actor=12426
        tag: Gene LeBell
        tagKey: 5d776827880197001ec90a73
        count: 3
        role: Religious Zealot (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/5/people/53f623deb51a1be86bf45518d715d465.jpg
      - id: 22468
        filter: actor=22468
        tag: Susan Breslau
        tagKey: 5d7768256f4521001ea98a1a
        role: Ticket Agent (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/b/people/bd28faef5d9ecd2d8b5a19729d04f6e9.jpg
    Producer:
      - id: 22498
        filter: producer=22498
        tag: Jon Davison
        tagKey: 5d776827151a60001f24ac10
    Field:
      - locked: true
        name: thumb
```
## Item Added Show

```yaml
payload:
  event: library.new
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Metadata:
    librarySectionType: show
    ratingKey: '2018'
    key: /library/metadata/2018/children
    guid: plex://show/5d9c081b7b5c2e001e654a03
    slug: veep
    studio: HBO
    type: show
    title: Veep
    librarySectionTitle: TV
    librarySectionID: 7
    librarySectionKey: /library/sections/7
    contentRating: TV-MA
    summary: >-
      A look into American politics, revolving around former Senator Selina
      Meyer who finds being Vice President of the United States is nothing like
      she expected and everything everyone ever warned her about.
    index: 1
    audienceRating: 7.4
    year: 2012
    tagline: The buck stops somewhere near here.
    thumb: /library/metadata/2018/thumb/1747275885
    art: /library/metadata/2018/art/1747275885
    theme: /library/metadata/2018/theme/1747275885
    duration: 1800000
    originallyAvailableAt: '2012-04-22'
    leafCount: 58
    viewedLeafCount: 0
    childCount: 6
    addedAt: 1733009546
    updatedAt: 1747275885
    audienceRatingImage: themoviedb://image.rating
    Image:
      - alt: Veep
        type: coverPoster
        url: /library/metadata/2018/thumb/1747275885
      - alt: Veep
        type: background
        url: /library/metadata/2018/art/1747275885
      - alt: Veep
        type: clearLogo
        url: /library/metadata/2018/clearLogo/1747275885
    UltraBlurColors:
      topLeft: '243033'
      topRight: 0d6687
      bottomRight: 45392e
      bottomLeft: 625c56
    Genre:
      - id: 126
        filter: genre=126
        tag: Comedy
    Country:
      - id: 87
        filter: country=87
        tag: United States of America
    Guid:
      - id: imdb://tt1759761
      - id: tmdb://2947
      - id: tvdb://237831
    Rating:
      - image: imdb://image.rating
        value: 8.4
        type: audience
      - image: rottentomatoes://image.rating.ripe
        value: 9.3
        type: critic
      - image: rottentomatoes://image.rating.upright
        value: 8.9
        type: audience
      - image: themoviedb://image.rating
        value: 7.4
        type: audience
    Role:
      - id: 4066
        filter: actor=4066
        tag: Julia Louis-Dreyfus
        tagKey: 5d7768275af944001f1f6ec8
        role: Selina Meyer
        thumb: >-
          https://metadata-static.plex.tv/6/people/648b8a419407acd8f532afffc9cc66d7.jpg
      - id: 32118
        filter: actor=32118
        tag: Anna Chlumsky
        tagKey: 5d77682c151a60001f24bf5b
        role: Amy Brookheimer
        thumb: >-
          https://metadata-static.plex.tv/0/people/0dab2222a5681038356005f511477d77.jpg
      - id: 9407
        filter: actor=9407
        tag: Tony Hale
        tagKey: 5d776829151a60001f24b164
        role: Gary Walsh
        thumb: >-
          https://metadata-static.plex.tv/1/people/1883a13b479a06453aa63e1e96364b4a.jpg
      - id: 13106
        filter: actor=13106
        tag: Reid Scott
        tagKey: 5d7768f0fb0d55001f51d6cc
        role: Dan Egan
        thumb: https://metadata-static.plex.tv/people/5d7768f0fb0d55001f51d6cc.jpg
      - id: 7268
        filter: actor=7268
        tag: Timothy Simons
        tagKey: 5d7769ea594b2b001e6add48
        role: Jonah Ryan
        thumb: >-
          https://metadata-static.plex.tv/5/people/5e67a75914d9291adf69ea46d03f9d79.jpg
      - id: 20628
        filter: actor=20628
        tag: Matt Walsh
        tagKey: 5d77682f6f4521001ea9ad83
        role: Mike McLintock
        thumb: >-
          https://metadata-static.plex.tv/2/people/29a9fc980b03d69bd2ba100c6883a49d.jpg
      - id: 24136
        filter: actor=24136
        tag: Gary Cole
        tagKey: 5d77682a961905001eb91e4b
        role: Kent Davison
        thumb: >-
          https://metadata-static.plex.tv/5/people/514ed7d32aebd3124b3920ec9196b9d6.jpg
      - id: 10545
        filter: actor=10545
        tag: Kevin Dunn
        tagKey: 5d7768285af944001f1f7223
        role: Ben Cafferty
        thumb: >-
          https://metadata-static.plex.tv/f/people/f9e50abd944a9639e37e09d68b7e7766.jpg
      - id: 16575
        filter: actor=16575
        tag: Sufe Bradshaw
        tagKey: 5d77683beb5d26001f1e1f2a
        role: Sue Wilson
        thumb: >-
          https://metadata-static.plex.tv/b/people/b8a54bef7201f1e763273f44b1b0dded.jpg
      - id: 32119
        filter: actor=32119
        tag: Sarah Sutherland
        tagKey: 5d776a4b51dd69001fe21ffc
        role: Catherine Meyer
        thumb: https://metadata-static.plex.tv/people/5d776a4b51dd69001fe21ffc.jpg
      - id: 7287
        filter: actor=7287
        tag: Sam Richardson
        tagKey: 5d77687b23d5a3001f4ecda8
        role: Richard Splett
        thumb: >-
          https://metadata-static.plex.tv/c/people/c5e2175f74607fcba445873fb46fb62a.jpg
      - id: 32120
        filter: actor=32120
        tag: Clea DuVall
        tagKey: 5d7768263c3c2a001fbcafc2
        role: Marjorie Palmiotti
        thumb: >-
          https://metadata-static.plex.tv/e/people/eebf6665848ec56cf6487d9fed6093b6.jpg
      - id: 32121
        filter: actor=32121
        tag: Dan Bakkedahl
        tagKey: 5d7769a1ad5437001f762b08
        role: Roger Furlong
        thumb: >-
          https://metadata-static.plex.tv/d/people/d289ace525c49b73a75c264ebb0a11b7.jpg
      - id: 15348
        filter: actor=15348
        tag: Diedrich Bader
        tagKey: 5d776826eb5d26001f1dd577
        role: Bill Ericsson
        thumb: >-
          https://metadata-static.plex.tv/4/people/45e14e119f64ec3a595a2077cc7affbb.jpg
      - id: 23777
        filter: actor=23777
        tag: Phil Reeves
        tagKey: 5d7768342ec6b5001f6bbda0
        role: Andrew Doyle
        thumb: >-
          https://metadata-static.plex.tv/8/people/84067623ba43ecdac274ecf7159cc751.jpg
      - id: 17254
        filter: actor=17254
        tag: Hugh Laurie
        tagKey: 5d776829103a2d001f564c5a
        role: Tom James
        thumb: >-
          https://metadata-static.plex.tv/0/people/0ed174d86ee4823c05c3cb4e71b1367e.jpg
      - id: 16807
        filter: actor=16807
        tag: Nelson Franklin
        tagKey: 5d77683f103a2d001f56a420
        role: Will
        thumb: >-
          https://metadata-static.plex.tv/3/people/36feede4a79f17c7a23f2cc4b04380b0.jpg
      - id: 22739
        filter: actor=22739
        tag: Brian Huskey
        tagKey: 5d7768327228e5001f1de168
        role: Leon West
        thumb: >-
          https://metadata-static.plex.tv/c/people/cd5aabb796694536359b8e850a2f2351.jpg
      - id: 16267
        filter: actor=16267
        tag: David Pasquesi
        tagKey: 5d776825880197001ec90541
        role: Andrew Meyer
        thumb: >-
          https://metadata-static.plex.tv/4/people/496b6e4b0b9754be25670c09515cf9ed.jpg
      - id: 7975
        filter: actor=7975
        tag: Randall Park
        tagKey: 5d77685585719b001f3a92c5
        role: Danny Chung
        thumb: >-
          https://metadata-static.plex.tv/7/people/702bd7002b650f2e21bce64ae4c25e7a.jpg
      - id: 32122
        filter: actor=32122
        tag: Peter Grosz
        tagKey: 5d776829151a60001f24b169
        role: Sidney Purcell
        thumb: >-
          https://metadata-static.plex.tv/4/people/4b8501456dbef2e56ff4beb243a228f8.jpg
      - id: 26725
        filter: actor=26725
        tag: Matt Oberg
        tagKey: 5d7768881999bc0020dc8411
        role: Buddy Calhoun
        thumb: >-
          https://metadata-static.plex.tv/e/people/ec80ff151a167ab205eb3ac148270b6c.jpg
      - id: 4632
        filter: actor=4632
        tag: Kathy Najimy
        tagKey: 5d77682654c0f0001f301ba8
        role: Wendy Keegan
        thumb: >-
          https://metadata-static.plex.tv/f/people/f2005e454422f73b74ee9c0b48d57f6f.jpg
      - id: 323
        filter: actor=323
        tag: Patton Oswalt
        tagKey: 5d7768253c3c2a001fbcac64
        role: Teddy Sykes
        thumb: >-
          https://metadata-static.plex.tv/1/people/15b2b24619953be2c59337ca811ebc60.jpg
      - id: 26050
        filter: actor=26050
        tag: Nancy Lenehan
        tagKey: 5d7768273c3c2a001fbcb1ee
        role: Nancy Ryan
        thumb: >-
          https://metadata-static.plex.tv/8/people/832bf9ac6b1e6886f1f604147e01e300.jpg
      - id: 32123
        filter: actor=32123
        tag: Peter MacNicol
        tagKey: 5d77682861141d001fb137b9
        role: Jeff Kane
        thumb: >-
          https://metadata-static.plex.tv/e/people/e7421f7b278141e7ce39eb8a25e2439a.jpg
      - id: 22050
        filter: actor=22050
        tag: Scott Adsit
        tagKey: 5d776827eb5d26001f1dd88d
        role: Greg Hart
        thumb: >-
          https://metadata-static.plex.tv/3/people/3a5f22096b4d758590b5d6858b635907.jpg
      - id: 24743
        filter: actor=24743
        tag: Wayne Wilderson
        tagKey: 5d7768273c3c2a001fbcb29d
        role: Wayne
        thumb: >-
          https://metadata-static.plex.tv/9/people/92ac3f1586195e5b7833fc4593e65310.jpg
      - id: 32124
        filter: actor=32124
        tag: Margaret Colin
        tagKey: 5d776827880197001ec90b11
        role: Jane McCabe
        thumb: >-
          https://metadata-static.plex.tv/d/cc68393fae/people/ddc01c53ee933793eb4117580801b368.jpg
      - id: 27873
        filter: actor=27873
        tag: Paul Scheer
        tagKey: 5d7768343c3c2a001fbce1f6
        role: Stevie
        thumb: >-
          https://metadata-static.plex.tv/8/people/8f7ff910003a99e8b6c552773e61aa45.jpg
      - id: 3282
        filter: actor=3282
        tag: J.P. Manoux
        tagKey: 5d776827103a2d001f56467f
        role: Congressman Clark
        thumb: >-
          https://metadata-static.plex.tv/4/people/48d515df07e7954ad7bd291acba622d2.jpg
      - id: 28102
        filter: actor=28102
        tag: Andrea Savage
        tagKey: 5d77683d54f42c001f8c5e66
        role: Laura Montez
        thumb: >-
          https://metadata-static.plex.tv/9/people/9bbcfa1d579512eb62701cfdbbff8964.jpg
      - id: 18134
        filter: actor=18134
        tag: David Rasche
        tagKey: 5d77682e8a7581001f12ca80
        role: Jim Marwood
        thumb: >-
          https://metadata-static.plex.tv/3/people/3343bd3d0f6e25ef3605e950993416c1.jpg
      - id: 32125
        filter: actor=32125
        tag: Emily Pendergast
        tagKey: 5e1653aefef2d4003e8b49e2
        role: Beth Ryan
        thumb: >-
          https://metadata-static.plex.tv/7/people/7f3ef04f70dcc5375f3f3c509883ce7d.jpg
      - id: 32126
        filter: actor=32126
        tag: Mary Catherine Garrison
        tagKey: 5d776a259ab54400214fb4f6
        role: Sophie Brookheimer
        thumb: >-
          https://metadata-static.plex.tv/0/people/078edb73dc15147a5093562267d873d3.jpg
      - id: 32127
        filter: actor=32127
        tag: Lennon Parham
        tagKey: 5d776846f59e58002189ab57
        role: Karen Collins
        thumb: >-
          https://metadata-static.plex.tv/9/cc68393fae/people/951c841a58362f8a8ffe3f27b52d1273.jpg
      - id: 1713
        filter: actor=1713
        tag: Megan Grano
        tagKey: 5d7768e8fb0d55001f51c818
        role: Donna
        thumb: >-
          https://metadata-static.plex.tv/8/people/8df436f1743a7320fee2c45530a6fe15.jpg
      - id: 32128
        filter: actor=32128
        tag: Jonathan Hadary
        tagKey: 5d77682a880197001ec91626
        role: Sherman Tanz
        thumb: >-
          https://metadata-static.plex.tv/b/people/b0c644546562f7eb9d5c85681014e7bf.jpg
      - id: 54304
        filter: actor=54304
        tag: Isiah Whitlock, Jr.
        tagKey: 5d7768282ec6b5001f6ba63b
        role: George Maddox
        thumb: >-
          https://metadata-static.plex.tv/2/people/21da2628df91c811b731068d3b0fb21c.jpg
      - id: 12611
        filter: actor=12611
        tag: Brad Leland
        tagKey: 5d7768266f4521001ea98cc4
        role: Bill O'Brien
        thumb: >-
          https://metadata-static.plex.tv/5/people/54b8f61b8d397d6f790b43d59c5fc4b9.jpg
      - id: 27496
        filter: actor=27496
        tag: Seth Morris
        tagKey: 5d77683c2e80df001ebdefc2
        role: Bill Jaeger
        thumb: >-
          https://metadata-static.plex.tv/6/people/6200590cded0068887d4e8962aaddf7a.jpg
      - id: 1241
        filter: actor=1241
        tag: John Slattery
        tagKey: 5d7768283c3c2a001fbcb6a3
        role: Charlie Baird
        thumb: >-
          https://metadata-static.plex.tv/1/people/176e5d78b58ee4fdf6eef9e2215859d4.jpg
      - id: 18212
        filter: actor=18212
        tag: Usman Ally
        tagKey: 5d77689533f255001e85a25e
        role: Mohammed Al Jaffar
        thumb: >-
          https://metadata-static.plex.tv/d/people/d16724578f1ea8b1884adbeafb4c0f60.jpg
      - id: 32129
        filter: actor=32129
        tag: Morgan Smith
        tagKey: 5f4031ac52f2000041524599
        role: Candi Caruso
        thumb: >-
          https://metadata-static.plex.tv/b/people/bd139e2c1e31fc3afaef078dd59104a9.jpg
      - id: 26898
        filter: actor=26898
        tag: India de Beaufort
        tagKey: 5d776831103a2d001f566dfd
        role: Brie Ramachandran
        thumb: >-
          https://metadata-static.plex.tv/a/people/ab27f5c4cffc6e342789317c9f62cfc6.jpg
      - id: 10592
        filter: actor=10592
        tag: Andy Daly
        tagKey: 5d776832151a60001f24d33d
        role: Keith Quinn
        thumb: >-
          https://metadata-static.plex.tv/a/people/a9fe2b57d31485a119aa7cf9a6ba888f.jpg
      - id: 32130
        filter: actor=32130
        tag: Craig Cackowski
        tagKey: 5d776b0dad5437001f791652
        role: Cliff
        thumb: >-
          https://metadata-static.plex.tv/1/people/1e8b886dc0e6be119cfd76d3d814be1a.jpg
      - id: 32131
        filter: actor=32131
        tag: Sally Phillips
        tagKey: 5d7768263c3c2a001fbcb00e
        role: Minna H√§kkinen
        thumb: >-
          https://metadata-static.plex.tv/d/people/df5cdb1d673115bbb7f5cab822b54c60.jpg
      - id: 32132
        filter: actor=32132
        tag: Jessica Chaffin
        tagKey: 5d77687b23d5a3001f4ecda4
        role: Congresswoman Gellardi
        thumb: >-
          https://metadata-static.plex.tv/0/people/0b6acf13834d6635f2b18f04b55b218f.jpg
      - id: 32133
        filter: actor=32133
        tag: Rhea Seehorn
        tagKey: 5d776835961905001eb93d32
        role: Michelle York
        thumb: >-
          https://metadata-static.plex.tv/6/people/61e9052c76950f3b3734c96c8ae861b7.jpg
      - id: 2625
        filter: actor=2625
        tag: Deb Hiett
        tagKey: 5d776b4796b655001fe0af47
        role: White House Reporter
        thumb: >-
          https://metadata-static.plex.tv/2/people/2e6d4e175bff6f5b85f22b0db966402f.jpg
      - id: 28503
        filter: actor=28503
        tag: Mary Holland
        tagKey: 5d776b60f617c900201754af
        role: Shawnee Tanz
        thumb: >-
          https://metadata-static.plex.tv/7/people/796450235dba7a635797417fe2ace49f.jpg
      - id: 27057
        filter: actor=27057
        tag: Toks Olagundoye
        tagKey: 5d776a7e7a53e9001e706d56
        role: Kemi Talbot
        thumb: >-
          https://metadata-static.plex.tv/1/people/1448b20aee2ccf5824fe8563ec62d01c.jpg
      - id: 32134
        filter: actor=32134
        tag: William L. Thomas
        tagKey: 5d776c347a53e9001e73cb49
        role: Martin Collins
        thumb: >-
          https://metadata-static.plex.tv/b/people/ba72cdf84bc63e1aa660843eed239809.jpg
      - id: 32135
        filter: actor=32135
        tag: Craig Rhodes
        tagKey: 5d77708781ba41001faf2449
        role: Statistician
      - id: 23540
        filter: actor=23540
        tag: Lauren Bowles
        tagKey: 5d776832151a60001f24d34b
        role: Monica
        thumb: >-
          https://metadata-static.plex.tv/5/people/5f5eaeb1128d6267c0f7f3c0bd5d5677.jpg
      - id: 32136
        filter: actor=32136
        tag: Martin Mull
        tagKey: 5d776828151a60001f24aef0
        role: Bob Bradley
        thumb: >-
          https://metadata-static.plex.tv/2/people/23494efe202b359a6cc31618e703135f.jpg
      - id: 4812
        filter: actor=4812
        tag: Tzi Ma
        tagKey: 5d77682b7e9a3c0020c6b736
        role: Lu Chi-Jang
        thumb: https://metadata-static.plex.tv/people/5d77682b7e9a3c0020c6b736.jpg
      - id: 1703
        filter: actor=1703
        tag: Phil LaMarr
        tagKey: 5d776827103a2d001f564619
        role: Paul Graves
        thumb: >-
          https://metadata-static.plex.tv/e/people/e37f3a5764a078ff3c3ecbb18b32b5c8.jpg
      - id: 32137
        filter: actor=32137
        tag: Bonnie Bentley
        tagKey: 5d7768a4d11dd300202290bd
        role: Emily
        thumb: >-
          https://metadata-static.plex.tv/c/people/cbe54211de59a8c68ec0dabdbc688c50.jpg
      - id: 32138
        filter: actor=32138
        tag: Heather McPhaul
        tagKey: 5d9c0913ffd9ef001e99f3db
        role: Tracy
        thumb: >-
          https://metadata-static.plex.tv/b/people/bd467765109641ee08b36b9a4a53bbf0.jpg
      - id: 32139
        filter: actor=32139
        tag: Lee Chen
        tagKey: 5d776b5f96b655001fe0e998
        role: Translator
        thumb: https://metadata-static.plex.tv/people/5d776b5f96b655001fe0e998.jpg
      - id: 32140
        filter: actor=32140
        tag: Sloane Letourneau
        tagKey: 5f40649902101b0040fd4c35
        role: Clay
        thumb: >-
          https://metadata-static.plex.tv/5/people/5d989feab41beb84ecd8c4ec4ae27c0d.jpg
      - id: 32141
        filter: actor=32141
        tag: Winslow Corbett
        tagKey: 5ec418a424bfc80041c3c212
        role: Reporter
      - id: 32142
        filter: actor=32142
        tag: Jessie Ennis
        tagKey: 5d776a8151dd69001fe24449
        role: Leigh Patterson
        thumb: >-
          https://metadata-static.plex.tv/4/cc68393fae/people/4894cdf3c017c02325e2e396469f1e19.jpg
      - id: 32143
        filter: actor=32143
        tag: Paul Fitzgerald
        tagKey: 5d7768a1ad5437001f74b802
        role: Owen Pierce
        thumb: https://image.tmdb.org/t/p/original/3BkOYXyKqwV2VGkd2uykuB75kJk.jpg
      - id: 29689
        filter: actor=29689
        tag: Marc Unger
        tagKey: 5f3fe07186422500427d3b2a
        role: Sean
        thumb: >-
          https://metadata-static.plex.tv/1/people/11804cda8a6be8f44a535336ed850f17.jpg
      - id: 24461
        filter: actor=24461
        tag: Glenn Wrage
        tagKey: 5d7768286f4521001ea9944f
        role: Joe Thornhill
        thumb: https://metadata-static.plex.tv/people/5d7768286f4521001ea9944f.jpg
      - id: 32144
        filter: actor=32144
        tag: Jessica St. Clair
        tagKey: 5d7768377e9a3c0020c6d217
        role: Dana
        thumb: >-
          https://metadata-static.plex.tv/9/people/9cc31e2591ddbd3359db6d0bc89d020f.jpg
      - id: 32145
        filter: actor=32145
        tag: Zach Woods
        tagKey: 5d776846e6d55c002040fbf7
        role: Ed Webster
        thumb: >-
          https://metadata-static.plex.tv/7/people/70833573267487798bd66c7c683f1132.jpg
      - id: 3779
        filter: actor=3779
        tag: Evan Arnold
        tagKey: 5d7768334de0ee001fccb1af
        role: White House Reporter
        thumb: https://metadata-static.plex.tv/people/5d7768334de0ee001fccb1af.jpg
      - id: 32146
        filter: actor=32146
        tag: Zak Orth
        tagKey: 5d77682685719b001f3a0b84
        role: Jim Owens
        thumb: >-
          https://metadata-static.plex.tv/8/people/888fd28334473e48f39798fa1f4e438e.jpg
      - id: 32147
        filter: actor=32147
        tag: K Callan
        tagKey: 5d77682c85719b001f3a1dfb
        role: Judy Sherman
        thumb: >-
          https://metadata-static.plex.tv/e/people/eb14eb185a898b634919954215e689bc.jpg
      - id: 16254
        filter: actor=16254
        tag: Brian Doyle-Murray
        tagKey: 5d77682761141d001fb13609
        role: George Huntzinger
        thumb: >-
          https://metadata-static.plex.tv/6/people/6057739bf1f3e4f58fcdd007431c129c.jpg
      - id: 27102
        filter: actor=27102
        tag: Kate Burton
        tagKey: 5d77682b54c0f0001f30242b
        role: Barbara Hallowes
        thumb: >-
          https://metadata-static.plex.tv/4/people/4eb52a322e6799cb61ad9da22967a63d.jpg
      - id: 28575
        filter: actor=28575
        tag: Todd Aaron Brotze
        tagKey: 5d776aa896b655001fdf529e
        role: Dr. Abernathy
        thumb: >-
          https://metadata-static.plex.tv/9/people/9ad006e610e387ee57f297999ac66cd0.jpg
      - id: 32148
        filter: actor=32148
        tag: Lisa Robbins
        tagKey: 5f40162a1ae710004104248a
        role: Mrs. Brookheimer
      - id: 28663
        filter: actor=28663
        tag: Jean Villepique
        tagKey: 5d77683f103a2d001f56a418
        role: NY Times Reporter
        thumb: >-
          https://metadata-static.plex.tv/8/people/875fecd4dfa84a6d43caa42b8c9dbbd9.jpg
      - id: 32149
        filter: actor=32149
        tag: James Wong
        tagKey: 5d776bce9ab544002150f845
        role: Jim
      - id: 12193
        filter: actor=12193
        tag: John Carroll Lynch
        tagKey: 5d7768256f4521001ea98a37
        role: Lloyd Hennick
        thumb: >-
          https://metadata-static.plex.tv/a/people/a8ec683a5528875d5816dea8ca9e1bb8.jpg
      - id: 32150
        filter: actor=32150
        tag: Allen Rueckert
        tagKey: 5d776b70ad5437001f79fa7d
        role: Reporter Allen
        thumb: >-
          https://metadata-static.plex.tv/b/people/b6c102756c399f7ba407f8fc3cb404c3.jpg
      - id: 26578
        filter: actor=26578
        tag: Suzy Nakamura
        tagKey: 5d7768313c3c2a001fbcd552
        role: Anna
        thumb: >-
          https://metadata-static.plex.tv/0/people/04e4cf661e8f611a15e883180411776f.jpg
      - id: 32151
        filter: actor=32151
        tag: Ayden Mayeri
        tagKey: 5d776b3cfb0d55001f561050
        role: Layla
        thumb: >-
          https://metadata-static.plex.tv/4/people/40e6ed210212bab6c6cdc2d6c1d0b5f3.jpg
      - id: 32152
        filter: actor=32152
        tag: Talulah Shadrick
        tagKey: 5f406021fea1a1003fa68ea4
        role: Ellen McLintock
        thumb: >-
          https://metadata-static.plex.tv/0/people/080a740c6d8032272ee99702a99ba847.jpg
      - id: 32153
        filter: actor=32153
        tag: GiGi Erneta
        tagKey: 5d776830103a2d001f566784
        role: JoJo Weaver
        thumb: https://image.tmdb.org/t/p/original/w8yBYlqI1tihNkvzKTKYbuvYcLm.jpg
      - id: 32154
        filter: actor=32154
        tag: Courtney Friel
        tagKey: 5f3fed44cae2c60042eb0b96
        role: Fox News Reporter
        thumb: >-
          https://metadata-static.plex.tv/8/people/81e6aab98bb07e13b74543efa70ce843.jpg
      - id: 32155
        filter: actor=32155
        tag: Dutch Johnson
        tagKey: 5d776c5d96b655001fe2e2a5
        role: Rick Youngblood
        thumb: >-
          https://metadata-static.plex.tv/9/people/97a55f344a97daf09dc18be6146ca700.jpg
      - id: 32156
        filter: actor=32156
        tag: Michael Torpey
        tagKey: 5d776c6dfb0d55001f5877a3
        role: Jason
        thumb: https://metadata-static.plex.tv/people/5d776c6dfb0d55001f5877a3.jpg
      - id: 32157
        filter: actor=32157
        tag: Shari Elliker
        tagKey: 5d776e96594b2b001e728213
        role: Andrea Tandy
      - id: 32158
        filter: actor=32158
        tag: Caitlynn Leary
        tagKey: 5ec412b6b7f4f7003ea1d15f
        role: White House Staffer
        thumb: >-
          https://metadata-static.plex.tv/5/people/51c644a0d806586b6392624426c73d63.jpg
      - id: 32159
        filter: actor=32159
        tag: Robert Poletick
        tagKey: 5d776c05594b2b001e6e936b
        role: Bill
        thumb: https://metadata-static.plex.tv/people/5d776c05594b2b001e6e936b.jpg
      - id: 7437
        filter: actor=7437
        tag: Andy Buckley
        tagKey: 5d7768502ec6b5001f6bf7bb
        role: Ted Cullen
        thumb: >-
          https://metadata-static.plex.tv/f/people/f904c0740a0ebe40426c7195cd4dd8c6.jpg
      - id: 26529
        filter: actor=26529
        tag: Dana Powell
        tagKey: 5d77689851dd69001fe0e887
        role: Kelly
        thumb: >-
          https://metadata-static.plex.tv/3/people/3483ae2a755c03bbf26cdf4c1eb79cae.jpg
      - id: 32160
        filter: actor=32160
        tag: Harris Yulin
        tagKey: 5d7768262e80df001ebdce07
        role: James Whitman
        thumb: >-
          https://metadata-static.plex.tv/iva/person/2168/94f6a5d2efaedc48c17f4fe56b9ef620.jpg
      - id: 9734
        filter: actor=9734
        tag: Rose Abdoo
        tagKey: 5d77682d8718ba001e3131aa
        role: Judge
        thumb: >-
          https://metadata-static.plex.tv/d/people/d96bba3454d3b50d0a5420b68d938f1f.jpg
      - id: 12681
        filter: actor=12681
        tag: Raymond Ma
        tagKey: 5d776833999c64001ec2eeea
        role: Zhang Shengxi
        thumb: https://metadata-static.plex.tv/people/5d776833999c64001ec2eeea.jpg
      - id: 25940
        filter: actor=25940
        tag: Nigel Gibbs
        tagKey: 5d776828880197001ec90e6f
        role: Keith
        thumb: >-
          https://metadata-static.plex.tv/c/people/c11103bcdf4218c855327be50eaf979c.jpg
      - id: 32161
        filter: actor=32161
        tag: Sumalee Montano
        tagKey: 5d7768502ec6b5001f6bf67a
        role: Joyce Cafferty
        thumb: >-
          https://metadata-static.plex.tv/f/people/fb5696ad79ddd32266efcbbd4e456596.jpg
      - id: 32162
        filter: actor=32162
        tag: Meredith Hagner
        tagKey: 5d7768c9ebdf2200209c8b2a
        role: Debralee
        thumb: >-
          https://metadata-static.plex.tv/3/people/3cfba1c1e6aa0b408edd07ae32ce6657.jpg
      - id: 32163
        filter: actor=32163
        tag: Hector Hugo
        tagKey: 5d77688351dd69001fe0d64a
        role: Alejandro Montez
        thumb: >-
          https://metadata-static.plex.tv/e/people/e5868cfe8133d522a0774ca26a37ac3c.jpg
      - id: 12869
        filter: actor=12869
        tag: Rick Overton
        tagKey: 5d7768268a7581001f12be17
        role: Congressman Spencer
        thumb: >-
          https://metadata-static.plex.tv/6/people/609578bf34652b77df2e4af591d3df47.jpg
      - id: 32164
        filter: actor=32164
        tag: Abbey DiGregorio
        tagKey: 5d7768692e80df001ebe361f
        role: Dr. Walcott
        thumb: https://metadata-static.plex.tv/people/5d7768692e80df001ebe361f.jpg
      - id: 32165
        filter: actor=32165
        tag: Wil Love
        tagKey: 5d776852eb5d26001f1e60d1
        role: Phillip Dorsey
      - id: 32166
        filter: actor=32166
        tag: Chike Johnson
        tagKey: 5d77682e7e9a3c0020c6bb1a
        role: Secret Service
        thumb: https://metadata-static.plex.tv/people/5d77682e7e9a3c0020c6bb1a.jpg
      - id: 32167
        filter: actor=32167
        tag: Jon Barinholtz
        tagKey: 5d7770469ab5440021534126
        role: O'Brien Aide
        thumb: >-
          https://metadata-static.plex.tv/5/people/5d2e50d16e94e5c3948f8ea1759af597.jpg
      - id: 32168
        filter: actor=32168
        tag: Hazel Anne Raymundo
        tagKey: 5d9f3551d5fd3f001ee1638c
        role: Reporter
      - id: 14141
        filter: actor=14141
        tag: Bob Rumnock
        tagKey: 5d77683261141d001fb14ede
        role: Election Official
        thumb: https://metadata-static.plex.tv/people/5d77683261141d001fb14ede.jpg
      - id: 32169
        filter: actor=32169
        tag: Jill Donnelly
        tagKey: 5d776a087a53e9001e6f82a0
        role: Mary
        thumb: >-
          https://metadata-static.plex.tv/c/people/cf1ba8b55a38f29e6145a3b1b7b964bd.jpg
      - id: 30190
        filter: actor=30190
        tag: Mike Hernandez
        tagKey: 5d77708631d95e001f1a396b
        role: Justice
      - id: 32170
        filter: actor=32170
        tag: Kelly Frazier
        tagKey: 5f3ff9e604a86500409ba8d3
        role: Deputy Press Secretary
        thumb: >-
          https://metadata-static.plex.tv/c/people/cdd709b44297d9dbf6841ff78867c96c.jpg
      - id: 24177
        filter: actor=24177
        tag: Shannon Welles
        tagKey: 5d77685433f255001e852eb2
        role: Catherine Eaton
      - id: 32171
        filter: actor=32171
        tag: Gita Pullapilly
        tagKey: 5d776852eb5d26001f1e611d
        role: News Anchor
        thumb: >-
          https://metadata-static.plex.tv/f/people/f9f8ccae35bffa1a5deb7d2af532098b.jpg
      - id: 27643
        filter: actor=27643
        tag: Wayne Alon Scott
        tagKey: 5d776c6596b655001fe2f426
        role: Sound Guy
        thumb: https://metadata-static.plex.tv/people/5d776c6596b655001fe2f426.jpg
      - id: 10582
        filter: actor=10582
        tag: Eugene Alper
        tagKey: 5d776b2296b655001fe057bb
        role: Murman Shalikashvili
        thumb: https://metadata-static.plex.tv/people/5d776b2296b655001fe057bb.jpg
      - id: 20975
        filter: actor=20975
        tag: Eugene Cordero
        tagKey: 5d77686761141d001fb19f3c
        role: Buzzy Kanahale
        thumb: >-
          https://metadata-static.plex.tv/7/people/74b288569f667b6b5ce0609b3ee8dad9.jpg
      - id: 32172
        filter: actor=32172
        tag: Crystal Hayes
        tagKey: 5f3fd72c02101b0040ee118f
        role: Alethia James
        thumb: >-
          https://metadata-static.plex.tv/1/people/1d7a39ccc37d9c3d8c4540748215b586.jpg
      - id: 25011
        filter: actor=25011
        tag: Toby Huss
        tagKey: 5d77682685719b001f3a0b36
        role: Quartie Sturges
        thumb: >-
          https://metadata-static.plex.tv/5/people/509ed12e58df0a98fecaa39fc8643afa.jpg
      - id: 12943
        filter: actor=12943
        tag: Julie Mun
        tagKey: 5d7768883ab0e7001f503dc5
        role: Reader
      - id: 32173
        filter: actor=32173
        tag: Jill Basey
        tagKey: 5d7768b551dd69001fe0fca2
        role: ''
        thumb: >-
          https://metadata-static.plex.tv/4/people/490358e2a34d5457e927b57acba21df1.jpg
      - id: 32174
        filter: actor=32174
        tag: Ian Roberts
        tagKey: 62fb7cb8443e060f7ad9453f
        role: Governor John DeVito
        thumb: >-
          https://metadata-static.plex.tv/9/people/9449f8020616aaee2c96c1146ad2a0bd.jpg
      - id: 11206
        filter: actor=11206
        tag: Troy Evans
        tagKey: 5d77682a5af944001f1f778a
        role: Montana Congressman
        thumb: >-
          https://metadata-static.plex.tv/c/people/c9131a9a011023c95c9e89570cdf1ce8.jpg
      - id: 32175
        filter: actor=32175
        tag: Melanie Nicholls-King
        tagKey: 5d7768810ea56a001e2a65e4
        role: Ms. Bennett
        thumb: >-
          https://metadata-static.plex.tv/a/people/af4261d14cdbaa2fc48299f59b0272cb.jpg
      - id: 32176
        filter: actor=32176
        tag: Ethan Phillips
        tagKey: 5d77682a151a60001f24b490
        role: Mr. Wallace
        thumb: https://metadata-static.plex.tv/people/5d77682a151a60001f24b490.jpg
      - id: 32177
        filter: actor=32177
        tag: David Beach
        tagKey: 5d77682b999c64001ec2d6b4
        role: Mr. Rakes
      - id: 32178
        filter: actor=32178
        tag: Juliet Adair Pritner
        tagKey: 5d776b6696b655001fe0f9a4
        role: Mrs. Brewer
        thumb: >-
          https://metadata-static.plex.tv/6/people/6b0ad075076f52afdd59d83a0b2c7f16.jpg
      - id: 32179
        filter: actor=32179
        tag: Michael Pemberton
        tagKey: 5d7768e996b655001fdc50ac
        role: Dexter
        thumb: https://metadata-static.plex.tv/people/5d7768e996b655001fdc50ac.jpg
      - id: 32180
        filter: actor=32180
        tag: Ellen Adair
        tagKey: 5e166bccd92d86003d37df9f
        role: Reporter
        thumb: >-
          https://metadata-static.plex.tv/6/people/641c39542659e327fc9abf4c59d11aa5.jpg
      - id: 32181
        filter: actor=32181
        tag: Scott Swope
        tagKey: 5eea5ca261112f003f1fb7a3
        role: Factory Worker
        thumb: >-
          https://metadata-static.plex.tv/d/people/d49b8b0db81cd996bd08f543796fa98a.jpg
      - id: 32182
        filter: actor=32182
        tag: Seth Barrish
        tagKey: 5d77682c85719b001f3a1e91
        role: Ben Haim
        thumb: >-
          https://metadata-static.plex.tv/6/people/6624c22738142ec77037a75533b8baa3.jpg
      - id: 32183
        filter: actor=32183
        tag: Andrew Ballard
        tagKey: 5f4029b6ce2564003f8ea268
        role: Reporter
      - id: 32184
        filter: actor=32184
        tag: Aaron Miller
        tagKey: 5f4038d31ae7100041076afa
        role: ''
      - id: 32185
        filter: actor=32185
        tag: Mimi Kennedy
        tagKey: 5d7768327228e5001f1de16f
        role: Mary King
        thumb: >-
          https://metadata-static.plex.tv/6/people/653a58c8f6a55b0b2d2896ccd72fa105.jpg
      - id: 32186
        filter: actor=32186
        tag: Andrew Barth
        tagKey: 5d776b46594b2b001e6d4f74
        role: ''
      - id: 32187
        filter: actor=32187
        tag: Marybeth Wise
        tagKey: 5f3fb8bf864225004279c8eb
        role: Janet
      - id: 12799
        filter: actor=12799
        tag: Christopher Meloni
        tagKey: 5d7768254de0ee001fcc8151
        role: Ray Whelans
        thumb: >-
          https://metadata-static.plex.tv/d/people/dffc8ca1df7366e4d14abd7816f785cc.jpg
      - id: 32188
        filter: actor=32188
        tag: Kevin O'Rourke
        tagKey: 5d77682b85719b001f3a1b8e
        role: Blake Stewart
        thumb: https://metadata-static.plex.tv/people/5d77682b85719b001f3a1b8e.jpg
      - id: 32189
        filter: actor=32189
        tag: Regen Wilson
        tagKey: 5d7769e8fb0d55001f53409a
        role: Press Guy
        thumb: >-
          https://metadata-static.plex.tv/3/people/38a798a30ce3032e76d5b16293e48f3a.jpg
      - id: 32190
        filter: actor=32190
        tag: Chris Perillo
        tagKey: 5f3ff0c8ce2564003f895303
        role: Staffer
      - id: 32191
        filter: actor=32191
        tag: Jayson Ward Williams
        tagKey: 5f89c4390a9dfa002d85bc9a
        role: Staffer
        thumb: https://metadata-static.plex.tv/people/5f89c4390a9dfa002d85bc9a.jpg
      - id: 32192
        filter: actor=32192
        tag: Eugene Young
        tagKey: 5e163d6bfef2d4003e8a0761
        role: Reggie
        thumb: >-
          https://metadata-static.plex.tv/c/people/c08d78bcd112ac448713eeb29e1cbdda.jpg
      - id: 32193
        filter: actor=32193
        tag: Christopher Moynihan
        tagKey: 5d77683d2e80df001ebdf294
        role: ''
        thumb: >-
          https://metadata-static.plex.tv/1/people/152ad5d9f6f57c46dc50a19127ca8731.jpg
      - id: 32194
        filter: actor=32194
        tag: Azhar Khan
        tagKey: 5d7770de31d95e001f1aba3a
        role: Sound Guy
        thumb: >-
          https://metadata-static.plex.tv/8/people/860d809c8ddea5bbd34969cb46785739.jpg
      - id: 32195
        filter: actor=32195
        tag: Matthew J.R. Bishop
        tagKey: 62fb8698518a7c45581f4df6
        role: Shaun
      - id: 32196
        filter: actor=32196
        tag: Leo Solomon
        tagKey: 5d7768686f4521001eaa5cd1
        role: Rahim
      - id: 32197
        filter: actor=32197
        tag: Ed Jewett
        tagKey: 5d77682a2ec6b5001f6baa31
        role: General Mercer
      - id: 2799
        filter: actor=2799
        tag: Patrick McDade
        tagKey: 5d7768274de0ee001fcc8dad
        role: Mr. Brookheimer
        thumb: >-
          https://metadata-static.plex.tv/3/people/36421ae81198a0d90c0482ecd8ee1125.jpg
      - id: 32198
        filter: actor=32198
        tag: Jon Norman Schneider
        tagKey: 5d77684d103a2d001f56c8d0
        role: Reporter
        thumb: >-
          https://metadata-static.plex.tv/c/people/c4c993f1cc1ed73cdd70c973b5e1ea27.jpg
      - id: 32199
        filter: actor=32199
        tag: Eddie Jones
        tagKey: 5d776827eb5d26001f1dd883
        role: Chuck Furnam
        thumb: https://metadata-static.plex.tv/people/5d776827eb5d26001f1dd883.jpg
      - id: 1957
        filter: actor=1957
        tag: Priyanga Burford
        tagKey: 5d7768342ec6b5001f6bbd9b
        role: Reporter
        thumb: >-
          https://metadata-static.plex.tv/3/people/3e0e05fa7c40d05d64358abd9f4c6abc.jpg
      - id: 29119
        filter: actor=29119
        tag: Phil Abrams
        tagKey: 5d77683c7e9a3c0020c6e201
        role: Rabbi
        thumb: https://image.tmdb.org/t/p/original/e6iHjKAYJjS7rYvAQU2eR9uoS9L.jpg
      - id: 27528
        filter: actor=27528
        tag: Andrew Leeds
        tagKey: 5d776836999c64001ec2f773
        role: Jackson
        thumb: >-
          https://metadata-static.plex.tv/3/people/3b8c607e03d90e382517fbc7793223c2.jpg
      - id: 32200
        filter: actor=32200
        tag: Ella Jay Basco
        tagKey: 5d776d9f594b2b001e70db57
        role: Ella
        thumb: >-
          https://metadata-static.plex.tv/0/people/04f62c52140ff79b0b641959b353b0ce.jpg
      - id: 32201
        filter: actor=32201
        tag: Sarayu Blue
        tagKey: 5d77685c7a53e9001e6ce033
        role: Dr. Mirpuri
        thumb: >-
          https://metadata-static.plex.tv/5/people/5d65f14d9dc3731c116f34c1a8984c53.jpg
      - id: 19625
        filter: actor=19625
        tag: Jim O'Heir
        tagKey: 5d7768adf617c9002015748f
        role: Mr. Brookheimer
        thumb: >-
          https://metadata-static.plex.tv/2/people/29e0f12b2cc2e6bd177680538c26f806.jpg
      - id: 28500
        filter: actor=28500
        tag: Jamie Denbo
        tagKey: 5d776835961905001eb94143
        role: Focus Group Leader
        thumb: >-
          https://metadata-static.plex.tv/2/people/264c7d86142eadb3fa8d4709501a75d1.jpg
      - id: 25330
        filter: actor=25330
        tag: Todd Jeffries
        tagKey: 5d77686b51dd69001fe0bc51
        role: Focus Group Member
        thumb: >-
          https://metadata-static.plex.tv/a/people/a2dbbffccb446cf03d022b84400fd44d.jpg
      - id: 32202
        filter: actor=32202
        tag: John Ross Bowie
        tagKey: 5d776829103a2d001f564cd4
        role: Focus Group Member
        thumb: >-
          https://metadata-static.plex.tv/5/people/57faf05aa0e7a99063ecec278eff7cf9.jpg
      - id: 10892
        filter: actor=10892
        tag: Rod McLachlan
        tagKey: 5d7768253c3c2a001fbcac71
        role: ''
        thumb: >-
          https://metadata-static.plex.tv/c/people/caec72186c8286eab5b0c0f130de601e.jpg
      - id: 32203
        filter: actor=32203
        tag: Concetta Tomei
        tagKey: 5d776830961905001eb92fef
        role: Connie DiBenedetto
        thumb: >-
          https://metadata-static.plex.tv/f/people/fd69ce907f5bf70e3c64acab05d245ad.jpg
      - id: 26579
        filter: actor=26579
        tag: Stephnie Weir
        tagKey: 5d77683c6f4521001ea9d61b
        role: Penny Nickerson
        thumb: >-
          https://metadata-static.plex.tv/e/people/e7ab94eff041d4ed36dd3e35e3cdb62f.jpg
      - id: 32204
        filter: actor=32204
        tag: Jim Titus
        tagKey: 5e163570ef1040003f24b8cf
        role: Reporter
        thumb: >-
          https://metadata-static.plex.tv/3/people/32f18b009178d18c8c178db2d70a5cb8.jpg
      - id: 32205
        filter: actor=32205
        tag: J. Anthony Pena
        tagKey: 5d776a0cad5437001f7705fd
        role: Stage Manager
        thumb: https://metadata-static.plex.tv/people/5d776a0cad5437001f7705fd.jpg
      - id: 32206
        filter: actor=32206
        tag: Tim Baltz
        tagKey: 5d776b5e7a53e9001e72383f
        role: Craig Jergensen
        thumb: >-
          https://metadata-static.plex.tv/9/people/9cc6b1ae8000463ff9581510676e28e8.jpg
      - id: 32207
        filter: actor=32207
        tag: Ben Cook
        tagKey: 5d776b9e96b655001fe16f12
        role: Walt
        thumb: >-
          https://metadata-static.plex.tv/e/people/ee6be432280f733f06e7dd2d8e75af94.jpg
      - id: 32208
        filter: actor=32208
        tag: Buckley Sampson
        tagKey: 5d7768bb431c830024c14ab5
        role: ''
        thumb: >-
          https://metadata-static.plex.tv/6/people/65c5b47a128e18d15327da27d7560af3.jpg
      - id: 22306
        filter: actor=22306
        tag: DeMark Thompson
        tagKey: 5d776e8b9ab5440021529875
        role: Air Force Major
        thumb: >-
          https://metadata-static.plex.tv/7/people/7444e221a6e9a7e1de58ecf2a994f381.jpg
      - id: 32209
        filter: actor=32209
        tag: Brey Chanadet
        tagKey: 5ec4235adf7e8e00412206f0
        role: ''
        thumb: >-
          https://metadata-static.plex.tv/3/people/3bb758465a6e7b0c38967da00482f027.jpg
      - id: 32210
        filter: actor=32210
        tag: David DeBoy
        tagKey: 5d776a2b23d5a3001f5013bb
        role: Bob Jeffries
      - id: 32211
        filter: actor=32211
        tag: Timothy Hayes Lynch
        tagKey: 5f3fab61cae2c60042e5c5b5
        role: Mike Dudley
      - id: 32212
        filter: actor=32212
        tag: Michael Mack
        tagKey: 5d77691df617c9002015d76e
        role: Paul Burton
      - id: 32213
        filter: actor=32213
        tag: Kevin Murray
        tagKey: 5d776858880197001ec99985
        role: Sam
        thumb: >-
          https://metadata-static.plex.tv/e/people/e8f4d364f64a7d4a9f291bfad95678f4.jpg
      - id: 32214
        filter: actor=32214
        tag: Kirk Penberthy
        tagKey: 5d9f34f9e4fc29001eb64e42
        role: Introducing Senator
      - id: 32215
        filter: actor=32215
        tag: Dan Franko
        tagKey: 5d776bc396b655001fe1b19b
        role: Eric
        thumb: >-
          https://metadata-static.plex.tv/4/people/4757d10a2227022460cfc1d6d04806f7.jpg
      - id: 32216
        filter: actor=32216
        tag: Tara Garwood
        tagKey: 5d77685b5af944001f200768
        role: White House Staffer
      - id: 27202
        filter: actor=27202
        tag: Brent Jennings
        tagKey: 5d7768316f4521001ea9b4e7
        role: Anthony Holland
        thumb: >-
          https://metadata-static.plex.tv/1/people/1fdf24b0c9c9fd26ea43faaf65c30278.jpg
      - id: 32217
        filter: actor=32217
        tag: Cedric Stewart
        tagKey: 5d776c9bad5437001f7c33f3
        role: Presidential Officer
        thumb: >-
          https://metadata-static.plex.tv/f/people/fdc440d13ee68bc676757eed753131df.jpg
      - id: 32218
        filter: actor=32218
        tag: Geraldine Waters
        tagKey: 5f401ef95a76a80042d505f3
        role: Maria Holland
      - id: 32219
        filter: actor=32219
        tag: Patsy Grady Abrams
        tagKey: 5d9f34ffd74e6700200203f7
        role: Mrs. Reeves
        thumb: https://image.tmdb.org/t/p/original/e5JHYzv2DKu6G9b8BPfMmT0XioM.jpg
      - id: 32220
        filter: actor=32220
        tag: Alison Anne Daniels
        tagKey: 5f4014d0c63b480040dd617f
        role: Carol Hallowes
      - id: 32221
        filter: actor=32221
        tag: Michael J. Lyons
        tagKey: 5f3fab61ce2564003f839210
        role: Jim Wiseman
        thumb: >-
          https://metadata-static.plex.tv/7/people/7c09b886fb002a0c871fe2c786acb9ad.jpg
      - id: 32222
        filter: actor=32222
        tag: Cormac Bluestone
        tagKey: 5d776d4696b655001fe44990
        role: Reporter
        thumb: >-
          https://metadata-static.plex.tv/8/people/8b1094f87234d398fbe6ad80e1f09cda.jpg
      - id: 32223
        filter: actor=32223
        tag: Louise Bennett
        tagKey: 5f3feaf2ce2564003f88d1e6
        role: CNN Newswoman
        thumb: >-
          https://metadata-static.plex.tv/2/people/29e9e53cb7a4ec65e54a8904eff9fc6e.jpg
      - id: 32224
        filter: actor=32224
        tag: Emma Jacobson-Sive
        tagKey: 5ff8c0367c97f5002b10645e
        role: Elizabeth Moorehouse
      - id: 32225
        filter: actor=32225
        tag: Gil Glasgow
        tagKey: 5d776828961905001eb917c0
        role: Election Official
        thumb: https://metadata-static.plex.tv/people/5d776828961905001eb917c0.jpg
      - id: 32226
        filter: actor=32226
        tag: Sarah Siadat
        tagKey: 5d77705e594b2b001e749a69
        role: Reporter
      - id: 32227
        filter: actor=32227
        tag: Carolyn Wilson
        tagKey: 62fb8024204dedab63a86554
        role: Election Official
        thumb: >-
          https://metadata-static.plex.tv/5/people/5c68251d4354b1efa0b9a16571c07aa5.jpg
      - id: 32228
        filter: actor=32228
        tag: Brendan Calton
        tagKey: 5fa9693653e8cf002e7e7dfd
        role: TV Tech
      - id: 32229
        filter: actor=32229
        tag: Nick Clifford
        tagKey: 5d776a28594b2b001e6b4887
        role: Event Coordinator
        thumb: https://metadata-static.plex.tv/people/5d776a28594b2b001e6b4887.jpg
      - id: 32230
        filter: actor=32230
        tag: Stephen DeCordova
        tagKey: 5d776aa896b655001fdf536d
        role: Franklin Washington
      - id: 31226
        filter: actor=31226
        tag: Nick Fontaine
        tagKey: 5e1649a11493cd003f0f0406
        role: Sam O'Keefe
        thumb: https://metadata-static.plex.tv/people/5e1649a11493cd003f0f0406.jpg
      - id: 21338
        filter: actor=21338
        tag: Matthew James Gulbranson
        tagKey: 5d776a599ab54400214fe200
        role: Secret Service Agent
        thumb: >-
          https://metadata-static.plex.tv/6/people/6d734d2f35698917e4e03dc0bda5d2fc.jpg
      - id: 11154
        filter: actor=11154
        tag: Brian Michael Jones
        tagKey: 5d7769a6ad5437001f763947
        role: Secret Service Agent
        thumb: https://metadata-static.plex.tv/people/5d7769a6ad5437001f763947.jpg
      - id: 18713
        filter: actor=18713
        tag: Andrew Thacher
        tagKey: 5d77686ceb5d26001f1eac9c
        role: Dr. Weisglass
        thumb: https://metadata-static.plex.tv/people/5d77686ceb5d26001f1eac9c.jpg
      - id: 32231
        filter: actor=32231
        tag: Ursula Whittaker
        tagKey: 5d7768368718ba001e314cb5
        role: Elisa Burke
        thumb: >-
          https://metadata-static.plex.tv/a/people/aa48748b12659e76d088e457c7ceeb38.jpg
      - id: 32232
        filter: actor=32232
        tag: G. Maximilian Zarou
        tagKey: 5d776ba423d5a3001f512b67
        role: Hotel Manager
        thumb: https://metadata-static.plex.tv/people/5d776ba423d5a3001f512b67.jpg
      - id: 32233
        filter: actor=32233
        tag: P.J. Brown
        tagKey: 5d776834880197001ec93229
        role: Phil
        thumb: >-
          https://metadata-static.plex.tv/f/people/f438534de978fa680b77fbcee79bf2fe.jpg
      - id: 32234
        filter: actor=32234
        tag: Janelle Froehlich
        tagKey: 5d77688c9ab54400214e78e4
        role: Stewardess
        thumb: >-
          https://metadata-static.plex.tv/2/people/25d3beb22b60b95ee2ced13f67ddc7f3.jpg
      - id: 32235
        filter: actor=32235
        tag: Chris Game
        tagKey: 5f3fe3515a76a80042cff508
        role: Maitre D'
      - id: 32236
        filter: actor=32236
        tag: Tim Ryan
        tagKey: 5d7768468718ba001e317d7d
        role: Howard
        thumb: >-
          https://metadata-static.plex.tv/3/people/34947f84a6e72008300e490ed503feac.jpg
      - id: 26904
        filter: actor=26904
        tag: Warren Sweeney
        tagKey: 5d776a46594b2b001e6b7ecb
        role: Chairman Steve O'Brien
        thumb: >-
          https://metadata-static.plex.tv/0/people/0dc442f9337de60aa7af690bdb5085fd.jpg
    Field:
      - locked: true
        name: thumb
    Location:
      - path: /storage/DS215J/Media/TV_Shows/Veep
```
## Item Added Episode

```yaml
payload:
  event: library.new
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Metadata:
    librarySectionType: show
    ratingKey: '18107'
    key: /library/metadata/18107
    parentRatingKey: '18096'
    grandparentRatingKey: '2018'
    guid: plex://episode/5d9c0e74705e7a001e729606
    parentGuid: plex://season/602e5f20b2c087002d0b650b
    grandparentGuid: plex://show/5d9c081b7b5c2e001e654a03
    grandparentSlug: veep
    type: episode
    title: Inauguration
    grandparentKey: /library/metadata/2018
    parentKey: /library/metadata/18096
    librarySectionTitle: TV
    librarySectionID: 7
    librarySectionKey: /library/sections/7
    grandparentTitle: Veep
    parentTitle: Season 5
    contentRating: TV-MA
    summary: >-
      Selina and her staff prepare for inauguration day. Mike suffers
      exhaustion. Catherine gets a makeover.
    index: 10
    parentIndex: 5
    audienceRating: 8.2
    year: 2016
    thumb: /library/metadata/18107/thumb/1749762354
    art: /library/metadata/2018/art/1747275885
    parentThumb: /library/metadata/18096/thumb/1749761797
    grandparentThumb: /library/metadata/2018/thumb/1747275885
    grandparentArt: /library/metadata/2018/art/1747275885
    grandparentTheme: /library/metadata/2018/theme/1747275885
    duration: 1740000
    originallyAvailableAt: '2016-06-26'
    addedAt: 1749762350
    updatedAt: 1749762354
    audienceRatingImage: themoviedb://image.rating
    chapterSource: media
    Image:
      - alt: Inauguration
        type: coverPoster
        url: /library/metadata/2018/thumb/1747275885
      - alt: Inauguration
        type: snapshot
        url: /library/metadata/18107/thumb/1749762354
      - alt: Inauguration
        type: background
        url: /library/metadata/2018/art/1747275885
      - alt: Inauguration
        type: clearLogo
        url: /library/metadata/2018/clearLogo/1747275885
    UltraBlurColors:
      topLeft: 4a1f18
      topRight: 8f4525
      bottomRight: 0b0310
      bottomLeft: 22544d
    Guid:
      - id: imdb://tt5049994
      - id: tmdb://1199312
      - id: tvdb://5532982
    Rating:
      - image: imdb://image.rating
        value: 8.6
        type: audience
      - image: themoviedb://image.rating
        value: 8.2
        type: audience
    Director:
      - id: 67111
        filter: director=67111
        tag: Becky Martin
        tagKey: 67f81139c02c887cc56a7b1f
    Writer:
      - id: 67129
        filter: writer=67129
        tag: Jim Margolis
        tagKey: 5e163579316a39003ef7eb41
    Role:
      - id: 4066
        filter: actor=4066
        tag: Julia Louis-Dreyfus
        tagKey: 5d7768275af944001f1f6ec8
        role: Selina Meyer
        thumb: >-
          https://metadata-static.plex.tv/6/people/648b8a419407acd8f532afffc9cc66d7.jpg
      - id: 32118
        filter: actor=32118
        tag: Anna Chlumsky
        tagKey: 5d77682c151a60001f24bf5b
        role: Amy Brookheimer
        thumb: >-
          https://metadata-static.plex.tv/0/people/0dab2222a5681038356005f511477d77.jpg
      - id: 9407
        filter: actor=9407
        tag: Tony Hale
        tagKey: 5d776829151a60001f24b164
        role: Gary Walsh
        thumb: >-
          https://metadata-static.plex.tv/1/people/1883a13b479a06453aa63e1e96364b4a.jpg
      - id: 13106
        filter: actor=13106
        tag: Reid Scott
        tagKey: 5d7768f0fb0d55001f51d6cc
        role: Dan Egan
        thumb: https://metadata-static.plex.tv/people/5d7768f0fb0d55001f51d6cc.jpg
      - id: 7268
        filter: actor=7268
        tag: Timothy Simons
        tagKey: 5d7769ea594b2b001e6add48
        role: Jonah Ryan
        thumb: >-
          https://metadata-static.plex.tv/5/people/5e67a75914d9291adf69ea46d03f9d79.jpg
      - id: 20628
        filter: actor=20628
        tag: Matt Walsh
        tagKey: 5d77682f6f4521001ea9ad83
        role: Mike McLintock
        thumb: >-
          https://metadata-static.plex.tv/2/people/29a9fc980b03d69bd2ba100c6883a49d.jpg
      - id: 10545
        filter: actor=10545
        tag: Kevin Dunn
        tagKey: 5d7768285af944001f1f7223
        role: Ben Cafferty
        thumb: >-
          https://metadata-static.plex.tv/f/people/f9e50abd944a9639e37e09d68b7e7766.jpg
      - id: 16575
        filter: actor=16575
        tag: Sufe Bradshaw
        tagKey: 5d77683beb5d26001f1e1f2a
        role: Sue Wilson
        thumb: >-
          https://metadata-static.plex.tv/b/people/b8a54bef7201f1e763273f44b1b0dded.jpg
      - id: 24136
        filter: actor=24136
        tag: Gary Cole
        tagKey: 5d77682a961905001eb91e4b
        role: Kent Davison
        thumb: >-
          https://metadata-static.plex.tv/5/people/514ed7d32aebd3124b3920ec9196b9d6.jpg
      - id: 7287
        filter: actor=7287
        tag: Sam Richardson
        tagKey: 5d77687b23d5a3001f4ecda8
        role: Richard Splett
        thumb: >-
          https://metadata-static.plex.tv/c/people/c5e2175f74607fcba445873fb46fb62a.jpg
      - id: 32119
        filter: actor=32119
        tag: Sarah Sutherland
        tagKey: 5d776a4b51dd69001fe21ffc
        role: Catherine Meyer
        thumb: https://metadata-static.plex.tv/people/5d776a4b51dd69001fe21ffc.jpg
      - id: 32120
        filter: actor=32120
        tag: Clea DuVall
        tagKey: 5d7768263c3c2a001fbcafc2
        role: Marjorie Palmiotti
        thumb: >-
          https://metadata-static.plex.tv/e/people/eebf6665848ec56cf6487d9fed6093b6.jpg
      - id: 23777
        filter: actor=23777
        tag: Phil Reeves
        tagKey: 5d7768342ec6b5001f6bbda0
        role: Andrew Doyle
        thumb: >-
          https://metadata-static.plex.tv/8/people/84067623ba43ecdac274ecf7159cc751.jpg
      - id: 17254
        filter: actor=17254
        tag: Hugh Laurie
        tagKey: 5d776829103a2d001f564c5a
        role: Tom James
        thumb: >-
          https://metadata-static.plex.tv/0/people/0ed174d86ee4823c05c3cb4e71b1367e.jpg
      - id: 22050
        filter: actor=22050
        tag: Scott Adsit
        tagKey: 5d776827eb5d26001f1dd88d
        role: Greg Hart
        thumb: >-
          https://metadata-static.plex.tv/3/people/3a5f22096b4d758590b5d6858b635907.jpg
      - id: 32121
        filter: actor=32121
        tag: Dan Bakkedahl
        tagKey: 5d7769a1ad5437001f762b08
        role: Roger Furlong
        thumb: >-
          https://metadata-static.plex.tv/d/people/d289ace525c49b73a75c264ebb0a11b7.jpg
      - id: 32136
        filter: actor=32136
        tag: Martin Mull
        tagKey: 5d776828151a60001f24aef0
        role: Bob Bradley
        thumb: >-
          https://metadata-static.plex.tv/2/people/23494efe202b359a6cc31618e703135f.jpg
      - id: 1241
        filter: actor=1241
        tag: John Slattery
        tagKey: 5d7768283c3c2a001fbcb6a3
        role: Charlie Baird
        thumb: >-
          https://metadata-static.plex.tv/1/people/176e5d78b58ee4fdf6eef9e2215859d4.jpg
      - id: 18212
        filter: actor=18212
        tag: Usman Ally
        tagKey: 5d77689533f255001e85a25e
        role: Mohammed Al Jaffar
        thumb: >-
          https://metadata-static.plex.tv/d/people/d16724578f1ea8b1884adbeafb4c0f60.jpg
      - id: 4812
        filter: actor=4812
        tag: Tzi Ma
        tagKey: 5d77682b7e9a3c0020c6b736
        role: Lu Chi-Jang
        thumb: https://metadata-static.plex.tv/people/5d77682b7e9a3c0020c6b736.jpg
      - id: 32132
        filter: actor=32132
        tag: Jessica Chaffin
        tagKey: 5d77687b23d5a3001f4ecda4
        role: Congresswoman Gellardi
        thumb: >-
          https://metadata-static.plex.tv/0/people/0b6acf13834d6635f2b18f04b55b218f.jpg
      - id: 16807
        filter: actor=16807
        tag: Nelson Franklin
        tagKey: 5d77683f103a2d001f56a420
        role: Will
        thumb: >-
          https://metadata-static.plex.tv/3/people/36feede4a79f17c7a23f2cc4b04380b0.jpg
      - id: 32162
        filter: actor=32162
        tag: Meredith Hagner
        tagKey: 5d7768c9ebdf2200209c8b2a
        role: Debralee
        thumb: >-
          https://metadata-static.plex.tv/3/people/3cfba1c1e6aa0b408edd07ae32ce6657.jpg
      - id: 32163
        filter: actor=32163
        tag: Hector Hugo
        tagKey: 5d77688351dd69001fe0d64a
        role: Alejandro Montez
        thumb: >-
          https://metadata-static.plex.tv/e/people/e5868cfe8133d522a0774ca26a37ac3c.jpg
      - id: 26725
        filter: actor=26725
        tag: Matt Oberg
        tagKey: 5d7768881999bc0020dc8411
        role: Buddy Calhoun
        thumb: >-
          https://metadata-static.plex.tv/e/people/ec80ff151a167ab205eb3ac148270b6c.jpg
      - id: 4632
        filter: actor=4632
        tag: Kathy Najimy
        tagKey: 5d77682654c0f0001f301ba8
        role: Wendy Keegan
        thumb: >-
          https://metadata-static.plex.tv/f/people/f2005e454422f73b74ee9c0b48d57f6f.jpg
      - id: 1703
        filter: actor=1703
        tag: Phil LaMarr
        tagKey: 5d776827103a2d001f564619
        role: Paul Graves
        thumb: >-
          https://metadata-static.plex.tv/e/people/e37f3a5764a078ff3c3ecbb18b32b5c8.jpg
      - id: 3282
        filter: actor=3282
        tag: J.P. Manoux
        tagKey: 5d776827103a2d001f56467f
        role: Congressman Clark
        thumb: >-
          https://metadata-static.plex.tv/4/people/48d515df07e7954ad7bd291acba622d2.jpg
      - id: 12869
        filter: actor=12869
        tag: Rick Overton
        tagKey: 5d7768268a7581001f12be17
        role: Congressman Spencer
        thumb: >-
          https://metadata-static.plex.tv/6/people/609578bf34652b77df2e4af591d3df47.jpg
      - id: 24743
        filter: actor=24743
        tag: Wayne Wilderson
        tagKey: 5d7768273c3c2a001fbcb29d
        role: Wayne
        thumb: >-
          https://metadata-static.plex.tv/9/people/92ac3f1586195e5b7833fc4593e65310.jpg
      - id: 28102
        filter: actor=28102
        tag: Andrea Savage
        tagKey: 5d77683d54f42c001f8c5e66
        role: Laura Montez
        thumb: >-
          https://metadata-static.plex.tv/9/people/9bbcfa1d579512eb62701cfdbbff8964.jpg
      - id: 18134
        filter: actor=18134
        tag: David Rasche
        tagKey: 5d77682e8a7581001f12ca80
        role: Jim Marwood
        thumb: >-
          https://metadata-static.plex.tv/3/people/3343bd3d0f6e25ef3605e950993416c1.jpg
      - id: 32164
        filter: actor=32164
        tag: Abbey DiGregorio
        tagKey: 5d7768692e80df001ebe361f
        role: Dr. Walcott
        thumb: https://metadata-static.plex.tv/people/5d7768692e80df001ebe361f.jpg
      - id: 32137
        filter: actor=32137
        tag: Bonnie Bentley
        tagKey: 5d7768a4d11dd300202290bd
        role: Emily
        thumb: >-
          https://metadata-static.plex.tv/c/people/cbe54211de59a8c68ec0dabdbc688c50.jpg
      - id: 2625
        filter: actor=2625
        tag: Deb Hiett
        tagKey: 5d776b4796b655001fe0af47
        role: White House Reporter
        thumb: >-
          https://metadata-static.plex.tv/2/people/2e6d4e175bff6f5b85f22b0db966402f.jpg
      - id: 32129
        filter: actor=32129
        tag: Morgan Smith
        tagKey: 5f4031ac52f2000041524599
        role: Candi Caruso
        thumb: >-
          https://metadata-static.plex.tv/b/people/bd139e2c1e31fc3afaef078dd59104a9.jpg
      - id: 28663
        filter: actor=28663
        tag: Jean Villepique
        tagKey: 5d77683f103a2d001f56a418
        role: NY Times Reporter
        thumb: >-
          https://metadata-static.plex.tv/8/people/875fecd4dfa84a6d43caa42b8c9dbbd9.jpg
      - id: 32139
        filter: actor=32139
        tag: Lee Chen
        tagKey: 5d776b5f96b655001fe0e998
        role: Translator
        thumb: https://metadata-static.plex.tv/people/5d776b5f96b655001fe0e998.jpg
      - id: 67130
        filter: actor=67130
        tag: Robert Arce
        tagKey: 5d7768528a7581001f1306c5
        role: Senator Summerlin
        thumb: >-
          https://metadata-static.plex.tv/b/people/be27afc6d242bb755740512966e2aeb4.jpg
      - id: 67131
        filter: actor=67131
        tag: Alan Brooks
        tagKey: 5d77683b4de0ee001fccca7e
        role: Senator Lowell
        thumb: >-
          https://metadata-static.plex.tv/5/people/54e1f554612202024928c16aa3d98f7c.jpg
      - id: 67132
        filter: actor=67132
        tag: John Bozeman
        tagKey: 5d776b54fb0d55001f5642e5
        role: Senator Nelson
        thumb: >-
          https://metadata-static.plex.tv/f/people/f6e785e573252cacb7db586ed3519020.jpg
      - id: 67133
        filter: actor=67133
        tag: Melvin Caldwell
        tagKey: 5d776e22ad5437001f7ebe55
        role: Senator Murray
        thumb: >-
          https://metadata-static.plex.tv/3/people/3cc15bdf40a06756eb7f4aa5b32ab1f8.jpg
      - id: 26734
        filter: actor=26734
        tag: Kate Comer
        tagKey: 5d7770326afb3d00206146a8
        role: Secretary
        thumb: >-
          https://metadata-static.plex.tv/4/people/4f9b8b05b190e46d5b2fa154e6df6dec.jpg
      - id: 67134
        filter: actor=67134
        tag: Noel D'Souza-Brown
        tagKey: 5f403aa3fea1a1003fa135d1
        role: Caterina Montez
        thumb: >-
          https://metadata-static.plex.tv/1/people/1103cc3010b2edc416671f05e9d6598b.jpg
      - id: 67135
        filter: actor=67135
        tag: Nico Evers-Swindell
        tagKey: 5d7768394de0ee001fccc4a2
        role: Colt
        thumb: >-
          https://metadata-static.plex.tv/e/people/e7f638c76d1837066a7deb1f40255492.jpg
      - id: 67136
        filter: actor=67136
        tag: Leslie Fleming-Mitchell
        tagKey: 5d7768b27a53e9001e6d6924
        role: Senator Willis
        thumb: >-
          https://metadata-static.plex.tv/e/people/e70531204e8c70022395cbbbe948310e.jpg
      - id: 67137
        filter: actor=67137
        tag: Waymond Lee
        tagKey: 5d776834880197001ec93206
        role: Senator Yinui
        thumb: >-
          https://metadata-static.plex.tv/4/people/4eb5d2195c72b4dde99cbb1e4b79638d.jpg
      - id: 28478
        filter: actor=28478
        tag: Monnae Michaell
        tagKey: 5d776836999c64001ec2f7b9
        role: Senate Clerk
        thumb: >-
          https://metadata-static.plex.tv/6/people/6bd84538f7a07e551b4a6b85130845c1.jpg
      - id: 67138
        filter: actor=67138
        tag: Sean O'Pry
        tagKey: 5d776c0396b655001fe2330f
        role: Brady
        thumb: https://metadata-static.plex.tv/people/5d776c0396b655001fe2330f.jpg
      - id: 67139
        filter: actor=67139
        tag: Frank Rich
        tagKey: 5d776b67fb0d55001f566c06
        role: Chief Justice
        thumb: https://metadata-static.plex.tv/people/5d776b67fb0d55001f566c06.jpg
      - id: 67140
        filter: actor=67140
        tag: Yoshi Sudarso
        tagKey: 5d77686c54c0f0001f308423
        role: Mason
        thumb: >-
          https://metadata-static.plex.tv/5/people/51f326a46792edb7cf0bf10eba292eab.jpg
      - id: 27590
        filter: actor=27590
        tag: Sterling Sulieman
        tagKey: 5d77688996b655001fdbafd9
        role: Storm
        thumb: >-
          https://metadata-static.plex.tv/f/people/fc3ae9c11e06c3e76082df5b6e3f66e4.jpg
    Producer:
      - id: 28677
        filter: producer=28677
        tag: David Hyman
        tagKey: 5d9c08190aaccd001f8ed715
```
## Item Added Artist

```yaml
payload:
  event: library.new
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Metadata:
    librarySectionType: artist
    ratingKey: '18108'
    key: /library/metadata/18108/children
    guid: plex://artist/5d07bc02403c6402904aa13d
    type: artist
    title: Nickelback
    librarySectionTitle: Music
    librarySectionID: 8
    librarySectionKey: /library/sections/8
    summary: "Nickelback makes loud, emotional rock with just enough pop sheen to carry them consistently to mainstream success. They took heavy post-grunge into the 2000s, and by most measures, the Canadian group were the most popular rockers of that decade, ruling rock radio from the moment \"How You Remind Me\" went to number one in both Canada and the U.S. after its release in 2001. They repeatedly dominated the rock charts, balancing crossover power ballads like \"Someday\" and \"Photograph\" with salacious rockers like \"Rock Star\" and \"Something in Your Mouth.\" During this reign, Nickelback's presence seemed outsized thanks to its gruff-voiced leader Chad Kroeger stepping outside the group to record \"Hero\" for the soundtrack for Sam Raimi's 2002 theatrical adaptation of Spider-Man, along with appearing on records by Santana and Kroeger's then-wife Avril Lavigne -- cameos that indicate how the band's popularity extended beyond die-hard rock audiences. Nevertheless, those were the fans that stayed true to Nickelback, helping the band stay successful in the 2010s and into 2022, when the crunching \"San Quentin,\" from their album Get Rollin', became the band's first American Top Ten Rock hit in nearly a decade.\r\nChad Kroeger honed his frontman skills by performing with cover bands in Hanna, a small Canadian town 215 kilometers northeast of Calgary. After growing tired of playing other people's songs, he borrowed money from his stepfather and relocated to Vancouver, where he recorded his first batch of original material. Mike Kroeger, Chad's bass-playing sibling, decided to join his brother's band, as did fellow Vancouver transplants Ryan Peake (a guitarist who had befriended the Kroegers in middle school) and Ryan Vikedal (a drummer from Peake's hometown of Brooks, Alberta). Nickelback officially took shape in 1995 and quickly set to work, releasing two albums -- the Hesher EP and full-length album Curb -- in 1996. By 1998, the bandmates were managing themselves; Chad courted radio stations, brother Mike handled distribution, Vikedal booked shows, and Peake maintained the band's website.\r\nJanuary 2000 saw the arrival of The State, Nickelback's second independent release. Issued at a time in which Canadian content requirements were increased (and, accordingly, local radio stations had begun to desperately seek out homegrown product), the album fared very well on indie charts. Nickelback toured ceaselessly in support of The State, logging approximately 200 shows while playing alongside other groups of the burgeoning post-grunge genre. Their commercial appeal wasn't lost on the record industry, either, and The State's distribution rights were quickly snapped up by Roadrunner Records in the U.S. and EMI in Canada. As the band continued to tour, Kroeger kept writing new songs, many of which were polished in front of live audiences. Much of that material found its way onto Silver Side Up, which was produced by Rick Parashar (who rose to prominence in the early '90s by helming Pearl Jam's Ten, Alice in Chains' Sap, and Blind Melon's self-titled debut) and recorded at Green House, the same Vancouver studio used for The State's creation. The combination of Nickelback's growing popularity and Kroeger's focused songwriting propelled Silver Side Up onto album charts across the world, spearheaded by the hit single \"How You Remind Me.\" Kroeger capitalized on that exposure by producing another Vancouver-based band, Default, and collaborating with Saliva's Josey Scott for the Spider-Man soundtrack. The Long Road then arrived in 2003, featuring an increasingly polished sound and another high-charting single, \"Someday.\" While some listeners criticized the apparent similarities between \"Someday\" and \"How You Remind Me,\" The Long Road had little trouble maintaining Nickelback's wide audience, eventually selling over five million copies worldwide.\r\nIn February 2005, Nickelback announced the departure of Vikedal. He was soon replaced by 3 Doors Down's former drummer Daniel Adair, and Nickelback returned to Kroeger's studio in Vancouver to begin work on another album. ZZ Top's Billy Gibbons and Pantera's Dimebag Darrell (who unfortunately died before the album's release) were guests on the chart-topping All the Right Reasons, which arrived in October 2005. It proved to be Nickelback's most popular effort to date, remaining in the Billboard Top 30 for over two years and selling over seven million copies in the U.S. alone. It also spawned five Top 20 singles, a feat that attracted the attention of veteran producer (and demonstrated hitmaker) Mutt Lange. Nickelback traveled to Lange's home in Switzerland to share songwriting ideas; impressed with the results, they also enlisted him to helm their next album. Recorded in a converted Vancouver barn, Dark Horse marked the band's sixth studio album upon its release in November 2008. Nickelback's seventh studio album arrived nearly three years after the multi-platinum-selling Dark Horse. The 11-track Here and Now, which was preceded by the singles \"Bottoms Up\" and \"When We Stand Together,\" hit the streets on November 21, 2011.\r\nThe following year Kroeger began working on fellow Canadian rock star Avril Lavigne's eponymous fifth album. Shortly after their working partnership began, they began dating and eventually married in early 2013. The band put together their first compilation, The Best of Nickelback, Vol. 1, which appeared in November of 2013; the 19-track collection contained no new songs. In 2014, the band's contract with Roadrunner expired and they decided not to renew, signing instead with Universal Republic for their eighth album, No Fixed Address. The album included a number of departures from Nickelback's usual fare, including the radio-friendly \"What Are You Waiting For?,\" the politicized \"Edge of a Revolution,\" and \"Got Me Runnin' 'Round,\" which featured a horn section and rapper Flo Rida. No Fixed Address appeared in November 2014, debuting at four on Billboard's Top 200 and generating rock radio hits in \"Edge of a Revolution\" and \"Million Miles an Hour.\" As they worked on their ninth album in 2016, Nickelback released a cover of Don Henley's \"Dirty Laundry\" and negotiated a switch from Republic to BMG. Feed the Machine, their first record for BMG, was co-produced by Chris Baseford (Disturbed) and appeared in June 2017. The LP debuted at number five on the U.S. Billboard 200, with its title track reaching 12 on Billboard's Mainstream Rock chart. A non-LP cover of the Charlie Daniels Band's \"The Devil Went Down to Georgia\" featuring guitarist Dave Martone appeared in 2020, as did a 15th anniversary edition of 2005's multi-platinum-selling All the Right Reasons. Nickelback returned with new material in 2022's \"San Quentin,\" the first taste of their tenth studio album, Get Rollin'. Another co-production with Chris Baseford, Get Rollin' focused on heavy riffs and good times, a combination highlighted on the breezy single \"High Time.\" ~ Andrew Leahey"
    index: 1
    viewCount: 21
    skipCount: 5
    lastViewedAt: 1749304101
    thumb: /library/metadata/18108/thumb/1749766113
    art: /library/metadata/18108/art/1749766113
    addedAt: 1749766110
    updatedAt: 1749766113
    Image:
      - alt: Nickelback
        type: coverPoster
        url: /library/metadata/18108/thumb/1749766113
      - alt: Nickelback
        type: background
        url: /library/metadata/18108/art/1749766113
    UltraBlurColors:
      topLeft: 11323d
      topRight: '924136'
      bottomRight: '8e4535'
      bottomLeft: 9a3837
    Genre:
      - id: 38623
        filter: genre=38623
        tag: Pop/Rock
    Country:
      - id: 2386
        filter: country=2386
        tag: Canada
    Style:
      - id: 39402
        filter: style=39402
        tag: Alternative Metal
      - id: 39403
        filter: style=39403
        tag: Heavy Metal
      - id: 39404
        filter: style=39404
        tag: Contemporary Pop/Rock
      - id: 39405
        filter: style=39405
        tag: Post-Grunge
    Guid:
      - id: mbid://bc710bcf-8815-42cf-bad2-3f1d12246aeb
    Similar:
      - id: 61386
        filter: similar=61386
        tag: Theory of a Deadman
      - id: 39406
        filter: similar=39406
        tag: Hinder
      - id: 39408
        filter: similar=39408
        tag: 3 Doors Down
      - id: 39411
        filter: similar=39411
        tag: Shinedown
      - id: 39409
        filter: similar=39409
        tag: Daughtry
      - id: 61385
        filter: similar=61385
        tag: Saving Abel
      - id: 39412
        filter: similar=39412
        tag: Seether
      - id: 39416
        filter: similar=39416
        tag: Creed
      - id: 39414
        filter: similar=39414
        tag: Puddle of Mudd
      - id: 39420
        filter: similar=39420
        tag: Three Days Grace
      - id: 39427
        filter: similar=39427
        tag: Staind
      - id: 61596
        filter: similar=61596
        tag: Papa Roach
      - id: 65191
        filter: similar=65191
        tag: Black Stone Cherry
      - id: 65316
        filter: similar=65316
        tag: Alter Bridge
      - id: 39432
        filter: similar=39432
        tag: Default
      - id: 65761
        filter: similar=65761
        tag: My Darkest Days
      - id: 39424
        filter: similar=39424
        tag: Buckcherry
      - id: 65762
        filter: similar=65762
        tag: Breaking Benjamin
      - id: 65760
        filter: similar=65760
        tag: Adelitas Way
      - id: 39428
        filter: similar=39428
        tag: Finger Eleven
      - id: 65763
        filter: similar=65763
        tag: Kid Rock
      - id: 65765
        filter: similar=65765
        tag: Rev Theory
      - id: 61387
        filter: similar=61387
        tag: Saliva
      - id: 39433
        filter: similar=39433
        tag: Pop Evil
      - id: 39430
        filter: similar=39430
        tag: Fuel
      - id: 61405
        filter: similar=61405
        tag: Hoobastank
      - id: 47747
        filter: similar=47747
        tag: Trapt
      - id: 65764
        filter: similar=65764
        tag: Art of Dying
      - id: 65100
        filter: similar=65100
        tag: Chad Kroeger
      - id: 66312
        filter: similar=66312
        tag: Thousand Foot Krutch
    Mood:
      - id: 38735
        filter: mood=38735
        tag: Brooding
      - id: 38938
        filter: mood=38938
        tag: Angst-Ridden
      - id: 39285
        filter: mood=39285
        tag: Bleak
      - id: 38741
        filter: mood=38741
        tag: Aggressive
      - id: 38845
        filter: mood=38845
        tag: Searching
      - id: 38940
        filter: mood=38940
        tag: Dramatic
      - id: 39276
        filter: mood=39276
        tag: Harsh
      - id: 39218
        filter: mood=39218
        tag: Intense
      - id: 38997
        filter: mood=38997
        tag: Reflective
      - id: 38740
        filter: mood=38740
        tag: Rousing
    Location:
      - path: /storage/DS215J/Media/Music/Nickelback
```
## Item Added Album

```yaml
payload:
  event: library.new
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Metadata:
    librarySectionType: artist
    ratingKey: '18121'
    key: /library/metadata/18121/children
    parentRatingKey: '18108'
    guid: plex://album/5d07c179403c640290849486
    parentGuid: plex://artist/5d07bc02403c6402904aa13d
    studio: Roadrunner Records
    type: album
    title: Silver Side Up
    parentKey: /library/metadata/18108
    librarySectionTitle: Music
    librarySectionID: 8
    librarySectionKey: /library/sections/8
    parentTitle: Nickelback
    summary: >-
      Industrial-strength rock & roll is back with a vengeance on the earnest
      Silver Side Up by Nickelback. The band wastes no time in getting into its
      brand of dark, high-octane rock. The album opener "Never Again," about
      spousal abuse, thrusts out of the starting gate with rocket-fueled
      intensity. Lead singer/guitarist/lyricist Chad Kroeger does not mince
      words in his portrayals of the darker sides of the human experience, and
      that is what Silver Side Up is essentially about. Nickelback's music is
      issue-oriented on the domestic and personal front, and it's a refreshing
      change of pace in 2001's sea of angry rockers. Another familial subject is
      tackled on the pounding "Too Bad." The song describes an emotionally and
      physically absent father figure as seen through the eyes of a regretful
      adult-child looking back. The cut that broke the band to mainstream
      audiences is "How You Remind Me," a thundering, mid-tempo rock track
      marked by thick chords and a brooding tone. Kroeger's voice is filled with
      weariness as he well captures the self-defeated feelings one experiences
      when being emotionally dissected by a lover. Such words as "'cause living
      with me must have damn near killed you" painfully zero in on the breakdown
      of the human spirit when it's badgered enough. Because, sadly, many have
      found themselves in this situation, the song connects with listeners.
      Coupled with a powerful and moody soundtrack, it's no wonder it took off
      on the radio. Grunge pays a visit on the set's closing number, "Good Times
      Gone." This well-crafted song slowly builds in intensity -- from the
      intro's fingered guitar notes and understated vocals, to the gradual
      addition of instruments, to Kroeger's explosive vocal release at the
      song's end, which retreats back into softly strummed guitar notes. "Good
      Times Gone" is reminiscent of a Pearl Jam number, and this is no surprise;
      Silver Side Up was co-produced by Rick Parashar, who has worked with
      Seattle's finest. Nickelback's style is edgy aggressive rock peppered with
      a taste of grunge. The band can easily sit alongside Staind and 3 Doors
      Down, among other like acts. However, what Nickelback has in spades and
      what gives the group an upper hand over its peers is intensity, realistic
      storytelling, and raw passion. ~ Liana Jonas
    index: 1
    rating: 6
    viewCount: 21
    lastViewedAt: 1749304101
    year: 2001
    thumb: /library/metadata/18121/thumb/1749766331
    art: /library/metadata/18108/art/1749766113
    parentThumb: /library/metadata/18108/thumb/1749766113
    originallyAvailableAt: '2001-09-11'
    leafCount: 10
    viewedLeafCount: 1
    addedAt: 1749766328
    updatedAt: 1749766331
    Image:
      - alt: Silver Side Up
        type: coverPoster
        url: /library/metadata/18121/thumb/1749766331
      - alt: Silver Side Up
        type: background
        url: /library/metadata/18108/art/1749766113
    UltraBlurColors:
      topLeft: '123433'
      topRight: 201b19
      bottomRight: 6f5b29
      bottomLeft: 6f5b29
    Genre:
      - id: 38623
        filter: genre=38623
        tag: Pop/Rock
    Style:
      - id: 39402
        filter: style=39402
        tag: Alternative Metal
      - id: 39405
        filter: style=39405
        tag: Post-Grunge
      - id: 39403
        filter: style=39403
        tag: Heavy Metal
      - id: 39404
        filter: style=39404
        tag: Contemporary Pop/Rock
    Format:
      - id: 38742
        filter: format=38742
        tag: Album
    Guid:
      - id: mbid://a948c622-e284-47aa-98fb-55050a37494d
    Mood:
      - id: 39125
        filter: mood=39125
        tag: Autumnal
      - id: 38739
        filter: mood=38739
        tag: Yearning
      - id: 39257
        filter: mood=39257
        tag: Nostalgic
      - id: 39131
        filter: mood=39131
        tag: Bittersweet
      - id: 39132
        filter: mood=39132
        tag: Wistful
      - id: 38938
        filter: mood=38938
        tag: Angst-Ridden
      - id: 38845
        filter: mood=38845
        tag: Searching
      - id: 38735
        filter: mood=38735
        tag: Brooding
      - id: 38740
        filter: mood=38740
        tag: Rousing
      - id: 38997
        filter: mood=38997
        tag: Reflective
      - id: 39107
        filter: mood=39107
        tag: Earnest
      - id: 38741
        filter: mood=38741
        tag: Aggressive
      - id: 39465
        filter: mood=39465
        tag: Menacing
      - id: 39122
        filter: mood=39122
        tag: Poignant
```
## Movie Rate
##### Movie is rated.
```yaml
payload:
  rating: 9
  event: media.rate
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: movie
    ratingKey: '73'
    key: /library/metadata/73
    guid: plex://movie/5e833bb566500c0041d29af9
    slug: nobody-2021
    studio: 87North Productions
    type: movie
    title: Nobody
    librarySectionTitle: Films
    librarySectionID: 6
    librarySectionKey: /library/sections/6
    contentRating: R
    summary: >-
      Hutch Mansell, a suburban dad, overlooked husband, nothing neighbor — a
      "nobody." When two thieves break into his home one night, Hutch's unknown
      long-simmering rage is ignited and propels him on a brutal path that will
      uncover dark secrets he fought to leave behind.
    rating: 8.4
    audienceRating: 9.4
    userRating: 9
    skipCount: 1
    lastRatedAt: 1749682611
    year: 2021
    tagline: Never underestimate a nobody.
    thumb: /library/metadata/73/thumb/1749091611
    art: /library/metadata/73/art/1749091611
    duration: 5460000
    originallyAvailableAt: '2021-03-18'
    addedAt: 1733008519
    updatedAt: 1749091611
    audienceRatingImage: rottentomatoes://image.rating.upright
    chapterSource: media
    primaryExtraKey: /library/metadata/82
    ratingImage: rottentomatoes://image.rating.ripe
    Image:
      - alt: Nobody
        type: coverPoster
        url: /library/metadata/73/thumb/1749091611
      - alt: Nobody
        type: background
        url: /library/metadata/73/art/1749091611
      - alt: Nobody
        type: clearLogo
        url: /library/metadata/73/clearLogo/1749091611
    UltraBlurColors:
      topLeft: 4f1a17
      topRight: 913b3a
      bottomRight: 8d4633
      bottomLeft: 8d3839
    Genre:
      - id: 50944
        filter: genre=50944
        tag: 4k HDR
        count: 48
      - id: 50946
        filter: genre=50946
        tag: Dolby Atmos
        count: 38
      - id: 50945
        filter: genre=50945
        tag: Dolby Vision
        count: 21
      - id: 19
        filter: genre=19
        tag: Thriller
        count: 86
      - id: 21
        filter: genre=21
        tag: Action
        count: 230
      - id: 20
        filter: genre=20
        tag: Crime
        count: 49
      - id: 17
        filter: genre=17
        tag: Drama
        count: 128
    Country:
      - id: 87
        filter: country=87
        tag: United States of America
        count: 470
    Guid:
      - id: imdb://tt7888964
      - id: tmdb://615457
      - id: tvdb://133393
    Rating:
      - image: imdb://image.rating
        value: 7.4
        type: audience
        count: 501
      - image: rottentomatoes://image.rating.ripe
        value: 8.4
        type: critic
        count: 330
      - image: rottentomatoes://image.rating.upright
        value: 9.4
        type: audience
        count: 411
      - image: themoviedb://image.rating
        value: 7.9
        type: audience
        count: 508
    Director:
      - id: 3266
        filter: director=3266
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
    Writer:
      - id: 3267
        filter: writer=3267
        tag: Derek Kolstad
        tagKey: 5d776a8afb0d55001f54921f
        count: 4
        thumb: >-
          https://metadata-static.plex.tv/5/people/5c97a829e3651739f2971e4e2898682c.jpg
    Role:
      - id: 3268
        filter: actor=3268
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        count: 2
        role: Hutch Mansell
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3269
        filter: actor=3269
        tag: Aleksey Serebryakov
        tagKey: 5d77682b151a60001f24b98c
        role: Yulian Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b743f3f7a75e1b5bd937e2060753837.jpg
      - id: 3270
        filter: actor=3270
        tag: Connie Nielsen
        tagKey: 5d7768267228e5001f1dcdb5
        count: 4
        role: Becca Mansell
        thumb: >-
          https://metadata-static.plex.tv/3/people/328b075ecee9e20d7e22e95a72596edb.jpg
      - id: 3271
        filter: actor=3271
        tag: Christopher Lloyd
        tagKey: 5d7768244de0ee001fcc80bb
        count: 6
        role: David Mansell
        thumb: >-
          https://metadata-static.plex.tv/c/people/c2d2c2ab21e34db5837877ca386d43c3.jpg
      - id: 3272
        filter: actor=3272
        tag: Michael Ironside
        tagKey: 5d7768268718ba001e311c35
        count: 3
        role: Eddie Williams
        thumb: >-
          https://metadata-static.plex.tv/5/people/562560faf349fed1531898b075cfdf54.jpg
      - id: 3273
        filter: actor=3273
        tag: Colin Salmon
        tagKey: 5d776826880197001ec906c3
        role: The Barber
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05fd85a41289fbd0375c013fbb6593f.jpg
      - id: 3274
        filter: actor=3274
        tag: RZA
        tagKey: 5d77682985719b001f3a132f
        role: Harry Mansell
        thumb: >-
          https://metadata-static.plex.tv/9/people/97914947f71b47e35f9e0e708f6b6054.jpg
      - id: 3275
        filter: actor=3275
        tag: Billy MacLellan
        tagKey: 5d7768355af944001f1f9ddb
        role: Charlie Williams
        thumb: >-
          https://metadata-static.plex.tv/7/people/793801223b142f24e8455525db4f98b0.jpg
      - id: 3276
        filter: actor=3276
        tag: Araya Mengesha
        tagKey: 5d77687633f255001e8571ca
        role: Pavel
        thumb: >-
          https://metadata-static.plex.tv/0/people/0c5cf3bf1ba0fc04f5dfbfe7787419cd.jpg
      - id: 3277
        filter: actor=3277
        tag: Gage Munroe
        tagKey: 5d776843961905001eb96d28
        role: Brady Mansell
        thumb: >-
          https://metadata-static.plex.tv/0/people/07bdd3e7b5c9bf0151f67c6e986e546c.jpg
      - id: 3278
        filter: actor=3278
        tag: Paisley Cadorath
        tagKey: 5e166be52d4d84003e4bede2
        role: Sammy Mansell
        thumb: >-
          https://metadata-static.plex.tv/4/people/46fce2ea69eca54daeb8ef48e4fb788c.jpg
      - id: 3279
        filter: actor=3279
        tag: Aleksandr Pal
        tagKey: 5d776a28fb0d55001f53c11f
        role: Teddy Kuznetsov
        thumb: >-
          https://metadata-static.plex.tv/4/people/418db25e4856946a298e70440778a26a.jpg
      - id: 3280
        filter: actor=3280
        tag: Humberly González
        tagKey: 5d776c7cad5437001f7bf60d
        role: Lupita Martin
        thumb: >-
          https://metadata-static.plex.tv/9/people/9e0cf7073f9849cb8c6a17157c0cb1df.jpg
      - id: 3281
        filter: actor=3281
        tag: Edsson Morales
        tagKey: 5d776870eb5d26001f1eb87d
        role: Luis Martin
        thumb: >-
          https://metadata-static.plex.tv/2/people/270e11868a651c1f64e076871a0ebe09.jpg
      - id: 3282
        filter: actor=3282
        tag: J.P. Manoux
        tagKey: 5d776827103a2d001f56467f
        count: 3
        role: Pentagon Darren
        thumb: >-
          https://metadata-static.plex.tv/4/people/48d515df07e7954ad7bd291acba622d2.jpg
      - id: 3283
        filter: actor=3283
        tag: Adrian McLean
        tagKey: 5d776f5bad5437001f80fbb5
        role: Joey
        thumb: >-
          https://metadata-static.plex.tv/7/people/78e72df33a9979c71f376c23639ff4dd.jpg
      - id: 3284
        filter: actor=3284
        tag: Ilya Naishuller
        tagKey: 5d776a0996b655001fde1a1b
        role: Hitman Anatoly
        thumb: >-
          https://metadata-static.plex.tv/7/people/74deea83811a333572d523cf64d07057.jpg
      - id: 3285
        filter: actor=3285
        tag: Sergey Shnurov
        tagKey: 5d7768466f4521001ea9f873
        role: Hitman Valentin
        thumb: >-
          https://metadata-static.plex.tv/f/people/f78b732363a4c27c39078cf9dee79277.jpg
      - id: 3286
        filter: actor=3286
        tag: Joanne Rodriguez
        tagKey: 5d7768342ec6b5001f6bbd05
        role: Bus Driver Donna
        thumb: >-
          https://metadata-static.plex.tv/9/people/9cccffdd78a83dd849a4a41f7199f169.jpg
      - id: 3287
        filter: actor=3287
        tag: Stephanie Sy
        tagKey: 5d776d3d96b655001fe438e4
        role: Realtor
        thumb: https://metadata-static.plex.tv/people/5d776d3d96b655001fe438e4.jpg
      - id: 3288
        filter: actor=3288
        tag: Dan Rizzuto
        tagKey: 5d9f35b0b0262f001f6ec2de
        count: 2
        role: Gunman
      - id: 3289
        filter: actor=3289
        tag: Ruslan Rusin
        tagKey: 5d776d267a53e9001e752a5e
        role: Gunman
      - id: 3290
        filter: actor=3290
        tag: Vladimir Levkovsky
        tagKey: 60b90595f28049002d7ec8e2
        role: Gunman
      - id: 3291
        filter: actor=3291
        tag: Dan Skene
        tagKey: 5d77683c4de0ee001fccce80
        count: 2
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/9/people/9a3aae3a0a9c552d8c9dd651d6244f89.jpg
      - id: 3292
        filter: actor=3292
        tag: BJ Verot
        tagKey: 5d776ca79ab5440021519486
        role: Gunman
        thumb: https://metadata-static.plex.tv/people/5d776ca79ab5440021519486.jpg
      - id: 3293
        filter: actor=3293
        tag: Dylan Rampulla
        tagKey: 5e1647cd46aceb003cee8a84
        role: Gunman
      - id: 3294
        filter: actor=3294
        tag: Margaryta Soldatova
        tagKey: 5d776de696b655001fe5645f
        role: Gunman
        thumb: >-
          https://metadata-static.plex.tv/2/people/2ef47acd293dd4e81ef6607c47af18aa.jpg
      - id: 3295
        filter: actor=3295
        tag: Megan Best
        tagKey: 5e166be52d4d84003e4bedde
        role: Woman on Bus
        thumb: >-
          https://metadata-static.plex.tv/d/people/d4ca27f2b660ae1fc76c8806b9b5a720.jpg
      - id: 3296
        filter: actor=3296
        tag: Darya Charusha
        tagKey: 5d7768bb374a5b001fece978
        role: Beta
        thumb: >-
          https://metadata-static.plex.tv/c/people/c503be6f3a83d9a3692d6c392679eb8e.jpg
      - id: 3297
        filter: actor=3297
        tag: Neil Davison
        tagKey: 5d9f3581adeb7a0021ce25ab
        role: Albert
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d1606a3ec7f8c775346b666d48aed59.jpg
      - id: 3298
        filter: actor=3298
        tag: Paul Essiembre
        tagKey: 5d77684f6f4521001eaa0e2c
        role: Jim the Neighbor
        thumb: >-
          https://metadata-static.plex.tv/1/people/143679603a8a9033feb9815d6a8eca29.jpg
      - id: 3299
        filter: actor=3299
        tag: Adam Hurtig
        tagKey: 5d7769e27a53e9001e6f36b4
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/c/people/cf6adb15c4d5a5ccd1dbe93fd684e807.jpg
      - id: 3300
        filter: actor=3300
        tag: Gabriel Daniels
        tagKey: 5d77689efb0d55001f5158ad
        role: Police
        thumb: >-
          https://metadata-static.plex.tv/7/people/764cf91ca84fd8e24d10682acda85510.jpg
      - id: 3301
        filter: actor=3301
        tag: Kristen Harris
        tagKey: 5d7769ebfb0d55001f534779
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/8/people/8b82bda4aa071a57092c5e0bd82765e6.jpg
      - id: 3302
        filter: actor=3302
        tag: Erik Athavale
        tagKey: 5d776ab59ab54400215027c9
        role: Detective
        thumb: >-
          https://metadata-static.plex.tv/b/people/b0f12073fb6fa6f25213256a4493ebde.jpg
      - id: 3303
        filter: actor=3303
        tag: Tom Soares
        tagKey: 5f4059d8a4f07a00421717aa
        role: Alan Breiseth
      - id: 3304
        filter: actor=3304
        tag: Neven Pajkic
        tagKey: 5d7768256f4521001ea989ba
        role: Big Brute
        thumb: https://metadata-static.plex.tv/people/5d7768256f4521001ea989ba.jpg
      - id: 3305
        filter: actor=3305
        tag: Stephen Eric McIntyre
        tagKey: 5d776831151a60001f24d011
        role: Veteran
        thumb: >-
          https://metadata-static.plex.tv/5/people/556a233e543d87d4d3d1a2dc2630b4bb.jpg
      - id: 3306
        filter: actor=3306
        tag: Rick Dobran
        tagKey: 5d77684261141d001fb171ab
        count: 2
        role: Tattoo Shop Owner
        thumb: >-
          https://metadata-static.plex.tv/3/people/313b89fef7dd52cd49d6c78d0c1cb7e2.jpg
      - id: 3307
        filter: actor=3307
        tag: Richard Thomas
        tagKey: 64c10b5fdcb9af3bd1eee9e7
        role: Security Guard (Obshak Basement)
      - id: 3308
        filter: actor=3308
        tag: Alan Wh Wong
        tagKey: 66981d0bdcafced077160d19
        role: Doctor
      - id: 3309
        filter: actor=3309
        tag: Sharon Bajer
        tagKey: 5d776838151a60001f24e8fe
        role: Receptionist
        thumb: https://metadata-static.plex.tv/people/5d776838151a60001f24e8fe.jpg
      - id: 3310
        filter: actor=3310
        tag: Yulia Guzhva
        tagKey: 60b90596526b16002d6b1d25
        role: Karaoke Singer
      - id: 3311
        filter: actor=3311
        tag: Boris Gulyarin
        tagKey: 5d776d267a53e9001e752a57
        role: Mob Boss
        thumb: https://metadata-static.plex.tv/people/5d776d267a53e9001e752a57.jpg
      - id: 3312
        filter: actor=3312
        tag: Alex Nikolaychuk
        tagKey: 64c10b5f5b2d39db72ea18b4
        role: Mob Boss
      - id: 3313
        filter: actor=3313
        tag: Volodymyr Yamnenko
        tagKey: 5d776a5196b655001fdeac0c
        role: Mob Boss
        thumb: >-
          https://metadata-static.plex.tv/e/people/e00c1e06d5bd36b8afef7abadb3397a7.jpg
      - id: 3314
        filter: actor=3314
        tag: Meaghan Ann De Werrenne-Walle
        tagKey: 60b905965f7d3f002cb034d1
        role: Waitress (Karaoke Club)
      - id: 3315
        filter: actor=3315
        tag: Eugene Baffoe
        tagKey: 5ec419e0f8a5e90040cfaadb
        role: Barber's Guard
        thumb: >-
          https://metadata-static.plex.tv/0/people/08f07e73e74d04362ff80af43e27af9a.jpg
      - id: 3316
        filter: actor=3316
        tag: Daniel Bernhardt
        tagKey: 5d776828a091de001f2e6428
        count: 4
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/8/people/894ce74954806b4f55fac059f5af9bd9.jpg
      - id: 3317
        filter: actor=3317
        tag: Alain Moussi
        tagKey: 5d776b5096b655001fe0c5ab
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/5/people/5de5e70da005d9bcd84ee387ccd06079.jpg
      - id: 3318
        filter: actor=3318
        tag: Stéphane Julien
        tagKey: 5d776ac796b655001fdf93cc
        count: 2
        role: Bus Goon
        thumb: >-
          https://metadata-static.plex.tv/c/people/c5501403d440b91a3c0d86cfe283523b.jpg
      - id: 3319
        filter: actor=3319
        tag: Robert Heinamaki
        tagKey: 60b90596b6a3c2002cb5df92
        role: Body Builder
      - id: 3320
        filter: actor=3320
        tag: Brent Alarie
        tagKey: 60b90596526b16002d6b1d27
        role: Tattoo Parlor
      - id: 66738
        filter: actor=66738
        tag: Tyrell Witherspoon
        tagKey: 6837cbc422219f2940060d8a
        role: Dancer
      - id: 3322
        filter: actor=3322
        tag: Frederick Allen
        tagKey: 5e166be52d4d84003e4bede0
        role: Russian Mafia Member (uncredited)
        thumb: >-
          https://metadata-static.plex.tv/7/people/7904579927adae5ff33b8149870c5cf4.jpg
      - id: 3323
        filter: actor=3323
        tag: Destini Boldt
        tagKey: 64b018cffa119025f00aa26c
        role: Club Patron (uncredited)
    Producer:
      - id: 3324
        filter: producer=3324
        tag: David Leitch
        tagKey: 5d776828151a60001f24ae96
        count: 3
        thumb: >-
          https://metadata-static.plex.tv/4/people/4d935845dd16ac700054162203566edd.jpg
      - id: 3325
        filter: producer=3325
        tag: Kelly McCormick
        tagKey: 5d776b49fb0d55001f5629d7
        count: 2
        thumb: >-
          https://metadata-static.plex.tv/0/people/09afce317f35900bdcd7518664795277.jpg
      - id: 3326
        filter: producer=3326
        tag: Bob Odenkirk
        tagKey: 5d77683254f42c001f8c3f69
        thumb: >-
          https://metadata-static.plex.tv/5/people/592f471ba9c48dfc0073f753e2235e22.jpg
      - id: 3327
        filter: producer=3327
        tag: Marc Provissiero
        tagKey: 5d776bb747dd6e001f6e242d
        thumb: >-
          https://metadata-static.plex.tv/2/people/2b65cf07ae7032dd37dfe24ff0b00870.jpg
      - id: 66739
        filter: producer=66739
        tag: Braden Aftergood
        tagKey: 6839e0351aa1f166b353d040
        thumb: >-
          https://metadata-static.plex.tv/9/people/9d5f88c6dbff24ede9bd423ea2fc0b95.jpg
    Field:
      - locked: true
        name: thumb
      - locked: true
        name: genre
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
payload:
  rating: 8
  event: media.rate
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex player uuid}
  Metadata:
    librarySectionType: artist
    ratingKey: '17955'
    key: /library/metadata/17955
    parentRatingKey: '17950'
    grandparentRatingKey: '17949'
    guid: plex://track/5d07cdb3403c640290f4d455
    parentGuid: plex://album/5d07c1e5403c6402908857d5
    grandparentGuid: plex://artist/5d07bc02403c6402904aa2a7
    parentStudio: Capitol Records
    type: track
    title: Hollywood Nights
    grandparentKey: /library/metadata/17949
    parentKey: /library/metadata/17950
    librarySectionTitle: Music
    librarySectionID: 8
    librarySectionKey: /library/sections/8
    grandparentTitle: Bob Seger & the Silver Bullet Band
    parentTitle: Greatest Hits
    summary: ''
    index: 5
    parentIndex: 1
    ratingCount: 33577
    userRating: 8
    viewCount: 12
    lastViewedAt: 1749681668
    lastRatedAt: 1749682449
    parentYear: 1994
    thumb: /library/metadata/17950/thumb/1747412353
    art: /library/metadata/17949/art/1749608188
    parentThumb: /library/metadata/17950/thumb/1747412353
    grandparentThumb: /library/metadata/17949/thumb/1749608188
    grandparentArt: /library/metadata/17949/art/1749608188
    addedAt: 1747412346
    updatedAt: 1748915428
    Image:
      - alt: Hollywood Nights
        type: coverPoster
        url: /library/metadata/17949/thumb/1749608188
      - alt: Hollywood Nights
        type: background
        url: /library/metadata/17949/art/1749608188
    Genre:
      - id: 38623
        filter: genre=38623
        tag: Pop/Rock
    Guid:
      - id: mbid://08f9ed5a-1c38-387d-9491-9cea9805a479
    Mood:
      - id: 39303
        filter: mood=39303
        tag: Earthy
      - id: 39107
        filter: mood=39107
        tag: Earnest
      - id: 38631
        filter: mood=38631
        tag: Passionate
      - id: 39696
        filter: mood=39696
        tag: Hungry
```
## Season Rate
##### TV Season is rated.
```yaml

```
## Episode Rate
##### TV Episode is rated.
```yaml
payload:
  rating: 7
  event: media.rate
  user: true
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex public uuid}
  Metadata:
    librarySectionType: show
    ratingKey: '1966'
    key: /library/metadata/1966
    parentRatingKey: '1965'
    grandparentRatingKey: '1964'
    guid: plex://episode/61e8260c263955a780cf92fd
    parentGuid: plex://season/602e7abd88e0a9002dfa0c65
    grandparentGuid: plex://show/5ec75ff037d69c0039b83267
    grandparentSlug: star-trek-strange-new-worlds
    type: episode
    title: Strange New Worlds
    grandparentKey: /library/metadata/1964
    parentKey: /library/metadata/1965
    librarySectionTitle: TV
    librarySectionID: 7
    librarySectionKey: /library/sections/7
    grandparentTitle: 'Star Trek: Strange New Worlds'
    parentTitle: Season 1
    contentRating: TV-PG
    summary: >-
      When one of Pike’s officers goes missing while on a secret mission for
      Starfleet, Pike has to come out of self-imposed exile. He must navigate
      how to rescue his officer, while struggling with what to do with the
      vision of the future he’s been given.
    index: 1
    parentIndex: 1
    audienceRating: 7.5
    userRating: 7
    skipCount: 1
    lastRatedAt: 1749682269
    year: 2022
    thumb: /library/metadata/1966/thumb/1749085463
    art: /library/metadata/1964/art/1747275883
    parentThumb: /library/metadata/1965/thumb/1733009675
    grandparentThumb: /library/metadata/1964/thumb/1747275883
    grandparentArt: /library/metadata/1964/art/1747275883
    grandparentTheme: /library/metadata/1964/theme/1747275883
    duration: 3180000
    originallyAvailableAt: '2022-05-05'
    addedAt: 1733009522
    updatedAt: 1749085463
    audienceRatingImage: themoviedb://image.rating
    chapterSource: media
    Image:
      - alt: Strange New Worlds
        type: coverPoster
        url: /library/metadata/1964/thumb/1747275883
      - alt: Strange New Worlds
        type: snapshot
        url: /library/metadata/1966/thumb/1749085463
      - alt: Strange New Worlds
        type: background
        url: /library/metadata/1964/art/1747275883
      - alt: Strange New Worlds
        type: clearLogo
        url: /library/metadata/1964/clearLogo/1747275883
    UltraBlurColors:
      topLeft: 49210d
      topRight: 5d250c
      bottomRight: '924324'
      bottomLeft: 3c2809
    Guid:
      - id: imdb://tt12330364
      - id: tmdb://3455959
      - id: tvdb://8785342
    Rating:
      - image: imdb://image.rating
        value: 8.1
        type: audience
      - image: themoviedb://image.rating
        value: 7.5
        type: audience
    Director:
      - id: 31782
        filter: director=31782
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/4/people/4b551e483c0f6e124a2b41d672808386.jpg
    Writer:
      - id: 31783
        filter: writer=31783
        tag: Akiva Goldsman
        tagKey: 5d7768265af944001f1f6708
        thumb: >-
          https://metadata-static.plex.tv/f/people/f8f7fa7c7b9e0a80f0a8a1bfb20961d0.jpg
      - id: 14215
        filter: writer=14215
        tag: Alex Kurtzman
        tagKey: 5d77682a999c64001ec2d250
        thumb: >-
          https://metadata-static.plex.tv/f/people/fa310b367421ffe27bc11a758135d751.jpg
      - id: 31784
        filter: writer=31784
        tag: Jenny Lumet
        tagKey: 5d77691a47dd6e001f6c3406
        thumb: >-
          https://metadata-static.plex.tv/5/people/5453958cc06c3dfb343a7b1e4fc4061f.jpg
    Role:
      - id: 31517
        filter: actor=31517
        tag: Anson Mount
        tagKey: 5d776833eb5d26001f1e02a7
        role: Captain Christopher Pike
        thumb: >-
          https://metadata-static.plex.tv/2/people/28cbe22261c22769cc73b861c4e96117.jpg
      - id: 31518
        filter: actor=31518
        tag: Ethan Peck
        tagKey: 5d7768535af944001f1ff612
        role: Spock
        thumb: >-
          https://metadata-static.plex.tv/b/people/b95e1c83662a27139421110fcdae9875.jpg
      - id: 31519
        filter: actor=31519
        tag: Jess Bush
        tagKey: 5d7770a17a53e9001e7a7820
        role: Christine Chapel
        thumb: >-
          https://metadata-static.plex.tv/a/people/ab53153640df8c8ed77ad2a0fd7f84e0.jpg
      - id: 24567
        filter: actor=24567
        tag: Christina Chong
        tagKey: 5d77689c3ab0e7001f505b3a
        role: La'an Noonien-Singh
        thumb: >-
          https://metadata-static.plex.tv/0/people/02a6d83b818f342308c7eb6f88d8a7a0.jpg
      - id: 31520
        filter: actor=31520
        tag: Celia Rose Gooding
        tagKey: 5f3fcc8302101b0040ed14d7
        role: Nyota Uhura
        thumb: >-
          https://metadata-static.plex.tv/7/people/72d95a6b2b1cb8dd864c417a2c5c1fca.jpg
      - id: 31521
        filter: actor=31521
        tag: Melissa Navia
        tagKey: 5d7768b5308bca0020330942
        role: Erica Ortegas
        thumb: >-
          https://metadata-static.plex.tv/d/people/d0d6d99c83ee88e134eee8514fd8f8c8.jpg
      - id: 31522
        filter: actor=31522
        tag: Babs Olusanmokun
        tagKey: 5d77691551dd69001fe14a16
        role: Dr. Joseph M'Benga
        thumb: >-
          https://metadata-static.plex.tv/e/people/e05c1cadfb147d2af5900bf0c730c1be.jpg
      - id: 5721
        filter: actor=5721
        tag: Rebecca Romijn
        tagKey: 5d7768283c3c2a001fbcb634
        role: Una Chin-Riley
        thumb: >-
          https://metadata-static.plex.tv/7/people/7c5a72847a551338d7cc9dd5ce29e168.jpg
      - id: 31523
        filter: actor=31523
        tag: Bruce Horak
        tagKey: 5f4009aa52f20000414ec84a
        role: Hemmer
        thumb: >-
          https://metadata-static.plex.tv/3/people/3fc2ed3209f1b41eed851f7968002cd8.jpg
      - id: 18013
        filter: actor=18013
        tag: Samantha Smith
        tagKey: 5d77682a2ec6b5001f6baa0d
        role: Eldredth Leader
        thumb: >-
          https://metadata-static.plex.tv/1/people/1f6f7c1f10d6144f0f6f2c248fbd37a8.jpg
      - id: 31536
        filter: actor=31536
        tag: Carla Bennett
        tagKey: 5f3fd28d03883a0040ac062e
        role: 'Palion Aide #2'
      - id: 31537
        filter: actor=31537
        tag: Peter Bou-Ghannam
        tagKey: 5f406ea5427eeb0041ee367f
        role: Palion Leader
        thumb: >-
          https://metadata-static.plex.tv/e/people/e1442a2dfe8442654806c2d6a7897a9d.jpg
      - id: 31538
        filter: actor=31538
        tag: Marienne Castro
        tagKey: 5f405c8ccae2c60042f7ac5f
        role: Shuttle Pilot
        thumb: >-
          https://metadata-static.plex.tv/0/people/07a4bbb1d2f99e444c9de59413530ceb.jpg
      - id: 31539
        filter: actor=31539
        tag: Bessie Cheng
        tagKey: 5f3fc306ce2564003f853ed9
        role: 'Eldredth Aide #2'
        thumb: >-
          https://metadata-static.plex.tv/5/people/54c80a73d51262aef9e3ab7a4c06ed6f.jpg
      - id: 31540
        filter: actor=31540
        tag: John Chou
        tagKey: 62753c184d3d1cb58e93d506
        role: 'Kiley Scientist #1'
      - id: 31541
        filter: actor=31541
        tag: Joseph Daly
        tagKey: 5f3ff78bfea1a1003f9b2369
        role: 'Eldredth Aide #1'
        thumb: >-
          https://metadata-static.plex.tv/5/people/53f78913242f64d56316ee75f341c1b2.jpg
      - id: 31542
        filter: actor=31542
        tag: Myles Dobson
        tagKey: 5d776a8f51dd69001fe250f1
        role: Vulcan Waiter
        thumb: https://metadata-static.plex.tv/people/5d776a8f51dd69001fe250f1.jpg
      - id: 31543
        filter: actor=31543
        tag: Chandra Galasso
        tagKey: 5d776b30594b2b001e6d24cd
        role: Lieutenant
        thumb: >-
          https://metadata-static.plex.tv/b/people/b88852fe91228e8f5e6c89bf8a5227b4.jpg
      - id: 31544
        filter: actor=31544
        tag: Jaimee Joe Gonzaga
        tagKey: 602d810722796e002dce6fd6
        role: 'Terminal Jockey #2'
      - id: 31545
        filter: actor=31545
        tag: Sandy Kerr
        tagKey: 5f3ff9e404a86500409ba8bd
        role: 'Starfleet Scientist #1'
      - id: 3378
        filter: actor=3378
        tag: Joel Lacoursiere
        tagKey: 5d776b32fb0d55001f55f89f
        role: 'Kiley Guard #1'
      - id: 31546
        filter: actor=31546
        tag: Dana Levenson
        tagKey: 629130c2ed685fc4708979bc
        role: Newscaster
      - id: 31547
        filter: actor=31547
        tag: Andrew Locke
        tagKey: 5f3fd0dd03883a0040abe2eb
        role: 'Terminal Jockey #1'
      - id: 31548
        filter: actor=31548
        tag: Etan Muskat
        tagKey: 5d77685f3ab0e7001f4ff787
        role: 'Starfleet Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/e/people/e5281dd2c6869adfc8c38b383f6ae3e8.jpg
      - id: 31549
        filter: actor=31549
        tag: Daniel Pagett
        tagKey: 5f4006d81ae710004102d3ae
        role: 'Kiley Scientist #2'
        thumb: >-
          https://metadata-static.plex.tv/a/people/a994871d39cc04fe6fda3de89130ab55.jpg
      - id: 31550
        filter: actor=31550
        tag: Rachel Sellan
        tagKey: 5d7768a0decfcd001f2ee614
        role: Woman in Elevator
        thumb: https://image.tmdb.org/t/p/original/1T4h8GPtXa2B3NWqzJ90whLZGvK.jpg
      - id: 31528
        filter: actor=31528
        tag: Adrian Holmes
        tagKey: 5d7768315af944001f1f8e5d
        role: Admiral Robert April
        thumb: >-
          https://metadata-static.plex.tv/8/people/847f9bd416bbeb7dfd1141508b9fce60.jpg
      - id: 31529
        filter: actor=31529
        tag: Gia Sandhu
        tagKey: 5d776b9fad5437001f7a51af
        role: T'Pring
        thumb: >-
          https://metadata-static.plex.tv/7/people/7134a5a24907c3624622f8eec68ea9b7.jpg
      - id: 31524
        filter: actor=31524
        tag: Dan Jeannotte
        tagKey: 5d7768726f4521001eaa76c0
        role: George Samuel 'Sam' Kirk
        thumb: >-
          https://metadata-static.plex.tv/0/people/061d8cd023a1a686ddbdf055cea91b5f.jpg
      - id: 31527
        filter: actor=31527
        tag: Melanie Scrofano
        tagKey: 5d77684b2e80df001ebe0e3a
        role: Captain Marie Batel
        thumb: >-
          https://metadata-static.plex.tv/c/people/cbc66df9d39f2ab6b5c35edba96721cc.jpg
      - id: 31525
        filter: actor=31525
        tag: Rong Fu
        tagKey: 5d776d9e47dd6e001f6f4b93
        role: Jenna Mitchell
        thumb: >-
          https://metadata-static.plex.tv/7/people/7593afaa022e743a3b7736dbe326a3e9.jpg
      - id: 31526
        filter: actor=31526
        tag: André Dae Kim
        tagKey: 5f401a4c03883a0040b2ae4b
        role: Chief Kyle
        thumb: >-
          https://metadata-static.plex.tv/7/people/77500e32058dbe3cea766035d600b250.jpg
      - id: 31594
        filter: actor=31594
        tag: David Kirby
        tagKey: 6308b629fbb5dda04b436928
        role: 'Palion Aide #1'
      - id: 31650
        filter: actor=31650
        tag: Jon Blair
        tagKey: 5f400f1e768fc70040549f43
        role: 'Kiley Guard #2'
    Producer:
      - id: 31789
        filter: producer=31789
        tag: Paul Gadd
        tagKey: 5e164048df4678003f524f3e
      - id: 31790
        filter: producer=31790
        tag: Andrea Raffaghello
        tagKey: 5d776cc7fb0d55001f5922a8
        thumb: >-
          https://metadata-static.plex.tv/0/people/0d1c2013efdbddf16d7ea172de7deb39.jpg

```
## Admin Database Backup
##### A database backup is completed successfully via Scheduled Tasks.
```yaml
payload:
  event: admin.database.backup
  user: true
  owner: true
  Account:
    id: 2116809
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
```
## Admin Database Corrupted
##### Corruption is detected in the server database.
```yaml

```
## New Device
```yaml
payload:
  event: device.new
  user: false
  owner: true
  Account:
    id: 0
    thumb: ''
    title: ''
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    title: {plex new player title}
    uuid: {plex player uuid}
```
## Playback Started
##### Playback is started by a shared user for the server.
```yaml
payload:
  event: playback.started
  user: false
  owner: true
  Account:
    id: {plex account id}
    thumb: https://plex.tv/users/{url to plex avatar}
    title: {plex account name}
  Server:
    title: {plex server title}
    uuid: {plex server uuid}
  Player:
    local: true
    publicAddress: {plex player public ip}
    title: {plex player title}
    uuid: {plex player uuid}
  Metadata:
    librarySectionType: artist
    ratingKey: '14343'
    key: /library/metadata/14343/children
    parentRatingKey: '8260'
    guid: plex://album/5d07c198403c64029085a378
    parentGuid: plex://artist/5d07bbfc403c6402904a634d
    studio: A&M Records
    type: album
    title: Waking Up the Neighbours
    parentKey: /library/metadata/8260
    librarySectionTitle: Music
    librarySectionID: 8
    librarySectionKey: /library/sections/8
    parentTitle: Bryan Adams
    summary: ''
    index: 1
    year: 1991
    thumb: /library/metadata/14343/thumb/1740441839
    art: /library/metadata/8260/art/1749178785
    parentThumb: /library/metadata/8260/thumb/1749178785
    originallyAvailableAt: '1991-09-23'
    leafCount: 15
    viewedLeafCount: 0
    addedAt: 1733013296
    updatedAt: 1740441839
    loudnessAnalysisVersion: '2'
    Image:
      - alt: Waking Up the Neighbours
        type: coverPoster
        url: /library/metadata/14343/thumb/1740441839
      - alt: Waking Up the Neighbours
        type: background
        url: /library/metadata/8260/art/1749178785
    UltraBlurColors:
      topLeft: 59041f
      topRight: 9b0424
      bottomRight: 1a1917
      bottomLeft: 4b4b53
    Format:
      - id: 38742
        filter: format=38742
        tag: Album
    Guid:
      - id: mbid://5c48c3c4-8e13-45f2-81e1-f011934c42ee
    Mood:
      - id: 38633
        filter: mood=38633
        tag: Lively
      - id: 38740
        filter: mood=38740
        tag: Rousing
      - id: 39155
        filter: mood=39155
        tag: Lush
      - id: 39121
        filter: mood=39121
        tag: Theatrical
      - id: 38995
        filter: mood=38995
        tag: Plaintive
      - id: 38738
        filter: mood=38738
        tag: Sentimental
      - id: 38846
        filter: mood=38846
        tag: Sweet
      - id: 38631
        filter: mood=38631
        tag: Passionate
      - id: 38948
        filter: mood=38948
        tag: Slick
      - id: 38940
        filter: mood=38940
        tag: Dramatic
      - id: 38739
        filter: mood=38739
        tag: Yearning
      - id: 38997
        filter: mood=38997
        tag: Reflective
      - id: 39132
        filter: mood=39132
        tag: Wistful
      - id: 39107
        filter: mood=39107
        tag: Earnest
      - id: 38625
        filter: mood=38625
        tag: Celebratory
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
