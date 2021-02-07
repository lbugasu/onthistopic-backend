## Object Schemas

The data items with empty strings and objects suggest one and a list of ids generated by MongoDB respectively
User:

```json
{
  "username": "tinaFaye",
  "password": "yw#L_70UzdqK#[ll",
  "contributions": {
    "podcasts": {},
    "comments": {},
    "themes": {},
    "topics": {},
    "people": {},
    "locations": {}
  }
}
```

Podcast:

```json
{
  "title": "Ted Radio Hour",
  "publisher": "NPR",
  "rssFeed": "https://feeds.npr.org/510298/podcast.xml",
  "link": "https://www.npr.org/programs/ted-radio-hour/",
  "image": "https://media.npr.org/assets/img/2020/03/09/trh_podcast-tile_sq-c05fb259465d433a5cf8a21248b8fa209a6b7690.png?s=1400",
  "categories": [
    "Technology",
    "Science",
    "Social Sciences",
    "Society & Culture"
  ],
  "episodes": {}
}
```

Episodes:

```json
{
  "title": "Building Our Zero-Emissions Future",
  "datePublished": "Fri, 06 Nov 2020 00:01:11 -0500",
  "description": "Fighting climate change is a big, messy task that will take a lot of work. This hour, TED's Science Curator David Biello joins Manoush to share some promising and fascinating solutions.",
  "length": 50322900,
  "sourceUrl": "https://play.podtrac.com/npr-510298/edge1.pod.npr.org/anon.npr-podcasts/podcast/npr/ted/2020/11/20201105_ted_zero_emissions_future-eb2a2def-0491-469e-9c40-f27a162a717a.mp3?awCollectionId=510298&awEpisodeId=931842071&orgId=1&d=3152&p=510298&story=931842071&t=podcast&e=931842071&size=50322900&ft=pod&f=510298",
  "likes": {},
  "comments": {},
  "topics": {},
  "people": {},
  "locations": {}
}
```

Comments:

```json
{
  "content": "There is a fine line between knowing how to speak about death and outright manipulating the listener. I think Krista does it well in this episode",
  "topic": {},
  "location": {},
  "people": {},
  "userID": "",
  "date": "Fri, 06 Nov 2020 00:01:11 -0500",
  "likes": 45
}
```

Topics:
Type can be either themes or people or locations:

```json
{
  "title": "Neo-Clonialism",
  "type": "theme",
  "contributor": "",
  "podcastEpisodes": {}
}
```

## Articles for reference:

- [Converting from Speech to Text with JavaScript](https://tutorialzine.com/2017/08/converting-from-speech-to-text-with-javascript)

## Concept notes for backend

- The features that will differenciate this site from others will be the ability to skip ads - on demand - to achieve this, the algorithm will have to train on some data - how to detect ads.
  It is basically an NLP task. How can one detect ads in a podcast?
- By looking for the following:
  - A break in the pattern/voice of speech,
  - Quotes like "we'll be right back after the break"
  - A different voice speaking. - this usually comes through Ad insertion - where even podcast episodes aired years ago would have recent ads
