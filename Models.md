# Things that need to be addressed

## Meta
- name
- domain
- logo
- licence
- git repo access
- dev teams/areas of responsibility?
- financing

## Content Delivery
- content policy (minimum resolution, multiple scanlations?, official translations, file naming scheme, smut/hentai, space efficient image format, vol covers, MTLs?, empty pages?, pixiv/twitter shorts?, DMCA)
- final decision on ipfs
- own forked implementation?
- who is a node? users with js-ipfs in the browser/instances/others
- private ipfs cluster/pinning consolidation?
- compensation?
- webtorrent?
- need to start collecting and uploading content as soon as possible
- record of who is hosting nodes

## Instances
- master server?
- approve db layout
- name and define every data point
- are volume covers and thumbnails metadata?
- REST api spec
- manga naming and id scheme
- submission system?
- record of who is hosting instances

## Frontend
- hosting
- authentication and admin access
- conditions for indexing
- REST api spec
- site design guidelines





# Metadata Database

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
| Name | Parameters |  Result
|---|---|---|
search | String: __query__ | Manga[]
from_id | Integer: __id__ | Manga
get_chapter | Integer: __mangaid__, Float: __chapter__ | Chapter
get_page | Integer: __mangaid__, Float: __chapter__, Integer: __page__ | Image(?)
--------
__All responses except get_page should be JSON-encoded__
