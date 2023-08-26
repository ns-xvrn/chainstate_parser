#### Chainstate Parser
Parses Bitcoin's LevelDB UTXO set (chainstate folder) and dumps to a flat sqlite table



![alt screenshot](chainstate_screenshot.png)


#### Setup

> **Warning**
> WIP! Requires optimization. This currently takes a few hours so there's a temporary [cut-off](https://github.com/ns-xvrn/chainstate_parser/blob/main/chainstate.py#L70) to limit rows right now.

- Required: >= python3.7
- `pip install -r requirements.txt`
- Shutdown bitcoind and copy chainstate folder inside this package folder
- Run `python chainstate.py`
- The parsed data will be saved down in chainstate.sqlite
- You can load it back in python/dataframes or use [SQLite browser](https://sqlitebrowser.org/) to query

---
#### References:
- https://github.com/in3rsha/bitcoin-chainstate-parser
- https://github.com/proger/utxo-dump
- https://github.com/jimmysong/programmingbitcoin