# HTTP Proposal Draft - `Content-Warning` headers

## The Purpose

My purpose in designing the `Content-Warning` header was making it more 
convenient for browsers to handle sensitive content such as flashing content,
NSFW, generally triggering or annoying stuff like racist or hateful content.

## The Proposal

The proposal consists of two parts:
- A `Content-Warning` header that provides human-readable warning about the sensitive content,
- A `Content-Warning-Tags` header that provides machine readable tags for the browser to classify the
  sensitive content more easily and display appropriate warnings.

Browsers **MUST** implement a settings menu section about content warning classifiers.
This menu page will contain switches for various sensitive content types that we have not
fully identified yet, and these switches can be set to four modes:

- Show the specific content explicitly, as-is;
- Blur the specific content and display what it is
  when explicitly interacted with;
- Display a specific page inside the browser that displays the contents of the
  `Content-Warning` header, and ask the user if whether want to continue or not.
- Refuse to render to the specific content entirely.
