## Instance
### Properties:
- Float: __API_Version__
- String: __Name__
- String: __Operator__ (Should be an email or other contact)
- String: __Icon__ (Should be a small picture encoded as Base64)
- String: __Description__ (Information about instance)

## API Reference

### Routes
| Name | Parameteres |  Result
|---|---|---|
/info | | Instance
/manga/search | String: __title__, String: __author__, String: __artist__, String: __genres[]__ | Manga[]
/manga/from_id | Integer: __id__ | Manga
/manga/get_chapters | Integer: __id__ | Chapter[]
/manga/thumbnail | Integer: __id__ | Image
---
__Parameters are passed as URL-encoded GET parameters__
__Multiple genres should be CSV__   
   
__Search help__  
```
Searches manga database based on title, author, artist and genres/tags
All of these are optional, can be used in any combination and are evaluated
in that specific order.
Args:
    title (str): This is tested in a case-insensitive LIKE clause.
    author (str): This is tested as "equals" and is case-sensitive.
    artist (str): This is tested as "equals" and is case-sensitive.
    tags (list): List of genres/tags. Can be prefixed with either + or -
                    to define inclusion/exclusion (if missing it defaults to +).
                    As for the tags themselves they are tested as "equal" 
                    and are case-sensitive.
```  
   

### Return types

#### __Manga__
```json
{
    "id": int, 
    "type": str, // Manga / Webtoon
    "titles": [str],
    "artists": [str],
    "authors": [str],
    "genres": [str],
    "country_of_origin": str, // (ISO-3166)
    "publication_status": str, // Ongoing, Axed, Completed
    "scanlation_status": bool,
    "mal_id": int,
    "anilist_id": int,
    "mangaupdates_id": int
}
```

#### __Chapter__
```json
{
    "id": int,
    "manga_id": int,
    "chapter_no": int,
    "chapter_postfix": str,
    "ordinal": int,
    "title": str,
    "page_count": int,
    "version": int,
    "language_id": str, // ISO 639-1
    "group_id": int,
    "date_added": int, // UTC Unix Timestamp
    "ipfs_link": str
}
```
