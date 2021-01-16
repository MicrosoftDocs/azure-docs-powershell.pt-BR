---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: 4ad2b7db5e212cf15748ac81ae28b9471d1678b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98261745"
---
# Get-AzWvdStartMenuItem

## Sinopse
Listar itens do menu iniciar no grupo de aplicativos específico.

## SYNTAX

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRITIVO
Listar itens do menu iniciar no grupo de aplicativos específico.

## EXEMPLOS

### Exemplo 2: listar os itens do menu Iniciar da área de trabalho virtual do Windows
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

Este comando lista os itens do menu Iniciar da área de trabalho virtual do Windows em um grupo do applicaton.

## OS

### -ApplicationGroupName
O nome do grupo de aplicativos

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
O nome do grupo de recursos.
O nome não diferencia maiúsculas de minúsculas.

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
A ID da assinatura de destino.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. DesktopVirtualization. Models. Api20201019Preview. IStartMenuItem

## INFORMA

ALIASES

## LINKS RELACIONADOS

