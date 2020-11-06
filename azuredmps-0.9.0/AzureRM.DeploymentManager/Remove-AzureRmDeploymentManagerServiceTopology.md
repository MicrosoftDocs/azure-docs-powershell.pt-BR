---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425722"
---
# Remove-AzureRmDeploymentManagerServiceTopology

## Sinopse
Exclui uma topologia de serviço e todos os seus recursos.

## SYNTAX

### Interativo (padrão)
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Identificação
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmDeploymentManagerServiceTopology** exclui uma topologia de serviço.

Especifique a topologia do serviço de acordo com o nome e o nome do grupo de recursos. Como alternativa, você pode fornecer o objeto imtopology ou o resourceId.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

Esse comando exclui uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.

### Exemplo 2: excluir uma topologia de serviço usando o identificador de recursos.
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

Esse comando exclui uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.

### Exemplo 3: excluir uma topologia de serviço usando o objeto de topologia de serviço.
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

Esse comando exclui uma topologia de serviço cujo nome e o meu nome do contato correspondam às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.

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

### -Force
Não peça confirmação.

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

### -PassThru
{{Descrição do PassThru de preenchimento}}

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
O recurso a ser removido.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource

## EXIBE

### System. Boolean

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmDeploymentManagerServiceTopology](./New-AzureRmDeploymentManagerServiceTopology.md)

[Get-AzureRmDeploymentManagerServiceTopology](./Get-AzureRmDeploymentManagerServiceTopology.md)

[Set-AzureRmDeploymentManagerServiceTopology](./Set-AzureRmDeploymentManagerServiceTopology.md)