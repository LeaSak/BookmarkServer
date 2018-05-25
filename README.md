# Bookmark server / URI Shortener

## About
This is a *bookmark server* or URI shortener that maintains a mapping (dictionary) between short names and long URIs, checking that each new URI added to the mapping actually works (i.e. returns a 200 OK). This was an exercise in the Udacity course ["HTTP & Web Servers"](https://eu.udacity.com/course/http-web-servers--ud303).

## Objective
This server is intended to serve three kinds of requests:
* A GET request to the / (root) path. The server returns a form allowing the user to submit a new name/URI pairing. The form also includes a listing of all the known pairings.
* A POST request containing "longuri" and "shortname" fields. The server checks that the URI is valid (by requesting it), and if so, stores the mapping from shortname to longuri in its dictionary.  The server then redirects back to the root path.
* A GET request whose path contains a short name.  The server looks up that short name in its dictionary and redirects to the corresponding long URI.

## Getting Started
Download this [file](https://github.com/LeaSak/BookmarkServer) or run
```sh
$ git clone https://github.com/LeaSak/BookmarkServer
```
Make sure you have Python 3.0 installed on your computer plus the project modules, then run:
```sh
$ python3 BookmarkServer.py
```


