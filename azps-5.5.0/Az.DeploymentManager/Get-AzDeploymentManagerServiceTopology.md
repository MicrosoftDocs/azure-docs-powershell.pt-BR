---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110968"
---
# Get-AzDeploymentManagerServiceTopology

## Sinopse
Obtém a topologia do serviço.

## Sintaxe

### Interativo (Padrão)
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourceid
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Inputobject
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzDeploymentManagerServiceTopology** obtém uma topologia de serviço.

Você pode modificar esse objeto localmente e aplicar alterações à topologia usando o cmdlet Set-AzDeploymentManagerServiceTopology texto.
Especifique a topologia do serviço pelo nome e pelo nome do grupo de recursos. Como alternativa, você pode fornecer o objeto ServiceTopology ou o ResourceId.

## Exemplos

### Exemplo 1
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.

### Exemplo 2: Obter uma topologia de serviço usando o identificador de recurso.
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no Grupo ContosoResource.

### Exemplo 3: Obter uma topologia de serviço usando o objeto de topologia de serviço.
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

Esse comando obtém uma topologia de serviço cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos do $serviceTopologyObject, respectivamente.

## Parâmetros

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

### -InputObject
Objeto de recurso de topologia de serviço.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
O nome da topologia do serviço.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O grupo de recursos.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
O identificador de recurso.

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## Entradas

### System.String

### Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource

## Saídas

### Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource

## Notas

## LINKS RELACIONADOS
