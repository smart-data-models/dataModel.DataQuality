<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
实体：数据质量评估  
=========<!-- /10-Header -->  
<!-- 15-License -->  
[开放许可](https://github.com/smart-data-models//dataModel.DataQuality/blob/master/DataQualityAssessment/LICENSE.md)  
[文件自动生成](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
全局描述：**该实体描述测量数据（如温度）的数据质量属性。  
版本： 0.0.4  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

## 属性列表  

<sup><sub>[*] 如果属性中没有类型，是因为它可能有多个类型或不同的格式/模式</sub></sup>。  
- `accuracy[number]`: 精度测量传感器测量中产生的最大系统数字误差  - `address[object]`: 邮寄地址  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: 国家。例如，西班牙  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)  
	- `addressLocality[string]`: 街道地址所在的地点，以及该地点所在的区域  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)  
	- `addressRegion[string]`: 地点所在的地区，以及该地区位于哪个国家  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)  
	- `district[string]`: 地区是一种行政区划，在一些国家由地方政府管理    
	- `postOfficeBoxNumber[string]`: 用于邮政信箱地址的邮政信箱号码。例如：03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)  
	- `postalCode[string]`: 邮政编码。例如：24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)  
	- `streetAddress[string]`: 街道地址  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)  
	- `streetNr[string]`: 标识公共街道上特定房产的编号    
