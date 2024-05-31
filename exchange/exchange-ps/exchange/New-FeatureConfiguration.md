---
external help file: Microsoft.Exchange.TransportMailflow-Help.xml
online version: https://learn.microsoft.com/powershell/module/exchange/new-featureconfiguration
applicable: Security & Compliance
title: New-FeatureConfiguration
schema: 2.0.0
---

# New-FeatureConfiguration

## SYNOPSIS
**Note**: Currently, this cmdlet is available only in Private Preview.

This cmdlet is available only in Security & Compliance PowerShell. For more information, see [Security & Compliance PowerShell](https://learn.microsoft.com/powershell/exchange/scc-powershell).

Use the New-FeatureConfiguration cmdlet to create Discovery policies.

For information about the parameter sets in the Syntax section below, see [Exchange cmdlet syntax](https://learn.microsoft.com/powershell/exchange/exchange-cmdlet-syntax).

## SYNTAX

```
New-FeatureConfiguration [-Name] <String> -Mode <Microsoft.Office.CompliancePolicy.Tasks.PolicyMode> -FeatureScenario <Microsoft.Office.CompliancePolicy.PolicyConfiguration.PolicyScenario> -ScenarioConfig <String>
 [-Comment <String>]
 [-Confirm]
 [-Locations <String>]
 [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
To use this cmdlet in Security & Compliance PowerShell, you need to be assigned permissions. For more information, see [Permissions in Security & Compliance](https://go.microsoft.com/fwlink/p/?LinkId=511920).

## EXAMPLES

### Example 1
```powershell
New-FeatureConfiguration -Name "Discovery policy for Contoso executives" -FeatureScenario KnowYourData -Mode Enable -ScenarioConfig '{"Activities": ["UploadText", "UploadFile"], "EnforcementPlanes": ["Browser"], "SensitiveTypeIds": ["a44669fe-0d48-453d-a9b1-2cc83f2cba77","50842eb7-edc8-4019-85dd-5a5c1f2bb085"]}' –Locations '[{"Workload": "Applications","Location": "51622","Inclusions": [{"Type": "Group","Identity": "executives@contoso.com"}]},{"Workload": "Applications","Location": "51399","Inclusions": [{"Type": "Group","Identity": "executives@contoso.com"}]},{"Workload": "Applications","Location": "51279","Inclusions": [{"Type": "Group","Identity": "executives@contoso.com"}]}]'
```

This example displays a discovery policy that includes the group "Executives" and targets a specific set of sensitive information types.

## PARAMETERS

### -Name
The Name parameter specifies the unique name for the Discovery policy. The maximum length is 64 characters. If the value contains spaces, enclose the value in quotation marks (").

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FeatureScenario
The FeatureScenario parameter specifies the scenario for the Discovery policy. Currently, the only valid value is KnowYourData.

```yaml
Type: Microsoft.Office.CompliancePolicy.PolicyConfiguration.PolicyScenario
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mode
The Mode parameter specifies the action and notification level of the Discovery policy. Valid values are:

- Enable: The policy is enabled for actions and notifications. This is the default value.
- Disable: The policy is disabled.

```yaml
Type: Microsoft.Office.CompliancePolicy.Tasks.PolicyMode
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScenarioConfig
The ScenarioConfig parameter specifies additional information about the policy configuration.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
The Comment parameter specifies an optional comment. If you specify a value that contains spaces, enclose the value in quotation marks ("), for example: "This is an admin note".

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: `-Confirm:$false`.
- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Locations
The locations parameter specifies where the policy applies.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch simulates the actions of the command. You can use this switch to view the changes that would occur without actually applying those changes. You don't need to specify a value with this switch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: Security & Compliance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS