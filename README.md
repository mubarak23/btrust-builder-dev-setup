


#  Bitcoin and Lightning Network Development Enviroment For Btrust Builder Fellowship 


-- This is document that explain the process i follow to setup my bitcoin and lightning network development enviroment


## Bitcoin Setup

Network : regtest


### create bitcoin wallet
 bitcoin-cli loadwallet regtestwallet
{
  "name": "regtestwallet"
}



bitcoin-cli -getinfo

Chain: regtest
Blocks: 427
Headers: 427
Verification progress: 100.0000%
Difficulty: 4.656542373906925e-10

Network: in 0, out 0, total 0
Version: 269900
Time offset (s): 0
Proxies: n/a
Min tx relay fee rate (BTC/kvB): 0.00001000

Wallet: regtestwallet
Keypool size: 4000
Transaction fee rate (-paytxfee) (BTC/kvB): 0.00000000

Balance: 11548.99999857


### Genetated the first 6 blocks

 bitcoin-cli -generate 6
{
  "address": "bcrt1qv4rc3qp5yrc00hgymmdcdhycsvyxju0wsdv3uy",
  "blocks": [
    "55a9abfe95f1d78ab5b4c8bacce2073736efbe0483c116b26b490debf39bf8a6",
    "35cda95cf0290e1607ef87650aafab94761a804d354d72ef53c54b191a7b9136",
    "0eac1fe6a094819c7cfd2e21c5f1d7d2b1a50fe3d13a24bc3213bf0d0389a7d2",
    "69d87fab739138973f68570db5f6a94d20a83b63588aff2a07e7936e172ef6b6",
    "575f79152707aa61bd1e05c8ad22ea2a4f7352feae39e5535fc3d117dd65501c",
    "21c3a2c562a52416ee6222d0bd04bf541038a968430e47419ffadec20beb6d8e"
  ]
}

### Get Bitcoin balance

bitcoin-cli getbalance
11548.99999857

### start LND1 
macbookpro@MacBooks-MBP-2 ~ % lnd1          
2024-01-26 11:35:29.098 [INF] LTND: Version: 0.17.0-beta commit=fn/v1.0.2-8-g0d37621bc, build=production, logging=default, debuglevel=info
2024-01-26 11:35:29.098 [INF] LTND: Active chain: Bitcoin (network=regtest)
2024-01-26 11:35:29.099 [INF] RPCS: RPC server listening on 127.0.0.1:10009
2024-01-26 11:35:29.100 [INF] RPCS: gRPC proxy started at 127.0.0.1:8080
2024-01-26 11:35:29.101 [INF] LTND: Opening the main database, this might t

### Start LND2 
lnd2          
2024-01-26 11:36:50.887 [INF] LTND: Version: 0.17.0-beta commit=fn/v1.0.2-8-g0d37621bc, build=production, logging=default, debuglevel=info
2024-01-26 11:36:50.888 [INF] LTND: Active chain: Bitcoin (network=regtest)
2024-01-26 11:36:50.889 [INF] RPCS: RPC server listening on 127.0.0.1:11009
2024-01-26 11:36:50.891 [INF] RPCS: gRPC proxy started at 0.0.0.0:8180
2024-01-26 11:36:50.891 [INF] LTND: Opening the main database, this might take a few minutes...


### lncli1 create

### lncli2 create



### lncli1 getinfo 

