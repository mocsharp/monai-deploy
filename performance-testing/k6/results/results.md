# Benchmark/ Baseline #

## Environment Details ##
All tests were performed on AWS cloud on a g4dn.2xlarge ec2 instance. Please see [here](https://aws.amazon.com/ec2/instance-types/g4/) for more details

## Results ##
### 5 sequential associations ###
#### Description ####
Send through the same study 5 times, with a 90 second gap to get average metric for a known study, environment and MAP (liver-seg) set up.

#### Metrics ####
Metrics are shown in seconds.

| Test         | MIG (Payload processed elapsed) | Workflow Manager (Workflow Instance Created) | Workflow Manager (Task Dispatched) | Task Manager (Plugin Started) | Argo (liver-seg execution) |
| ------------ | ------------------------------- | -------------------------------------------- | ---------------------------------- | ----------------------------- | -------------------------- |
| Association1 | 32.8835657                      |                                              |                                    |                               | 60                         |
| Association2 | 29.9969251                      |                                              |                                    |                               | 60                         |
| Association3 | 29.7551576                      |                                              |                                    |                               | 60                         |
| Association4 | 28.8816108                      |                                              |                                    |                               | 61                         |
| Association5 | 27.1322536                      |                                              |                                    |                               | 62                         |
| Average      | 29.72990256                     |                                              |                                    |                               | 60.6                       |


### 5 parallel associations ###

#### Description ####
Send through the same study 5 times in parallel, and gather metrics for a known study, environment and MAP (liver-seg) set up.

#### Metrics ####
| Test         | MIG (Payload processed elapsed) | Workflow Manager (Workflow Instance Created) | Workflow Manager (Task Dispatched) | Task Manager (Plugin Started) | Argo (liver-seg execution) |
| ------------ | ------------------------------- | -------------------------------------------- | ---------------------------------- | ----------------------------- | -------------------------- |
| Association1 | 46.6967919                      |                                              |                                    |                               | 61                         |
| Association2 | 67.1354584                      |                                              |                                    |                               | 60                         |
| Association3 | 72.6302684                      |                                              |                                    |                               | 61                         |
| Association4 | 86.4762341                      |                                              |                                    |                               | 63                         |
| Association5 | 95.7458654                      |                                              |                                    |                               | 63                         |
| Average      | 73.73692364                     |                                              |                                    |                               | 61.6                       |
