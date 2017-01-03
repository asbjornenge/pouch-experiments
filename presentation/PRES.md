title: PouchDB
author:
  name: Asbjorn Enge
  twitter: asbjornenge
  url: http://blog.asbjornenge.com
output: index.html
style: pres.css
controls: false

--

<img src="logo.svg" alt="logo" style="width: 800px;"/>

> PouchDB is an open-source JavaScript database inspired by [Apache CouchDB](http://couchdb.apache.org/) that is designed to run well within the browser.

> PouchDB was created to help web developers build applications that work as well offline as they do online

--

<img src="logo.svg" alt="logo" style="width: 800px;"/>

* All major browsers
* IndexedDB with WebSQL fallback
* Offline support
* Replication (CouchDB and compatible)
* LevelUp + LevelDown API 

--

# LevelDB

* Google 2011 (IndexedDB spec)
* Inspired by BigTable
* Really good!!

--

# LevelDOWN

> LevelDB comes to Node.

* LevelDOWN -> LevelDB
* LevelUP -> High level API
* Write against LevelUP and you can swap DB engine

:tada:

--

# LevelDOWN

* MemDOWN
* RiakDOWN
* MongoDOWN

...and [many](https://github.com/Level/levelup/wiki/Modules#storage-back-ends) others.

-- center

```javascript
var db = new PouchDB('dbname');

db.put({
  _id: 'dave@gmail.com',
  name: 'David',
  age: 69
});

db.changes().on('change', function() {
  console.log('Ch-Ch-Changes');
});

db.replicate.to('http://example.com/mydb');
```

--

https://pouchdb.com/2014/07/25/pouchdb-levels-up.html

--

En test hva er dette?
