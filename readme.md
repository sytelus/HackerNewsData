#Hacker News Data Dump Up to May 2014#
There are two files that contains all stories and comments posted at Hacker News (https://news.ycombinator.com/) from its start in 2006 to May 29, 2014 (exact dates are below). This was downloaded using simple program available at https://github.com/sytelus/HackerNewsDownloader by making REST API calls to https://hn.algolia.com/api. The program used API parameters to paginate through created date of items to retrieve all posts and comments. The file contains entire sequence of JSON responses exactly as returned by API call in JSON array.

##HNStoriesAll.json##
Contains all the stories posted on HN from Mon, 09 Oct 2006 18:21:51 GMT to Thu, 29 May 2014 08:25:40 GMT.

###Total count###
1,333,789

###File size###
1.2GB uncompressed, 115MB compressed

###How was this created###
The program used to create this file is available at https://github.com/sytelus/HackerNewsDownloader.

###Format###
Entire file is JSON compliant array. Each element in array is json object that is exactly the response that returned by HN Algolia REST API. The property named `hits` contains the actual list of stories. As this file is very large we recommend json parsers that can work on file streams instead of reading entire data in memory.

```json
{
	"hits": [{
		"created_at": "2014-05-31T00:05:54.000Z",
		"title": "Publishers withdraw more than 120 gibberish papers",
		"url": "http://www.nature.com/news/publishers-withdraw-more-than-120-gibberish-papers-1.14763?WT.mc_id=TWT_NatureNews",
		"author": "danso",
		"points": 1,
		"story_text": "",
		"comment_text": null,
		"num_comments": 0,
		"story_id": null,
		"story_title": null,
		"story_url": null,
		"parent_id": null,
		"created_at_i": 1401494754,
		"_tags": ["story",
		"author_danso",
		"story_7824727"],
		"objectID": "7824727",
		"_highlightResult": {
			"title": {
				"value": "Publishers withdraw more than 120 gibberish papers",
				"matchLevel": "none",
				"matchedWords": []
			},
			"url": {
				"value": "http://www.nature.com/news/publishers-withdraw-more-than-120-gibberish-papers-1.14763?WT.mc_id=TWT_NatureNews",
				"matchLevel": "none",
				"matchedWords": []
			},
			"author": {
				"value": "danso",
				"matchLevel": "none",
				"matchedWords": []
			},
			"story_text": {
				"value": "",
				"matchLevel": "none",
				"matchedWords": []
			}
		}
	}],
	"nbHits": 636094,
	"page": 0,
	"nbPages": 1000,
	"hitsPerPage": 1,
	"processingTimeMS": 5,
	"query": "",
	"params": "advancedSyntax=true\u0026analytics=false\u0026hitsPerPage=1\u0026tags=story"
}
```

##HNCommentsAll.json##
Contains all the comments posted on HN from Mon, 09 Oct 2006 19:51:01 GMT to Fri, 30 May 2014 08:19:34 GMT.

###Total count###
5,845,908

###File size###
9.5GB uncompressed, 862MB compressed

###How was this created###
The program used to create this file is available at https://github.com/sytelus/HackerNewsDownloader.

###Format###
Entire file is JSON compliant array. Each element in array is json object that is exactly the response that returned by HN Algolia REST API. The property named `hits` contains the actual list of stories. As this file is very large we recommend json parsers that can work on file streams instead of reading entire data in memory.

```json
{
	"hits": [{
		"created_at": "2014-05-31T00:22:01.000Z",
		"title": null,
		"url": null,
		"author": "rikacomet",
		"points": 1,
		"story_text": null,
		"comment_text": "Isn\u0026#x27;t the word dyes the right one to use here? Instead of dies?",
		"num_comments": null,
		"story_id": null,
		"story_title": null,
		"story_url": null,
		"parent_id": 7821954,
		"created_at_i": 1401495721,
		"_tags": ["comment",
		"author_rikacomet",
		"story_7824763"],
		"objectID": "7824763",
		"_highlightResult": {
			"author": {
				"value": "rikacomet",
				"matchLevel": "none",
				"matchedWords": []
			},
			"comment_text": {
				"value": "Isn\u0026#x27;t the word dyes the right one to use here? Instead of dies?",
				"matchLevel": "none",
				"matchedWords": []
			}
		}
	}],
	"nbHits": 1371364,
	"page": 0,
	"nbPages": 1000,
	"hitsPerPage": 1,
	"processingTimeMS": 8,
	"query": "",
	"params": "advancedSyntax=true\u0026analytics=false\u0026hitsPerPage=1\u0026tags=comment"
}
```

##Where to download##
As GitHub restricts each file to be only 100MB and also has policies against data ware housing, these files are currently hosted at FileDropper.com. Unfortunately FileDropper currently shows ads with misleading download link so be careful on what link you click. Below is the screenshot FileDropper shows and currently the button marked in red would download the actual file.
![](FileDropperDownloadScreen.png?raw=true)

####Stories Download URL####
Download Using Browser: http://www.filedropper.com/hnstoriesall


Download Using Torrent (thanks to @saturation):

`magnet:?xt=urn:btih:00bfc9143ecdc8d3c27a170c2d1474e05ccdbc59&dn=HNStoriesAll.7z&tr=udp%3A%2F%2Ftracker.openbittorrent.com%3A80%2Fannounce`


Now also available at Internet Archive (thanks to Bertrand Fan): https://archive.org/details/HackerNewsStoriesAndCommentsDump

####Comments Download URL####
Download Using Browser: http://www.filedropper.com/hncommentsall


Download Using Torrent (thanks to @saturation):

`magnet:?xt=urn:btih:21abd27bfe4c01264eb0548543606140ee48d19b&dn=HNCommentsAll.7z&tr=udp%3A%2F%2Ftracker.openbittorrent.com%3A80%2Fannounce`


Now also available at Internet Archive (thanks to Bertrand Fan): https://archive.org/details/HackerNewsStoriesAndCommentsDump


##More Info##
See blog entry at http://shitalshah.com/p/downloading-all-of-hacker-news-posts-and-comments/

If you have a suggestion for better place to host these files please create a new inssue in this repo with info and I would take a look at it (or better just fork and host :)).
