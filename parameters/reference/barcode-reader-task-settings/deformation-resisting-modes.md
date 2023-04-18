
## DeformationResistingModes

<table style = "text-align:left">
    <thead>
        <tr>
            <th nowrap="nowrap">Child Parameter Name</th>
            <th nowrap="nowrap">Child Parameter Summary</th>
        </tr>
    </thead>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Specifies a mode for deformation resisting.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>DRM_GENERAL
            <br>DRM_BROAD_WARP
            <br>DRM_LOCAL_REFERENCE
            <br>DRM_DEWRINKLE
            <br>DRM_AUTO
            <br>DRM_SKIP
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        </td>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Level<br>(Optional)</td>
        <td><b>Description</b><br>Sets the Argument Level.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[1,9]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>5
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">GrayscaleEnhancementMode<br>(Optional)</td>
        <td><b>Description</b><br>Sets the Argument GrayscaleEnhancementMode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>GrayScaleEnhancementMode object</i>
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>View <a href="../image-parameter/grayscale-enhancement-modes.md">GrayScaleEnhancementModes</a> page for how to set this mode.
        </td>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">BinarizationMode<br>(Optional)</td>
        <td><b>Description</b><br>Sets the Argument BinarizationMode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>BinarizationMode object</i>
        </td>
    </tr>
    <tr>
        <td><b>Remarks</b><br>View <a href="../image-parameter/binarization-modes.md">BinarizationMode</a> page for how to set this parameter.
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
