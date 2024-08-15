# Docker Compose for OpenSearch and OpenSearch Dashboards

This repository provides a simple setup to run [OpenSearch](https://opensearch.org/docs/latest/getting-started/intro/)
and [OpenSearch Dashboards](https://www.opensearch.org/docs/latest/dashboards/)
using [Docker Compose](https://docs.docker.com/compose/),
based on the [example docker-compose.yml](https://opensearch.org/docs/latest/install-and-configure/install-opensearch/docker/#deploy-an-opensearch-cluster-using-docker-compose).

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

Also make sure you configure your host settings according to the [OpenSearch documentation](https://opensearch.org/docs/latest/install-and-configure/install-opensearch/docker/#configure-important-host-settings).

## Getting Started

1. **Clone the repository**:
   ```bash
   git clone https://github.com/blauwe-lucht/docker-compose-opensearch-dashboards.git
   cd docker-compose-opensearch-dashboards
   ```

2. **Start the OpenSearch and OpenSearch Dashboards**:

    ```bash
    docker compose up -d
    ```

    This will start the OpenSearch server and the OpenSearch Dashboards interface.

3. **Access the OpenSearch Dashboards**:

    Once the services are up and running, you can access the OpenSearch Dashboards by navigating to http://localhost:5601.

    For versions 2.12.0 and newer use admin/T!mberW0lf#92 to login.
    For older versions use admin/admin.

## Clean up

```bash
docker compose down -v
```

Note: this will also clean up the data that you have imported. If you want to keep that data, leave out the '-v' from the command.
