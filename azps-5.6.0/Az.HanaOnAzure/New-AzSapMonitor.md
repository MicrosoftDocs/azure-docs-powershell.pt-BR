---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/powershell/module/az.hanaonazure/new-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/New-AzSapMonitor.md
ms.openlocfilehash: a13b0a936eeecd1d7a18b18bb8878b79225da030
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893322"
---
# New-AzSapMonitor

## SYNOPSIS
Cria um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do recurso.

## SINTAXE

```
New-AzSapMonitor -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-EnableCustomerAnalytic] [-LogAnalyticsWorkspaceId <String>] [-LogAnalyticsWorkspaceResourceId <String>]
 [-LogAnalyticsWorkspaceSharedKey <String>] [-MonitorSubnetResourceId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Cria um monitor SAP para a assinatura especificada, o grupo de recursos e o nome do recurso.

## EXEMPLOS

### Exemplo 1: Novo monitor SAP 
```powershell
PS C:\> $Workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName nancyc-hn1 -Name sapmonitor-test  -Location westus2 -Sku "Standard"
PS C:\> $WorkspaceKey = Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName nancyc-hn1 -Name sapmonitor-test
PS C:\> New-AzSapMonitor -Name ps-sapmonitor-t01 -ResourceGroupName nancyc-hn1 -Location westus2 -EnableCustomerAnalytic -MonitorSubnet "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.Network/virtualNetworks/vnet-sap/subnets/subnet-admin" -LogAnalyticsWorkspaceSharedKey $WorkspaceKey.PrimarySharedKey -LogAnalyticsWorkspaceId $Workspace.CustomerId -LogAnalyticsWorkspaceResourceId $Workspace.ResourceId

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

Este comando cria um monitor SAP.

## PARÂMETROS

### -AsJob
Executar o comando como um trabalho

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.

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

### -EnableCustomerAnalytic
O valor que indica se a análise deve ser enviado para a Microsoft

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
A localização geográfica onde o recurso mora

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

### -LogAnalyticsWorkspaceId
A ID do espaço de trabalho do espaço de trabalho de análise de log a ser usado para monitoramento

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogAnalyticsWorkspaceResourceId
A ARM ID do Espaço de Trabalho de Análise de Log usado para monitoramento

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogAnalyticsWorkspaceSharedKey
A chave compartilhada do espaço de trabalho de análise de log usado para monitoramento

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitorSubnetResourceId
A sub-rede na qual o monitor SAP será implantado.
Deve ser a mesma sub-rede do banco de dados HANA.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome do recurso de monitor SAP.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Executar o comando de forma assíncrona

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

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
ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura faz parte do URI para cada chamada de serviço.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Marcas de recurso.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## SAÍDAS

### Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor

## NOTES

ALIASES

## LINKS RELACIONADOS

