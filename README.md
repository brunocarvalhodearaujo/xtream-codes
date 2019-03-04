XTream Codes
============
3rd party SDK api for stream-codes write in javascript

```js
import { Player } from 'xtream-codes'
// or const { Player } = require('xtream-codes')

// initialize player line api
const player = new Player({
  baseUrl: 'http://server:port',
  // username and password of user line
  auth: {
    username: 'test',
    password: 'test'
  }
})

player.baseURL = 'http://server:port'

// retrieve account line information
player.getAccountInfo()
  .then(console.log)
  .catch(console.log)

// GET Live Stream Categories
player.getLiveStreamCategory()
  .then(console.log)
  .catch(console.log)

// GET VOD Stream Categories
player.getVODStreamCategories()
  .then(console.log)
  .catch(console.log)

// GET LIVE Streams
player.getLiveStreams(category?: number) // (This will get All LIVE Streams in the selected category ONLY)
  .then(console.log)
  .catch(console.log)

// GET VOD Streams 
player.getVODStreams(category?: number)
  .then(console.log)
  .catch(console.log)

// GET VOD Info
player.getVODInfo(id: number) // This will get info such as video codecs, duration, description, directors for 1 VOD
  .then(console.log)
  .catch(console.log)

// GET short_epg for LIVE Streams (same as stalker portal, prints the next X EPG that will play soon)
player.getEPGLivetreams(id: number, limit: number)
  .then(console.log)
  .catch(console.log)

// GET ALL EPG for LIVE Streams (same as stalker portal, but it will print all epg listings regardless of the day)
player.getEPGLivetreams(id: number)
  .then(console.log)
  .catch(console.log)
```
