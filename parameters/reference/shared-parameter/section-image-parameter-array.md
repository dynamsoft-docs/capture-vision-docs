
## SectionImageParameterArray

`SectionImageParameterArray` is the parameter for you to set the image processing algorithms that implemented in the task. Each member of the array defines an algorithm section as well as its image processing parameters.

<table style = "text-align:left">
    <tr>
        <th>Child Parameter Name</th>
        <th>Child Parameter Summary</th>
    </tr>
    <tr>
        <td rowspan = "3" style="vertical-align:text-top">Section<br></td>
        <td><b>Description</b><br>Specifies an algorithm section.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
    <tr>
        <td><b>Range</b><br>One of the <a href="#">SectionType</a> that available for the task.
        </td>
    </tr>
    <tr>
        <td rowspan = "2" style="vertical-align:text-top">ImageParameterName<br></td>
        <td><b>Description</b><br>Specifies a mode for ordering.
        </td>
    </tr>
    <tr>
        <td><b>Type</b><br><i>String</i>
        </td>
    </tr>
</table>

BarcodeReaderTaskSetting
LabelRecognizerTaskSetting
DocumentNormalizerTaskSetting
