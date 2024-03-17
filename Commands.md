```bash
# Activate redis server
redis-server config/redis.conf

# Connect to redis server via CLI
redis-cli -h localhost -p 6379

# Select Database
SELECT 0

# Retrieve all keys
KEYS *
```

### Troubleshoot:

```bash
65902:C 18 Mar 2024 04:08:02.853 # oO0OoO0OoO0Oo Redis is starting oO0OoO0OoO0Oo
65902:C 18 Mar 2024 04:08:02.853 # Redis version=7.0.15, bits=64, commit=00000000, modified=0, pid=65902, just started
65902:C 18 Mar 2024 04:08:02.853 # Configuration loaded
65902:M 18 Mar 2024 04:08:02.853 * Increased maximum number of open files to 10032 (it was originally set to 8192).
65902:M 18 Mar 2024 04:08:02.853 * monotonic clock: POSIX clock_gettime
65902:M 18 Mar 2024 04:08:02.853 # Warning: Could not create server TCP listening socket 192.168.162.21:6379: bind: Cannot assign requested address
65902:M 18 Mar 2024 04:08:02.853 # Failed listening on port 6379 (TCP), aborting.
```
```bash
# solve
netstat -nltp
sudo lsof -t -i tcp:6379

kill -9 output_command_above
```

```bash
docker-compose up -d

docker exec -it learnredis-db redis-cli -h localhost -p 6379
```