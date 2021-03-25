# Models

## Manga
### Properties:
- Integer: __manga_id__
- String[]: __titles__
- String: __description__

## Creator
### Properties:
- Integer: __manga_id__
- String: __name__

## Chapter
### Properties:
- Integer: __manga_id__
- Float: __number__
- Integer: __page_count__
- Image(?): __image__  
Images should be either Bytes or Base64 String, let's discuss this.

## Instance
### Properties:
- Float: __API_Version__
- String: __Name__
- String: __Operator__ (Should be an email or other contact)
- String: __Icon__ (Should be a small picture encoded as Base64)
- String: __Description__ (Information about instance)

### Methods:
| Name | Parameteres |  Result
|---|---|---|
search | String: __query__ | Manga[]
from_id | Integer: __id__ | Manga
get_chapter | Integer: __mangaid__, Float: __chapter__ | Chapter
get_page | Integer: __mangaid__, Float: __chapter__, Integer: __page__ | Image(?)
--------
__All responses except get_page should be JSON-encoded__