hypercat-php
============

PHP client binding for the Hypercat (Interop) API. 

Example Usage
-------------

1- Retrieving a Catalogue

```
	config=("key"=> "api_key_here",
            "baseUrl"=> "base_url_here",
            "catalogueUri"=> "catalogue_uri_here"
            );
	$client = new Hypercat($config);
	$offset = 0; //set page offset to 0
	$limit = 10; //set page limit to 10
	$catalogue = $client->getCatalogue($offset, $limit); //returns JSON response object
```
2- Catalogue Simple Search

* The accepted simple search parameters include: "rel", "val" and "href". And they are optional.

```
	config={"key"=> "api_key_here",
            "baseUrl"=> "base_url_here",
            "catalogueUri"=> "catalogue_uri_here"
            };
	$client = new Hypercat($config);
	$offset = 0; //set page offset to 0
	$limit = 10; //set page limit to 10

	// Set search parameters
	param={"rel"=> "rel_here",
            "val"=> "vall_here",
            "href"=> "href_here"
            };
	$catalogue = $client->searchCatalogue($param, $offset, $limit); //returns JSON response object
```
