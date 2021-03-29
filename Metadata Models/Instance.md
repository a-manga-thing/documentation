## Instance
### Properties:
- Float: __API_Version__
- String: __Name__
- String: __Operator__ (Should be an email or other contact)
- String: __Icon__ (Should be a small picture encoded as Base64)
- String: __Description__ (Information about instance)

### REST API Routes:
| Name | Parameteres |  Result
|---|---|---|
/manga/search | String: __title__, String: __authors[]__, String: __artists[]__, String: __tags[]__ | Manga[]
/manga/from_id | Integer: __id__ | Manga
/manga/get_chapter | Integer: __mangaid__, Integer: __ordinal__ | Chapter
/manga/thumbnail | Integer: __mangaid__ | Image
--------
__All multiple parameters (eg authors, tags) should be CSV__  
__Tags can have a `+` or `-` to signify inclusion or exclusion (`+` is default)__  
__All responses except get_page should be JSON-encoded__