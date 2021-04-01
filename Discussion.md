# Things that need to be addressed

## Meta
- name __Settled on Mangaloid as project name. Commercial name will be decided upon when the time comes.__
- domain __Same as above.__
- logo __[/a/ mascot](https://cdn.mangaloid.moe/file/mangaloid/static/img/mangaloid-tan.png)__
- licence __MIT__
- git repo access __Core Dev team: compscifag, cynic, Usag, zhetic__
- dev teams/areas of responsibility? __compscifag, mojo: Instance software, zhetic, Usag: Front-end, qeeble: Testing, cynic: Content__
- financing __There will be financing__

## Content Delivery
- content policy
  - minimum resolution __readable__  
  - multiple scanlations __Up to instance__  
  - official translations __Probably no__  
  - file naming scheme __cid/{int, 2 leading zeros}.{ext}__  
  - smut/hentai __Up to instance__  
  - space efficient image format __Needs more research__  
  - vol covers __Space-efficient thumbnails served by instances__  
  - MTLs __Up to instance__  
  - pixiv/twitter shorts: __Up to instance__  
  - DMCA __fingers crossed__
- final decision on ipfs __We will keep working with it for now__
- own forked implementation? __No__
- who is a node? users with js-ipfs in the browser/instances/others __Only instances until we evaluate JS-IPFS__
- compensation? __Not important__
- webtorrent? __Dismissed, in favor of IPFS__
- need to start collecting and uploading content as soon as possible __cynic's area__
- record of who is hosting nodes __Yes, will be managed by the mangaloid project__

## Instances
- master server? __No__
- approve db layout [__Approved__](https://github.com/a-manga-thing/documentation/blob/main/Metadata%20Models/Manga.md)
- REST api spec [__Speced__](https://github.com/a-manga-thing/documentation/blob/main/Metadata%20Models/Instance.md)
- submission system? __token-based auth, zipped or independent files__
- record of who is hosting instances __yes__

## Frontend
- hosting __yes (github pages?)__
- authentication and admin access __localhost only, until we expand spec to user accounts and perms__
- REST api spec __Coming soon__
- site design guidelines __Go crazy__