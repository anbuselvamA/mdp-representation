# MDP REPRESENTATION

## AIM:
The aim of this experiment is to create a Markov Decision Process (MDP) representation and implement it in Python to model the decision-making process in optimize the movement of a warehouse robot .
## PROBLEM STATEMENT:

### Problem Description
Design an RL agent in a Kabaddi game, a raider tries to score points by touching opponents and returning safely. Defenders aim to stop the raider by tackling them. The problem is to create a model where both teams make the best decisions to score or prevent scoring.

### State Space
7,tackle,raid



### Sample State

Raid

### Action Space
Raiding,Tackling



### Sample Action
Raid,Defend


### Reward Function
score



### Graphical Representation
![rl](https://github.com/user-attachments/assets/f7d1e765-a7b0-439b-be9b-69898a01b0d8)





## PYTHON REPRESENTATION:

Kabaddi = {
    # State 0: Idle
    0: {
        1: [(0.85, 1, 0, False), (0.15, 2, 0, False)],  
        2: [(0.80, 2, 0, False), (0.20, 0, 0, False)]   #
    },
    
    # State 1: Raiding
    1: {
        1: [(0.90, 3, 1, True), (0.10, 4, 0, False)],    
        2: [(0.70, 2, 0, False), (0.30, 0, 0, False)]   
    },

    # State 2: Defending
    2: {
        1: [(0.60, 1, 0, False), (0.40, 0, 0, False)],
        2: [(0.75, 3, 0, False), (0.25, 4, 0, False)]    #
    },

    # State 3: Scored
    3: {
        1: [(0.95, 1, 0, False), (0.05, 0, 0, False)],  
        2: [(0.80, 0, 0, False), (0.20, 1, 0, False)]    
    },

    # State 4: Out
    4: {
        1: [(0.90, 0, 0, False), (0.10, 4, 0, False)],   
        2: [(0.85, 0, 0, False), (0.15, 4, 0, False)]    
    }
}

Kabaddi


## OUTPUT:
![image](https://github.com/user-attachments/assets/b067f5d6-5b65-4ee4-9d11-b9d84ec4982e)






## RESULT:
Thus, The MDP Represntation of optimized strategy for both raiders and defenders, maximizing points for raiders and preventing tackles.

