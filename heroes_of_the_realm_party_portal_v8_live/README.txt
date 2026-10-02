HEROES OF THE REALM — LIVE D&D PARTY PORTAL v8

This build turns the campaign website into a live collaborative D&D knowledge base.

ROLES

ADMIN / DM
- Full campaign access and DM Vault access.
- Creates accounts and assigns roles.
- Controls which sections and entries players can see.
- Can edit/delete all campaign entries and all party notes.
- Can preview exactly what any Player or Trusted Player sees.

TRUSTED PLAYER
- Can read any sections the Admin grants.
- Can add NPCs, Factions, Locations, Lore, Monsters, Items and Quests.
- Their name is permanently shown on entries they create.
- Can edit/delete only structured entries they personally created.
- Cannot create or edit hidden DM fields such as Secrets or DM Notes.
- Can add and edit their own Party Field Notes on visible entries.

PLAYER
- Can read sections released by the Admin.
- Can add Party Field Notes to any entry they can see.
- Can edit/delete only their own notes.
- Cannot modify the DM's sourcebook/canon entries.

LIVE UPDATES
The server uses Server-Sent Events (SSE). When somebody adds or edits a note/entry,
other logged-in users receive the update without manually refreshing the page.
The dashboard shows Live Party Activity, and record pages update with Party Field Notes.

ATTRIBUTION
Community-created entries show who added them and their role.
Party Field Notes show the author and timestamp.

START LOCALLY
1. Install Node.js 18 or newer.
2. Open a terminal in this folder.
3. Run:
       npm start
   or:
       node server.js
4. Visit:
       http://localhost:3000

RAILWAY
This build remains Railway-ready. See RAILWAY_DEPLOY.md.
Mount a Railway Volume at /app/data so logins, notes and campaign edits persist.

DATA
- data/campaign.json: live campaign, party notes, permissions and board.
- data/users.json: accounts and password hashes.
- initial_campaign.json: clean starter campaign copied into a new empty Railway Volume.

BACKUPS
Use the Admin Export button regularly, and back up the Railway Volume when possible.
