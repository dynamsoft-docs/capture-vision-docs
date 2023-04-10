
## BarcodeColourModes

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Details</th>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Specifies a target barcode colour mode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>
            <li>BICM_DARK_ON_LIGHT</li>
            <li>BICM_LIGHT_ON_DARK</li>
            <li>BICM_DARK_ON_DARK</li>
            <li>BICM_LIGHT_ON_LIGHT</li>
            <li>BICM_DARK_LIGHT_MIXED</li>
            <li>BICM_DARK_ON_LIGHT_DARK_SURROUNDING</li>
            <li>BICM_SKIP</li>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>BICM_DARK_ON_LIGHT
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LightReflection<br>(Optional)</td>
        <td><b>Description</b><br>A number from value range of LightReflection.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,1]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>1
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>
            <li>0: no light reflection.</li>
            <li>1: has light reflection.</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LibraryFileName<br>(Optional)</td>
        <td><b>Description</b><br>Sets the file name of the library to load dynamically.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing file name.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes.
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">LibraryParameters<br>(Optional)</td>
        <td><b>Description</b><br>The library must be in the same place with Dynamsoft Barcode Reader Library.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>A string value representing parameters.
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>""
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>All modes.
        </td>
    </tr>
</table>
