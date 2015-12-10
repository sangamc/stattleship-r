# stattleship-r

Stattleship R Wrapper brought to you by [@stattleship](https://twitter.com/stattleship).

## Install
`devtools::install_github("stattleship/stattleship-r")`

## Getting Started
Obtain an access TOKEN from [stattleship.com](www.stattleship.com). Load R and initialize your TOKEN for your session and load the library:

```
library(stattleshipR)
TOKEN <- 'insert-your-token-here'
```

Get all NBA players:

```
library(stattleshipR)
league = "nba"
sport = "basketball"
ep = "players"
q_body = list()
players = stattle(TOKEN, sport=sport, league=league, ep=ep, query=q_body, version=1, verbose=TRUE, walk=TRUE)
```

Get all triple doubles this NBA season:

```
league = "nba"
sport = "basketball"
ep = "stats"
q_body=list(stat="triple_double", type="basketball_doubles_stat")
tripdubs = stattle(TOKEN, sport=sport, league=league, ep=ep, query=q_body, version=1, walk=T)
```

## Next Steps
Want more? Check out our available stats across an expanding number of sports at the [Stattleship Playbook](http://playbook.stattleship.com/).
