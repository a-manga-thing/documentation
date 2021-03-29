## Manga
### Properties:
- long: __id__
- enum: __type__
- string: __country_of_origin__
- enum(ongoing, axed, completed): __publication_status__
- boolean: __scanlation_status__
- int: __mal_id__
- int __anilist_id__
- int __mangaupdates_id__

## Title
### Properties:
- long: __manga_id__
- string: __title__

## manga_genre
### Properties:
- int: __id__
- string: __name__

## Genres
### Properties:
- int: __id__
- string: __title__

## Person
### Properties:
- int: __id__
- string: __name__

## Author
### Properties:
- long: __manga_id__
- int: __person_id__

## Artist
### Properties:
- long: __manga_id__
- int: __person_id__

## Chapter
### Properties:
- long: __id__
- long: __manga_id__
- int: __chapter_no__
- string: __chapter_postfix__
- int: __ordinal__
- int: __pages__
- string: __title__
- int: __version__
- string: __language_id__
- long: __group_id__
- long: __date_added__
- string: __ipfs_link__
