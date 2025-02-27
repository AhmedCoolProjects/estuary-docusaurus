# estuary-client

This is the API for the Pin.Storage application.

This Python package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 0.0.0
- Package version: 1.0.6
- Build package: io.swagger.codegen.v3.generators.python.PythonClientCodegen
  For more information, please visit [https://docs.pin.storage/feedback](https://docs.pin.storage/feedback)

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage

### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```

(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:

```python
import estuary_client
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```

(or `sudo python setup.py install` to install the package for all users)

Then import the package:

```python
import estuary_client
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```python
from __future__ import print_function
import time
import estuary_client
from estuary_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: bearerAuth
configuration = estuary_client.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = estuary_client.UserApi(estuary_client.ApiClient(configuration))

try:
    # Get API keys for a user
    api_response = api_instance.user_api_keys_get()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->user_api_keys_get: %s\n" % e)

# Configure API key authorization: bearerAuth
configuration = estuary_client.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = estuary_client.UserApi(estuary_client.ApiClient(configuration))
key_or_hash = 'key_or_hash_example' # str | Key or Hash

try:
    # Revoke a User API Key.
    api_response = api_instance.user_api_keys_key_or_hash_delete(key_or_hash)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->user_api_keys_key_or_hash_delete: %s\n" % e)

# Configure API key authorization: bearerAuth
configuration = estuary_client.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = estuary_client.UserApi(estuary_client.ApiClient(configuration))
expiry = 'expiry_example' # str | Expiration - Expiration - Valid time units are ns, us (or µs),  ms,  s,  m,  h.  for  example  300h (optional)
perms = 'perms_example' # str | Permissions -- currently unused (optional)

try:
    # Create API keys for a user
    api_response = api_instance.user_api_keys_post(expiry=expiry, perms=perms)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->user_api_keys_post: %s\n" % e)

# Configure API key authorization: bearerAuth
configuration = estuary_client.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = estuary_client.UserApi(estuary_client.ApiClient(configuration))

try:
    # Export user data
    api_response = api_instance.user_export_get()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->user_export_get: %s\n" % e)

# Configure API key authorization: bearerAuth
configuration = estuary_client.Configuration()
configuration.api_key['Authorization'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Authorization'] = 'Bearer'

# create an instance of the API class
api_instance = estuary_client.UserApi(estuary_client.ApiClient(configuration))

try:
    # Get stats for the current user
    api_response = api_instance.user_stats_get()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling UserApi->user_stats_get: %s\n" % e)
```

## Documentation for API Endpoints

All URIs are relative to _//api.estuary.tech/_

| Class             | Method                                                                                                                    | HTTP request                                           | Description                                           |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ | ----------------------------------------------------- |
| _UserApi_         | [**user_api_keys_get**](docs/UserApi.md#user_api_keys_get)                                                                | **GET** /user/api-keys                                 | Get API keys for a user                               |
| _UserApi_         | [**user_api_keys_key_or_hash_delete**](docs/UserApi.md#user_api_keys_key_or_hash_delete)                                  | **DELETE** /user/api-keys/{key_or_hash}                | Revoke a User API Key.                                |
| _UserApi_         | [**user_api_keys_post**](docs/UserApi.md#user_api_keys_post)                                                              | **POST** /user/api-keys                                | Create API keys for a user                            |
| _UserApi_         | [**user_export_get**](docs/UserApi.md#user_export_get)                                                                    | **GET** /user/export                                   | Export user data                                      |
| _UserApi_         | [**user_stats_get**](docs/UserApi.md#user_stats_get)                                                                      | **GET** /user/stats                                    | Get stats for the current user                        |
| _AdminApi_        | [**admin_miners_get**](docs/AdminApi.md#admin_miners_get)                                                                 | **GET** /admin/miners/                                 | Get all miners                                        |
| _AdminApi_        | [**admin_peering_peers_delete**](docs/AdminApi.md#admin_peering_peers_delete)                                             | **DELETE** /admin/peering/peers                        | Remove peers on Peering Service                       |
| _AdminApi_        | [**admin_peering_peers_get**](docs/AdminApi.md#admin_peering_peers_get)                                                   | **GET** /admin/peering/peers                           | List all Peering peers                                |
| _AdminApi_        | [**admin_peering_peers_post**](docs/AdminApi.md#admin_peering_peers_post)                                                 | **POST** /admin/peering/peers                          | Add peers on Peering Service                          |
| _AdminApi_        | [**admin_peering_start_post**](docs/AdminApi.md#admin_peering_start_post)                                                 | **POST** /admin/peering/start                          | Start Peering                                         |
| _AdminApi_        | [**admin_peering_status_get**](docs/AdminApi.md#admin_peering_status_get)                                                 | **GET** /admin/peering/status                          | Check Peering Status                                  |
| _AdminApi_        | [**admin_peering_stop_post**](docs/AdminApi.md#admin_peering_stop_post)                                                   | **POST** /admin/peering/stop                           | Stop Peering                                          |
| _AdminApi_        | [**admin_system_config_get**](docs/AdminApi.md#admin_system_config_get)                                                   | **GET** /admin/system/config                           | Get systems(estuary/shuttle) config                   |
| _AdminApi_        | [**admin_users_get**](docs/AdminApi.md#admin_users_get)                                                                   | **GET** /admin/users                                   | Get all users                                         |
| _AutoretrieveApi_ | [**admin_autoretrieve_init_post**](docs/AutoretrieveApi.md#admin_autoretrieve_init_post)                                  | **POST** /admin/autoretrieve/init                      | Register autoretrieve server                          |
| _AutoretrieveApi_ | [**admin_autoretrieve_list_get**](docs/AutoretrieveApi.md#admin_autoretrieve_list_get)                                    | **GET** /admin/autoretrieve/list                       | List autoretrieve servers                             |
| _AutoretrieveApi_ | [**autoretrieve_heartbeat_post**](docs/AutoretrieveApi.md#autoretrieve_heartbeat_post)                                    | **POST** /autoretrieve/heartbeat                       | Marks autoretrieve server as up                       |
| _CollectionsApi_  | [**collections_coluuid_commit_post**](docs/CollectionsApi.md#collections_coluuid_commit_post)                             | **POST** /collections/{coluuid}/commit                 | Produce a CID of the collection contents              |
| _CollectionsApi_  | [**collections_coluuid_contents_delete**](docs/CollectionsApi.md#collections_coluuid_contents_delete)                     | **DELETE** /collections/{coluuid}/contents             | Deletes a content from a collection                   |
| _CollectionsApi_  | [**collections_coluuid_delete**](docs/CollectionsApi.md#collections_coluuid_delete)                                       | **DELETE** /collections/{coluuid}                      | Deletes a collection                                  |
| _CollectionsApi_  | [**collections_coluuid_get**](docs/CollectionsApi.md#collections_coluuid_get)                                             | **GET** /collections/{coluuid}                         | Get contents in a collection                          |
| _CollectionsApi_  | [**collections_coluuid_post**](docs/CollectionsApi.md#collections_coluuid_post)                                           | **POST** /collections/{coluuid}                        | Add contents to a collection                          |
| _CollectionsApi_  | [**collections_fs_add_post**](docs/CollectionsApi.md#collections_fs_add_post)                                             | **POST** /collections/fs/add                           | Add a file to a collection                            |
| _CollectionsApi_  | [**collections_get**](docs/CollectionsApi.md#collections_get)                                                             | **GET** /collections/                                  | List all collections                                  |
| _CollectionsApi_  | [**collections_post**](docs/CollectionsApi.md#collections_post)                                                           | **POST** /collections/                                 | Create a new collection                               |
| _ContentApi_      | [**admin_invites_code_post**](docs/ContentApi.md#admin_invites_code_post)                                                 | **POST** /admin/invites/{code}                         | Create an Pin.Storage invite                          |
| _ContentApi_      | [**admin_invites_get**](docs/ContentApi.md#admin_invites_get)                                                             | **GET** /admin/invites                                 | Get Pin.Storage invites                               |
| _ContentApi_      | [**content_add_car_post**](docs/ContentApi.md#content_add_car_post)                                                       | **POST** /content/add-car                              | Add Car object                                        |
| _ContentApi_      | [**content_add_ipfs_post**](docs/ContentApi.md#content_add_ipfs_post)                                                     | **POST** /content/add-ipfs                             | Add IPFS object                                       |
| _ContentApi_      | [**content_add_post**](docs/ContentApi.md#content_add_post)                                                               | **POST** /content/add                                  | Add new content                                       |
| _ContentApi_      | [**content_aggregated_content_get**](docs/ContentApi.md#content_aggregated_content_get)                                   | **GET** /content/aggregated/{content}                  | Get aggregated content stats                          |
| _ContentApi_      | [**content_all_deals_get**](docs/ContentApi.md#content_all_deals_get)                                                     | **GET** /content/all-deals                             | Get all deals for a user                              |
| _ContentApi_      | [**content_bw_usage_content_get**](docs/ContentApi.md#content_bw_usage_content_get)                                       | **GET** /content/bw-usage/{content}                    | Get content bandwidth                                 |
| _ContentApi_      | [**content_contents_get**](docs/ContentApi.md#content_contents_get)                                                       | **GET** /content/contents                              | Get user contents                                     |
| _ContentApi_      | [**content_create_post**](docs/ContentApi.md#content_create_post)                                                         | **POST** /content/create                               | Add a new content                                     |
| _ContentApi_      | [**content_deals_get**](docs/ContentApi.md#content_deals_get)                                                             | **GET** /content/deals                                 | Content with deals                                    |
| _ContentApi_      | [**content_ensure_replication_datacid_get**](docs/ContentApi.md#content_ensure_replication_datacid_get)                   | **GET** /content/ensure-replication/{datacid}          | Ensure Replication                                    |
| _ContentApi_      | [**content_failures_content_get**](docs/ContentApi.md#content_failures_content_get)                                       | **GET** /content/failures/{content}                    | List all failures for a content                       |
| _ContentApi_      | [**content_id_get**](docs/ContentApi.md#content_id_get)                                                                   | **GET** /content/{id}                                  | Content                                               |
| _ContentApi_      | [**content_list_get**](docs/ContentApi.md#content_list_get)                                                               | **GET** /content/list                                  | List all pinned content                               |
| _ContentApi_      | [**content_staging_zones_get**](docs/ContentApi.md#content_staging_zones_get)                                             | **GET** /content/staging-zones                         | Get staging zone for user, excluding its contents     |
| _ContentApi_      | [**content_staging_zones_staging_zone_contents_get**](docs/ContentApi.md#content_staging_zones_staging_zone_contents_get) | **GET** /content/staging-zones/{staging_zone}/contents | Get contents for a staging zone                       |
| _ContentApi_      | [**content_staging_zones_staging_zone_get**](docs/ContentApi.md#content_staging_zones_staging_zone_get)                   | **GET** /content/staging-zones/{staging_zone}          | Get staging zone without its contents field populated |
| _ContentApi_      | [**content_stats_get**](docs/ContentApi.md#content_stats_get)                                                             | **GET** /content/stats                                 | Get content statistics                                |
| _ContentApi_      | [**content_status_id_get**](docs/ContentApi.md#content_status_id_get)                                                     | **GET** /content/status/{id}                           | Content Status                                        |
| _DealsApi_        | [**deal_estimate_post**](docs/DealsApi.md#deal_estimate_post)                                                             | **POST** /deal/estimate                                | Estimate the cost of a deal                           |
| _DealsApi_        | [**deal_info_dealid_get**](docs/DealsApi.md#deal_info_dealid_get)                                                         | **GET** /deal/info/{dealid}                            | Get Deal Info                                         |
| _DealsApi_        | [**deal_proposal_propcid_get**](docs/DealsApi.md#deal_proposal_propcid_get)                                               | **GET** /deal/proposal/{propcid}                       | Get Proposal                                          |
| _DealsApi_        | [**deal_query_miner_get**](docs/DealsApi.md#deal_query_miner_get)                                                         | **GET** /deal/query/{miner}                            | Query Ask                                             |
| _DealsApi_        | [**deal_status_by_proposal_propcid_get**](docs/DealsApi.md#deal_status_by_proposal_propcid_get)                           | **GET** /deal/status-by-proposal/{propcid}             | Get Deal Status by PropCid                            |
| _DealsApi_        | [**deal_status_miner_propcid_get**](docs/DealsApi.md#deal_status_miner_propcid_get)                                       | **GET** /deal/status/{miner}/{propcid}                 | Deal Status                                           |
| _DealsApi_        | [**deal_transfer_in_progress_get**](docs/DealsApi.md#deal_transfer_in_progress_get)                                       | **GET** /deal/transfer/in-progress                     | Transfer In Progress                                  |
| _DealsApi_        | [**deal_transfer_status_post**](docs/DealsApi.md#deal_transfer_status_post)                                               | **POST** /deal/transfer/status                         | Transfer Status                                       |
| _DealsApi_        | [**deals_failures_get**](docs/DealsApi.md#deals_failures_get)                                                             | **GET** /deals/failures                                | Get storage failures for user                         |
| _DealsApi_        | [**deals_make_miner_post**](docs/DealsApi.md#deals_make_miner_post)                                                       | **POST** /deals/make/{miner}                           | Make Deal                                             |
| _DealsApi_        | [**deals_status_deal_get**](docs/DealsApi.md#deals_status_deal_get)                                                       | **GET** /deals/status/{deal}                           | Get Deal Status                                       |
| _DealsApi_        | [**public_deals_failures_get**](docs/DealsApi.md#public_deals_failures_get)                                               | **GET** /public/deals/failures                         | Get storage failures                                  |
| _DealsApi_        | [**public_miners_storage_query_miner_get**](docs/DealsApi.md#public_miners_storage_query_miner_get)                       | **GET** /public/miners/storage/query/{miner}           | Query Ask                                             |
| _DefaultApi_      | [**viewer_get**](docs/DefaultApi.md#viewer_get)                                                                           | **GET** /viewer                                        | Fetch viewer details                                  |
| _MetricsApi_      | [**public_metrics_deals_on_chain_get**](docs/MetricsApi.md#public_metrics_deals_on_chain_get)                             | **GET** /public/metrics/deals-on-chain                 | Get deal metrics                                      |
| _MinerApi_        | [**miner_claim_miner_get**](docs/MinerApi.md#miner_claim_miner_get)                                                       | **GET** /miner/claim/{miner}                           | Get Claim Miner Message                               |
| _MinerApi_        | [**miner_claim_post**](docs/MinerApi.md#miner_claim_post)                                                                 | **POST** /miner/claim                                  | Claim Miner                                           |
| _MinerApi_        | [**miner_set_info_miner_put**](docs/MinerApi.md#miner_set_info_miner_put)                                                 | **PUT** /miner/set-info/{miner}                        | Set Miner Info                                        |
| _MinerApi_        | [**miner_suspend_miner_post**](docs/MinerApi.md#miner_suspend_miner_post)                                                 | **POST** /miner/suspend/{miner}                        | Suspend Miner                                         |
| _MinerApi_        | [**miner_unsuspend_miner_put**](docs/MinerApi.md#miner_unsuspend_miner_put)                                               | **PUT** /miner/unsuspend/{miner}                       | Unuspend Miner                                        |
| _MinerApi_        | [**public_miners_deals_miner_get**](docs/MinerApi.md#public_miners_deals_miner_get)                                       | **GET** /public/miners/deals/{miner}                   | Get all miners deals                                  |
| _MinerApi_        | [**public_miners_stats_miner_get**](docs/MinerApi.md#public_miners_stats_miner_get)                                       | **GET** /public/miners/stats/{miner}                   | Get miner stats                                       |
| _NetApi_          | [**admin_miners_get**](docs/NetApi.md#admin_miners_get)                                                                   | **GET** /admin/miners/                                 | Get all miners                                        |
| _NetApi_          | [**public_miners_failures_miner_get**](docs/NetApi.md#public_miners_failures_miner_get)                                   | **GET** /public/miners/failures/{miner}                | Get all miners                                        |
| _NetApi_          | [**public_net_addrs_get**](docs/NetApi.md#public_net_addrs_get)                                                           | **GET** /public/net/addrs                              | Net Addrs                                             |
| _NetApi_          | [**public_net_peers_get**](docs/NetApi.md#public_net_peers_get)                                                           | **GET** /public/net/peers                              | Net Peers                                             |
| _PinningApi_      | [**pinning_pins_get**](docs/PinningApi.md#pinning_pins_get)                                                               | **GET** /pinning/pins                                  | List all pin status objects                           |
| _PinningApi_      | [**pinning_pins_pinid_delete**](docs/PinningApi.md#pinning_pins_pinid_delete)                                             | **DELETE** /pinning/pins/{pinid}                       | Delete a pinned object                                |
| _PinningApi_      | [**pinning_pins_pinid_get**](docs/PinningApi.md#pinning_pins_pinid_get)                                                   | **GET** /pinning/pins/{pinid}                          | Get a pin status object                               |
| _PinningApi_      | [**pinning_pins_pinid_post**](docs/PinningApi.md#pinning_pins_pinid_post)                                                 | **POST** /pinning/pins/{pinid}                         | Replace a pinned object                               |
| _PinningApi_      | [**pinning_pins_post**](docs/PinningApi.md#pinning_pins_post)                                                             | **POST** /pinning/pins                                 | Add and pin object                                    |
| _PublicApi_       | [**get_cid_get**](docs/PublicApi.md#get_cid_get)                                                                          | **GET** /get/{cid}                                     | Get Full Content by Cid                               |
| _PublicApi_       | [**public_by_cid_cid_get**](docs/PublicApi.md#public_by_cid_cid_get)                                                      | **GET** /public/by-cid/{cid}                           | Get Content by Cid                                    |
| _PublicApi_       | [**public_info_get**](docs/PublicApi.md#public_info_get)                                                                  | **GET** /public/info                                   | Get public node info                                  |
| _PublicApi_       | [**public_metrics_deals_on_chain_get**](docs/PublicApi.md#public_metrics_deals_on_chain_get)                              | **GET** /public/metrics/deals-on-chain                 | Get deal metrics                                      |
| _PublicApi_       | [**public_miners_deals_miner_get**](docs/PublicApi.md#public_miners_deals_miner_get)                                      | **GET** /public/miners/deals/{miner}                   | Get all miners deals                                  |
| _PublicApi_       | [**public_miners_failures_miner_get**](docs/PublicApi.md#public_miners_failures_miner_get)                                | **GET** /public/miners/failures/{miner}                | Get all miners                                        |
| _PublicApi_       | [**public_miners_stats_miner_get**](docs/PublicApi.md#public_miners_stats_miner_get)                                      | **GET** /public/miners/stats/{miner}                   | Get miner stats                                       |
| _PublicApi_       | [**public_net_addrs_get**](docs/PublicApi.md#public_net_addrs_get)                                                        | **GET** /public/net/addrs                              | Net Addrs                                             |
| _PublicApi_       | [**public_net_peers_get**](docs/PublicApi.md#public_net_peers_get)                                                        | **GET** /public/net/peers                              | Net Peers                                             |
| _PublicApi_       | [**public_stats_get**](docs/PublicApi.md#public_stats_get)                                                                | **GET** /public/stats                                  | Public stats                                          |

## Documentation For Models

- [AddressAddress](docs/AddressAddress.md)
- [ApiChannelIDParam](docs/ApiChannelIDParam.md)
- [ApiClaimMsgResponse](docs/ApiClaimMsgResponse.md)
- [ApiClaimResponse](docs/ApiClaimResponse.md)
- [ApiCreateCollectionBody](docs/ApiCreateCollectionBody.md)
- [ApiDeleteContentFromCollectionBody](docs/ApiDeleteContentFromCollectionBody.md)
- [ApiEmptyResp](docs/ApiEmptyResp.md)
- [ApiEstimateDealBody](docs/ApiEstimateDealBody.md)
- [ApiGetApiKeysResp](docs/ApiGetApiKeysResp.md)
- [ApiMinerResp](docs/ApiMinerResp.md)
- [ApiPublicNodeInfo](docs/ApiPublicNodeInfo.md)
- [AutoretrieveInitBody](docs/AutoretrieveInitBody.md)
- [CidCid](docs/CidCid.md)
- [CollectionsCidType](docs/CollectionsCidType.md)
- [CollectionsCollection](docs/CollectionsCollection.md)
- [CollectionsCollectionListResponse](docs/CollectionsCollectionListResponse.md)
- [ContentAddBody](docs/ContentAddBody.md)
- [MinerClaimMinerBody](docs/MinerClaimMinerBody.md)
- [MinerMinerChainInfo](docs/MinerMinerChainInfo.md)
- [MinerMinerSetInfoParams](docs/MinerMinerSetInfoParams.md)
- [MinerSuspendMinerBody](docs/MinerSuspendMinerBody.md)
- [PeeringPeeringPeer](docs/PeeringPeeringPeer.md)
- [TypesIpfsListPinStatusResponse](docs/TypesIpfsListPinStatusResponse.md)
- [TypesIpfsPin](docs/TypesIpfsPin.md)
- [TypesIpfsPinStatusResponse](docs/TypesIpfsPinStatusResponse.md)
- [TypesPinningStatus](docs/TypesPinningStatus.md)
- [UtilContentAddResponse](docs/UtilContentAddResponse.md)
- [UtilContentCreateBody](docs/UtilContentCreateBody.md)
- [UtilContentType](docs/UtilContentType.md)
- [UtilDbCID](docs/UtilDbCID.md)
- [UtilHttpError](docs/UtilHttpError.md)
- [UtilUserSettings](docs/UtilUserSettings.md)
- [UtilViewerResponse](docs/UtilViewerResponse.md)

## Documentation For Authorization

## bearerAuth

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header

## Author
