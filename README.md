# Run your own DeSo node

```bash

cat > data.json <<EOL
{
    "name": "deso",
    "deso_dns": "deso.example.com",
    "deso_backend_docker_image": "docker.io/desoprotocol/backend:stable",
    "deso_frontend_docker_image": "docker.io/desoprotocol/frontend:stable",
    "deso_backend_port": 17001,
    "deso_frontend_port": 8080,
    "deso_frontend_healthcheck_port": 8081,

    "GLOG_V": 0,
    "GLOG_VMODULE": "",
    "TESTNET": false,
    "EXTERNAL_IPS": "",
    "CONNECT_IPS": "",
    "MINER_PUBLIC_KEYS": "BC1YLjDCy9WWFPeyV4J64AhgHNV8KHgvxyAeFvBLGz5nLZTx6Vf1i8x",
    "NUM_MINING_THREADS": 2,
    "ADD_IPS": "",
    "ADD_SEEDS": "",
    "ADMIN_PUBLIC_KEYS": "BC1YLjDCy9WWFPeyV4J64AhgHNV8KHgvxyAeFvBLGz5nLZTx6Vf1i8x",
    "SUPER_ADMIN_PUBLIC_KEYS": "BC1YLjDCy9WWFPeyV4J64AhgHNV8KHgvxyAeFvBLGz5nLZTx6Vf1i8x",
    "PROTOCOL_PORT": 17000,
    "API_PORT": 17001,
    "RATE_LIMIT_FEERATE": 0,
    "MIN_FEERATE": 1000,
    "TARGET_OUTBOUND_PEERS": 8,
    "MAX_PEERS": 125,
    "DATA_DIR": "/db",
    "ONE_INBOUND_PER_IP": true,
    "STALL_TIMEOUT_SECONDS": 900,
    "PRIVATE_MODE": false,
    "TXINDEX": true,
    "STARTER_DESO_NANOS": 1000000,
    "STARTER_PREFIX_NANOS_MAP": "",
    "STARTER_DESO_SEED": "",
    "GLOBAL_STATE_REMOTE_NODE": "",
    "GLOBAL_STATE_REMOTE_SECRET": "",
    "ACCESS_CONTROL_ALLOW_ORIGINS": "*",
    "SECURE_HEADER_DEVELOPMENT": true,
    "SECURE_HEADER_ALLOW_HOSTS": "",
    "AMPLITUDE_KEY": "",
    "AMPLITUDE_DOMAIN": "api.amplitude.com",
    "TWILIO_ACCOUNT_SID": "",
    "TWILIO_AUTH_TOKEN": "",
    "TWILIO_VERIFY_SERVICE_ID": "",
    "MIN_SATOSHIS_FOR_PROFILE": 50000,
    "SUPPORT_EMAIL": "dominik.deren@live.com",
    "MAX_BLOCK_TEMPLATES_CACHE": 0,
    "MIN_BLOCK_UPDATE_INTERVAL": 10,
    "BLOCK_CYPHER_API_KEY": "",
    "MEMPOOL_DUMP_DIR": "",
    "DISABLE_NETWORKING": false,
    "IGNORE_INBOUND_INVS": false,
    "READ_ONLY_MODE": true,
    "BITCOIN_CONNECT_PEER": "",
    "LOG_DB_SUMMARY_SNAPSHOTS": false,
    "SHOW_PROCESSING_SPINNERS": true,
    "IGNORE_UNMINED_BITCOIN": false,
    "GCP_CREDENTIALS_PATH": "",
    "GCP_BUCKET_NAME": "images.bitclout.com",
    "CADDY_FILE": "/app/Caddyfile.dev"
}
EOL

brew install gomplate
gomplate
./run.sh
```
