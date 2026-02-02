> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Serverless Redisson

> This tutorial shows how to use Upstash with Redisson client.

This tutorial shows how to use Upstash with Redisson client.

See [code](https://github.com/upstash/examples/tree/master/examples/redisson)

### `1` Create a Maven Project

Create a maven project and copy the following dependency to your pom.xml

```xml  theme={"system"}
<dependency>
    <groupId>org.redisson</groupId>
    <artifactId>redisson</artifactId>
    <version>3.15.4</version>
</dependency>
```

### `2` Create a Redis (Upstash) Database

Create a database as [getting started](../overall/getstarted)

### `3` Code

Create your java file and replace Redis password and URL below. If you enabled
TLS, the endpoint should start with `rediss`

```typescript  theme={"system"}
public class Main {

    public static void main(String[] args) {
        Config config = new Config();
        config.useSingleServer().setPassword("YOUR_PASSWORD")
                // use "rediss://" for SSL connection
                .setAddress("YOUR_ENDPOINT");
        RedissonClient redisson = Redisson.create(config);
        RMap<String, String> map = redisson.getMap("map");
        map.put("foo", "bar");
        System.out.println(map.get("foo"));
    }
}
```
