# solrmarc-film-scripts
These scripts are used with SolrMarc to extract and index film metadata from MARC records.

SolrMarc can use BeanShell scripts to do additional processing and indexing into Solr. These scripts were used in the [UDVD](https://github.com/UMiamiLibraries/UDVD) project to extract metadata related to films (Directors, Actors, Screenwriters, etc). 

To use these scripts you'll need to add references to them in your index.properties file:
  
    actors = script(actor.bsh), getActorFacet
    composer = script(others.bsh), getComposerFacet
    screenwriter = script(others.bsh), getScreenWriterFacet
    producer = script(others.bsh), getProducerFacet
    director = script(director.bsh), getDirectorFacet

