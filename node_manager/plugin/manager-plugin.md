---
description:  
---
# Manager plugin

>  **Package : pilot.plugin**

## ManagerPlugin

{% hint style="info" %}
**ManagerPlugin Methods:**

{%  endhint %}


| NO |  Method | Request Type | Response Type | Description |
| :--- | :--- | :--- | :--- | :--- |
| 1 | [**init**](manager-plugin.md#init)| [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto)|   [PluginInfo](manager-plugin.md#plugininfo) |  |
| 2 | [**verify**](manager-plugin.md#verify)| [google.protobuf.Empty](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/empty.proto)|   [VerifyInfo](manager-plugin.md#verifyinfo) |  |
| 3 | [**execute**](manager-plugin.md#execute)|   [ExecuteRequest](manager-plugin.md#executerequest) |   [ExecuteResponse](manager-plugin.md#executeresponse) |  | 
 

 
### init


| Type | Message |
| :--- | :--- |
| Request | [Empty] |
| Response |  [PluginInfo](manager-plugin.md#plugininfo)  |
 
 

 
### verify


| Type | Message |
| :--- | :--- |
| Request | [Empty] |
| Response |  [VerifyInfo](manager-plugin.md#verifyinfo)  |
 
 

 
### execute


| Type | Message |
| :--- | :--- |
| Request | [ExecuteRequest](manager-plugin.md#executerequest) |
| Response |  [ExecuteResponse](manager-plugin.md#executeresponse)  |


## 

## Message

### CollectorVerifyInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | options |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |

### ExecuteRequest
| No | Field | Type | Required | Description |
| :--- | :--- | :--- | :---: | :--- |
| 1 | execute_info |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|✅| |
| 2 | options |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto)|✅| |

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
      <td style="text-align:left">resource_type</td>
      <td style="text-align:left">string</td>
<td style="text-align:left"></td>

   </tr>
  </tbody>
</table>



### PluginInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | metadata |[google.protobuf.Struct](https://github.com/protocolbuffers/protobuf/blob/master/src/google/protobuf/struct.proto) | |

### VerifyInfo
| No | Field | Type |  Description |
| :--- | :--- | :--- | :--- |
| 1 | verify_msg |string | |
