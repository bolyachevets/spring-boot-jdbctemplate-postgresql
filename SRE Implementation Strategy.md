# Service Level Indicators

### Up time / Down time
Set up API monitoring (aka scream testing). API monitoring service (e.g. Uptime.com) submits API calls at regular time intervals. If a response other than 200 is obtained as a result of the API call, alert is issued that the service is down. This ensures that failures are recognized as early as possible.

### API response latency
In addition to response code monitoring, we can set up API call latency time alerts. Latency times above a threshold could indicate service issues (e.g. resource starvation)

### Pod resource utilization peaks
We should also monitor pods/nodes running app instances for resource utilization. We want to make sure that sufficient CPU/memory is allocated to each pod/node, representative of typical workloads. Autoscaling lifecycle events for pods/nodes need to be collected (e.g. number/frequency of additional pod deployments, failures to autoscale, etc.)

### DB writes durability
Proportion of uncorrupted DB writes

# Service Level Objectives

Service Level Objectives constantly evolve with the environment and our understanding of the environment.

### Up time / Down time
Observed uptime metric will allow us to get a realistic estimate of current service availability (i.e. number of 9s), which should serve as a benchmark for evaluating future initiative to improve service availability.

### API response latency
We can use collected latency data to compute current latency times for various percentiles (e.g. 90th, 95th, 99th). Not only do we want majority of the re	quests to have fast turnaround (i.e. 90th percentile to have low latency average), but also keep outlier high latency times reasonably low. We can also use latency metrics to uncover code/stack bottlenecks and optimization opportunities.

### Pod resource utilization peaks
Will allow us to fine tune pod resource requests/limits and choose an effective pod autoscaling strategy

### DB writes durability
Will allow us to choose effective DB failover strategy
