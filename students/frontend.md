# Student Engineer Frontend Challenge

There are two parts to ths challenge.

## Part 1 - Getting started

_build a click counter in your favorite frontend framework._

yes, this is meant to be simple, but there is still alot to show in your understanding of the chosen framework.

## Part 2 - Deeper dive

_Implement an autocomplete component in React or your favorite frontend framework and CSS._

- Users should be able to search by typing into the search field.
- Search requests should be sent once every 300ms seconds while the user is typing.
- Entering a new character, the old request should be discarded.
- The search returns objects of two types: photos and live events.
- Search results should be displayed in a container below the input grouped by their type.

### Design:

![full input](https://preview.ibb.co/crTrqk/full.png)

Consider the following API endpoint is available:

`URL: https://your.service.com/api/assets?search=<searchTerm>`
that returns the following

```json
[{
    "id": "1",
    "type": "live",
    "title": "People rule",
    "label": "rules",
    "url": "/live-event-1"
  },
  {
    "id": "2",
    "type": "photo",
    "title": "man with a hat",
    "label": "hat",
    "url": "/photo-1"
  },
  {
    "id": "3",
    "type": "photo",
    "title": "man with a car",
    "label": "car",
    "url": "/photo-2"
  },
  {
    "id": "4",
    "type": "live",
    "title": "people watching tv",
    "label": "televison",
    "url": "/live-event-2"
  },
  ...]
```

Hint: Lodash/UnderscoreJS can be used.