- `alternateName[string]`: 该项目的替代名称  - `areaServed[string]`: 提供服务或提供物品的地理区域  . Model: [https://schema.org/Text](https://schema.org/Text)- `completeness[number]`: 完整性量化了特定时间窗口内遗漏的测量或观测数据的数量  - `dataProvider[string]`: 标识统一数据实体提供者的字符序列  - `dateCalculated[date-time]`: 用户定义的计算实体的日期  - `dateCreated[date-time]`: 实体创建时间戳。通常由存储平台分配  - `dateModified[date-time]`: 实体最后一次修改的时间戳。通常由存储平台分配  - `description[string]`: 项目描述  - `duplicate[object]`: 包括有关重复数据的信息  	- `foundMatches[array]`: 如果是重复的，请确定测量值是否与以下内容相匹配    
	- `isDuplicate[boolean]`: 确定测量是否重复    
- `id[*]`: 实体的唯一标识符  - `location[*]`: 项目的 Geojson 引用。它可以是点、线条字符串、多边形、多点、多线条字符串或多多边形  - `name[string]`: 该项目的名称  - `outlier[object]`: 包括测量的离群特征信息  	- `isOutlier[boolean]`: 确定测量结果是否被视为离群值    
	- `methodology[*]`: 提及其他实体，包括人工智能方法信息    
	- `outlierScore[number]`: 表示离群程度的分数    
- `owner[array]`: 包含一个 JSON 编码字符序列的列表，其中引用了所有者的唯一 Ids  - `precision[number]`: 精度衡量数据集的标准偏差。也就是说，它衡量数据集中各值之间的接近程度  - `seeAlso[*]`: 指向有关该项目的其他资源的 uri 列表  - `source[string]`: 以 URL 形式给出实体数据原始来源的字符串。建议使用源提供者的完全合格域名或源对象的 URL  - `synthetic[object]`: 包括测量来源的信息  	- `isSynthetic[boolean]`: 确定测量结果是否是合成的    
	- `methodology[*]`: 提及其他实体，包括人工智能方法信息    
- `timeliness[number]`: 数据流的平均及时性  - `type[string]`: NGSI 实体类型。必须是 DataQualityAssessment  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
所需属性  
- `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-NotesYaml -->  
<!-- /40-NotesYaml -->  
<!-- 50-DataModelHeader -->  
## 属性的数据模型描述  
按字母顺序排列（点击查看详情）  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
DataQualityAssessment:    
  description: 'This entity describes the data quality properties of a measurement, such as temperature.'    
  properties:    
    accuracy:    
      description: Accuracy measures the maximum systematic numerical error produced in a sensor measurement    
      type: number    
      x-ngsi:    
        type: Property    
    address:    
      description: The mailing address    
      properties:    
        addressCountry:    
          description: 'The country. For example, Spain'    
          type: string    
          x-ngsi:    
            model: https://schema.org/addressCountry    
            type: Property    
        addressLocality:    
          description: 'The locality in which the street address is, and which is in the region'    
          type: string    
          x-ngsi:    
            model: https://schema.org/addressLocality    
            type: Property    
        addressRegion:    
          description: 'The region in which the locality is, and which is in the country'    
          type: string    
          x-ngsi:    
            model: https://schema.org/addressRegion    
            type: Property    
        district:    
          description: 'A district is a type of administrative division that, in some countries, is managed by the local government'    
          type: string    
          x-ngsi:    
            type: Property    
        postOfficeBoxNumber:    
          description: 'The post office box number for PO box addresses. For example, 03578'    
          type: string    
          x-ngsi:    
            model: https://schema.org/postOfficeBoxNumber    
            type: Property    
        postalCode:    
          description: 'The postal code. For example, 24004'    
          type: string    
          x-ngsi:    
            model: https://schema.org/https://schema.org/postalCode    
            type: Property    
        streetAddress:    
          description: The street address    
          type: string    
          x-ngsi:    
            model: https://schema.org/streetAddress    
            type: Property    
        streetNr:    
          description: Number identifying a specific property on a public street    
          type: string    
          x-ngsi:    
            type: Property    
      type: object    
      x-ngsi:    
        model: https://schema.org/address    
        type: Property    
    alternateName:    
      description: An alternative name for this item    
      type: string    
      x-ngsi:    
        type: Property    
    areaServed:    
      description: The geographic area where a service or offered item is provided    
      type: string    
      x-ngsi:    
        model: https://schema.org/Text    
        type: Property    
    completeness:    
      description: Completeness quantifies the number of missed measurements or observations in a given time window    
      maximum: 1    
      minimum: 0    
      type: number    
      x-ngsi:    
        type: Property    
        units: P1    
    dataProvider:    
      description: A sequence of characters identifying the provider of the harmonised data entity    
      type: string    
      x-ngsi:    
        type: Property    
    dateCalculated:    
      description: Date of the calculated entity defined by the user    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateCreated:    
      description: Entity creation timestamp. This will usually be allocated by the storage platform    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateModified:    
      description: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    description:    
      description: A description of this item    
      type: string    
      x-ngsi:    
        type: Property    
    duplicate:    
      description: Includes information about duplicated data    
      properties:    
        foundMatches:    
          description: 'If this is a duplicate, determine measurements it does match with'    
          items:    
            description: Every match found in the data    
            type: string    
            x-ngsi:    
              type: Property    
          type: array    
          x-ngsi:    
            type: Property    
        isDuplicate:    
          description: Determine whether the measurement is duplicated or not    
          type: boolean    
          x-ngsi:    
            type: Property    
      type: object    
      x-ngsi:    
        type: Property    
    id:    
      anyOf:    
        - description: Identifier format of any NGSI entity    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
          x-ngsi:    
            type: Property    
        - description: Identifier format of any NGSI entity    
          format: uri    
          type: string    
          x-ngsi:    
            type: Property    
      description: Unique identifier of the entity    
      x-ngsi:    
        type: Property    
    location:    
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'    
      oneOf:    
        - description: Geojson reference to the item. Point    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                type: number    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - Point    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON Point    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. LineString    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              minItems: 2    
              type: array    
            type:    
              enum:    
                - LineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON LineString    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. Polygon    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 4    
                type: array    
              type: array    
            type:    
              enum:    
                - Polygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON Polygon    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. MultiPoint    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  type: number    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPoint    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON MultiPoint    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. MultiLineString    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    type: number    
                  minItems: 2    
                  type: array    
                minItems: 2    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiLineString    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON MultiLineString    
          type: object    
          x-ngsi:    
            type: GeoProperty    
        - description: Geojson reference to the item. MultiLineString    
          properties:    
            bbox:    
              items:    
                type: number    
              minItems: 4    
              type: array    
            coordinates:    
              items:    
                items:    
                  items:    
                    items:    
                      type: number    
                    minItems: 2    
                    type: array    
                  minItems: 4    
                  type: array    
                type: array    
              type: array    
            type:    
              enum:    
                - MultiPolygon    
              type: string    
          required:    
            - type    
            - coordinates    
          title: GeoJSON MultiPolygon    
          type: object    
          x-ngsi:    
            type: GeoProperty    
      x-ngsi:    
        type: GeoProperty    
    name:    
      description: The name of this item    
      type: string    
      x-ngsi:    
        type: Property    
    outlier:    
      description: Includes information about the outlier characteristics of the measurement    
      properties:    
        isOutlier:    
          description: Determine whether the measurement has been considered an outlier or not    
          type: boolean    
          x-ngsi:    
            type: Property    
        methodology:    
          anyOf:    
            - description: Identifier format of any NGSI entity    
              maxLength: 256    
              minLength: 1    
              pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
              type: string    
              x-ngsi:    
                type: Property    
            - description: Identifier format of any NGSI entity    
              format: uri    
              type: string    
              x-ngsi:    
                type: Property    
          description: Reference to the other entity including AI methodology information    
          x-ngsi:    
            type: Relationship    
        outlierScore:    
          description: A score indicating the degree of outlierness    
          type: number    
          x-ngsi:    
            type: Property    
      type: object    
      x-ngsi:    
        type: Property    
    owner:    
      description: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)    
      items:    
        anyOf:    
          - description: Identifier format of any NGSI entity    
            maxLength: 256    
            minLength: 1    
            pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
            type: string    
            x-ngsi:    
              type: Property    
          - description: Identifier format of any NGSI entity    
            format: uri    
            type: string    
            x-ngsi:    
              type: Property    
        description: Unique identifier of the entity    
        x-ngsi:    
          type: Property    
      type: array    
      x-ngsi:    
        type: Property    
    precision:    
      description: 'Precision measures the standard deviation of a dataset. That is, it measures how close the values in the dataset are to each other'    
      type: number    
      x-ngsi:    
        type: Property    
    seeAlso:    
      description: list of uri pointing to additional resources about the item    
      oneOf:    
        - items:    
            format: uri    
            type: string    
          minItems: 1    
          type: array    
        - format: uri    
          type: string    
      x-ngsi:    
        type: Property    
    source:    
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object'    
      type: string    
      x-ngsi:    
        type: Property    
    synthetic:    
      description: Includes information about the origin of the measurement    
      properties:    
        isSynthetic:    
          description: Determine whether the measurement has been created synthetically or not    
          type: boolean    
          x-ngsi:    
            type: Property    
        methodology:    
          anyOf:    
            - description: Identifier format of any NGSI entity    
              maxLength: 256    
              minLength: 1    
              pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
              type: string    
              x-ngsi:    
                type: Property    
            - description: Identifier format of any NGSI entity    
              format: uri    
              type: string    
              x-ngsi:    
                type: Property    
          description: Reference to the other entity including AI methodology information    
          x-ngsi:    
            type: Relationship    
      type: object    
      x-ngsi:    
        type: Property    
    timeliness:    
      description: Average timeliness of the data-stream    
      type: number    
      x-ngsi:    
        type: Property    
        units: minutes    
    type:    
      description: NGSI Entity type. It has to be DataQualityAssessment    
      enum:    
        - DataQualityAssessment    
      type: string    
      x-ngsi:    
        type: Property    
  required:    
    - id    
    - type    
  type: object    
  x-derived-from: ""    
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2024 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.DataQuality/blob/master/DataQualityAssessment/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.DataQuality/DataQualityAssessment/schema.json    
  x-model-tags: ""    
  x-version: 0.0.4    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## 有效载荷示例  
#### 数据质量评估 NGSI-v2 关键值 示例  
下面是一个以 JSON-LD 格式作为键值的 DataQualityAssessment 示例。当使用 `options=keyValues` 时，它与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3058",  
  "type": "DataQualityAssessment",  
  "dateCalculated": "2022-09-10T10:01:20Z",  
  "source": "https://salted-project.eu",  
  "outlier": {  
    "isOutlier": true,  
    "outlierScore": 0.7,  
    "methodology": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
  },  
   "duplicate": {  
    "isDuplicate": true,  
    "foundMatches": ["urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3062"  
    ]  
  },  
  "synthetic": {  
    "isSynthetic": false,  
    "methodology": "urn:ngsi-ld:AI-Methodology:Synthetic:Temperature:smartsantander:u7jcfa:f3058"  
  },  
  "accuracy": 0.25,  
  "timeliness": 3,  
  "precision": 1.3,  
  "completeness": 0.5  
}  
```  
</details>  
#### 数据质量评估 NGSI-v2 标准化示例  
下面是一个规范化 JSON-LD 格式的 DataQualityAssessment 示例。当不使用选项时，它与 NGSI-v2 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3058",  
  "type": "DataQualityAssessment",  
  "dateCalculated": {  
    "type": "DateTime",  
    "value": "2022-09-10T10:01:20Z"  
  },  
  "source": {  
    "type": "Text",  
    "value": "https://salted-project.eu"  
  },  
  "outlier": {  
    "type": "StructuredValue",  
    "value": {  
      "isOutlier": true,  
      "outlierScore": 0.7,  
      "methodology": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
    }  
  },  
  "duplicate": {  
    "type": "StructuredValue",  
    "value": {  
      "isDuplicate": true,  
      "foundMatches": ["urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3062"]  
    }  
  },  
  "synthetic": {  
    "type": "StructuredValue",  
    "value": {  
      "isSynthetic": false,  
      "methodology": "urn:ngsi-ld:AI-Methodology:Synthetic:Temperature:smartsantander:u7jcfa:f3058"  
    }  
  },  
  "precision": {  
    "type": "Number",  
    "value": 1.3  
  },  
  "accuracy": {  
    "type": "Number",  
    "value": 0.25  
  },  
  "timeliness": {  
    "type": "Number",  
    "value": 3  
  },  
  "completeness": {  
    "type": "Number",  
    "value": 0.5  
  }  
}  
```  
</details>  
#### 数据质量评估 NGSI-LD 关键值 示例  
下面是一个以 JSON-LD 格式作为键值的 DataQualityAssessment 示例。当使用 `options=keyValues` 时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3058",  
  "type": "DataQualityAssessment",  
  "dateCalculated": "2022-09-10T10:01:20Z",  
  "source": "https://salted-project.eu",  
  "outlier": {  
    "isOutlier": true,  
    "outlierScore": 0.7,  
    "methodology": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
  },  
  "duplicate": {  
    "isDuplicate": true,  
    "foundMatches": ["urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3062"  
    ]  
  },  
  "synthetic": {  
    "isSynthetic": false,  
    "methodology": "urn:ngsi-ld:AI-Methodology:Synthetic:Temperature:smartsantander:u7jcfa:f3058"  
  },  
  "accuracy": 0.25,  
  "timeliness": 3,  
  "precision": 1.3,  
  "completeness": 0.5,  
  "@context": [  
    "https://raw.githubusercontent.com/smart-data-models/dataModel.DataQuality/master/context.jsonld",  
    "https://smartdatamodels.org/context.jsonld"  
  ]  
}  
```  
</details>  
#### 数据质量评估 NGSI-LD 标准化示例  
下面是一个规范化 JSON-LD 格式的 DataQualityAssessment 示例。在不使用选项时，它与 NGSI-LD 兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3058",  
  "type": "DataQualityAssessment",  
  "dateCalculated": {  
    "type": "Property",  
    "value": {  
      "@type": "DateTime",  
      "@value": "2022-09-10T10:01:20Z"  
    }  
  },  
  "source": {  
    "type": "Property",  
    "value": "https://salted-project.eu"  
  },  
  "outlier": {  
    "type": "Property",  
    "value": {  
      "isOutlier": {  
        "type": "Property",  
        "value": true  
      },  
      "outlierScore": {  
        "type": "Property",  
        "value": 0.7  
      },  
      "methodology": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
      }  
    },  
    "observedAt": "2022-09-10T10:01:20Z"  
  },  
  "duplicate": {  
    "type": "Property",  
    "value": {  
      "isDuplicate": {  
        "type": "Property",  
        "value": true  
      },  
      "foundMatches": {  
        "type": "Property",  
        "value": ["urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3062"  
      ]  
      }  
    }  
  },  
  "synthetic": {  
    "type": "Property",  
    "value": {  
      "isSynthetic": {  
        "type": "Property",  
        "value": false  
    },  
    "methodology": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:AI-Methodology:Synthetic:Temperature:smartsantander:u7jcfa:f3058"  
      }  
    },  
    "observedAt": "2022-09-10T10:01:20Z"  
  },  
  "accuracy": {  
    "type": "Property",  
    "value": 0.25,  
    "observedAt": "2022-09-10T10:01:20Z",  
    "unitCode": "CEL"  
  },  
  "timeliness": {  
    "type": "Property",  
    "value": 3,  
    "observedAt": "2022-09-10T10:01:20Z",  
    "unitCode": "minutes"  
  },  
  "precision": {  
    "type": "Property",  
    "value": 1.3,  
    "observedAt": "2022-09-10T10:01:20Z",  
    "unitCode": "CEL"  
  },  
  "completeness": {  
    "type": "Property",  
    "value": 0.5,  
    "observedAt": "2022-09-10T10:01:20Z",  
    "unitCode": "P1"  
  },  
  "@context": [  
      "https://raw.githubusercontent.com/smart-data-models/dataModel.DataQuality/master/context.jsonld",  
      "https://smartdatamodels.org/context.jsonld"  
  ]  
}  
```  
</details><!-- /80-Examples -->  
<!-- 90-FooterNotes -->  
<!-- /90-FooterNotes -->  
<!-- 95-Units -->  
请参阅 [FAQ 10](https://smartdatamodels.org/index.php/faqs/)，获取如何处理幅度单位的答案。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
