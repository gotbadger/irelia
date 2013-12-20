#Irelia
======

Irelia is a Node.js Wrapper that will allow you to start coding easily with the [League of Legends Oficial API](http://developer.riotgames.com).

Get your API Key at [http://developer.riotgames.com](http://developer.riotgames.com)

There are API limits right now, so use the API with caching with Redis, Memcache, etc.

### Installation

```
npm install irelia
```

### Usage

```javascript
var Irelia = require('irelia');
var irelia = new Irelia({
	endpoint: 'http://prod.api.pvp.net/api/lol/',
	key: 'your_key_goes_here',
	debug: true
});
irelia.getSummonerByName('euw', 'NSZombie', function (err, res){
	console.log(err, res);
});
```
### Constants

irelia.regions['euw'] -> returns: *String* 'Europe West'



### Methods

Callbacks - Response is given asyncronly using callbacks.
```javascript
irelia.getChampions('euw', true, function (err, champions){
	console.log(err, champions);
});
```

- irelia.getChampions(region, freeToPlay[optional], callback);
- irelia.getRecentGamesBySummonerId(region, summonerId, callback);
- irelia.getLeagueBySummonerId(region, summonerId, callback);
- irelia.getSummaryStatsBySummonerId(region, summonerId, season [optional], callback);
- irelia.getRankedStatsBySummonerId(region, summonerId, season [optional], callback);
- irelia.getMasteriesBySummonerId(region, summonerId, callback);
- irelia.getRunesBySummonerId(region, summonerId, callback);
- irelia.getSummonerByName(region, name, callback);
- irelia.getSummonerBySummonerId(region, summonerId, callback);
- irelia.getNamesBySummonerIds(region, summonerIds[Array list], callback);
- irelia.getTeamsBySummonerId(region, summonerId, callback);