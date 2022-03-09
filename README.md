# IDunion Indy DID Resolver

This Github project was forked from [IDunion indy-did-resolver](https://github.com/IDunion/indy-did-resolver) to be used locally as a part of our Interoperable SSI Access Control System. All credits go to [IDunion](https://github.com/IDunion).

## Indy DID Resolver

This project is used as a driver of the [Universal Resolver](https://github.com/decentralized-identity/universal-resolver) for resolving Decentralized Identifiers (DIDs) of the Indy DID Method. 

The driver is configured to connect to a local Indy network (local instance of the [VON network](https://github.com/bcgov/von-network)). The genesis file of this network is stored in `/networks/local/pool_transactions_genesis.json`. To resolve a DID anchored on this Indy network, use the following did syntax: did:indy:local:<identifier>. The driver is reached by the Universal Resolver via HTTP requests (default on port 8080) using the following url: `http://<container_name>:8080/1.0/identifiers/did:indy:local:<DID_identifier>`

## Additional Information from original repository

### CLI options for starting the driver. See docker/Dockerfile
```
    -f, --genesis-filename <GENESIS_FILENAME>
            Pool transaction genesis filename [default: pool_transactions_genesis.json]

    -h, --help
            Print help information

    -n, --github-network <GITHUB_NETWORKS>
            github repository for registered networks [default: https://github.com/IDunion/indy-did-
            networks]

    -p, --port <PORT>
            Port to expose [default: 8080]

    -s, --source <SOURCE>
            source to use, allowed values are path or github [default: ]

    -V, --version
            Print version information
```
