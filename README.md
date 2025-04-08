# Server-Performance-Stats
Write a script to analyse basic server performance stats.

## Requirements
You are required to write a script server-stats.sh that can analyse basic server performance stats. You should be able to run the script on any Linux server and it should give you the following stats:

- [X] Total CPU usage
- [X] Total memory usage (Free vs Used including percentage)
- [ ] Total disk usage (Free vs Used including percentage)
- [ ] Top 5 processes by CPU usage
- [ ] Top 5 processes by memory usage

### Commands CLI
1. ``` top -bn1 | grep "%CPU" | head -n 1 | awk '{print "CPU Usage:", 100-$8"%"}' ```
2. ``` free -m | awk '/Mem:/ {print "Total Mem: " $2 "MB = 100%"}' ```

``` free -m | awk '/Mem:/ {print "Free Mem: " ($4/$2)*100 "%"}' ```

``` free -m | awk '/Mem:/ {print "Usage Mem: " ($3/$2)*100 "%"}' ```


https://roadmap.sh/projects/server-stats
