# IqHub Log Script
### Script Data
---
 
| **Name** | **Description** |
| --- | --- |
| Script Type | python3 |
| Tags |  |
| Demisto Version | 6.0.2 |

### Inputs
---

| **Argument Name** | **Description** |
| --- | --- |
|  |  |

### Outputs
---

| **Path** | **Description** | **Type** |
| --- | --- | --- |
|  || |


### Script Example
```!IqHub_Log```

### Context Example

### Human Readable Output
## 
```
{
    "data": [
        {
            "Count": "Detections: 57",
            "URL": null
        },
        {
            "Count": "Progressions:18",
            "URL": null
        }
    ],
    "total": 2
}
```
---
# Detections Count Script
### Script Data
---

| **Name** | **Description** |
| --- | --- |
| Script Type | python3 |
| Tags |  |
| Demisto Version | 6.0.2 |

## Inputs
---

| **Argument Name** | **Description** |
| --- | --- |
|  |  | |


## Outputs
---

| **Path** | **Description** | **Type** |
| --- | --- | --- |
|  |  | |

### Context Example





### Script Example
```!Detections_Count```



### Human Readable Output
```
53
``` 
---
# Detection_Summary_Warroom Script
### Script Data
---

| **Name** | **Description** |
| --- | --- |
| Script Type | python3 |
| Tags |  |
| Demisto Version | 6.0.2 |



### Script Example
```!Detections_Summary_Warroom```

## Inputs
---

| **Argument Name** | **Description** |
| --- | --- |
|  |  | |


## Outputs
---

| **Path** | **Description** | **Type** |
| --- | --- | --- |
|  |  | |

### Context Example

### Human Readable Output
![alt text](https://github.com/kavyansh-coditas/content/blob/confluera/Packs/Confluera/Scripts/Images/Detection_summary_warroom.png))

---

# Detections_Data Script
### Script Data
---

| **Name** | **Description** |
| --- | --- |
| Script Type | python3 |
| Tags |  |
| Demisto Version | 6.0.2 |

### Inputs
---

| **Argument Name** | **Description** |
| --- | --- |
|  |  | |


### Outputs
---

| **Path** | **Description** | **Type** |
| --- | --- | --- |
|  |  | |

### Context Example





### Script Example
```!Detections_Data```



### Human Readable Output
```
[
    {
        "name": "Detection-1",
        "data": [10], 
        "color": "red"
    }, 
    {
        "name": "Detection-2", 
        "data": [10], 
        "color": "red"
    }, 
    {
        "name": "Detection-3", 
        "data": [10], 
        "color": "red"
    }, 
    {
        "name": "Detection-4", 
        "data": [10], 
        "color": "red"
    }, 
    {
        "name": "Detection-5", 
        "data": [10], 
        "color": "red"
    }, 
    {
        "name": "Detection-6", 
        "data": [10], 
        "color": "red"
    },
        ......................N data................
        ............................................ 
   {
       "name": "Detection-29", 
       "data": [0], 
       "color": "blue"
    }, 
    {
        "name":"Detection-57", 
        "data": [10], 
        "color": "red"
    }
    
]



```
---
# Detection_Summery Script
### Script Data
---

| **Name** | **Description** |
| --- | --- |
| Script Type | python3 |
| Tags |  |
| Demisto Version | 6.0.2 |



### Script Example
```!Detections_Summary```

### Inputs
---

| **Argument Name** | **Description** |
| --- | --- |
|  |  | |


### Outputs
---

| **Path** | **Description** | **Type** |
| --- | --- | --- |
|  |  | |

### Context Example



### Human Readable Output

```
[
    {
        "name": "Command and Control", 
        "data": [21], 
        "color": "#dc5e50"
    },
    {
        "name": "LATERAL_MOVEMENT",
        "data": [11], 
        "color": "#64bb18"
    }, 
    {
        "name": "Discovery",
        "data": [17],
        "color": "#8b639a"}, 
    {
        "name": "Credential Access",
        "data": [6],
        "color": "#d8a747"
    },
    {
        "name": "Persistence",
        "data": [1],
        "color": "#528fb2"
    }, 
    {
        "name": "Exfiltration", 
        "data": [1], 
        "color": "#9cc5aa"
    }

]
```
---
# Detections_Data_Warrrom Script
### Script Data
---

| **Name** | **Description** |
| --- | --- |
| Script Type | python3 |
| Tags |  |
| Demisto Version | 6.0.2 |

### Inputs
---

| **Argument Name** | **Description** |
| --- | --- |
|  |  | |


### Outputs
---

| **Path** | **Description** | **Type** |
| --- | --- | --- |
|  |  | |

### Context Example




### Script Example
```!Detections_Data_Warroom```



### Human Readable Output
![alt text]()

---
# Progressions_Count Script
### Script Data
---

| **Name** | **Description** |
| --- | --- |
| Script Type | python3 |
| Tags |  |
| Demisto Version | 6.0.2 |

### Inputs
---

| **Argument Name** | **Description** |
| --- | --- |
|  |  |

### Outputs
---

| **Path** | **Description** | **Type** |
| --- | --- | --- |
|  || |


### Script Example
```!Progressions_Count```

### Context Example

### Human Readable Output
### 
```
18
```
---
# Progressions Data Script
### Script Data
---

| **Name** | **Description** |
| --- | --- |
| Script Type | python3 |
| Tags |  |
| Demisto Version | 6.0.2 |

### Inputs
---

| **Argument Name** | **Description** |
| --- | --- |
|  |  |

### Outputs
---

| **Path** | **Description** | **Type** |
| --- | --- | --- |
|  || |


### Script Example
```!Progressions_Data```

### Context Example

### Human Readable Output
 
```
[
    {
        "name": "AP-950928", 
        "data": [20], 
        "color": "green"
    },
    {
        "name": "AP-753817", 
        "data": [6], 
        "color": "green"
    }, 
    {
        "name": "AP-942184", 
        "data": [10], 
        "color": "green"
    }, 
    {
        "name": "AP-551491", 
        "data": [10], 
        "color": "green"
    }, 
    {
        "name": "AP-945062", 
        "data": [20], 
        "color": "green"
    },
    ...........................N Data.......................
    ...................................................
    {
        "name": "AP-559637", 
        "data": [30], 
        "color": "red"
    }, 
    {
        "name": "AP-809127", 
        "data": [10], 
        "color": "green"
    }
]
```
---
# Progressions_Data_Warroom Script
### Script Data
---

| **Name** | **Description** |
| --- | --- |
| Script Type | python3 |
| Tags |  |
| Demisto Version | 6.0.2 |

### Inputs
---

| **Argument Name** | **Description** |
| --- | --- |
|  |  |

### Outputs
---

| **Path** | **Description** | **Type** |
| --- | --- | --- |
|  || |


### Script Example
```!Progressions_Data_Warroom```

### Context Example

### Human Readable Output
### 

![alt text](https://github.com/kavyansh-coditas/content/blob/confluera/Packs/Confluera/Scripts/Images/Progression_data_warrrom.png)



