# mmrl-metadata

__Intro__

Experimental schema for describing diversity and identity for individuals in and casts of media objects. Where *media object* is defined as a particular media instance: a film, a season of a netflix show, an episode of a broadcast television series, a software release, an album release, a leak of a CDC report, a document containing a year of presidential tax reports, etc.

This schema is in development, is considered experimental, and will remain versioned yet stubbornly unfixed. 

__Design Goals__ 
* Enumerate six dimensions of identity: age, sexuality, gender, nationality, ethnicity, and "z" or transhuman/human/meta categories
* Enumerate a useful but minimal set of tags for describing each of the identity dimensions
* Enumerate tags for common biases 
* Represent Bechdel, Villalobos, Gagen, DuVernay tests. With additional tagging to quantify or infer “diverse ensemble,”  “fully realized lives”, “scenery in white lives” tags. 
* Provide a serialized form of metadata for each media object; useful for creating in-memory objects at runtime
* Support for mechanical/computational sorting and organizing of media objects by streaming platform, genre, and cast diversity
* Used to visualize individual character/role dimensions
* Used to visualize multiple individuals as a cast of a specific media object
* Used to visualize multiple media objects in aggregate
* Use major/minor tagging grammars like "20-29 playing 30-39" to represent complexity 
* Explore use of lean data practices with "just enough" data to ask pre-defined data questions 

 __Background__

 * mailing list (ask for access): mmrl@googlegroups.com
 * Shared Google Drive (ask for access): https://drive.google.com/drive/folders/1ntRMW6nlBdmg9PC9DLw67l2im-vYcZYz
 * Research Questions: https://docs.google.com/document/d/1HOTHqnXEvVQruwxvVD_nsizBc_jA5eItwPY4wHyLkMU/edit#
 * Tagging Diary: https://docs.google.com/document/d/13EYleLGOzrNcB8ZtPQnwgNBLCf0IIjOl9Yq2rMCCDjY/edit
 * Metadata Media Glyph Notes: https://docs.google.com/document/d/1VNKFYL3B7LRe46GPbgxPFM9ne1knue7i_RrU09gRvDw/edit#heading=h.hiv3sny6952h
 
* * *

__Schema Description__

    {
    "name": "",
    "name-key": "",
    "name-key-sub": "",
    "name-key-canonical": "",
    "type": "",
    "id": "",

    "id-imdb": "",
    "id-wikipedia": "",

    "genre-tags": [""],
    "bias-tags": [""],

    "plot-tags": [""],
    "plot-geo": [""],
    "plot-date": [""],

    "distribution-tags": [""],
    
    "production-tags": [""],
    "production-geo": [""],

    "reception-positive-tags": [""],
    "reception-negative-tags": [""],

    "cast-lead-1-ethnicities": [""],
    "cast-lead-1-nationalities": [""],
    "cast-lead-1-genders": [""],
    "cast-lead-1-sexualities": [""],
    "cast-lead-1-ages": [""],
    "cast-lead-1-z": [""],
    "cast-lead-1-name": [""],

    "cast-lead-2-ethnicities": [""],
    "cast-lead-2-nationalities": [""],
    "cast-lead-2-genders": [""],
    "cast-lead-2-sexualities": [""],
    "cast-lead-2-ages": [""],
    "cast-lead-2-z": [""],
    "cast-lead-2-name": [""],
    
    "cast-lead-3-ethnicities": [""],
    "cast-lead-3-nationalities": [""],
    "cast-lead-3-genders": [""],
    "cast-lead-3-sexualities": [""],
    "cast-lead-3-ages": [""],
    "cast-lead-3-z": [""],
    "cast-lead-3-name": [""],
    
    "cast-lead-4-ethnicities": [""],
    "cast-lead-4-nationalities": [""],
    "cast-lead-4-genders": [""],
    "cast-lead-4-sexualities": [""],
    "cast-lead-4-ages": [""],
    "cast-lead-4-z": [""],
    "cast-lead-4-name": [""],    

    "cast-lead-5-ethnicities": [""],
    "cast-lead-5-nationalities": [""],
    "cast-lead-5-genders": [""],
    "cast-lead-5-sexualities": [""],
    "cast-lead-5-ages": [""],
    "cast-lead-5-z": [""],
    "cast-lead-5-name": [""],
    
    "cast-lead-6-ethnicities": [""],
    "cast-lead-6-nationalities": [""],
    "cast-lead-6-genders": [""],
    "cast-lead-6-sexualities": [""],
    "cast-lead-6-ages": [""],
    "cast-lead-6-z": [""],
    "cast-lead-6-name": [""],    

    "cast-lead-7-ethnicities": [""],
    "cast-lead-7-nationalities": [""],
    "cast-lead-7-genders": [""],
    "cast-lead-7-sexualities": [""],
    "cast-lead-7-ages": [""],
    "cast-lead-7-z": [""],
    "cast-lead-7-name": [""],

    "cast-lead-8-ethnicities": [""],
    "cast-lead-8-nationalities": [""],
    "cast-lead-8-genders": [""],
    "cast-lead-8-sexualities": [""],
    "cast-lead-8-ages": [""],
    "cast-lead-8-z": [""],
    "cast-lead-8-name": [""],

    "notes": [""],

    "data-version": "20210317"
    }

    
* * *
 
* __name__ what the media property calls itself: identifier with capitalization and typographic flourish, such as "Westworld" or "#blackAF"
* __name-key__ *machine generated* key to hydrate this persistent representation to an in-memory a60::collection object. *Don't change this.*
* __name-key-sub__ optional *machine generated* key for subsetting collections to a particular episode or title. *Don't change this.*
* __type__ media characteristics, such as "film", "serial", "software", "book"
* __id__ optional numeric identity. If film, nothing, if serial either the season, such as "4" or the season and episode in compressed format, where 301 means SSEE of Season 3 Episode 1, leading zero of season dropped
* __id-imdb__ the root page of the media property's IMDB.com entry
* __id-wikipedia__ the root page of the media property's wikipedia.org entry
* __genre-tags__ union of alpha 60 genre rubric, imdb genres, wikipedia genres, and "diverse ensembles"
* __plot-tags__ union of alpha 60 plot tagging rubric, imdb plot keywords
* __plot-geo__ ostensible geography of media property
* __plot-date__ ostensible time period, deduced from media property, with multiple time periods separated by comma if be
* __cast-lead-1..8-ethnicities__ lead ethnicity, comma separated list
* __cast-lead-1..8-nationalities__ lead nationality, comma separated list
* __cast-lead-1..8-genders__ lead gender, comma separated list
* __cast-lead-1..8-sexualities__ lead sexuality, comma separated list
* __cast-lead-1..8-ages__ lead age deciles, comma separated list
* __cast-lead-1..8-z__ lead form: animal, vegetable, mineral, spirit or other, comma separated list
* __distribution-tags__ wikipedia distributor, such as "netflix" or "disney+" or "cbs all access"
* __production-tags__ optional, unknown if useful, put prouduction overflow here
* __production-geo__ union wikipedia country of origin and imdb production details locations 
* __notes__ optional, overflow and space for custom or prototype tagging 
* __data-version__ last time new data fields were added, in compressed ISO date format, where 20200524 means YYYY-MM-DD of 2020-05-24. *Don't change this.*

* * *

