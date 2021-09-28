# Student Engineer backend Challenge

There are two parts to this challenge:

## Part 1 - Getting started

_Implement an CLI in your favorite language._

The assets CLI should a `twentythree` handle and it should have the following commands:

- create : `$ twentythree create -type "video" | "Photo" -title "a title" -label "a label" -url "an url"`
- read :
  - all : `$ twentythree read`
  - one : `$ twentythree read [ID]`
- update : `$ twentythree update [ID] -title "a new title" -label "a new label" -url "a new url"`
- delete : `$ twentythree delete [ID]`

The commands should return meaningful success and error messages upon interaction.

### The object model

```ts
interface Asset {
  // Should be UUID
  id: string,
  type: "video" | "photo"
  title: string,
  label: string,
  // Should be a valid RFC 3987 url
  url: string
}
```

- The id should be generated and not be editable.
- The type is only set on creation

## Part 2 - Extending the CLI to web

Implement the assets CLI as a RESTFUL CRUD `API` endpoint based on your CLI.

- create : `POST http://localhost/assets`
- read :
  - `GET http://localhost/assets`
  - `GET http://localhost/assets/[ID]`
- update : `PUT http://localhost/assets/[ID]`
- delete : `DELETE http://localhost/assets/[ID]`