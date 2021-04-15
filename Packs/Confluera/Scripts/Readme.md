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
[{"name": "Detection-1", "data": [10], "color": "red"}, {"name": "Detection-2", "data": [10], "color": "red"}, {"name": "Detection-3", "data": [10], "color": "red"}, {"name": "Detection-4", "data": [10], "color": "red"}, {"name": "Detection-5", "data": [10], "color": "red"}, {"name": "Detection-6", "data": [10], "color": "red"}, {"name": "Detection-7", "data": [10], "color": "red"}, {"name": "Detection-8", "data": [10], "color": "red"}, {"name": "Detection-9", "data": [10], "color": "red"}, {"name": "Detection-10", "data": [0], "color": "blue"}, {"name": "Detection-11", "data": [1], "color": "green"}, {"name": "Detection-12", "data": [1], "color": "green"}, {"name": "Detection-13", "data": [0], "color": "blue"}, {"name": "Detection-14", "data": [1], "color": "green"}, {"name": "Detection-15", "data": [1], "color": "green"}, {"name": "Detection-16", "data": [0], "color": "blue"}, {"name": "Detection-17", "data": [1], "color": "green"}, {"name": "Detection-18", "data": [1], "color": "green"}, {"name": "Detection-19", "data": [0], "color": "blue"}, {"name": "Detection-20", "data": [1], "color": "green"}, {"name": "Detection-21", "data": [1], "color": "green"}, {"name": "Detection-22", "data": [0], "color": "blue"}, {"name": "Detection-23", "data": [1], "color": "green"}, {"name": "Detection-24", "data": [0], "color": "blue"}, {"name": "Detection-25", "data": [1], "color": "green"}, {"name": "Detection-26", "data": [0], "color": "blue"}, {"name": "Detection-27", "data": [1], "color": "green"}, {"name": "Detection-28", "data": [1], "color": "green"}, {"name": "Detection-29", "data": [0], "color": "blue"}, {"name": "Detection-30", "data": [1], "color": "green"}, {"name": "Detection-31", "data": [1], "color": "green"}, {"name": "Detection-32", "data": [0], "color": "blue"}, {"name": "Detection-33", "data": [1], "color": "green"}, {"name": "Detection-34", "data": [0], "color": "blue"}, {"name": "Detection-35", "data": [1], "color": "green"}, {"name": "Detection-36", "data": [0], "color": "blue"}, {"name": "Detection-37", "data": [10], "color": "red"}, {"name": "Detection-38", "data": [10], "color": "red"}, {"name": "Detection-39", "data": [1], "color": "green"}, {"name": "Detection-40", "data": [1], "color": "green"}, {"name": "Detection-41", "data": [1], "color": "green"}, {"name": "Detection-42", "data": [1], "color": "green"}, {"name": "Detection-43", "data": [1], "color": "green"}, {"name": "Detection-44", "data": [10], "color": "red"}, {"name": "Detection-45", "data": [10], "color": "red"}, {"name": "Detection-46", "data": [10], "color": "red"}, {"name": "Detection-47", "data": [10], "color": "red"}, {"name": "Detection-48", "data": [5], "color": "green"}, {"name": "Detection-49", "data": [5], "color": "green"}, {"name": "Detection-50", "data": [10], "color": "red"}, {"name": "Detection-51", "data": [10], "color": "red"}, {"name": "Detection-52", "data": [1], "color": "green"}, {"name": "Detection-53", "data": [5], "color": "green"}, {"name": "Detection-54", "data": [10], "color": "red"}, {"name": "Detection-55", "data": [10], "color": "red"}, {"name": "Detection-56", "data": [10], "color": "red"}, {"name": "Detection-57", "data": [10], "color": "red"}]
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
[{"name": "AP-950928", "data": [20], "color": "green"}, {"name": "AP-753817", "data": [6], "color": "green"}, {"name": "AP-942184", "data": [10], "color": "green"}, {"name": "AP-551491", "data": [10], "color": "green"}, {"name": "AP-945062", "data": [20], "color": "green"}, {"name": "AP-559633", "data": [10], "color": "green"}, {"name": "AP-564707", "data": [10], "color": "green"}, {"name": "AP-769367", "data": [40], "color": "red"}, {"name": "AP-777968", "data": [20], "color": "green"}, {"name": "AP-945074", "data": [20], "color": "green"}, {"name": "AP-545443", "data": [30], "color": "red"}, {"name": "AP-959564", "data": [20], "color": "green"}, {"name": "AP-962446", "data": [20], "color": "green"}, {"name": "AP-749363", "data": [20], "color": "green"}, {"name": "AP-67135", "data": [10], "color": "green"}, {"name": "AP-953810", "data": [20], "color": "green"}, {"name": "AP-559637", "data": [30], "color": "red"}, {"name": "AP-809127", "data": [10], "color": "green"}]
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



