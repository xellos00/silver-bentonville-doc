---
description:  
---
# Manager

>  **Package : pilot.manager**

## NodeManager

{% hint style="info" %}
**NodeManager Methods:**

{%  endhint %}


| NO |  Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [**Init**](manager.md#Init)|   [InitRequest](manager.md#initrequest) |   [InitResponse](manager.md#initresponse) |  |
| 2 | [**Verify**](manager.md#Verify)|   [VerifyRequest](manager.md#verifyrequest) |   [VerifyInfo](manager.md#verifyinfo) |  |
| 3 | [**End**](manager.md#End)|   [EndRequest](manager.md#endrequest) |   [EndResponse](manager.md#endresponse) |  |
| 4 | [**Execute**](manager.md#Execute)|   [ExecuteRequest](manager.md#executerequest) |   [ExecuteResponse](manager.md#executeresponse) |  |
| 5 | [**UpdateConfig**](manager.md#UpdateConfig)|   [UpdateRequest](manager.md#updaterequest) |   [UpdateResponse](manager.md#updateresponse) |  | 
 

 
### Init


| Type | Message |
| :--- | :--- |
| Request | [InitRequest](manager.md#initrequest) |
| Response |  [InitResponse](manager.md#initresponse)  |
 
 

 
### Verify


| Type | Message |
| :--- | :--- |
| Request | [VerifyRequest](manager.md#verifyrequest) |
| Response |  [VerifyInfo](manager.md#verifyinfo)  |
 
 

 
### End


| Type | Message |
| :--- | :--- |
| Request | [EndRequest](manager.md#endrequest) |
| Response |  [EndResponse](manager.md#endresponse)  |
 
 

 
### Execute


| Type | Message |
| :--- | :--- |
| Request | [ExecuteRequest](manager.md#executerequest) |
| Response |  [ExecuteResponse](manager.md#executeresponse)  |
 
 

 
### UpdateConfig


| Type | Message |
| :--- | :--- |
| Request | [UpdateRequest](manager.md#updaterequest) |
| Response |  [UpdateResponse](manager.md#updateresponse)  |


## 

## Message

### EndRequest
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | metadata |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |

### EndResponse
<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">result</td>
      <td style="text-align:left"><ul>
          	<li>SUCCESS</li>
          	<li>FAIL</li>
        </ul></td>
<td style="text-align:left"></td>

   </tr>
  </tbody>
</table>



### ExecuteRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :---: | :--- |
| 1 | target_info |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|✅| |
| 2 | command |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|✅| |

### ExecuteResponse
<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">state</td>
      <td style="text-align:left"><ul>
          	<li>NONE</li>
          	<li>PENDING</li>
          	<li>INPROGRESS</li>
          	<li>SUCCESS</li>
          	<li>FAILURE</li>
          	<li>TIMEOUT</li>
        </ul></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">message</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">3</td>
      <td style="text-align:left">protocol</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">4</td>
      <td style="text-align:left">options</td>
      <td style="text-align:left"><a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a></td>
<td style="text-align:left"></td>

   </tr>
  </tbody>
</table>



### InitRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :---: | :--- |
| 1 | options |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|✅| |

### InitResponse
<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">result</td>
      <td style="text-align:left"><ul>
          	<li>SUCCESS</li>
          	<li>FAIL</li>
        </ul></td>
<td style="text-align:left"></td>

   </tr>
    <tr>
      <td style="text-align:left">2</td>
      <td style="text-align:left">metadata</td>
      <td style="text-align:left"><a href="https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto">google.protobuf.Struct</a></td>
<td style="text-align:left"></td>

   </tr>
  </tbody>
</table>



### UpdateRequest
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |

### UpdateResponse
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |

### VerifyInfo
<table>
  <thead>
    <tr>
      <th style="text-align:left">No</th>
      <th style="text-align:left">Field</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">1</td>
      <td style="text-align:left">result</td>
      <td style="text-align:left"><ul>
          	<li>SUCCESS</li>
          	<li>FAIL</li>
        </ul></td>
<td style="text-align:left"></td>

   </tr>
  </tbody>
</table>



### VerifyRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :---: | :--- |
| 1 | options |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|✅| |
