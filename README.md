# HTTP Benchmark Container
Container that replicates a traffic pattern based on a function passed to the container

## Environment Variables
TIMESTART and TIMEEND in UNIX time
TIMESTEP in seconds as integer
TARGET as IPV4 or FQDN # FUNCTION has to be a valid function that can be calculated by bc -l

#### https://www.gnu.org/software/bc/manual/html_chapter/bc_5.html

#### Feel free to overwrite these environment variables, using -e (--env):
TIMESTART=0 TIMEEND=2147483647 TIMESTEP=60 TARGET=1.2.3.4 FUNCTION="(-1)*(x-10)^2+100"

## Example:
#### Function (plot on the right): (-1)*(x-10)^2+100
#### Resulting requests per minute (graph on the left)

![Pattern Comparison](https://github.com/CM2Walki/BenchmarkContainer/blob/master/docs/metricDiag.png)
