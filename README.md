# Iceberg REST Catalog

## Available Endpoints

**Base Endpoint:** https://kevinjqliu.github.io/kevinjqliu-irc

| Endpoint | Description | Example URL |
|----------|-------------|-------------|
| `GET /v1/config` | Server configuration | https://kevinjqliu.github.io/kevinjqliu-irc/v1/config/ |
| `GET /v1/namespaces` | List all namespaces | https://kevinjqliu.github.io/kevinjqliu-irc/v1/namespaces/ |
| `GET /v1/namespaces/{namespace}` | Load namespace metadata | https://kevinjqliu.github.io/kevinjqliu-irc/v1/namespaces/default/ |
| `GET /v1/namespaces/{namespace}/tables` | List tables in namespace | https://kevinjqliu.github.io/kevinjqliu-irc/v1/namespaces/default/tables/ |
| `GET /v1/namespaces/{namespace}/tables/{table}` | Load table metadata | https://kevinjqliu.github.io/kevinjqliu-irc/v1/namespaces/default/tables/test_table_version/ |

## PyIceberg Example Commands

List all namespaces:
```bash
uvx pyiceberg --uri https://kevinjqliu.github.io/kevinjqliu-irc list
```

List tables in default namespace:
```bash
uvx pyiceberg --uri https://kevinjqliu.github.io/kevinjqliu-irc list default
```

Describe namespace:
```bash
uvx pyiceberg --uri https://kevinjqliu.github.io/kevinjqliu-irc describe default
```

Describe table:
```bash
uvx pyiceberg --uri https://kevinjqliu.github.io/kevinjqliu-irc describe default.test_table_version
```
