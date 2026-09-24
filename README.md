# lessons

Class definitions for the [Deepgram AI Collaboration Hub](https://dgeventhub.com) event site.

One folder per class. Everything the site shows about a class — its slides, its running
order, its prerequisites, what attendees leave with — lives in `<class-id>/site/class.json`.

| Class | Runs as |
| --- | --- |
| [`vapi-partner-event`](vapi-partner-event/site/class.json) — Your First Phone Agent | Slides, a live Flux interview, then more slides |
| [`avatar-workshop`](avatar-workshop/site/class.json) — Avatar Workshop | A browser-based avatar build, then slides |

## What belongs here

Reusable class content, and nothing else.

**Never put in this repository:** API keys or tokens, event dates, invite codes, attendee
names or lists, interview transcripts, or anything specific to one running of a class.
Those live in the site's database, attached to an event rather than to a class. This
repository is public.

A class manifest containing anything shaped like a credential is rejected on import.

## Editing a class

Edit the `class.json` and commit. The site validates every change before it takes effect;
if a change fails validation the previous version keeps serving and the error is shown to
the organizer rather than to attendees.

See [SCHEMA.md](SCHEMA.md) for every field, the allowed values, and the validation rules.

## What a class cannot do

A class is content. It cannot introduce code.

The `runner` field may only name an interactive runtime the site already ships — today
`avatar` or `interview`, or `null` for a class that is slides only. A new runtime needs a
reviewed change to the application itself. That is deliberate: it is what lets this
repository be public and freely editable.
