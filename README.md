# Connect4-Python

(The original readme was translated to English with DeepL)

This project consists of two main components:

* src: which contains the implementation of the game and the agents (robots)
* content: which contains all the teaching material on the subject.

The entire implementation was done in Python. This project is a fork of Keith Galli's project. Some modifications have been made to the implementation, mainly to allow robot-on-robot play.

All the teaching material is new.

The license for this project is MIT License, as can be seen in the [LICENSE](LICENSE) file in the repository. In other words, you can use all the material for any purpose you like. However, it is necessary to cite the authors of this project.

Fabrício Barth is a full-time professor at [Insper Instituto de Ensino e Pesquisa](https://www.insper.edu.br/).

## Setup

To set up the project, I recommend creating a virtual environment:

````bash
python3.9 -m virtualenv venv
source venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
````

## Running the mkdocs server on the local machine

To run the documentation server on a local machine just type:

````bash
cd content
mkdocs serve
````

## Deploying documentation using github actions

There is a `main.yml` file in the `.github/workflows` directory that defines the deployment of documentation on github's gh-pages using actions.

## Examples of running the Liga4 or Connect4 game

The game can be initialized in a few ways via `src/connect4.py` or `src/connect4_with_ai.py`:

* `src/connect4.py`: two players playing manually.
* `src/connect4_with_ai.py`: one manual player and one artificial player.
* `python connect4_with_ai.py random`: the artificial player behaves randomly.
* `python connect4_with_ai.py minmax 5`: the artificial player implements the min-max algorithm. The number entered is the depth that the min-max algorithm will consider - it must be a value greater than or equal to 1.

* `python connect4_with_ai.py flat`: is equivalent to running minmax at depth 1. It is used to show the behavior of an agent that only evaluates the first level of the tree.

* `python connect4_with_ai.py complete`: is equivalent to running minmax at depth 20. It is used to show the behavior of an agent that evaluates the entire search tree.

* `python connect4_ai_versus_ai.py random 0 minmax 5`: the first argument defines the first player. If it is `random` then the second argument can be any value. The third argument defines the second player. If the player is `minmax` then the subsequent argument must always be the depth adopted by `minmax`.


## Compile the slides

To view the files in the slides folder or generate `pdf` from them, just use any Markdown plugin in VSCode.



