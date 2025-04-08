# Server-Performance-Stats
Write a script to analyse basic server performance stats.

## Requirements
You are required to write a script server-stats.sh that can analyse basic server performance stats. You should be able to run the script on any Linux server and it should give you the following stats:

- [X] Total CPU usage
- [ ] Total memory usage (Free vs Used including percentage)
- [ ] Total disk usage (Free vs Used including percentage)
- [ ] Top 5 processes by CPU usage
- [ ] Top 5 processes by memory usage

### Commands CLI
1. ``` top -bn1 | grep "%CPU" | head -n 1 | awk '{print "CPU Usage:", 100-$8"%"}' ```


https://roadmap.sh/projects/server-stats
