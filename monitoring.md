# Monitoring

## docker stats

Shows how much CPU, memory, network I/O and block I/O your containers are using.

~~~bash
docker stats
~~~

To limit what you see, use the ```--format``` flag

Limit the output to only show CPU and memory stats:

~~~bash
docker stats --format "table {{.Container}}\t{{.CPUPerc}}\t{{.MemUsage}}"
~~~
