## AlphaZero-Gomoku
This is an implementation of the AlphaZero algorithm for playing the simple board game Gomoku (also called Gobang or Five in a Row) from pure self-play training. The game Gomoku is much simpler than Go or chess, so that we can focus on the training scheme of AlphaZero and obtain a pretty good AI model on a single PC in a few hours. 

References:  
1. AlphaZero: Mastering Chess and Shogi by Self-Play with a General Reinforcement Learning Algorithm
2. AlphaGo Zero: Mastering the game of Go without human knowledge

### Example Games Between Trained Models
- Each move  with 400 playouts:  
![playout400](https://raw.githubusercontent.com/junxiaosong/AlphaZero_Gomoku/master/playout400.gif)
- Each move  with 800 playouts:  
![playout800](https://raw.githubusercontent.com/junxiaosong/AlphaZero_Gomoku/master/playout800.gif)

### Requirements
To play with the trained AI models, only need:
- Python >= 2.7
- Numpy >= 1.11

To train the AI model from scratch, further need:
- Theano >= 0.7
- Lasagne >= 0.1

### Getting Started
To play with provided models, run the following script from the directory:  
> python human_play.py  

You may modify human_play.py to try different provided models or the pure MCTS.

To train the AI model from scratch:   
> python train.py

**Tips for training:**
1. It is good to start with a 6 * 6 board and 4 in a row. For this case, we may obtain a reasonably good model within 500~1000 self-play games in about 2 hours.
2. For the case of 8 * 8 board and 5 in a row, it may need 2000~3000 self-play games to get a good model, and it may take about 2 days on a single PC.

