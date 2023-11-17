<!-- 10-Header -->    
[![Smart Data Models](https://smartdatamodels.org/wp-content/uploads/2022/01/SmartDataModels_logo.png "Logo")](https://smartdatamodels.org)    
Entity: DataQualityAssessment    
=============================<!-- /10-Header -->    
<!-- 15-License -->    
[Open License](https://github.com/smart-data-models//dataModel.DataQuality/blob/master/DataQualityAssessment/LICENSE.md)    
[document generated automatically](https://docs.google.com/presentation/d/e/2PACX-1vTs-Ng5dIAwkg91oTTUdt8ua7woBXhPnwavZ0FxgR8BsAI_Ek3C5q97Nd94HS8KhP-r_quD4H0fgyt3/pub?start=false&loop=false&delayms=3000#slide=id.gb715ace035_0_60)    
<!-- /15-License -->    
<!-- 20-Description -->    
Global description: **This entity describes the data quality properties of a measurement, such as temperature.**    
version: 0.0.2    
<!-- /20-Description -->    
<!-- 30-PropertiesList -->    
## List of properties    
<sup><sub>[*] If there is not a type in an attribute is because it could have several types or different formats/patterns</sub></sup>    
- `accuracy[number]`: Accuracy measures the maximum systematic numerical error produced in a sensor measurement  - `address[object]`: The mailing address  . Model: [https://schema.org/address](https://schema.org/address)	- `addressCountry[string]`: The country. For example, Spain  . Model: [https://schema.org/addressCountry](https://schema.org/addressCountry)    
	- `addressLocality[string]`: The locality in which the street address is, and which is in the region  . Model: [https://schema.org/addressLocality](https://schema.org/addressLocality)    
	- `addressRegion[string]`: The region in which the locality is, and which is in the country  . Model: [https://schema.org/addressRegion](https://schema.org/addressRegion)    
	- `district[string]`: A district is a type of administrative division that, in some countries, is managed by the local government      
	- `postOfficeBoxNumber[string]`: The post office box number for PO box addresses. For example, 03578  . Model: [https://schema.org/postOfficeBoxNumber](https://schema.org/postOfficeBoxNumber)    
	- `postalCode[string]`: The postal code. For example, 24004  . Model: [https://schema.org/https://schema.org/postalCode](https://schema.org/https://schema.org/postalCode)    
	- `streetAddress[string]`: The street address  . Model: [https://schema.org/streetAddress](https://schema.org/streetAddress)    
- `alternateName[string]`: An alternative name for this item  - `areaServed[string]`: The geographic area where a service or offered item is provided  . Model: [https://schema.org/Text](https://schema.org/Text)- `completeness[number]`: Completeness quantifies the number of missed measurements or observations in a given time window  - `dataProvider[string]`: A sequence of characters identifying the provider of the harmonised data entity  - `dateCalculated[date-time]`: Date of the calculated entity defined by the user  - `dateCreated[date-time]`: Entity creation timestamp. This will usually be allocated by the storage platform  - `dateModified[date-time]`: Timestamp of the last modification of the entity. This will usually be allocated by the storage platform  - `description[string]`: A description of this item  - `id[*]`: Unique identifier of the entity  - `location[*]`: Geojson reference to the item. It can be Point, LineString, Polygon, MultiPoint, MultiLineString or MultiPolygon  - `name[string]`: The name of this item  - `outlier[object]`: Includes information about the outlier characteristics of the measurement  	- `isOutlier[boolean]`: Determine whether the measurement has been considered an outlier or not      
- `owner[array]`: A List containing a JSON encoded sequence of characters referencing the unique Ids of the owner(s)  - `precision[number]`: Precision measures the standard deviation of a dataset. That is, it measures how close the values in the dataset are to each other  - `seeAlso[*]`: list of uri pointing to additional resources about the item  - `source[string]`: A sequence of characters giving the original source of the entity data as a URL. Recommended to be the fully qualified domain name of the source provider, or the URL to the source object  - `synthetic[object]`: Includes information about the origin of the measurement  	- `isSynthetic[boolean]`: Determine whether the measurement has been created synthetically or not      
- `timeliness[number]`: Average timeliness of the data-stream  - `type[string]`: NGSI Entity type. It has to be DataQualityAssessment  <!-- /30-PropertiesList -->    
<!-- 35-RequiredProperties -->    
Required properties    
- `id`  - `type`  <!-- /35-RequiredProperties -->    
<!-- 40-RequiredProperties -->    
<!-- /40-RequiredProperties -->    
<!-- 50-DataModelHeader -->    
## Data Model description of properties    
Sorted alphabetically (click for details)    
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
## Example payloads      
#### DataQualityAssessment NGSI-v2 key-values Example      
Here is an example of a DataQualityAssessment in JSON-LD format as key-values. This is compatible with NGSI-v2 when  using `options=keyValues` and returns the context data of an individual entity.    
<details><summary><strong>show/hide example</strong></summary>      
```json  
{  
  "id": "urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3058",  
  "type": "DataQualityAssessment",  
  "dateCalculated": "2022-09-10T10:01:20Z",  
  "source": "https://salted-project.eu",  
  "outlier": {  
    "isOutlier": true,  
    "methodology": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
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
#### DataQualityAssessment NGSI-v2 normalized Example      
Here is an example of a DataQualityAssessment in JSON-LD format as normalized. This is compatible with NGSI-v2 when not using options and returns the context data of an individual entity.    
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
      "methodology": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
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
#### DataQualityAssessment NGSI-LD key-values Example      
Here is an example of a DataQualityAssessment in JSON-LD format as key-values. This is compatible with NGSI-LD when  using `options=keyValues` and returns the context data of an individual entity.    
<details><summary><strong>show/hide example</strong></summary>      
```json  
{  
  "id": "urn:ngsi-ld:DataQualityAssessment:Temperature:smartsantander:u7jcfa:f3058",  
  "type": "DataQualityAssessment",  
  "dateCalculated": "2022-09-10T10:01:20Z",  
  "source": "https://salted-project.eu",  
  "outlier": {  
    "isOutlier": true,  
    "methodology": "urn:ngsi-ld:AI-Methodology:Outlier:Temperature:smartsantander:u7jcfa:f3058"  
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
#### DataQualityAssessment NGSI-LD normalized Example      
Here is an example of a DataQualityAssessment in JSON-LD format as normalized. This is compatible with NGSI-LD when not using options and returns the context data of an individual entity.    
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
See [FAQ 10](https://smartdatamodels.org/index.php/faqs/) to get an answer on how to deal with magnitude units    
<!-- /95-Units -->    
<!-- 97-LastFooter -->    
---    
[Smart Data Models](https://smartdatamodels.org) +++ [Contribution Manual](https://bit.ly/contribution_manual) +++ [About](https://bit.ly/Introduction_SDM)<!-- /97-LastFooter -->    
