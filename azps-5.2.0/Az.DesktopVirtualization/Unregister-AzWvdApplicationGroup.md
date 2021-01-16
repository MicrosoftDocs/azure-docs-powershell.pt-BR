---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/unregister-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Unregister-AzWvdApplicationGroup.md
ms.openlocfilehash: 0533864f3fd16e9810e837629782b767fbdc0435
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259560"
---
# Unregister-AzWvdApplicationGroup

## Sinopse
Cancelar o registro do grupo de aplicativos área de trabalho virtual do Windows.

## SYNTAX

```
Unregister-AzWvdApplicationGroup -ApplicationGroupPath <String> -ResourceGroupName <String>
 -WorkspaceName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRITIVO
Cancelar o registro do grupo de aplicativos área de trabalho virtual do Windows.

## EXEMPLOS

### Exemplo 1: cancelar o registro de um grupo de aplicativos de área de trabalho virtual do Windows
```powershell
PS C:\> Unregister-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                                    -WorkspaceName WorkspaceName `
                                    -ApplicationGroupPath '/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

Esse comando cancela o registro de um grupo de aplicativos de área de trabalho virtual do Windows em um espaço de trabalho.

## OS

### -ApplicationGroupPath
Caminho ResourceGroupName

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
ID da assinatura

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Nome do espaço de trabalho

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20191210Preview. IWorkspace

## INFORMA

ALIASES

## LINKS RELACIONADOS

