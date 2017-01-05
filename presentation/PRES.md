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
* Solid Replication (CouchDB and compatible)
* LevelUp compliant...? 

--

<img src="leveldb.svg" alt="logo" style="width: 200px; float: left"/>
<div style="color: #666; font-size: 5em; font-weight: 400; padding-top: 15px; margin-left: 250px">leveldb</div>

* HTML5 ~ WebSQL 💥 (2009 ish) 
* IndexedDB 🙌
* LevelDB by Google (2011)
* Inspired by BigTable
* Really good!!

--

<img src="leveldb.svg" alt="logo" style="width: 200px; float: left"/>
<div style="color: #666; font-size: 5em; font-weight: 400; padding-top: 15px; margin-left: 250px">leveldb</div>


* LevelDB comes to Node 🚀
* LevelUP - Node-friendly API for LevelDB (2012)
* LevelUP 💪 lingua franca for persistent datastores 
* LevelDOWN -> LevelDB
* Write against LevelUP and you can swap DB engine

:tada:

--

# LevelDOWN

* MemDOWN
* RiakDOWN
* MongoDOWN
* SQLdown

...and [many](https://github.com/Level/levelup/wiki/Modules#storage-back-ends) others.

--

<img src="logo.svg" alt="logo" style="width: 800px;"/>

* LevelUp Compliant :heart_eyes: 

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
