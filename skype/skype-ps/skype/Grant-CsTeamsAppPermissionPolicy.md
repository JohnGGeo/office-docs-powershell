---
external help file: Microsoft.Rtc.Management.dll-help.xml
online version: https://docs.microsoft.com/powershell/module/skype/grant-csteamsapppermissionpolicy
applicable: Microsoft Teams, Skype for Business Online
title: Grant-CsTeamsAppPermissionPolicy
schema: 2.0.0
ms.reviewer:
manager: bulenteg
ms.author: tomkau
author: tomkau
---

# Grant-CsTeamsAppPermissionPolicy

## SYNOPSIS

As an admin, you can use app permission policies to enable or block specific apps for your users.  Learn more about the App Permission Policies: https://docs.microsoft.com/en-us/microsoftteams/teams-app-permission-policies.

**We require that all creation and modification of app setup polices (not including the assignment or removal of policies from users) happens in the Microsoft Teams & Skype for Business Admin Center to ensure that the policy matches your expectations for the end user experience.**

You can use this cmdlet to assign a specific custom policy to a user.

## SYNTAX

### Identity (Default)
```
Grant-CsTeamsAppPermissionPolicy [[-Identity] <UserIdParameter>] [-PolicyName] <String> [-Tenant <System.Guid>]
 [-DomainController <Fqdn>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### GrantToTenant
```
Grant-CsTeamsAppPermissionPolicy [-PolicyName] <String> [-Tenant <System.Guid>] [-DomainController <Fqdn>]
 [-PassThru] [-Global] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
As an admin, you can use app permission policies to enable or block specific apps for your users.  Learn more about the App Permission Policies: https://docs.microsoft.com/en-us/microsoftteams/teams-app-permission-policies.

**We require that all creation and modification of app setup polices (not including the assignment or removal of policies from users) happens in the Microsoft Teams & Skype for Business Admin Center to ensure that the policy matches your expectations for the end user experience.**

You can use this cmdlet to assign a specific custom policy to a user.

## EXAMPLES

### Example 1
```powershell
PS C:\> Grant-CsTeamsAppPermissionPolicy -Identity "Ken Myer" -PolicyName StudentAppPermissionPolicy
```

In this example, a user with identity "Ken Myer" is being assigned the StudentAppPermissionPolicy

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainController
Do not use.
```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Global
Resets the values in the global policy to match those in the provided (PolicyName) policy.  Note that this means all users with no explicit policy assigned will have these new policy settings.

```yaml
Type: SwitchParameter
Parameter Sets: GrantToTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
The user to whom the policy should be assigned.

```yaml
Type: UserIdParameter
Parameter Sets: Identity
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PassThru

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyName
The name of the custom policy that is being assigned to the user.  To remove a specific assignment and fall back to the default tenant policy, you can assign to $Null.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant
Do not use.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Rtc.Management.AD.UserIdParameter


## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
