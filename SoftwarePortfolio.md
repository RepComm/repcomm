# Jon's Software Portfolio
Hi, I'm Jon Crowder
My interests and skills make up a broad range of technical and creative capacity.

I don't evaluate the "mile-wide inch-deep" concept to be useful, and I enjoy diving deeply into the subjects I work on.

## Interests

I create projects related to:
- My own interests, primarily to gain new kinds of skills

- problems available to solve at my day-job such as:
  - device inventory database / asset tagging
  - chrome extensions to simplify tasks requiring unnecessary work
  - At-A-Glance notifications for keeping up with content filtering for several hundred students.
  - modernizing IT infrastructure w/o breaking the budget + keeping up with security w/o alienating user way-of-life

## Perspective

Spreadsheets are good for one-offs and pre-solution prototyping, but not permenant replacements for databases.

A good solution shouldn't stop someone from performing a manual task, but rather remove requirement of repetitive work, and reduce the chance for human error. 

It is highly rewarding to take manual processes and turn them into scalable ease-of-use human-in-the-loop solutions.

## Projects
### gimbal
Device / Asset tracking database for Mt St Mary Catholic HS

**Key Tech:**
- [pocketbase](pocketbase.io)
- [preact](preactjs.com)
- Google Workspace
- [GAM](https://github.com/GAM-team/GAM)

Previously an airtable project was used to track student chromebook inventory; assigned users, and repair entries.

I inherited the task of tracking devices and handling maintenance, and quickly ran into several issues:
- Human error in records
- Manual typing of AssetIDs at every turn
- No bar codes on anything
- Incorrect matching of AssetIDs to serial numbers
- Running out of 'free' rows and requiring monthly payment

Initially I migrated to NocoDB, which is meant to emulate airtable, in order to keep the user experience the same.

When I realized NocoDB was lacking in stability and that I was the only remaining person experienced with airtable, I decided to develop gimbal using pocketbase.

The new 2022 devices replaced the old set, which was an opportunity to create new AssetID labels with barcodes of the serial number, as well as comply with OK State regulations on EANS II funds requirements for labelling of tech.

With serial number as the database index, data could then be pulled from either barcode scanning of the device packing material, or alternatively directly from Google Workspace Admin console, or GAM automation tool.

Additionally, any human input error was cleaned up in a second pass by cross referencing from the new database and the google workspace using a script to automatically identify issues.
