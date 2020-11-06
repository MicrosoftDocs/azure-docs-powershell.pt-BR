---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426190"
---
# Get-AzureRmDeploymentManagerServiceTopology

## Sinopse
Obtém uma topologia de serviço.

## SYNTAX

### Interativo (padrão)
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Identificação
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmDeploymentManagerServiceTopology** Obtém uma topologia de serviço.

Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações à topologia usando o cmdlet Set-AzureRmDeploymentManagerServiceTopology.
Especifique a topologia do serviço de acordo com o nome e o nome do grupo de recursos. Como alternativa, você pode fornecer o objeto imtopology ou o resourceId.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.

### Exemplo 2: obter uma topologia de serviço usando o identificador de recursos.
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

Esse comando obtém uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.

### Exemplo 3: obter uma topologia de serviço usando o objeto de topologia de serviço.
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

Esse comando obtém uma topologia de serviço cujo nome e o meu nome de fonte correspondem às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
O nome da topologia de serviço.

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
O identificador do recurso.

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

### -Outtopology
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmDeploymentManagerServiceTopology](./New-AzureRmDeploymentManagerServiceTopology.md)

[Remove-AzureRmDeploymentManagerServiceTopology](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[Set-AzureRmDeploymentManagerServiceTopology](./Set-AzureRmDeploymentManagerServiceTopology.md)