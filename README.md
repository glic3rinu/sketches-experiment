# sketches-experiment

```bash
pip install requests
cd
git clone https://github.com/glic3rinu/sketches-experiment.git
```

```bash
# env is the working directory
cd sketches-experiment/env
export PATH=$PATH:$(pwd)/../src

# Collect all the slivers IP addresses
export SLICE_ID=1514
getips > ips.txt

# Deploy the experiment on all the nodes
# `run` will run the provided script on the remote nodes, it also accept direct commands like: run ls
put ../src/timing.cpp
run ../src/deploy
^C

# Run the experiment
run ../src/experiment
^C

# Collect the results once the experiment is finished
# Results will be stored in env/results/date/
get test.pcap
^C

```
