> ## Documentation Index
> Fetch the complete documentation index at: https://upstash.com/docs/llms.txt
> Use this file to discover all available pages before exploring further.

# Prometheus - Upstash Redis Integration

To monitor your Upstash database in Prometheus and visualize metrics in Grafana, follow these steps:

<Check>
  **Integration Scope**

  Upstash Prometheus Integration only covers Pro databases or those included in the Enterprise Plan.
</Check>

## **Step 1: Log in to Your Upstash Account**

1. Open your web browser and navigate to [Upstash](https://console.upstash.com/).
2. Navigate to the main dashboard, where you’ll see a list of your databases.

## **Step 2: Select your Database**

1. Select the database you want to integrate with Prometheus.
2. This will open the database settings, where you can manage various configuration options for your selected database.

<img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/configuration.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=40fe38535d9e2fbdb7d59428c6a94f6d" alt="configuration.png" data-og-width="1938" width="1938" data-og-height="610" height="610" data-path="img/prometheus/configuration.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/configuration.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=c92a8f1602b50cde5ec240868f45e0d2 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/configuration.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=d07d75368b10aa356a11c185a3cd4f99 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/configuration.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=e0fe31a301dbfaaf6371636cf1ea3830 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/configuration.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=6854568834b20b13ae8b9fff9c2ec58e 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/configuration.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=b159937d273d58bf69326cea3a0d6e53 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/configuration.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=76e60d4cc2474fbfe5841a1ae5d7f86e 2500w" />

3. Enable Prometheus by toggling the switch. This allows you to monitor metrics related to your Upstash database performance, usage, and other key metrics.

## **Step 3: Connect Accounts**

1. After enabling Prometheus, a monitoring token is generated and displayed.

2. Copy this token. This token is unique to your database and is required to authenticate Prometheus with the Upstash metrics endpoint.

<Check>
  **Header Format**

  You should add monitoring token according to this format `Bearer <MONITORING_TOKEN>`
</Check>

<img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/monitoring-token.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=2618f754b9209f28f30d27b16a652786" alt="monitoring-token.png" data-og-width="950" width="950" data-og-height="520" height="520" data-path="img/prometheus/monitoring-token.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/monitoring-token.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=bd809c06e4421719c1195a3542a16cfb 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/monitoring-token.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=b2721266c30939e15e371087ba8d8531 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/monitoring-token.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=dbf58ef63addcf094f3cd2ea1e4ddd2b 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/monitoring-token.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=65e3183a923ab6bfcb7c1e55cbce5a27 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/monitoring-token.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=0d9ad474b754c5a3ac37fff5155f22c0 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/monitoring-token.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=bb17a652adc3478d3b68704d29886aa4 2500w" />

## **Step 4: Set Up Prometheus Connection**

### **Grafana Dashboard Setup**

1. Open your Grafana instance, navigate to the Data Sources section, and select Prometheus as the data source.

<img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=3dce2b10059a2eb96d8d560bdabb7303" alt="datasource.png" data-og-width="1848" width="1848" data-og-height="464" height="464" data-path="img/prometheus/datasource.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=325217df537ca2f7269c4d38803b952f 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=9264339789011443e61167e443c0ae8a 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=c1a7c769e5b857d21a733aec149233a8 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=1e156eabf6c5c92c9ab2aa54d175667a 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=eb464cb41c5bc5d8906f09c6a70f5c2b 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=9a0c6ef2b3f5989c557a6b9d054dc0b7 2500w" />

2. Enter the data source name, set `https://api.upstash.com/monitoring/prometheus` as the data source address, and then add your monitoring token in the HTTP Headers section.

<img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/headers.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=f32611d6c8cedb2b6a73d21e9b8a1cd5" alt="headers.png" data-og-width="1322" width="1322" data-og-height="346" height="346" data-path="img/prometheus/headers.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/headers.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=613ce8cdff83bfadfbd95e40fac9548f 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/headers.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=c3edb89b53a21ffc79173c03e0c0bd7b 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/headers.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=d624ffcce430e3014319386a7de649d5 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/headers.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=4fb91d8f22449f95fc91704839fb1eb5 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/headers.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=6a5a66bed411dde641fbcf8a6111de7d 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/headers.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=1f60d9ffdf856ad140c8f470e1e9028e 2500w" />

3. Then, click <b>Test and Save</b> to verify that the data source is working properly.

<img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource-final.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=6e3f9cc214486c59085fe036a0dd6a28" alt="datasource-final.png" data-og-width="1560" width="1560" data-og-height="412" height="412" data-path="img/prometheus/datasource-final.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource-final.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=a97d2c20d4cae7002e57524de561937b 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource-final.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=e93e44229ab80a44a9115225b65c8742 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource-final.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=2d542697335e6b8e3ca346cd5371292d 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource-final.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=bde3d4b76f3d4f0f4712a307d1d90f12 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource-final.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=a15201c139e232a3ca6a6599e35a119a 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/datasource-final.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=2950933a8fb225e5ddfc04143a36a111 2500w" />

### **Prometheus Federation Setup**

Federation lets your Prometheus pull metrics from Upstash’s API and store them in **your own** Prometheus instance, so Grafana can query your Prometheus instead of hitting the Upstash endpoint directly.

#### When to use federation

* You already run Prometheus and want to persist Upstash metrics locally.
* You want to control retention, recording rules, or alerts on Upstash metrics

1. Set up a new scrape job in your Prometheus configuration file (`prometheus.yml`):

```yaml  theme={"system"}
scrape_configs:
  # Federation job: pull from Upstash API
  - job_name: "federate_upstash"
    honor_labels: true
    metrics_path: "/monitoring/prometheus/federate"
    scheme: https
    params:
      match[]:
        - 'upstash_db_metrics{}'
    static_configs:
      - targets:
          - "api.upstash.com"
    authorization:
      type: Bearer
      credentials: "<MONITORING_TOKEN>"
```

<Check>
  This configuration assumes you want to pull all metrics. You can adjust the `match[]` parameter to filter specific metrics if needed.

  * `upstash_db_metrics{database_id="your_database_id"}` can be used to pull metrics for a specific database
  * `upstash_db_metrics{replica_id=~"us-east-1.*"}` can be used to pull metrics for replicas in a specific region
</Check>

2. Verify the Federation Target

* Reload (or restart) your Prometheus server to apply the new configuration.
* Visit **Prometheus → Status → Targets** and confirm `federate_upstash` is **UP**

## **Step 5: Wait for Metrics Availability**

To visualize your Upstash metrics, you can use a pre-built Grafana dashboard.

Select your Prometheus data source when prompted, and complete the import.

Please check this address to access Upstash Grafana Dashboard <a href="https://grafana.com/grafana/dashboards/22257-upstash-redis-dashboard/"> Dashboard </a>

<img src="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/grafana-dashboard.png?fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=372dafae3c34f39565a23447bbc4446f" alt="grafana-dashboard.png" data-og-width="1800" width="1800" data-og-height="1118" height="1118" data-path="img/prometheus/grafana-dashboard.png" data-optimize="true" data-opv="3" srcset="https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/grafana-dashboard.png?w=280&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=078efa29ccdeff007763151e040738eb 280w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/grafana-dashboard.png?w=560&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=e30a8d619a54ee3c237fd81a47b7f8a0 560w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/grafana-dashboard.png?w=840&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=eb6ded213e28397f031a313a7f6db6e8 840w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/grafana-dashboard.png?w=1100&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=3d1f54b522869dbfb12106f76f066149 1100w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/grafana-dashboard.png?w=1650&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=23b8d80dfec0485b0e581964d764a230 1650w, https://mintcdn.com/upstash/pqZtv0gXFMQuy8rU/img/prometheus/grafana-dashboard.png?w=2500&fit=max&auto=format&n=pqZtv0gXFMQuy8rU&q=85&s=05144eda40660dd53e0465cee0aad5e5 2500w" />

## **Conclusion**

You've now integrated your database with Upstash Prometheus, providing access to improved monitoring and analytics.

Feel free to explore Upstash's features and dashboards to gain deeper insights into your system's performance.

If you encounter any issues or have questions, please refer to the Upstash support documentation or contact our support team for assistance.
