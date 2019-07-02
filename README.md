# BiboGoldAPI

Version: v1.1.2_19-04-1O
Data type: json
Data encoding: utf-8
Address: api.bibo.gold


## Trading Pairs

https://bibo.gold/openApi/market/symbols

Lists all the trading pairs available on the exchange
```
{
	"errno":0,
	"errmsg":"success",
	"result":[
		{
			"id":1,
			"symbol":"ZXT-KTC",
			"base_currency":"ZXT",
			"quote_currency":"KTC",
			"min_size":0.01,
			"max_size":10000.0,
			"min_price":0.001,
			"max_price":0.1,
			"maker_fee":0.002,
			"taker_fee":0.0015
		},
		{
			"id":2,
			"symbol":"BTC-USDT",
			"base_currency":"BTC",
			"quote_currency":"USDT",
			"min_size":1.0E-6,
			"max_size":10000.0,
			"min_price":1000.0,
			"max_price":100000.0,
			"maker_fee":0.0015,
			"taker_fee":0.002
		}
	]
}
```


## Pair details

https://bibo.gold/openApi/market/detail

e.g: https://bibo.gold/openApi/market/detail?symbol=BTC-USDT

Details of a trading pair: 24h volume...

GET Parameter: symbol

```
{
	"errno":0,
	"errmsg":"success",
	"result":
	{
		"id":1561941360,
		"amount":"1.3401000000000000145",
		"count":336,
		"open":"12315.3",
		"close":"10904.7",
		"low":"12241.9",
		"high":"12317.6",
		"vol":"15782.39805000000016651644"
	}
}
```

## Trading depth

https://bibo.gold/openApi/market/depth

e.g: https://bibo.gold/openApi/market/depth?symbol=BTC-USDT

Get current order book depth (limit: 50 orders)

