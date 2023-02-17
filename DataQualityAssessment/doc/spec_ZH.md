<!-- 10-Header -->  
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)  
实体。数据质量评估（DataQualityAssessment  
===============================<!-- /10-Header -->  
<!-- 15-License -->  
[开放许可](https://github.com/smart-data-models//dataModel.DataQuality/blob/master/DataQualityAssessment/LICENSE.md)  
[文件自动生成](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)  
<!-- /15-License -->  
<!-- 20-Description -->  
全局描述。**该实体描述了测量的数据质量属性，如温度。  
版本：0.0.1  
<!-- /20-Description -->  
<!-- 30-PropertiesList -->  

##属性列表  

<sup><sub>[*] 如果一个属性中没有一个类型，是因为它可能有几种类型或不同的格式/模式</sub></sup>。  
- `accuracy[number]`: 准确度衡量传感器测量中产生的最大系统数字误差。  - `address[object]`: 邮寄地址  . Model: [https://schema.org/address](https://schema.org/address)- `alternateName[string]`: 这个项目的一个替代名称  - `areaServed[string]`: 提供服务或提供项目的地理区域  . Model: [https://schema.org/Text](https://schema.org/Text)- `completeness[number]`: 完整性量化了特定时间窗口内遗漏的测量或观测的数量  - `dataProvider[string]`: 一串识别统一数据实体提供者的字符。  - `dateCalculated[string]`: 由用户定义的计算实体的日期。  - `dateCreated[string]`: 实体创建时间戳。这通常会由存储平台分配。  - `dateModified[string]`: 实体最后一次修改的时间戳。这通常会由存储平台分配。  - `description[string]`: 对这个项目的描述  - `id[*]`: 实体的唯一标识符  - `location[*]`: 对该项目的Geojson引用。它可以是点、线字符串、多边形、多点、多线字符串或多多边形。  - `name[string]`: 这个项目的名称。  - `outlier[object]`: 包括关于测量的离群特性的信息。  - `owner[array]`: 一个包含JSON编码的字符序列的列表，引用所有者的唯一Ids。  - `precision[number]`: 精度衡量一个数据集的标准偏差。也就是说，它衡量的是数据集中的数值彼此之间的接近程度。  - `seeAlso[*]`: 指向有关该项目的其他资源的URI列表  - `source[string]`: 提供实体数据原始来源的一连串字符，作为一个URL。建议为源提供者的完全合格域名，或源对象的URL。  - `synthetic[object]`: 包括关于测量的来源的信息。  - `timeliness[number]`: 数据流的平均时效性  - `type[string]`: NGSI实体类型。它必须是DataQualityAssessment。  <!-- /30-PropertiesList -->  
<!-- 35-RequiredProperties -->  
所需属性  
- `id`  - `type`  <!-- /35-RequiredProperties -->  
<!-- 40-RequiredProperties -->  
<!-- /40-RequiredProperties -->  
<!-- 50-DataModelHeader -->  
## 数据模型的属性描述  
按字母顺序排列（点击查看详情）。  
<!-- /50-DataModelHeader -->  
<!-- 60-ModelYaml -->  
<details><summary><strong>full yaml details</strong></summary>    
```yaml  
DataQualityAssessment:    
  description: 'This entity describes the data quality properties of a measurement, such as temperature.'    
  properties:    
    accuracy:    
      description: Accuracy measures the maximum systematic numerical error produced in a sensor measurement.    
      type: number    
      x-ngsi:    
        type: Property    
    address:    
      description: The mailing address    
      properties:    
        addressCountry:    
          description: 'Property. The country. For example, Spain. Model:''https://schema.org/addressCountry'''    
          type: string    
        addressLocality:    
          description: 'Property. The locality in which the street address is, and which is in the region. Model:''https://schema.org/addressLocality'''    
          type: string    
        addressRegion:    
          description: 'Property. The region in which the locality is, and which is in the country. Model:''https://schema.org/addressRegion'''    
          type: string    
        district:    
          description: 'A district is a type of administrative division that, in some countries, is managed by the local government.'    
          type: string    
        postOfficeBoxNumber:    
          description: 'Property. The post office box number for PO box addresses. For example, 03578. Model:''https://schema.org/postOfficeBoxNumber'''    
          type: string    
        postalCode:    
          description: 'Property. The postal code. For example, 24004. Model:''https://schema.org/https://schema.org/postalCode'''    
          type: string    
        streetAddress:    
          description: 'Property. The street address. Model:''https://schema.org/streetAddress'''    
          type: string    
        streetNr:    
          description: Number identifying a specific property on a public street.    
          type: string    
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
        units: P1.    
    dataProvider:    
      description: A sequence of characters identifying the provider of the harmonised data entity.    
      type: string    
      x-ngsi:    
        type: Property    
    dateCalculated:    
      description: Date of the calculated entity defined by the user.    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateCreated:    
      description: Entity creation timestamp. This will usually be allocated by the storage platform.    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    dateModified:    
      description: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform.    
      format: date-time    
      type: string    
      x-ngsi:    
        type: Property    
    description:    
      description: A description of this item    
      type: string    
      x-ngsi:    
        type: Property    
    id:    
      anyOf: &dataqualityassessment_-_properties_-_owner_-_items_-_anyof    
        - description: Property. Identifier format of any NGSI entity    
          maxLength: 256    
          minLength: 1    
          pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
          type: string    
        - description: Property. Identifier format of any NGSI entity    
          format: uri    
          type: string    
      description: Unique identifier of the entity    
      x-ngsi:    
        type: Property    
    location:    
      description: 'Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon'    
      oneOf:    
        - description: Geoproperty. Geojson reference to the item. Point    
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
        - description: Geoproperty. Geojson reference to the item. LineString    
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
        - description: Geoproperty. Geojson reference to the item. Polygon    
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
        - description: Geoproperty. Geojson reference to the item. MultiPoint    
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
        - description: Geoproperty. Geojson reference to the item. MultiLineString    
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
        - description: Geoproperty. Geojson reference to the item. MultiLineString    
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
        type: Geoproperty    
    name:    
      description: The name of this item.    
      type: string    
      x-ngsi:    
        type: Property    
    outlier:    
      description: Includes information about the outlier characteristics of the measurement.    
      properties:    
        isOutlier:    
          description: Property. Determine whether the measurement has been considered an outlier or not.    
          type: boolean    
        methodology:    
          anyOf:    
            - description: Property. Identifier format of any NGSI entity    
              maxLength: 256    
              minLength: 1    
              pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
              type: string    
            - description: Property. Identifier format of any NGSI entity    
              format: uri    
              type: string    
          description: Relationship. Reference to the other entity including AI methodology information.    
      type: object    
      x-ngsi:    
        type: Property    
    owner:    
      description: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)    
      items:    
        anyOf: *dataqualityassessment_-_properties_-_owner_-_items_-_anyof    
        description: Property. Unique identifier of the entity    
      type: array    
      x-ngsi:    
        type: Property    
    precision:    
      description: 'Precision measures the standard deviation of a dataset. That is, it measures how close the values in the dataset are to each other.'    
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
      description: 'A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object.'    
      type: string    
      x-ngsi:    
        type: Property    
    synthetic:    
      description: Includes information about the origin of the measurement.    
      properties:    
        isSynthetic:    
          description: Property. Determine whether the measurement has been created synthetically or not.    
          type: boolean    
        methodology:    
          anyOf:    
            - description: Property. Identifier format of any NGSI entity    
              maxLength: 256    
              minLength: 1    
              pattern: ^[\w\-\.\{\}\$\+\*\[\]`|~^@!,:\\]+$    
              type: string    
            - description: Property. Identifier format of any NGSI entity    
              format: uri    
              type: string    
          description: Relationship. Reference to the other entity including AI methodology information.    
      type: object    
      x-ngsi:    
        type: Property    
    timeliness:    
      description: Average timeliness of the data-stream    
      type: number    
      x-ngsi:    
        type: Property    
        units: minutes.    
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
  x-disclaimer: 'Redistribution and use in source and binary forms, with or without modification, are permitted  provided that the license conditions are met. Copyleft (c) 2022 Contributors to Smart Data Models Program'    
  x-license-url: https://github.com/smart-data-models/dataModel.DataQuality/blob/master/DataQualityAssessment/LICENSE.md    
  x-model-schema: https://smart-data-models.github.io/dataModel.DataQuality/DataQualityAssessment/schema.json    
  x-model-tags: ""    
  x-version: 0.0.2    
```  
</details>    
<!-- /60-ModelYaml -->  
<!-- 70-MiddleNotes -->  
<!-- /70-MiddleNotes -->  
<!-- 80-Examples -->  
## ＃＃＃＃有效载荷的例子  
#### DataQualityAssessment NGSI-v2 key-values 示例  
下面是一个以JSON-LD格式作为key-values的DataQualityAssessment的例子。当使用`options=keyValues`时，这与NGSI-v2兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3058",  
  "type": "DataQualityAssessment",  
  "dateCalculated": "2022-09-10T10:01:20Z",  
  "source": "https://salted-project.eu",  
  "outlier":{  
    "isOutlier": true,  
    "methodology": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
  },       
  "synthetic":{  
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
#### DataQualityAssessment NGSI-v2规范化示例  
下面是一个以JSON-LD格式规范化的DataQualityAssessment的例子。当不使用选项时，这与NGSI-v2兼容，并返回单个实体的上下文数据。  
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
      "isOutlier": {  
        "type": "Boolean",  
        "value": true  
      },  
      "methodology": {  
        "type": "Text",  
        "value": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
      }  
    }  
  },  
  "synthetic": {  
    "type": "StructuredValue",  
    "value": {  
      "isSynthetic": {  
        "type": "Boolean",  
        "value": false  
      },  
      "methodology": {  
        "type": "Text",  
        "value": "urn:ngsi-ld:AI-Methodology:Synthetic:Temperature:smartsantander:u7jcfa:f3058"  
      }  
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
#### DataQualityAssessment NGSI-LD key-values 示例  
这里是一个以JSON-LD格式作为key-values的DataQualityAssessment的例子。当使用`options=keyValues`时，这与NGSI-LD兼容，并返回单个实体的上下文数据。  
<details><summary><strong>show/hide example</strong></summary>    
```json  
{  
  "id": "urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3058",  
  "type": "DataQualityAssessment",  
  "dateCalculated": {  
    "@type": "DateTime",  
    "@value": "2022-09-10T10:01:20Z"  
  },  
  "source": "https://salted-project.eu",  
  "outlier":{  
    "isOutlier": true,  
    "methodology": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
  },       
  "synthetic":{  
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
#### DataQualityAssessment NGSI-LD规范化示例  
下面是一个以JSON-LD格式规范化的DataQualityAssessment的例子。当不使用选项时，这与NGSI-LD兼容，并返回单个实体的上下文数据。  
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
      "methodology": {  
        "type": "Relationship",  
        "object": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
      }  
    },  
    "observedAt": "2022-09-10T10:01:20Z"  
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
参见[常见问题10](https://smartdatamodels.org/index.php/faqs/)，以获得关于如何处理量级单位的答案。  
<!-- /95-Units -->  
<!-- 97-LastFooter -->  
---  
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->  
