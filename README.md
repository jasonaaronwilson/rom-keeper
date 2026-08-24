# ROM Keeper

This a (Linux) tool for retro gamers with large collections of games and multiple (emulation station) based consoles.

Command line tools allow "importing" (or reimporting) a consoles ROMs into a master database (file based blob-store for now - a sqlite database may eventually handle other metadata). The database itself is based of SHA1 hashes so if a large ROM appears in multiple systems then it's still stored only once per database.

(Coming soon - we will also put game metadata like screenshots into the database saving scraping things again).

Additional tools allow you to directly export a few games directly to a ROOM directly to the SD card copy over the metadata and fixing up the xml file emulation station uses. Of course you may just want to try out a game so we let you delete a game from the console (but checks that the game is still in your master database)_.

Command line tools are probably not what you are looking for so we supply integreation with a TUI file-manager app called yazi so you can select multiple files to operate on.

The current status is that the importing tool works and I've vibe coded but not tested the yazi integration.

Future thinking is to scraping more meta-data particularly the game rating and syncing that up across devices.

SHA1 is a flawed checksum algorithm but was chosen since there are databases already keyed by the SHA1 hash out there. (SHA1 collisions don't appear randomly, a bad actor has to create them so everything should be fine.)
