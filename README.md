# NNSelfDrivingCar : Self Driving Car using Unity3D
> A fully self driving car in Unity from scratch using Neural Networks and Genetic Algorithms inspired by [AJTech's series of tutorials](https://www.youtube.com/watch?v=C6SZUU8XQQ0&list=PL9FeLoYIHiTwyS18t1RUJQCKFy_abl3qe&ab_channel=AJTechAJTech).

## How it works
We consider a population of cars. Each car is controlled by a MLP (multi-layer perceptron) which initialy has random weights. At each frame, the entry of this MLP is the distance between the car and 5 points towards it (see the red lines below) and the outputs allow to chose between accelerating or not (from 1 to 0), and turning left or right (from 1 to -1). Then, the car travels through the circuit and gets a score - fitness- which corresponds to the distance travelled by the car. Of course, the car is instantly killed when touching a wall or if the fitness reach a threshold put to 4000.
Once every car of the population has gain its fitness, we keep the best ones, select some of the best ones to create new individuals slightly modified (small random modification of the values of their weights), and finally, the worst cars are reinitialized (weights are randomized).
This is repeated for a number of iterations called "Generations".

## Results


## Requirements
You need Unity3D to use this project.