lncli1 getinfo
{
    "version": "0.17.0-beta commit=fn/v1.0.2-8-g0d37621bc",
    "commit_hash": "0d37621bcba49d2d1af34edd18f9689ace233231",
    "identity_pubkey": "02b10de020b6ea70862ad297269972fe0e95ced6cc2c0f25fdd9bff129e357c2ce",
    "alias": "02b10de020b6ea70862a",
    "color": "#3399ff",
    "num_pending_channels": 0,
    "num_active_channels": 1,
    "num_inactive_channels": 0,
    "num_peers": 1,
    "block_height": 427,
    "block_hash": "6aa22a84036824fe520c7495d0756b7c42af35e780b82222358d35fd2d2169b2",
    "best_header_timestamp": "1706267082",
    "synced_to_chain": true,
    "synced_to_graph": true,
    "testnet": false,
    "chains": [
        {
            "chain": "bitcoin",
            "network": "regtest"
        }
    ],
    "uris": [],
    "features": {
        "0": {
            "name": "data-loss-protect",
            "is_required": true,
            "is_known": true
        },
        "5": {
            "name": "upfront-shutdown-script",
            "is_required": false,
            "is_known": true
        },
        "6": {
            "name": "gossip-queries",
            "is_required": true,
            "is_known": true
        },
        "8": {
            "name": "tlv-onion",
            "is_required": true,
            "is_known": true
        },
        "12": {
            "name": "static-remote-key",
            "is_required": true,
            "is_known": true
        },
        "14": {
            "name": "payment-addr",
            "is_required": true,
            "is_known": true
        },
        "17": {
            "name": "multi-path-payments",
            "is_required": false,
            "is_known": true
        },
        "23": {
            "name": "anchors-zero-fee-htlc-tx",
            "is_required": false,
            "is_known": true
        },
        "27": {
            "name": "shutdown-any-segwit",
            "is_required": false,
            "is_known": true
        },
        "30": {
            "name": "amp",
            "is_required": true,
            "is_known": true
        },
        "31": {
            "name": "amp",
            "is_required": false,
            "is_known": true
        },
        "45": {
            "name": "explicit-commitment-type",
            "is_required": false,
            "is_known": true
        },
        "2023": {
            "name": "script-enforced-lease",
            "is_required": false,
            "is_known": true
        }
    },
    "require_htlc_interceptor": false,
    "store_final_htlc_resolutions": false
}

### lncli2 getinfo

lncli2 getinfo
{
    "version": "0.17.0-beta commit=fn/v1.0.2-8-g0d37621bc",
    "commit_hash": "0d37621bcba49d2d1af34edd18f9689ace233231",
    "identity_pubkey": "02512859b0c62d0277055e71f6cd8ce207ea41972afc2cdd007df9dd48b8380585",
    "alias": "02512859b0c62d027705",
    "color": "#3399ff",
    "num_pending_channels": 0,
    "num_active_channels": 1,
    "num_inactive_channels": 0,
    "num_peers": 1,
    "block_height": 427,
    "block_hash": "6aa22a84036824fe520c7495d0756b7c42af35e780b82222358d35fd2d2169b2",
    "best_header_timestamp": "1706267082",
    "synced_to_chain": true,
    "synced_to_graph": true,
    "testnet": false,
    "chains": [
        {
            "chain": "bitcoin",
            "network": "regtest"
        }
    ],
    "uris": [],
    "features": {
        "0": {
            "name": "data-loss-protect",
            "is_required": true,
            "is_known": true
        },
        "5": {
            "name": "upfront-shutdown-script",
            "is_required": false,
            "is_known": true
        },
        "6": {
            "name": "gossip-queries",
            "is_required": true,
            "is_known": true
        },
        "8": {
            "name": "tlv-onion",
            "is_required": true,
            "is_known": true
        },
        "12": {
            "name": "static-remote-key",
            "is_required": true,
            "is_known": true
        },
        "14": {
            "name": "payment-addr",
            "is_required": true,
            "is_known": true
        },
        "17": {
            "name": "multi-path-payments",
            "is_required": false,
            "is_known": true
        },
        "23": {
            "name": "anchors-zero-fee-htlc-tx",
            "is_required": false,
            "is_known": true
        },
        "27": {
            "name": "shutdown-any-segwit",
            "is_required": false,
            "is_known": true
        },
        "30": {
            "name": "amp",
            "is_required": true,
            "is_known": true
        },
        "31": {
            "name": "amp",
            "is_required": false,
            "is_known": true
        },
        "45": {
            "name": "explicit-commitment-type",
            "is_required": false,
            "is_known": true
        },
        "2023": {
            "name": "script-enforced-lease",
            "is_required": false,
            "is_known": true
        }
    },
    "require_htlc_interceptor": false,
    "store_final_htlc_resolutions": false
}

### lncli1 connect 
-- lncli1 connect with lncli2 via the identity_pubkey and its port
lncli1 connect lncli2_identity_pubkey@localhost:lncli2_port

lncli1 connect 02512859b0c62d0277055e71f6cd8ce207ea41972afc2cdd007df9dd48b8380585@localhost:9734
{}


### lncli1 list peers

