---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: 
schema: 2.0.0
---

# Enable-AzureRmActivityLogAlert

## SYNOPSIS
Enables an activity log alert and sets its Tags.

## SYNTAX

```
Enable-AzureRmActivityLogAlert [-InputObject <PSActivityLogAlertResource>] [-ResourceId <String>] [-Name <String> -ResourceGroupName <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.
This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource and it accepts the -Force argument.

## EXAMPLES

### Example 1: Disable an activity log alert
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.

### Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input
```

PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

This command enables an activity log alert called alert1. For this it uses a PSActivityLogAlertResource object as input argument.

### Example 3: Enable the ActivityLogAlert using the ResourceId parameter
```

PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert

```

This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.

## PARAMETERS

### -Name
The name of the activity log alert.

```yaml
Type: System.String
Parameter Sets: EnableActivityLogAlertDeafultParamGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
The name of the resource group where the alert resource is going to exist.

```yaml
Type: System.String
Parameter Sets: EnableActivityLogAlertDeafultParamGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableActivityLogAlertFromPipeParamGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (FromPipeline)
Accept wildcard characters: False
```

### -ResourceId
Sets the ResourceId tags property of the call to extract the required name, resource group name properties.

```yaml
Type: System.String
Parameter Sets: EnableActivityLogAlertFromResourceIdParamGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource

## NOTES

## RELATED LINKS

[Set-AzureRmActivityLogAlert](./Set-AzureRmActivityLogAlert.md)

[Get-AzureRmActivityLogAlert](./Get-AzureRmActivityLogAlert.md)

[Remove-AzureRmActivityLogAlert](./Remove-AzureRmActivityLogAlert.md)

[New-AzureRmActionGroup](./New-AzureRmActionGroup.md)

[New-AzureRmActivityLogAlertCondition](./Get-AzureRmActivityLogAlertCondition.md)

[Disable-AzureRmActivityLogAlert](./Disable-AzureRmActivityLogAlert.md)