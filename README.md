# throttle
Rate limiter. Throttle incoming traffic using `Throttle`!, 

## Requirement

1. It needs to be middleware, which means it should be configurable as middleware of each of framework (v2 will be standalone system)
  1.1) it should support `django`
  1.2) it should support `flask`
  1.3) it should support `fastapi`

2. Support multiple algorithms
  2.1) Token bucket
  2.2) Leaking bucket
  2.3) Fixed window counter
  2.4) Sliding window log
  2.5) Sliding window counter
     
3. Once all traffic is delivered to the `throttle`, it should be
  2.1) calling `callback` function
  2.2) passing it to configured `message queue`

4. Connectivity with `Redis` and `memcached`

5. Scalability support
   5.1) Guideline making connection to the cache server to share state
