# DIET-paper

Source code to reproduce results of our paper "DIET: Lightweight Language Understanding for Dialogue Systems"

In order to reproduce the experiments results, execute the following steps:

(1) We used Rasa for running the experiments. 
You first need to clone the repository, checkout the branch `diet-paper` and install Rasa.

```bash
git clone https://github.com/RasaHQ/rasa
git checkout diet-paper
make install-full
```

(2) Execute the `run.sh` script to train and test models on ATIS, SNIPS, and NLU Evaluation Dataset. 
You need to specify what results you want to reproduce by specifying the table in the paper.
Make sure you are at the root directory of this repository before executing the script.

```bash
./run.sh [table-1|table-2|table-3|table-4|table-5]
```

Consider executing the experiments on a machine with a GPU to speed up the experiments.

(3) The experiments results can be found in the folder `experiments`.

To test other featurization or hyperparameters update the configuration files in the `configs` folder.
Available featurization components and a list of available hyperparameters can be found 
[here](https://rasa.com/docs/rasa/nlu/components/).