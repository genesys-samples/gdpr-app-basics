---
title: "Conclusion"
chapter: true
weight: 90
---

## Conclusion

Congrats! You've reached the end of today's workshop.

You have created and deployed a new client application to process GDPR requests.

Please fill out today's feedback form via this [TODO](TODO).

## Limitations

- Requests are not sorted by `Created Date` because each request to the Users API does not take the same amount of time and come back in a random order
- Some fields do not render properly because an extra API call would be required to get the full value (e.g. shows an `id` instead of a readable name)
