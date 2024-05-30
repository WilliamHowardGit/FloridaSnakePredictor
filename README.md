# FloridaSnakePredictor
![EDB2](https://github.com/WilliamHowardGit/FloridaSnakePredictor/assets/47336206/e2075857-787c-4295-8aa8-ff930311c0b0)

## Introduction
Owning property comes hand in hand with the occasional critter stopping by for a visit or attempting to make a more permanent residence. Such critters commonly include birds, racoons, squirrels, and various insects. In Florida, many homeowners encounter snakes on their property. While not extremely common, these encounter are sure to occur more frequently as more and more people move to the state. In 2024 Florida is predicted to have 275,000 new residents move from out of state. Most of these new residents have no knowledge of the local wildlife, and unfortunately snakes are not well liked. 

([Florida Population Growth](https://www.flchamber.com/breaking-down-migration-in-and-out-of-florida/#:~:text=Florida%20has%20seen%20rapid%20population%20growth%20over%20the,in%20its%20recently%20released%20economic%20predictions%20for%202024.))

## Buisness Problem
Snakes are a vital part of the Florida ecosystem. The new Florida residents likely do not know the benefits and risks of living near and around snakes. Snakes are not only fantastic pest control, but many nonvenomous/harmless species such as the Florida Kingsnake will drive away venomous snakes making your property safer. It is my goal to provide an image classification model to help identify whether a snake is venomous or nonvenomous to help residents begin to adjust to their scaley neighbors. 

## Data
The data used to train this model is a collection of snake photographs. The data includes multiple photos of each individual snake species in Florida, native and invasive. Species and photographs were verified using [Florida Museum](https://www.floridamuseum.ufl.edu/florida-snake-id/)

## Models
The data was used to train two Convolutional Neural Network's which predict whether or not a Florida snake is venomous. The first model uses an SGD optimizer and the second model model uses an Adam optimizer. Both models have three convolutional layers, use class weights for the imbalance of venomous/non-venomous snakes, and utilize early stopping as well as regularization to prevent overfitting. Both models consitently have the same Accuracy and F1-Score, but I favor the SGD model as it has the lower test loss value.

    - Accuracy: 89%

    - F1-Score: 83.3%

## Future Insights
  - I would like the model to take all snake photos, good and poor quality.
  - I would like the model to be able to identify individual species.
  - I would like the model to account for locational data for snake species likelehood.

## For More Information
If you would like to review the model and code you may vist my Jupyter Notebook [here](https://github.com/WilliamHowardGit/FloridaSnakePredictor/blob/main/Notebook.ipynb)

If you would like a review my Presentation you may visit it [here](https://docs.google.com/presentation/d/1qlt9wflXGoZEIAHTv1Vztp9pRm-p1yX7od9RHwV2v2A/edit#slide=id.g2e09ca5adf7_1_70)

## Sources 
    - [Snake Bites](https://pawsomeadvice.com/wild/snake-bite-statistics/#:~:text=Venomous%20Snakes%20Bite%207%2C000%E2%80%938%2C000%20People%20in%20the%20US,of%20bites%20occur%20on%20the%20legs%20or%20feet.)
    - [Snake Identification](https://www.floridamuseum.ufl.edu/florida-snake-id/)

## Repository Structure
```
|— README.md                                                 <- The top-level README for reviewers of this project
|— Notebook.ipynb                                            <- Interactive computing environment including analysis in Jupyter notebook
|— .gitignore                                                <- gitignore exclude selected files
|— Snake Photos                                              <- Images used in training and prediction


