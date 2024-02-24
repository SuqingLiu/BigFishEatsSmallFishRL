# BigFishEatsSmallFishRL
Reinforcement Learning Agent with Fishy game : freefishy.org

# Link to My Video: 

  TikTok: https://vm.tiktok.com/ZMMdSberF/

  YouTube (Not complete because I went over 1 minute): https://youtube.com/shorts/DIiVbr6EXKI?si=eSMhCuvsoAbrIxDS

  小红书: http://xhslink.com/q30m7B

In this game, the player controls a fish that consumes smaller fish to gain points and grow larger. The player loses when a larger fish consumes them. The objective is to survive and consume more fish to accumulate points.

I utilized DQN because I needed to simulate the environment frame by frame. I employed OpenAI's Gym to customize my agent and developed functions to observe the entire screen, detect game over, and track the current score.

The reward function I selected is based on the time the agent survives and the points it accumulates. I increment the reward by 1 for each frame the agent survives, and deduct 100 upon death. Additionally, I increase the reward by the difference in score between the current and previous scores. However, this approach did not yield the intended results, as the agent tended to prioritize survival over consuming other fishes. This may be attributed to the fact that the agent grows larger with each fish consumed, complicating the model's understanding of the situation.

The outcome is surprising. After training for a night (8 hours), the resulting agent focuses on surviving and does not prioritize getting more score by eating other fishes. It adapted a mechanism that made it keep moving either left or right and making small adjustments by going up and down. This method effectively mimics the player's behavior in the game, as when the player wants to move in the opposite direction, it pauses momentarily before starting to move. This surprising discovery confirms that reinforcement learning is effective and the reward system has taught it knowledge that it could never acquire otherwise.

To improve, I plan to allow the agent to determine the duration for which it holds the arrow key, which is currently set at 1 second. While this may increase complexity and training costs, I believe it would lead to better decision-making by the agent.

Additionally, I intend to learn how to use Unity to create custom environments for testing reinforcement learning methods.
