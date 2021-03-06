# Chainlink External Adapter for iv-outlier-detection

This adapter will fetch the value from GenesisVolatility and check the value difference against Derbit and the latest
on-chain answer. If difference surpasses the threshold for any, it will fail.

Thresholds can be configured with the following env vars:

- `DIFF_ON_CHAIN_THRESHOLD`: Percentage threshold against on-chain answer. Default: 50
- `DIFF_DERBIT_THRESHOLD`: Percentage threshold against derbit value. Default: 30

## Input Params

- `base`, `from`, `coin` or `symbol`: The symbol of the currency to query
- `days` or `period`: The number of days to get the IV result from

## Output

```json
{
   "jobRunID":"1",
   "data":{
      "result":60.1
   },
   "result":60.1,
   "statusCode":200
}
```
