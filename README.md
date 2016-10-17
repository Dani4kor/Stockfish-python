------------
## Stockfishpy
------------

Simple python Stockfish UCI Chess Engine wrapper


---------
## SETUP:
---------
* Python 2.7
* [Download](http://www.stockfishchess.com/) and make 'Stockfish' executable


------
## USAGE:
------
Python console Example
```python
>>> from stockfishpy import *
>>> chessEngine = Engine(STOCKFISH_PATH, param={'Threads': 2, 'Ponder': 'true'})
>>> print chessEngine.uciok()
uciok

>>> print chessEngine.isready()
readyok

>>> chessEngine.ucinewgame()
>>> chessEngine.setposition('rnbqkbnr/pppppppp/8/8/4P3/8/PPPP1PPP/RNBQKBNR b KQkq e3 0 1')
>>> move = chessEngine.bestmove()
>>> print move['move']
e7e5

>>> print move['ponder']
g1f3

>>> print move['info']
info depth 12 seldepth 16 multipv 1 score cp -32 nodes 296597 nps 2879582 tbhits 0 time 103 pv e7e5 g1f3 b8c6 f1b5 g8f6 d2d3 f8c5 e1g1 e8g8 b5c6 d7c6 f3e5 d8e7


>>> chessEngine.ucinewgame()
>>> chessEngine.setposition(['e2e4', 'e7e5', 'g1f3'])
>>> move = chessEngine.bestmove()
>>> print move['move']
b8c6

```


-----
## TEST:
-----
```
execute stockfishtest.py
```