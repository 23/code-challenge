# Student Engineer backend Challenge

There are two parts to this challenge

## Part 1 - getting started

`Implement an CLI in your favorite language.`

The CLI should have the following commands, I needed it TwentyThree but you are free to call it what you like.

- create : `$ twentythree create --type "the type" --title "a title" --label "a label" --url "a url"`
- read : 
  - one : `$ twentythree read [ID]`
  - all : `$ twentythree read`
- update : `$ twentythree update [ID]`
- delete : `$ twentythree delete [ID]`

### The object model as json

```json
{
    "id": id,
    "type": "video" or "photo",
    "title": string,
    "label": string,
    "url": url
  }
```

- The id should be generated and not be editable.
- The type is only set on creation

## Part 2 - extending the CLI to web

Implement the assets CLI as an API endpoint

Build an REST API that can Create, Read, Update and Delete based on your CLI.

- create : `POST http://localhost/assets`
- read :
  - `GET http://localhost/assets`
  - `GET http://localhost/assets/[ID]`
- update : `PUT http://localhost/assets/[ID]`
- delete : `DELETE http://localhost/assets/[ID]`