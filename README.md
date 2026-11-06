# Game_SQLscript
This project is written entirely in SQL, for a sqlite database. It aims to create a database behind a hypothetical video game, which creates data entries (event entries) through gameplay. The database is meant to store the status of the characters of the game with efficiency and integrity and serves to return the data to the game when required. This project is still in its early stages and thus incomplete. It may be subject to additional requirements during development.

Current requirements:

-Turns entries into a database of characters. If a character has its first event entry, a new line will be added in the data storage. An already existing character's trait and status will be updated according to the event.

-It should keep a track of the character's inventory.

-It should keep records of which events have taken place, as well as providing the possibility to get insight into identical events.

-Historic data should be stored to ensure data integrity.

The event entries are AI-generated.


Event entry table structure

    id (text) Primary key: Assigns each entry an unique identifier, differentiating identical entries for data integrity,
    timestamp (text) NOT NULL: Reflects time of event.
    name_person (text) NOT NULL: Name of the character to whom the event happened.
    age_person int NOT NULL: Age of the character involved.
    event (text) NOT NULL: the description of the event as presented to the player.
    lp_change (integer): gives the change in life points as consequence of the event. Score is kept in the character table.
    xp_change (integer): gives the change in experience points as consequence of the event. Score is kept in the character table.
    item (text): Optionally, the name of the item lost or gained in the event.
    item_ability (text): Optionally, it gives an ability an item gained or lost the item would give to the character.
    item_colour (text): The color of the object, if one is gained or lost.
    item_lost boolean: TRUE if item is lost, False if not.
    item_gained boolean: TRUE if item is gained, False if not .
    event_location (text): Location in which the event took place.
    event_country (text): Country of the location in which the event took place.
    event_city (text): City where or the city nearest to which the event took place.
