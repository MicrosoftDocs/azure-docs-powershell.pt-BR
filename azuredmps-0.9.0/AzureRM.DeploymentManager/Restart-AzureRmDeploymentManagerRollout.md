---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426068"
---
# Restart-AzureRmDeploymentManagerRollout

## Sinopse
Reinicie uma distribuição com falha.

## SYNTAX

### Interativo (padrão)
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Identificação
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObject
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Restart-AzureRmDeploymentManagerRollout** reinicia uma distribuição com falha e retorna um objeto que representa essa distribuição com todas as informações detalhadas sobre o andamento da distribuição.
Especifique a distribuição por nome e nome do grupo de recursos. Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.
O parâmetro opcional SkipSucceeded permite que você ignore todas as etapas bem-sucedidas na execução anterior da distribuição.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

Esse comando reinicia uma distribuição chamada ContosoRollout no ContosoResourceGroup. O sinalizador SkipSucceeded indica que todas as etapas que já executaram com êxito devem ser ignoradas e a distribuição deve continuar a execução a partir de onde ela foi interrompida pela última vez.

### Exemplo 2: reiniciar uma distribuição usando o identificador de recursos
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

Esse comando reinicia uma distribuição chamada ContosoRollout no ContosoResourceGroup.

### Exemplo 3: reiniciar uma distribuição usando o objeto de distribuição.
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

Esse comando reinicia uma distribuição cujo nome e o nome da fonte de reinicialização correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.

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
O nome da distribuição.

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

### -Distribuição
O recurso a ser removido.

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SkipSucceeded
Ignorar etapas bem-sucedidas na execução anterior da distribuição.

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

### Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout

## EXIBE

### Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmDeploymentManagerRollout](./Get-AzureRmDeploymentManagerRollout.md)

[Parar-AzureRmDeploymentManagerRollout](./Stop-AzureRmDeploymentManagerRollout.md)

[Remove-AzureRmDeploymentManagerRollout](./Remove-AzureRmDeploymentManagerRollout.md)