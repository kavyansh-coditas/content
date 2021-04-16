
### Confluera Integration

This is Confluera Integration.

Please make sure you look at the integration source code and comments.

This integration was built to get the insights of Confluera API(Autonomouse Detetcions and Response).

## Configure Confluera on Cortex XSOAR

1. Navigate to **Settings** > **Integrations** > **Servers & Services**.
2. Search for Confluera.
3. Click **Add instance** to create and configure a new integration instance.

| **Parameter** | **Description** | **Required** |
| --- | --- | --- |
| IQ-Hub url | Server URL \(e.g. https://test.confluera.com\) | True |
| Trust any certificate | Not Secure | False |
| Use system proxy settings | Proxy Settings | False |
| Username |Usernme \(eg. admin@confluera.com\) | True|
| Password | Password \( Your Password\) | True |
| Detections Url | URL \(e.g. https://test.confluera.com/detections/) | Optional |
| Progressions Url | URL \(e.g. https://test.confluera.com/progressions/) | Optional |


4. Click **Test** to validate the URLs, token, and connection.
## Commands
You can execute these commands from the Cortex XSOAR CLI, as part of an automation, or in a playbook.
After you successfully execute a command, a DBot message appears in the War Room with the command details.
### confluera-login
***
confluera-login - Authenticates user to confuera Iq-Hub portal


#### Base Command

`confluera-login`
#### Input

| **Argument Name** | **Description** | **Required** |
| --- | --- | --- |
| | |  | 


#### Context Output

| **Path** | **Type** | **Description** |
| --- | --- | --- |
| Confluera.LoginData| Unknown | Login response | 


#### Command Example
```!confluera-login```

#### Context Example
```
{
    "message": "Logged in as admin@confluera.com",
    "firstname": "admin",
    "lastname": "confluera",
    "email": "admin@confluera.com",
    "access_token": "***",
    "expires": 161855311,
    "onboard": {}
}
```

#### Human Readable Output


| **access_token** | **email** | **expires** | **Pfirstname** | **lastname** | **onboard** |
| --- | --- | --- |--- | --- | --- |
| *** | admin@confluera.com| 161855311|admin|confluera |  |


### confluera-fetch-detections
***
Fetches list of detections in confluera for past x hours.


#### Base Command

`confluera-fetch-detections`
#### Input

| **Argument Name** | **Description** | **Required** |
| --- | --- | --- |
| access-token | Token used to access API endpoints from Iq-Hub portal. | Mandatory | 
| hours | Specifies the time duration for which detections need to be fetched  | Optional | 



#### Context Output

| **Path** | **Type** | **Description** |
| --- | --- | --- |
| Confluera.Detections | Unknown| Detections Response | 


#### Command Example
```!confluera-fetch-detections access-token="***" hours="23"```

#### Context Example
```
[
    {
        "agentId": "prod_0_5_.agent-5",
        "allowListId": null,
        "attackIdList": [
            1046922
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-828dda0c47c87f894cefd942d00a1bf9-1618553696441607784",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618553696441607784,
        "trailId": "8574513",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_5_.agent-5:8574513"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": " ",
        "iocHash": "hc-04f87e4f44f7ed5e7b2d13e423f803a0-1618472157328925024",
        "iocSummary": "container lateral movement ",
        "iocTactic": "LATERAL_MOVEMENT",
        "ruleid": 0,
        "scoreContribution": 0,
        "seenTime": 1618472157328925024,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": "release_agent.s launched a suspicious tool: nc",
        "iocHash": "Edge-005098d11d4423473ade627b1cc58886-1618471852668191541",
        "iocSummary": "Suspicious network tool launched",
        "iocTactic": "Discovery",
        "ruleid": 2,
        "scoreContribution": 1,
        "seenTime": 1618471852668191541,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": "release_agent.s launched a suspicious tool: nc",
        "iocHash": "Edge-005098d11d4423473ade627b1cc58886-1618471845847238985",
        "iocSummary": "Suspicious network tool launched",
        "iocTactic": "Discovery",
        "ruleid": 2,
        "scoreContribution": 1,
        "seenTime": 1618471845847238985,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": " ",
        "iocHash": "hc-72f431f9d745369b6d13ab76f27a2db2-1618471843588617223",
        "iocSummary": "container lateral movement ",
        "iocTactic": "LATERAL_MOVEMENT",
        "ruleid": 0,
        "scoreContribution": 0,
        "seenTime": 1618471843588617223,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": "release_agent.s launched a suspicious tool: nc",
        "iocHash": "Edge-005098d11d4423473ade627b1cc58886-1618469717237293120",
        "iocSummary": "Suspicious network tool launched",
        "iocTactic": "Discovery",
        "ruleid": 2,
        "scoreContribution": 1,
        "seenTime": 1618469717237293120,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": "release_agent.s launched a suspicious tool: nc",
        "iocHash": "Edge-005098d11d4423473ade627b1cc58886-1618469705421750946",
        "iocSummary": "Suspicious network tool launched",
        "iocTactic": "Discovery",
        "ruleid": 2,
        "scoreContribution": 1,
        "seenTime": 1618469705421750946,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": " ",
        "iocHash": "hc-89eddc7cd85a7265604e6a665b9f6829-1618469702487366133",
        "iocSummary": "container lateral movement ",
        "iocTactic": "LATERAL_MOVEMENT",
        "ruleid": 0,
        "scoreContribution": 0,
        "seenTime": 1618469702487366133,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": "release_agent.s launched a suspicious tool: nc",
        "iocHash": "Edge-005098d11d4423473ade627b1cc58886-1618469013524936885",
        "iocSummary": "Suspicious network tool launched",
        "iocTactic": "Discovery",
        "ruleid": 2,
        "scoreContribution": 1,
        "seenTime": 1618469013524936885,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": "release_agent.s launched a suspicious tool: nc",
        "iocHash": "Edge-005098d11d4423473ade627b1cc58886-1618469004649052986",
        "iocSummary": "Suspicious network tool launched",
        "iocTactic": "Discovery",
        "ruleid": 2,
        "scoreContribution": 1,
        "seenTime": 1618469004649052986,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            945058
        ],
        "iocDetail": " ",
        "iocHash": "hc-2e95393669329e71a85895c319754e7b-1618469000794514772",
        "iocSummary": "container lateral movement ",
        "iocTactic": "LATERAL_MOVEMENT",
        "ruleid": 0,
        "scoreContribution": 0,
        "seenTime": 1618469000794514772,
        "trailId": "165675012",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:165675012"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_1_.agent-33",
        "allowListId": null,
        "attackIdList": [
            1046830
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-828dda0c47c87f894cefd942d00a1bf9-1618553428039684190",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618553428039684190,
        "trailId": "33038564",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_1_.agent-33:33038564"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            959564
        ],
        "iocDetail": "bash established a reverse shell",
        "iocHash": "Edge-c1ed41a993aff3b19085916ff993d7eb-1618471855687793436",
        "iocSummary": "Reverse shell established",
        "iocTactic": "Command and Control",
        "ruleid": 4,
        "scoreContribution": 10,
        "seenTime": 1618471855687793436,
        "trailId": "173015047",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:173015047"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            959564
        ],
        "iocDetail": "bash established a reverse shell",
        "iocHash": "Edge-c1ed41a993aff3b19085916ff993d7eb-1618471848861198481",
        "iocSummary": "Reverse shell established",
        "iocTactic": "Command and Control",
        "ruleid": 4,
        "scoreContribution": 10,
        "seenTime": 1618471848861198481,
        "trailId": "173015047",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:173015047"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            962446
        ],
        "iocDetail": "bash established a reverse shell",
        "iocHash": "Edge-c1ed41a993aff3b19085916ff993d7eb-1618472169652652403",
        "iocSummary": "Reverse shell established",
        "iocTactic": "Command and Control",
        "ruleid": 4,
        "scoreContribution": 10,
        "seenTime": 1618472169652652403,
        "trailId": "174063622",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:174063622"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            962446
        ],
        "iocDetail": "bash established a reverse shell",
        "iocHash": "Edge-c1ed41a993aff3b19085916ff993d7eb-1618472163265174492",
        "iocSummary": "Reverse shell established",
        "iocTactic": "Command and Control",
        "ruleid": 4,
        "scoreContribution": 10,
        "seenTime": 1618472163265174492,
        "trailId": "174063622",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:174063622"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            950928
        ],
        "iocDetail": "bash established a reverse shell",
        "iocHash": "Edge-c1ed41a993aff3b19085916ff993d7eb-1618469016547533109",
        "iocSummary": "Reverse shell established",
        "iocTactic": "Command and Control",
        "ruleid": 4,
        "scoreContribution": 10,
        "seenTime": 1618469016547533109,
        "trailId": "168820741",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:168820741"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            950928
        ],
        "iocDetail": "bash established a reverse shell",
        "iocHash": "Edge-c1ed41a993aff3b19085916ff993d7eb-1618469007664334582",
        "iocSummary": "Reverse shell established",
        "iocTactic": "Command and Control",
        "ruleid": 4,
        "scoreContribution": 10,
        "seenTime": 1618469007664334582,
        "trailId": "168820741",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:168820741"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_17_.agent-17",
        "allowListId": null,
        "attackIdList": [
            753817
        ],
        "iocDetail": "Potential DNS Exfiltration using Subdomains",
        "iocHash": "MLEDGE-501-449586-f2df316a78b1beeff9553028700715c6",
        "iocSummary": "Potential DNS Exfiltration using Subdomains",
        "iocTactic": "Exfiltration",
        "ruleid": 501,
        "scoreContribution": 1,
        "seenTime": 1618512898755566200,
        "trailId": "360710187",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_17_.agent-17:360710187"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_3_.agent-3",
        "allowListId": null,
        "attackIdList": [
            1017038
        ],
        "iocDetail": "Reverse SSH tunnel created by ssh",
        "iocHash": "Edge-3925941cf171a173bb666eab3f046692-1618527895694908237",
        "iocSummary": "Reverse SSH tunnel created",
        "iocTactic": "Lateral Movement",
        "ruleid": 10,
        "scoreContribution": 10,
        "seenTime": 1618527895694908237,
        "trailId": "22796349",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_3_.agent-3:22796349"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_3_.agent-3",
        "allowListId": null,
        "attackIdList": [
            1017038
        ],
        "iocDetail": "Reverse SSH tunnel created by ssh",
        "iocHash": "Edge-3925941cf171a173bb666eab3f046692-1618527874837606854",
        "iocSummary": "Reverse SSH tunnel created",
        "iocTactic": "Lateral Movement",
        "ruleid": 10,
        "scoreContribution": 10,
        "seenTime": 1618527874837606854,
        "trailId": "22796349",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_3_.agent-3:22796349"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            985690
        ],
        "iocDetail": "Invoked \"sleep 1000000\"",
        "iocHash": "CBResult--66900",
        "iocSummary": "(AWS Lambda Result) arn:aws:lambda:us-east-2:769734503469:function:testSSMLambda invokes SendCommand ",
        "iocTactic": "Defense Evasion",
        "ruleid": 0,
        "scoreContribution": 10,
        "seenTime": 1618511548000000000,
        "trailId": "16351",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:16351"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            985690
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-5e97887e615f49a353db10d57754640d-1618510536408125099",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618510536408125099,
        "trailId": "16351",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:16351"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            985690
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-5e97887e615f49a353db10d57754640d-1618510046127744056",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618510046127744056,
        "trailId": "16351",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:16351"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            985860
        ],
        "iocDetail": "Invoked \"sleep 1000000\"",
        "iocHash": "CBResult--66927",
        "iocSummary": "(AWS Lambda Result) arn:aws:lambda:us-east-2:769734503469:function:testSSMLambda invokes SendCommand ",
        "iocTactic": "Defense Evasion",
        "ruleid": 0,
        "scoreContribution": 10,
        "seenTime": 1618512011000000000,
        "trailId": "22016",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:22016"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            985860
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-5e97887e615f49a353db10d57754640d-1618511964593974026",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618511964593974026,
        "trailId": "22016",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:22016"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            985860
        ],
        "iocDetail": "[\"prod_0_7_.agent-39:16351\"]",
        "iocHash": "InfluencedBy-9a56be0d76fe58f2373d64c4910aa40b-1618511546260570882",
        "iocSummary": "Uses tainted file (/var/lib/amazon/ssm/i-0736b112f2496f381/document/state/current/fd2b1a18-2c09-47f2-afc3-fe013a364250) influencerTrails [\"prod_0_7_.agent-39:16351\"]",
        "iocTactic": "Defense Evasion",
        "ruleid": 0,
        "scoreContribution": 2,
        "seenTime": 1618511546260570882,
        "trailId": "22016",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:22016"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509920518658861",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509920518658861,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509919293723593",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509919293723593,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509893214363394",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509893214363394,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509892347131086",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509892347131086,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509891387591244",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509891387591244,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509890243542389",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509890243542389,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509851233674054",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509851233674054,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509850279172474",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509850279172474,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509848449574659",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509848449574659,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "allowListId": null,
        "attackIdList": [
            972763
        ],
        "iocDetail": "User  accessing website ",
        "iocHash": "Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509682715309683",
        "iocSummary": "Long sleep executed by process",
        "iocTactic": "Lateral Movement",
        "ruleid": 1016,
        "scoreContribution": 5,
        "seenTime": 1618509682715309683,
        "trailId": "2",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_7_.agent-39:2"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            953810
        ],
        "iocDetail": "bash established a reverse shell",
        "iocHash": "Edge-c1ed41a993aff3b19085916ff993d7eb-1618469720254586836",
        "iocSummary": "Reverse shell established",
        "iocTactic": "Command and Control",
        "ruleid": 4,
        "scoreContribution": 10,
        "seenTime": 1618469720254586836,
        "trailId": "170917892",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:170917892"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "allowListId": null,
        "attackIdList": [
            953810
        ],
        "iocDetail": "bash established a reverse shell",
        "iocHash": "Edge-c1ed41a993aff3b19085916ff993d7eb-1618469708443112439",
        "iocSummary": "Reverse shell established",
        "iocTactic": "Command and Control",
        "ruleid": 4,
        "scoreContribution": 10,
        "seenTime": 1618469708443112439,
        "trailId": "170917892",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_26_.agent-26:170917892"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    },
    {
        "agentId": "prod_0_17_.agent-17",
        "allowListId": null,
        "attackIdList": [
            986620
        ],
        "iocDetail": "Scanning activity detected",
        "iocHash": "MLEDGE-504-449587-d1d207df671df34df49069f887e7d55a",
        "iocSummary": "Scanning activity detected",
        "iocTactic": "Discovery",
        "ruleid": 504,
        "scoreContribution": 5,
        "seenTime": 1618513883123888400,
        "trailId": "374634817",
        "trailIocInfoType": "DETECTION",
        "trailList": [
            "prod_0_17_.agent-17:374634817"
        ],
        "trailStateList": [
            "ACTIVE"
        ]
    }
]
```

#### Human Readable Output

>### Results
>|agentId |allowListId |attackIdList|iocDetail |iocHash|iocSummary| iocTactic| ruleid|scoreContribution|seenTime |trailId|trailIocInfoType |trailList | trailStateList |
>|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
>|prod_0_7_.agent-39 || 985860| ["prod_0_7_.agent-39:16351"] | InfluencedBy-9a56be0d76fe58f2373d64c4910aa40b-1618511546260570882 | Uses tainted file (/var/lib/amazon/ssm/i-0736b112f2496f381/document/state/current/fd2b1a18-2c09-47f2-afc3-fe013a364250) influencerTrails ["prod_0_7_.agent-39:16351"] | Defense Evasion|0 |2 |1618511546260570882 | 22016|DETECTION| prod_0_7_.agent-39:22016|ACTIVE |
>|prod_0_7_.agent-39 || 985860| ["prod_0_7_.agent-39:16351"] | InfluencedBy-9a56be0d76fe58f2373d64c4910aa40b-1618511546260570882 | Uses tainted file (/var/lib/amazon/ssm/i-0736b112f2496f381/document/state/current/fd2b1a18-2c09-47f2-afc3-fe013a364250) influencerTrails ["prod_0_7_.agent-39:16351"] | Defense Evasion|0 |2 |1618511546260570882 | 22016|DETECTION| prod_0_7_.agent-39:22016|ACTIVE |
>|prod_0_7_.agent-39 || 972763| User  accessing website | Edge-ae3b3d9a3c5d4b17491d3f6d924bd3b8-1618509851233674054 | Long sleep executed by process| Lateral Movement|0 |2 |1618511546260570882 | 22016|DETECTION| prod_0_7_.agent-39:22016|ACTIVE |
>|prod_0_7_.agent-39 || 972763| User  accessing website | InfluencedBy-9a56be0d76fe58f2373d64c4910aa40b-1618511546260570882 | Uses tainted file (/var/lib/amazon/ssm/i-0736b112f2496f381/document/state/current/fd2b1a18-2c09-47f2-afc3-fe013a364250) influencerTrails ["prod_0_7_.agent-39:16351"] | Defense Evasion|0 |2 |1618511546260570882 | 22016|DETECTION| prod_0_7_.agent-39:22016|ACTIVE |




### confluera-fetch-progressions
***
Fetches list of progressions in confluera for past x hours.


#### Base Command

`confluera-fetch-progressions`
#### Input

| **Argument Name** | **Description** | **Required** |
| --- | --- | --- |
|access-token| token used to access apis from Iq-Hub portal. | Required | 
|hours|Specifies the time duration for which progressions need to be fetched |Optional|


#### Context Output

| **Path** | **Type** | **Description** |
| --- | --- | --- |
| Confluera.Progressions| Unknown | Progressions response | 


#### Command Example
```!confluera-fetch-progressions access-token="***" hours="72"```

#### Context Example
```
[
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 942184,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618466218792013459
        },
        "lastIocSeenTime": 1618466218792013459,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618466218792013459,
        "numberOfDetections": 1,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618466218792013459,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:164626437",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618466218792013459,
                "trailId": "164626437"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 551491,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618377136684142214
        },
        "lastIocSeenTime": 1618377136684142214,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618377136684142214,
        "numberOfDetections": 1,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618377136684142214,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:156237829",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618377136684142214,
                "trailId": "156237829"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 945062,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618467431287580822
        },
        "lastIocSeenTime": 1618467456420177752,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618467456420177752,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618467431287580822,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:166723593",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618467431287580822,
                "trailId": "166723593"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618467456420177752,
                "trailId": "166723593"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 559633,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618378594837195479
        },
        "lastIocSeenTime": 1618378594837195479,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618378594837195479,
        "numberOfDetections": 1,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618378594837195479,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:157286403",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618378594837195479,
                "trailId": "157286403"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 564707,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618379630722739178
        },
        "lastIocSeenTime": 1618379630722739178,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618379630722739178,
        "numberOfDetections": 1,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618379630722739178,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:159383560",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618379630722739178,
                "trailId": "159383560"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 769367,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618417629053160077
        },
        "lastIocSeenTime": 1618419753818041182,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618419753818041182,
        "numberOfDetections": 4,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 40,
        "startTime": 1618417629053160077,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:162529286",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618417629053160077,
                "trailId": "162529286"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618417643483695872,
                "trailId": "162529286"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618419745913521063,
                "trailId": "162529286"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618419753818041182,
                "trailId": "162529286"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 777968,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618419916812380979
        },
        "lastIocSeenTime": 1618419932374598355,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618419932374598355,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618419916812380979,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:163577862",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618419916812380979,
                "trailId": "163577862"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618419932374598355,
                "trailId": "163577862"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 959564,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618471848861198481
        },
        "lastIocSeenTime": 1618471855687793436,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618471855687793436,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618471848861198481,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:173015047",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618471848861198481,
                "trailId": "173015047"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618471855687793436,
                "trailId": "173015047"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 962446,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618472163265174492
        },
        "lastIocSeenTime": 1618472169652652403,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618472169652652403,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618472163265174492,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:174063622",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618472163265174492,
                "trailId": "174063622"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618472169652652403,
                "trailId": "174063622"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 749363,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618415101941155778
        },
        "lastIocSeenTime": 1618415112193060197,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618415112193060197,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618415101941155778,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:160432130",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618415101941155778,
                "trailId": "160432130"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618415112193060197,
                "trailId": "160432130"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 559637,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618378755353200744
        },
        "lastIocSeenTime": 1618378828286969292,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618378828286969292,
        "numberOfDetections": 3,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 30,
        "startTime": 1618378755353200744,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:158334980",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618378755353200744,
                "trailId": "158334980"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618378806141616200,
                "trailId": "158334980"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618378828286969292,
                "trailId": "158334980"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_13_.agent-13",
        "attackId": 809127,
        "containsAnchor": true,
        "fingerprint": "602b86c4043d41d014496e14cb0b1fb5761b4d0d3e7092b43401cea39da02922",
        "hostTimeInfoMap": {
            "prod_0_13_.agent-13": 1618428361897896500
        },
        "lastIocSeenTime": 1618428490000217300,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618428490000217300,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618428361897896500,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_13_.agent-13:97518357",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_13_.agent-13",
                "scoreContribution": 0,
                "seenTime": 1618428361897896500,
                "trailId": "97518357"
            },
            {
                "agentId": "prod_0_13_.agent-13",
                "scoreContribution": 5,
                "seenTime": 1618428490000217300,
                "trailId": "97518357"
            }
        ],
        "trailTacticSet": [
            "persistence",
            "credential_access"
        ],
        "trailTechniqueSet": [
            "T1003",
            "T1050"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 950928,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618469007664334582
        },
        "lastIocSeenTime": 1618469016547533109,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618469016547533109,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618469007664334582,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:168820741",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618469007664334582,
                "trailId": "168820741"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618469016547533109,
                "trailId": "168820741"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_17_.agent-17",
        "attackId": 753817,
        "containsAnchor": false,
        "fingerprint": "df8519f5bbe6a8503c4b63da7a569cb1a1d51cd2d5784301e8d6dcec1950c93f",
        "hostTimeInfoMap": {
            "prod_0_17_.agent-17": 1618415669880332700
        },
        "lastIocSeenTime": 1618512898755566200,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618512898755566200,
        "numberOfDetections": 3,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 7,
        "startTime": 1618415669880332700,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_17_.agent-17:360710187",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_17_.agent-17",
                "scoreContribution": 0,
                "seenTime": 1618415669880332700,
                "trailId": "360710187"
            },
            {
                "agentId": "prod_0_17_.agent-17",
                "scoreContribution": 5,
                "seenTime": 1618417429913456400,
                "trailId": "360710187"
            },
            {
                "agentId": "prod_0_17_.agent-17",
                "scoreContribution": 1,
                "seenTime": 1618512898755566200,
                "trailId": "360710187"
            }
        ],
        "trailTacticSet": [
            "discovery",
            "exfiltration"
        ],
        "trailTechniqueSet": [
            "T1048",
            "T1046"
        ]
    },
    {
        "agentId": "prod_0_3_.agent-3",
        "attackId": 1017038,
        "containsAnchor": true,
        "fingerprint": "1a3618e0737531b1059fcbf5b8b0ed171d5a88ed1c6f562324365c8427a7f0af",
        "hostTimeInfoMap": {
            "prod_0_3_.agent-3": 1618527874837606854
        },
        "lastIocSeenTime": 1618527895694908237,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618527895694908237,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618527874837606854,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_3_.agent-3:22796349",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_3_.agent-3",
                "scoreContribution": 0,
                "seenTime": 1618527874837606854,
                "trailId": "22796349"
            },
            {
                "agentId": "prod_0_3_.agent-3",
                "scoreContribution": 10,
                "seenTime": 1618527895694908237,
                "trailId": "22796349"
            }
        ],
        "trailTacticSet": [
            "lateral_movement"
        ],
        "trailTechniqueSet": [
            "T1021"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 945074,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618467671541148246
        },
        "lastIocSeenTime": 1618467680214802321,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618467680214802321,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618467671541148246,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:167772163",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618467671541148246,
                "trailId": "167772163"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618467680214802321,
                "trailId": "167772163"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 545443,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618375888610124348
        },
        "lastIocSeenTime": 1618375961079921233,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618375961079921233,
        "numberOfDetections": 3,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 30,
        "startTime": 1618375888610124348,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:155189255",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618375888610124348,
                "trailId": "155189255"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618375921655271782,
                "trailId": "155189255"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618375961079921233,
                "trailId": "155189255"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "attackId": 972763,
        "containsAnchor": false,
        "fingerprint": "e6ef10e7963a1c4a2e973523e51a0ed6a027661a63a65fb57494eaf5d2bfaa05",
        "hostTimeInfoMap": {
            "prod_0_7_.agent-39": 1618503465522547303
        },
        "lastIocSeenTime": 1618512000354104687,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618512000354104687,
        "numberOfDetections": 56,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 60,
        "startTime": 1618503465522547303,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_7_.agent-39:2",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 0,
                "seenTime": 1618503465522547303,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618503801337850143,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618503801365102003,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618504390794505175,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618506343199369069,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618507633105705368,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618507637871574428,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618507644034649760,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618508297597220946,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618508297623461268,
                "trailId": "2"
            }
        ],
        "trailTacticSet": [
            "execution",
            "lateral_movement",
            "credential_access"
        ],
        "trailTechniqueSet": [
            "T1021",
            "T1003"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 953810,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618469708443112439
        },
        "lastIocSeenTime": 1618469720254586836,
        "lastIocSeenTimeInternal": 0,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618469720254586836,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618469708443112439,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:170917892",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618469708443112439,
                "trailId": "170917892"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618469720254586836,
                "trailId": "170917892"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    }
]
```

#### Human Readable Output

>### Progressions Log:
>|Progression URL|Total Progressions|
>|---|---|
>||19|
>### Successfully fetched 19 progressions.
>|agentId|attackId|containsAnchor|fingerprint|hostTimeInfoMap|lastIocSeenTime|lastIocSeenTimeInternal|lastMitigatedTime|local|mitigateTime|numberOfDetections|numberOfHosts|numberOfLateralMovements|riskMomentum|riskScore|startTime|state|trailIdHash|trailRiskHistInfoList|trailTacticSet|trailTechniqueSet|
>|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
>|prod_0_26_.agent-26|942184|true|34386ee468f53dc45582f45ed15f204794d|prod_0_26_.agent-26: 1618466218792013459|1618466218792013459|0|0|true|1618466218792013459|1|1|0|0|10|1618466218792013459|ACTIVE|prod_0_26_.agent-26:164626437|{'agentId': 'prod_0_26_.agent-26', 'scoreContribution': 0, 'seenTime': 1618466218792013459, 'trailId': '164626437'}|command_and_control|T1219|
>|prod_0_26_.agent-26|559633|true|2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d|prod_0_26_.agent-26: 1618378594837195479|1618378594837195479|0|0|true|1618379630722739179|1|1|0|0|10|1618466218792013459|ACTIVE|prod_0_26_.agent-26:157286403|{'agentId': 'prod_0_26_.agent-26', 'scoreContribution': 0, 'seenTime': 1618378594837195479, 'trailId': '157286403'}|command_and_control|T1219|
>|prod_0_26_.agent-26|769367|true|34386ee468f53dc45582f45ed15f204794d|prod_0_26_.agent-26: 1618417629053160077|1618417629053160077|0|0|true|1618417629053160077|4|1|0|0|40|1618419753818041182|ACTIVE|prod_0_26_.agent-26:162529286|{'agentId': 'prod_0_26_.agent-26', 'scoreContribution': 10, 'seenTime': 1618419753818041182, 'trailId': '162529286'}|command_and_control|T1219|



### confluera-fetch-trail-details
***
Fetches progression details of which provided trailId is a part of.


#### Base Command

`confluera-fetch-trail-details`
#### Input

| **Argument Name** | **Description** | **Required** |
| --- | --- | --- |
| access-token| Token used to access apis from Iq-Hub portal. | Required | 
| trail-id| Id of a detection in iq-hub protal. | Required | 


#### Context Output

| **Path** | **Type** | **Description** |
| --- | --- | --- |
| Confluera.TrailDetails| Unknown| Progression Details | 


#### Command Example
```!confluera-fetch-trail-details access-token="***" trail-id="22796349"```

#### Context Example
```
[
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 942184,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618466218792013459
        },
        "lastIocSeenTime": 1618466218792013459,
        "lastIocSeenTimeInternal": 1618466218792013459,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618466218792013459,
        "numberOfDetections": 1,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618466218792013459,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:164626437",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618466218792013459,
                "trailId": "164626437"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 551491,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618377136684142214
        },
        "lastIocSeenTime": 1618377136684142214,
        "lastIocSeenTimeInternal": 1618377136684142214,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618377136684142214,
        "numberOfDetections": 1,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618377136684142214,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:156237829",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618377136684142214,
                "trailId": "156237829"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 945062,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618467431287580822
        },
        "lastIocSeenTime": 1618467456420177752,
        "lastIocSeenTimeInternal": 1618467456420177752,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618467456420177752,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618467431287580822,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:166723593",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618467431287580822,
                "trailId": "166723593"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618467456420177752,
                "trailId": "166723593"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 559633,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618378594837195479
        },
        "lastIocSeenTime": 1618378594837195479,
        "lastIocSeenTimeInternal": 1618378594837195479,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618378594837195479,
        "numberOfDetections": 1,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618378594837195479,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:157286403",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618378594837195479,
                "trailId": "157286403"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 564707,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618379630722739178
        },
        "lastIocSeenTime": 1618379630722739178,
        "lastIocSeenTimeInternal": 1618379630722739178,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618379630722739178,
        "numberOfDetections": 1,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618379630722739178,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:159383560",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618379630722739178,
                "trailId": "159383560"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 769367,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618417629053160077
        },
        "lastIocSeenTime": 1618419753818041182,
        "lastIocSeenTimeInternal": 1618419753818041182,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618419753818041182,
        "numberOfDetections": 4,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 40,
        "startTime": 1618417629053160077,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:162529286",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618417629053160077,
                "trailId": "162529286"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618417643483695872,
                "trailId": "162529286"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618419745913521063,
                "trailId": "162529286"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618419753818041182,
                "trailId": "162529286"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 777968,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618419916812380979
        },
        "lastIocSeenTime": 1618419932374598355,
        "lastIocSeenTimeInternal": 1618419932374598355,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618419932374598355,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618419916812380979,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:163577862",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618419916812380979,
                "trailId": "163577862"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618419932374598355,
                "trailId": "163577862"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 959564,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618471848861198481
        },
        "lastIocSeenTime": 1618471855687793436,
        "lastIocSeenTimeInternal": 1618471855687793436,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618471855687793436,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618471848861198481,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:173015047",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618471848861198481,
                "trailId": "173015047"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618471855687793436,
                "trailId": "173015047"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 962446,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618472163265174492
        },
        "lastIocSeenTime": 1618472169652652403,
        "lastIocSeenTimeInternal": 1618472169652652403,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618472169652652403,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618472163265174492,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:174063622",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618472163265174492,
                "trailId": "174063622"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618472169652652403,
                "trailId": "174063622"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 749363,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618415101941155778
        },
        "lastIocSeenTime": 1618415112193060197,
        "lastIocSeenTimeInternal": 1618415112193060197,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618415112193060197,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618415101941155778,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:160432130",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618415101941155778,
                "trailId": "160432130"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618415112193060197,
                "trailId": "160432130"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 67135,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618292857657065566
        },
        "lastIocSeenTime": 1618292857657065566,
        "lastIocSeenTimeInternal": 1618292857657065566,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618292857657065566,
        "numberOfDetections": 1,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "ownerId": {
            "email": "admin@confluera.com",
            "firstname": "admin",
            "lastname": "admin",
            "profile_img": null
        },
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618292857657065566,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:150994952",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618292857657065566,
                "trailId": "150994952"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 559637,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618378755353200744
        },
        "lastIocSeenTime": 1618378828286969292,
        "lastIocSeenTimeInternal": 1618378828286969292,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618378828286969292,
        "numberOfDetections": 3,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 30,
        "startTime": 1618378755353200744,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:158334980",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618378755353200744,
                "trailId": "158334980"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618378806141616200,
                "trailId": "158334980"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618378828286969292,
                "trailId": "158334980"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_13_.agent-13",
        "attackId": 809127,
        "containsAnchor": true,
        "fingerprint": "602b86c4043d41d014496e14cb0b1fb5761b4d0d3e7092b43401cea39da02922",
        "hostTimeInfoMap": {
            "prod_0_13_.agent-13": 1618428361897896500
        },
        "lastIocSeenTime": 1618428490000217300,
        "lastIocSeenTimeInternal": 1618428490000217300,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618428490000217300,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 10,
        "startTime": 1618428361897896500,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_13_.agent-13:97518357",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_13_.agent-13",
                "scoreContribution": 0,
                "seenTime": 1618428361897896500,
                "trailId": "97518357"
            },
            {
                "agentId": "prod_0_13_.agent-13",
                "scoreContribution": 5,
                "seenTime": 1618428490000217300,
                "trailId": "97518357"
            }
        ],
        "trailTacticSet": [
            "persistence",
            "credential_access"
        ],
        "trailTechniqueSet": [
            "T1050",
            "T1003"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 950928,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618469007664334582
        },
        "lastIocSeenTime": 1618469016547533109,
        "lastIocSeenTimeInternal": 1618469016547533109,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618469016547533109,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618469007664334582,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:168820741",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618469007664334582,
                "trailId": "168820741"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618469016547533109,
                "trailId": "168820741"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_17_.agent-17",
        "attackId": 753817,
        "containsAnchor": false,
        "fingerprint": "df8519f5bbe6a8503c4b63da7a569cb1a1d51cd2d5784301e8d6dcec1950c93f",
        "hostTimeInfoMap": {
            "prod_0_17_.agent-17": 1618415669880332700
        },
        "lastIocSeenTime": 1618512898755566200,
        "lastIocSeenTimeInternal": 1618512898755566200,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618512898755566200,
        "numberOfDetections": 3,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 7,
        "startTime": 1618415669880332700,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_17_.agent-17:360710187",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_17_.agent-17",
                "scoreContribution": 0,
                "seenTime": 1618415669880332700,
                "trailId": "360710187"
            },
            {
                "agentId": "prod_0_17_.agent-17",
                "scoreContribution": 5,
                "seenTime": 1618417429913456400,
                "trailId": "360710187"
            },
            {
                "agentId": "prod_0_17_.agent-17",
                "scoreContribution": 1,
                "seenTime": 1618512898755566200,
                "trailId": "360710187"
            }
        ],
        "trailTacticSet": [
            "discovery",
            "exfiltration"
        ],
        "trailTechniqueSet": [
            "T1048",
            "T1046"
        ]
    },
    {
        "agentId": "prod_0_3_.agent-3",
        "attackId": 1017038,
        "containsAnchor": true,
        "fingerprint": "1a3618e0737531b1059fcbf5b8b0ed171d5a88ed1c6f562324365c8427a7f0af",
        "hostTimeInfoMap": {
            "prod_0_3_.agent-3": 1618527874837606854
        },
        "lastIocSeenTime": 1618527895694908237,
        "lastIocSeenTimeInternal": 1618527895694908237,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618527895694908237,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618527874837606854,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_3_.agent-3:22796349",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_3_.agent-3",
                "scoreContribution": 0,
                "seenTime": 1618527874837606854,
                "trailId": "22796349"
            },
            {
                "agentId": "prod_0_3_.agent-3",
                "scoreContribution": 10,
                "seenTime": 1618527895694908237,
                "trailId": "22796349"
            }
        ],
        "trailTacticSet": [
            "lateral_movement"
        ],
        "trailTechniqueSet": [
            "T1021"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 945074,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618467671541148246
        },
        "lastIocSeenTime": 1618467680214802321,
        "lastIocSeenTimeInternal": 1618467680214802321,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618467680214802321,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618467671541148246,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:167772163",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618467671541148246,
                "trailId": "167772163"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618467680214802321,
                "trailId": "167772163"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 545443,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618375888610124348
        },
        "lastIocSeenTime": 1618375961079921233,
        "lastIocSeenTimeInternal": 1618375961079921233,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618375961079921233,
        "numberOfDetections": 3,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 30,
        "startTime": 1618375888610124348,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:155189255",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618375888610124348,
                "trailId": "155189255"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618375921655271782,
                "trailId": "155189255"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618375961079921233,
                "trailId": "155189255"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    },
    {
        "agentId": "prod_0_7_.agent-39",
        "attackId": 972763,
        "containsAnchor": false,
        "fingerprint": "e6ef10e7963a1c4a2e973523e51a0ed6a027661a63a65fb57494eaf5d2bfaa05",
        "hostTimeInfoMap": {
            "prod_0_7_.agent-39": 1618503465522547303
        },
        "lastIocSeenTime": 1618512000354104687,
        "lastIocSeenTimeInternal": 1618512000354104687,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618512000354104687,
        "numberOfDetections": 56,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 60,
        "startTime": 1618503465522547303,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_7_.agent-39:2",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 0,
                "seenTime": 1618503465522547303,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618503801337850143,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618503801365102003,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618504390794505175,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618506343199369069,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618507633105705368,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618507637871574428,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618507644034649760,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618508297597220946,
                "trailId": "2"
            },
            {
                "agentId": "prod_0_7_.agent-39",
                "scoreContribution": 1,
                "seenTime": 1618508297623461268,
                "trailId": "2"
            }
        ],
        "trailTacticSet": [
            "execution",
            "lateral_movement",
            "credential_access"
        ],
        "trailTechniqueSet": [
            "T1021",
            "T1003"
        ]
    },
    {
        "agentId": "prod_0_26_.agent-26",
        "attackId": 953810,
        "containsAnchor": true,
        "fingerprint": "2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d",
        "hostTimeInfoMap": {
            "prod_0_26_.agent-26": 1618469708443112439
        },
        "lastIocSeenTime": 1618469720254586836,
        "lastIocSeenTimeInternal": 1618469720254586836,
        "lastMitigatedTime": 0,
        "local": true,
        "mitigateTime": 1618469720254586836,
        "numberOfDetections": 2,
        "numberOfHosts": 1,
        "numberOfLateralMovements": 0,
        "riskMomentum": 0,
        "riskScore": 20,
        "startTime": 1618469708443112439,
        "state": "ACTIVE",
        "trailIdHash": "prod_0_26_.agent-26:170917892",
        "trailRiskHistInfoList": [
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 0,
                "seenTime": 1618469708443112439,
                "trailId": "170917892"
            },
            {
                "agentId": "prod_0_26_.agent-26",
                "scoreContribution": 10,
                "seenTime": 1618469720254586836,
                "trailId": "170917892"
            }
        ],
        "trailTacticSet": [
            "command_and_control"
        ],
        "trailTechniqueSet": [
            "T1219"
        ]
    }
]
```

#### Human Readable Output

>### Trail Details:
>|agentId|attackId|containsAnchor|fingerprint|hostTimeInfoMap|lastIocSeenTime|lastIocSeenTimeInternal|lastMitigatedTime|local|mitigateTime|numberOfDetections|numberOfHosts|numberOfLateralMovements|riskMomentum|riskScore|startTime|state|trailIdHash|trailRiskHistInfoList|trailTacticSet|trailTechniqueSet|
>|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
>|prod_0_26_.agent-26|942184|true|34386ee468f53dc45582f45ed15f204794d|prod_0_26_.agent-26: 1618466218792013459|1618466218792013459|0|0|true|1618466218792013459|1|1|0|0|10|1618466218792013459|ACTIVE|prod_0_26_.agent-26:164626437|{'agentId': 'prod_0_26_.agent-26', 'scoreContribution': 0, 'seenTime': 1618466218792013459, 'trailId': '164626437'}|command_and_control|T1219|
>|prod_0_26_.agent-26|559633|true|2fca6467a9dccd2729ace9ce1832334386ee468f53dc45582f45ed15f204794d|prod_0_26_.agent-26: 1618378594837195479|1618378594837195479|0|0|true|1618379630722739179|1|1|0|0|10|1618466218792013459|ACTIVE|prod_0_26_.agent-26:157286403|{'agentId': 'prod_0_26_.agent-26', 'scoreContribution': 0, 'seenTime': 1618378594837195479, 'trailId': '157286403'}|command_and_control|T1219|
>|prod_0_26_.agent-26|769367|true|34386ee468f53dc45582f45ed15f204794d|prod_0_26_.agent-26: 1618417629053160077|1618417629053160077|0|0|true|1618417629053160077|4|1|0|0|40|1618419753818041182|ACTIVE|prod_0_26_.agent-26:162529286|{'agentId': 'prod_0_26_.agent-26', 'scoreContribution': 10, 'seenTime': 1618419753818041182, 'trailId': '162529286'}|command_and_control|T1219|



---
