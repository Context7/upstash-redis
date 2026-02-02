> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Celery with Upstash Redis

You can use **Celery** with Upstash Redis to build scalable and serverless task queues. Celery is a Python library that manages asynchronous task execution, while Upstash Redis acts as both the broker (queue) and the result backend.

## Setup

### Install Celery

To get started, install the necessary libraries using `pip`:

```bash  theme={"system"}
pip install "celery[redis]"
```

### Database Setup

Create a Redis database using the [Upstash Console](https://console.upstash.com). Export the `UPSTASH_REDIS_HOST`, `UPSTASH_REDIS_PORT`, and `UPSTASH_REDIS_PASSWORD` to your environment:

```bash  theme={"system"}
export UPSTASH_REDIS_HOST=<YOUR_HOST>
export UPSTASH_REDIS_PORT=<YOUR_PORT>
export UPSTASH_REDIS_PASSWORD=<YOUR_PASSWORD>
```

You can also use `python-dotenv` to load environment variables from a `.env` file:

```text .env theme={"system"}
UPSTASH_REDIS_HOST=<YOUR_HOST>
UPSTASH_REDIS_PORT=<YOUR_PORT>
UPSTASH_REDIS_PASSWORD=<YOUR_PASSWORD
```

## Example Application

### Setting up Celery with Upstash Redis

```python tasks.py theme={"system"}
import os
from celery import Celery
from dotenv import load_dotenv

load_dotenv()

# Configure Celery with Upstash Redis
UPSTASH_REDIS_HOST = os.getenv("UPSTASH_REDIS_HOST")
UPSTASH_REDIS_PORT = os.getenv("UPSTASH_REDIS_PORT")
UPSTASH_REDIS_PASSWORD = os.getenv("UPSTASH_REDIS_PASSWORD")

connection_link = f"rediss://:{UPSTASH_REDIS_PASSWORD}@{UPSTASH_REDIS_HOST}:{UPSTASH_REDIS_PORT}?ssl_cert_reqs=required"

celery_app = Celery("tasks", broker=connection_link, backend=connection_link)

@celery_app.task
def add(x, y):
    return x + y
```

Note that we should use the `rediss://` protocol to connect to redis over TLS and set `ssl_cert_reqs=required` to enforce certificate validation.

### Running the Worker

Start the Celery worker to execute tasks:

```bash  theme={"system"}
celery -A tasks worker --loglevel=info
```

### Using the Task

You can now use the `add` task to perform background computations:

```python main.py theme={"system"}
from tasks import add

result = add.delay(4, 6)
print(f"Task state: {result.state}")  # Outputs 'PENDING' initially

# Wait for the result
output = result.get(timeout=10)
print(f"Task result: {output}")  # Outputs '10'
```

## Conclusion

To see a more detailed example of using Celery with Upstash Redis, check out the [Job Processor with Celery example](https://upstash.com/examples/jobprocessorwithcelery) on our website.

For more details on Celery, visit the [Celery Documentation](https://docs.celeryproject.org). For Upstash Redis, check out the [Upstash Redis Documentation](/redis).
