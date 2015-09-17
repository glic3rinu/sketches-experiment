# sketches-experiment

```bash
pip install requests

# env is the working directory
cd env
export PATH=$PATH:$(pwd)/../src
getips > ips.txt

# Deploy the experiment on all the nodes
# `run` will run the provided script on the remote nodes, it also accept direct commands like: run ls
run ../src/deploy
^C

# Run the experiment
run ../src/experiment
^C

# Collect the results once the experiment is finished
# Results will be stored in env/results/date/
collect
^C

```
