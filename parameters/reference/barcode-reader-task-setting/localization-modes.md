
# LocalizationModes

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Details</th>
    </tr>
    <tr>
        <td rowspan = "4" style="vertical-align:text-top">Mode<br>(Required)</td>
        <td><b>Description</b><br>Any one in Candidate Mode List as string
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Candidate Mode List</b><br>
            <li>LM_CONNECTED_BLOCKS</li>
            <li>LM_STATISTICS</li>
            <li>LM_LINES</li>
            <li>LM_SCAN_DIRECTLY</li>
            <li>LM_STATISTICS_MARKS</li>
            <li>LM_STATISTICS_POSTAL_CODE</li>
            <li>LM_CENTRE</li>
            <li>LM_ONED_FAST_SCAN</li>
            <li>LM_SKIP</li>
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ScanStride<br>(Optional)</td>
        <td><b>Description</b><br>Sets the stride in pixels between scans when searching for barcodes.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,0x7fffffff]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>LM_SCAN_DIRECTLY</li>
            <li>LM_ONED_FAST_SCAN</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ScanDirection<br>(Optional)</td>
        <td><b>Description</b><br>Sets the scan direction when searching barcode.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,2]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>LM_SCAN_DIRECTLY</li>
            <li>LM_ONED_FAST_SCAN</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">ConfidenceThreshold<br>(Optional)</td>
        <td><b>Description</b><br>Sets the confidence threshold.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0,100]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>60
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>LM_ONED_FAST_SCAN</li>
        </td>
    </tr>
    <tr>
        <td rowspan = "5" style="vertical-align:text-top">IsOneDStacked<br>(Optional)</td>
        <td><b>Description</b><br>Sets whether the oned barcodes are stacked.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>int</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>[0, 1]
        </td>
    </tr>
    <tr>
        <td><b>Default Value</b><br>0
        </td>
    </tr>
    <tr>
        <td><b>Valid For</b><br>
            <li>LM_SCAN_DIRECTLY</li>
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
