# Reading Notes
### class 13


## The Past, Present & Future of local storage for web applications

### Before html 5

- Navtive client applications have held an advantage over web applications because of persistent local storage

- For native applications, the operating system typically provides a layer for storing and retrieving application-specific data

- Cookies are what web pages use now for persistent local storage

- Cookies are limited to 4 kb of data

### Brief history of loacl storage hacks beofre html 5

- userData allowed web pages to store up to 64 KB of data per domain.

- Trusted domains could store 10 times that amout

- In 2002, adobe introduced a feature in Flash 6 called Flash cookies. 

- Briefly, it allows Flash objects to store up to 100 KB of data per domain.

- By 2006, with ExternalInterface in Flash 8 accesing Local Storage Objects became a lot easier and faster

- In 2007, Google launched Gears, an open source browser plugin aimed at providing additional capabilities in browsers.

- After obtaining permission from the user once, Gears can store unlimited amounts of data per domain in SQL database tables.

### Inro HTML5 storage

- HTML5 Storage is a specification named Web Storage, which was at one time part of the HTML5 specification proper.

- Certain browser vendors also refer to it as “Local Storage” or “DOM Storage” 

- Local Storage is implemented natively in web browsers, so it is available even when third-party browser plugins are not

- StorageEvent Object
```
key    	   string	      the named key that was added, removed, or modified
oldValue	  any	        the previous value (now overwritten), or null if a new item was added
newValue	  any	        the new value, or null if an item was removed
url*	     string	      the page which called a method that triggered this change

```
- 5 megabytes is how much storage space each origin gets by default

- How does local storage work

'''

function saveGameState() {
    if (!supportsLocalStorage()) { return false; }
    localStorage["halma.game.in.progress"] = gGameInProgress;
    for (var i = 0; i < kNumPieces; i++) {
	localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
	localStorage["halma.piece." + i + ".column"] = gPieces[i].column;
    }
    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
    localStorage["halma.movecount"] = gMoveCount;
    return true;
}

```

- it uses the localStorage object to save whether there is a game in progress (gGameInProgress, a Boolean)




- Local Storage is a way for web pages to store named key/value pairs locally, within the client web browser

- Like cookies, this data persists even after you navigate away from the web site

- 

