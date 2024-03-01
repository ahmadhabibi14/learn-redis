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