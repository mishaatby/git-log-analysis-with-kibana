# git-log-analysis-with-kibana
Visualizes git history - prepares helpful dashboards in Kibana based on parsed git log.
Besides, it shows volume of changes (in loc) done by individual developer.

## Setup
1. Install ELK
2. Define git mailmap to normalize developers names (because they might be using different emails):
3. Import kibana objects

## Usage
1. Get git data:
```sh
git log --pretty=format:"%ai %h a=%aN e=%ae s=%s f=" --numstat --use-mailmap --since="2016-08-23" origin/develop
```
2. Feed the data to logstash using provided config
