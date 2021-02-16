---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 5a29c0bbad712d99b03ab1ff5347cba5c07b02aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118308"
---
# New-AzNetworkWatcherConnectionMonitorEndpointObject

## Sinopse
Cria o ponto de extremidade do monitor de conexão.

## Sintaxe

### AzureVM
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVM] -ResourceId <String>
 [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureVNet
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureVNet] -ResourceId <String>
 [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AzureSubnet
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-AzureSubnet] -ResourceId <String>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Externaladdress
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-ExternalAddress] -Address <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MMAWorkspaceMachine
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceMachine] -ResourceId <String>
 -Address <String> [-IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MMAWorkspaceNetwork
```
New-AzNetworkWatcherConnectionMonitorEndpointObject -Name <String> [-MMAWorkspaceNetwork] -ResourceId <String>
 -IncludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>
 [-ExcludeItem <PSNetworkWatcherConnectionMonitorEndpointScopeItem[]>] [-CoverageLevel <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrição
New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet cria o ponto de extremidade do monitor de conexão.

## Exemplos

### Exemplo 1
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointScopeItem1 = New-AzNetworkWatcherConnectionMonitorEndpointScopeItemObject -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndpointObject -Name "workspaceEndpoint" -MMAWorkspaceMachine -ResourceId $MySrcResourceId1 -IncludeItem $SrcEndpointScopeItem1
```

Nome: tipo de ponto de trabalhoEndpoint: MMAWorkspaceMachine ResourceId: /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: Scope: { "Include": [ { "Address": "WIN-P0HGNDO2S1B" } ] } }

## Parâmetros

### -Endereço
Endereço do ponto de extremidade do monitor de conexão (IP ou nome de domínio).

```yaml
Type: System.String
Parameter Sets: AzureVM
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExternalAddress, MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureSubnet
Opção de ponto de extremidade da Sub-rede do Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureVM
Opção de ponto de extremidade VM do Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVM
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureVNet
Opção de ponto de extremidade do Azure Vnet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVNet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoverageLevel
Cobertura de teste para o ponto de extremidade.
Os valores com suporte são Padrão, Baixo, Abaixo de Média, Média, Acima deAvergae, Completo.

```yaml
Type: System.String
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeItem
Lista de itens que precisam ser excluídos do escopo do ponto de extremidade.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, AzureSubnet, MMAWorkspaceNetwork
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExternalAddress
Opção do ponto de extremidade endereço externo.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExternalAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeItem
Lista de itens que precisam ser incluídos no escopo de endpont.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: AzureVNet, MMAWorkspaceMachine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointScopeItem[]
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MMAWorkspaceMachine
Opção de ponto de extremidade MMA Workspace Machine.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceMachine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MMAWorkspaceNetwork
Opção de ponto de extremidade MMA Workspace Network.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome do ponto de extremidade do monitor de conexão.

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

### -ResourceId
ID do recurso do ponto de extremidade do monitor de conexão.

```yaml
Type: System.String
Parameter Sets: AzureVM, AzureVNet, AzureSubnet, MMAWorkspaceMachine, MMAWorkspaceNetwork
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirmar
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
Mostra o que acontece se o cmdlet for executado.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### Nenhum

## Saídas

### Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject

## Notas

## LINKS RELACIONADOS
