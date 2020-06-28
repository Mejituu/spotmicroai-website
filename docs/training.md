## Reinforcement Learning Environment

We now have a [Reinforcement Learning Environment](https://github.com/moribots/spot_mini_mini) which uses Pybullet and OpenAI Gym! It contains a variety of optional terrains, which can be activated using **heightfield=True** in the environment class constructor.

If you try to launch the vanilla gait on fairly difficult terrain, Spot will fall very quickly:

![PyBullet](assets/spot_rough_falls.gif)


By training an Augmented Random Search agent, this can be overcome:

![PyBullet](assets/spot_rough_ARS.gif)


If you are new to RL, I recommend you try a simpler example. Notice that if we choose non-ideal parameters for the generated gait, the robot drifts over time with a forward command:

![PyBullet](assets/spot_drift.gif)

You should try to train a policy which outputs a yaw command to eliminate the robot's drift, like this:

![PyBullet](assets/spot_no_drift.gif)

You can choose a PNG-generated terrain:

![PyBullet](assets/spot_png_terrain.png)

Or, for more control, you can choose a programmatically generated heightfield:

![PyBullet](assets/spot_prog_terrain.png)

Notice that when the simulation resets, the terrain changes. What you cannot see is that the robot's link masses and frictions also change under the hood:

![PyBullet](assets/spot_random_terrain.gif)

### Quickstart Reinforcement Learning

```
pip3 install numpy
pip3 install pybullet
pip3 install gym

git checkout spot_forward

cd spot_bullet/src

./spot_ars_eval.py

enter trained policy number: (e.g 149)
```