lncli1 listpeers
{
    "peers": [
        {
            "pub_key": "02512859b0c62d0277055e71f6cd8ce207ea41972afc2cdd007df9dd48b8380585",
            "address": "127.0.0.1:9734",
            "bytes_sent": "394",
            "bytes_recv": "394",
            "sat_sent": "0",
            "sat_recv": "0",
            "inbound": false,
            "ping_time": "-1",
            "sync_type": "ACTIVE_SYNC",
            "features": {
                "0": {
                    "name": "data-loss-protect",
                    "is_required": true,
                    "is_known": true
                },
                "5": {
                    "name": "upfront-shutdown-script",
                    "is_required": false,
                    "is_known": true
                },
                "6": {
                    "name": "gossip-queries",
                    "is_required": true,
                    "is_known": true
                },
                "8": {
                    "name": "tlv-onion",
                    "is_required": true,
                    "is_known": true
                },
                "12": {
                    "name": "static-remote-key",
                    "is_required": true,
                    "is_known": true
                },
                "14": {
                    "name": "payment-addr",
                    "is_required": true,
                    "is_known": true
                },
                "17": {
                    "name": "multi-path-payments",
                    "is_required": false,
                    "is_known": true
                },
                "23": {
                    "name": "anchors-zero-fee-htlc-tx",
                    "is_required": false,
                    "is_known": true
                },
                "27": {
                    "name": "shutdown-any-segwit",
                    "is_required": false,
                    "is_known": true
                },
                "31": {
                    "name": "amp",
                    "is_required": false,
                    "is_known": true
                },
                "45": {
                    "name": "explicit-commitment-type",
                    "is_required": false,
                    "is_known": true
                },
                "2023": {
                    "name": "script-enforced-lease",
                    "is_required": false,
                    "is_known": true
                }
            },
            "errors": [],
            "flap_count": 1,
            "last_flap_ns": "1706265945652055000",
            "last_ping_payload": ""
        }
    ]
}



### generate an address for lncli2 

 lncli2 newaddress np2wkh
{
    "address": "2Mzm4Tsai4gPrWnLWa6V4NAANdiypQ8jpBj"
}

## create channel 

### send sats to the new lncli2 address -  sendtoaddress

bitcoin-cli sendtoaddress 2Mzm4Tsai4gPrWnLWa6V4NAANdiypQ8jpBj 1 -fallbackfee
0158ed0e66969af3a52b4369b0f02dd8a454beee283b77fae1438cd10d72e82f



### Open a channel 
#### lncli2 connect with lncli1 via it's identity_pubkey (02b10de020b6ea70862ad297269972fe0e95ced6cc2c0f25fdd9bff129e357c2ce)
 lncli2 openchannel 02b10de020b6ea70862ad297269972fe0e95ced6cc2c0f25fdd9bff129e357c2ce 100000
{
	"funding_txid": "413f1bef89d64d17d42865c42c5e1bfae9a66a06f90ea654573028c72d720d1b"
}

### list our lncli1 channles 

 lncli1 listchannels
{
    "channels": [
        {
            "active": true,
            "remote_pubkey": "02512859b0c62d0277055e71f6cd8ce207ea41972afc2cdd007df9dd48b8380585",
            "channel_point": "413f1bef89d64d17d42865c42c5e1bfae9a66a06f90ea654573028c72d720d1b:0",
            "chan_id": "465093418614784",
            "capacity": "100000",
            "local_balance": "0",
            "remote_balance": "96530",
            "commit_fee": "3140",
            "commit_weight": "772",
            "fee_per_kw": "2500",
            "unsettled_balance": "0",
            "total_satoshis_sent": "0",
            "total_satoshis_received": "0",
            "num_updates": "0",
            "pending_htlcs": [],
            "csv_delay": 144,
            "private": false,
            "initiator": false,
            "chan_status_flags": "ChanStatusDefault",
            "local_chan_reserve_sat": "1000",
            "remote_chan_reserve_sat": "1000",
            "static_remote_key": false,
            "commitment_type": "ANCHORS",
            "lifetime": "15",
            "uptime": "15",
            "close_address": "",
            "push_amount_sat": "0",
            "thaw_height": 0,
            "local_constraints": {
                "csv_delay": 144,
                "chan_reserve_sat": "1000",
                "dust_limit_sat": "354",
                "max_pending_amt_msat": "99000000",
                "min_htlc_msat": "1",
                "max_accepted_htlcs": 483
            },
            "remote_constraints": {
                "csv_delay": 144,
                "chan_reserve_sat": "1000",
                "dust_limit_sat": "354",
                "max_pending_amt_msat": "99000000",
                "min_htlc_msat": "1",
                "max_accepted_htlcs": 483
            },
            "alias_scids": [],
            "zero_conf": false,
            "zero_conf_confirmed_scid": "0",
            "peer_alias": "unable to lookup peer alias: alias for node not found",
            "peer_scid_alias": "0",
            "memo": ""
        }
    ]
}

