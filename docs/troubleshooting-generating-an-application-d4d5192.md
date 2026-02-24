<!-- loiod4d5192a517348a097c5907c795f5a49 -->

# Troubleshooting: Generating an Application

Learn how to solve the most common errors when generating an application with the Project Accelerator.

**RAP Accelerator**


<table>
<tr>
<th valign="top">

**Error**

</th>
<th valign="top">

**Cause**

</th>
<th valign="top">

**Solution**

</th>
</tr>
<tr>
<td valign="top">

You are not authorized to make changes \(authorization object `S_DEVELOP`\)

</td>
<td valign="top">

Invalid permissions. You must have the `S_DEVELOP` authorization to perform operations on an ABAP back-end system.

</td>
<td valign="top">

Acquire the `S_Develop` authorization.

</td>
</tr>
<tr>
<td valign="top">

Error calling ADT service for OData service creation: *AxiosError: Request failed with status code 504* 

</td>
<td valign="top">

Generation exceeded the configured timeout period. HTTP 504 typically indicates a timeout issue.

</td>
<td valign="top">

Increase the `HTML5.Timeout` value in the SAP BTP destination configuration.

</td>
</tr>
<tr>
<td valign="top">

An error occurred while working on your request. Details: Error reading metadata for `https://host/sap/opu/odata/`... AxiosError: Request failed with status code 404

</td>
<td valign="top">

The metadata cannot be retrieved from the back-end system.

</td>
<td valign="top">

Retry generation.

</td>
</tr>
<tr>
<td valign="top">

Error while starting application preview. Details: AggregateError

</td>
<td valign="top">

The SAP BTP destination URL ends with a trailing slash \(/\).

</td>
<td valign="top">

Remove the trailing slash from the destination URL configuration.

</td>
</tr>
</table>

