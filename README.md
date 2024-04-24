# MiniMax-algorithm
The game using MiniMax algorithm

The game involves two players taking turns selecting numbers from an n-element vector. Each player can choose either the first or the last number from the vector on their turn. The game continues until all numbers have been chosen. The objective for each player is to maximize the sum of the numbers they collect. The player who achieves the highest sum wins the game.

For example n = 4, consider the vector [2, 0, 3, 1]. The optimal gameplay for the starting player would be to select [2, 3], leaving the second player with [0, 1] or [1, 0].

Implemented are three different players against whom the MinMax player plays:

Random Agent:
The Random Agent makes decisions randomly without considering any specific strategy. It simply chooses a move randomly from the available options. This agent can be unpredictable and may not always make optimal decisions. However, it can sometimes introduce an element of surprise into the game, which might be advantageous in certain situations.

Greedy Agent:
The Greedy Agent follows a simple strategy of always choosing the move that maximizes its immediate gain without considering the long-term consequences. It typically selects the option that appears most favorable at each step without considering future moves or opponent strategies. While this approach can lead to quick gains in the short term, it may not always result in the best overall outcome.

Ninja Agent:
The Ninja Agent is a more sophisticated player that employs a combination of defensive and opportunistic strategies. It evaluates potential moves based on their immediate benefits as well as their impact on future gameplay. The Ninja Agent aims to minimize risks while capitalizing on opportunities, often adopting a more adaptive and strategic approach compared to the Random and Greedy Agents. This agent is more likely to anticipate opponent moves and adjust its strategy accordingly, making it a formidable opponent in many scenarios.

# Unit Tests
test.py
Unit tests have been conducted to verify whether the algorithm has been implemented correctly.
The algorithm passed all tests successfully.

![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/7b5f7b95-3fd0-4fca-8585-f61897f7df74)
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/a5628c0e-a492-4241-bf2a-90300053af8f)
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/5b6c92b6-dfd1-42ec-8eb1-28ca333e15d5)
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/79652708-923e-4b8b-83be-40852f79367a)
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/f316c2b7-6178-4517-9bde-a8c7fa0dc1e8)

# Results
- Głębokość - Depth
- Średni czas - Mean time
- Średnia suma punktów - Mean sum of points
- Odchylenie standardowe - Standard deviation

Depth: Indicates how far the algorithm goes in analyzing the game tree.
Mean time: Measures the dispersion of data around the average score.
Mean sum of points: The average value of points collected by the algorithm during the game.
Standard deviation: The average time it takes for the algorithm to make a move in the game.

1) MinMaxAgent vs RandomAgent
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/8a7624a2-01b3-46eb-9700-119ac7a0f012)

3) MinMaxAgent vs GreedyAgent
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/4692f472-5b4d-46fa-b30e-8e62395b8f37)

5) MinMaxAgent vs NinjaAgent
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/8b446fe4-dba9-42a8-acc7-7223b478983f)

7) MinMaxAgent vs MinMaxAgent(15)
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/60d0f07f-3eb4-475a-aec2-bb5f5802ef2f)

Depth: The depth of the state tree, which is a parameter of the Minimax algorithm, has a significant impact on the results obtained by the agent in various situations. With increasing depth of the tree, i.e., the number of levels at which the algorithm considers possible moves, the agent can make more thoughtful decisions, potentially leading to better game results. However, the impact of the tree depth is not straightforward and may depend on many factors, such as the opponent's strategy, the complexity of the game, and even randomness or random elements in the game.

Mean time: The game execution time may also depend on the opponent's strategy. If the opponent makes quick decisions or has lower computational complexity, the game execution time may be shorter. On the other hand, more advanced opponent strategies may require longer computation time by the MinMaxAgent.

Mean sum of points: The results obtained by the MinMaxAgent tend to decrease as the opponent's difficulty increases. If the opponent is more sophisticated or employs a more optimal strategy, the MinMaxAgent may struggle to achieve high point sums.

Standard Deviation: The stability of MinMaxAgent's results may also depend on the opponent's strategy. If the opponent is more predictable or employs similar strategies in different games, the standard deviation of MinMaxAgent's results may be lower. On the other hand, more diverse opponent strategies may lead to greater variability in results.
# Histograms
1) Test for tree depth 2 MinMaxAgent vs RandomAgent
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/685eeec0-c5e3-4f92-b2e1-6b9ad077d06c)

3) Test for tree depth 15 MinMaxAgent vs RandomAgent
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/9fbf9a5c-415a-4d73-af61-78f83455c804)

5) Test for tree depth 2 MinMaxAgent vs GreedyAgent
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/83e11047-e27f-439e-a5f9-bb6feb10f4a2)

7) Test for tree deptha 15 MinMaxAgent vs GreedyAgent
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/f8ce0e8e-6867-4712-b873-616fb848d648)

9) Test for tree depth 2 MinMaxAgent vs NinjaAgent
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/5350a2c5-357b-4440-88eb-568066bff2a9)

11) Test for tree depth 15 MinMaxAgent vs NinjaAgent
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/0ae6d457-a44d-46ef-8407-49344830044e)

13) Test for tree depth 2 MinMaxAgent vs MinMaxAgent(15)
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/c25d7285-9d90-49ef-b964-e3dfb08f45a4)

15) Test for tree depth 15 MinMaxAgent vs MinMaxAgent(15)
![image](https://github.com/mik00laj/MiniMax-algorithm/assets/108618874/1fa2811b-84df-4caf-9c0c-da1c387b249f)


The distribution of point sums obtained by the MinMaxAgent for tree depths 2 and 15 can be approximated as a normal distribution, specifically a binomial distribution, as the random variable is discrete rather than continuous. For both tree depths, the majority of results cluster around the mean value, and deviations from this value become increasingly rare, which aligns with the characteristics of a distribution approaching normality.

If the histogram of point sums for one of the agents is shifted towards higher values and has a smaller spread than the histogram for the other agent, we can consider that agent to be better. This implies that the agent achieves higher average scores and is more effective in maximizing the sum of points.


