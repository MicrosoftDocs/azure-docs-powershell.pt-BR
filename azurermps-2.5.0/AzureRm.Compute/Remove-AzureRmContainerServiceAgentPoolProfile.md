---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerserviceagentpoolprofile
schema: 2.0.0
ms.openlocfilehash: 2bbc7d9e1ac125134931be483d3a693252ce12d0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786149"
---
# Remove-AzureRmContainerServiceAgentPoolProfile

## Sinopse
Remove um perfil de pool de agente de um serviço de contêiner.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Remove-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmContainerServiceAgentPoolProfile** remove um perfil de pool de agente de um serviço de contêiner.

## EXEMPLOS

### Exemplo 1: remover um perfil de um serviço de contêiner
```
PS C:\> $Container = Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzureRmContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

O primeiro comando obtém um serviço de contêiner chamado CSResourceGroup17 usando o cmdlet Get-AzureRmContainerService.
O comando armazena o serviço na variável $Container.

O segundo comando Remove o perfil chamado AgentPool01 do serviço de contêiner em $Container.

## OS

### -ContainerService
Especifica o objeto de serviço de contêiner do qual esse cmdlet Remove um perfil de pool do agente.

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome do perfil do pool de agentes que este cmdlet Remove.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

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

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### ContainerService
O parâmetro ' ContainerService ' aceita o valor do tipo ' ContainerService ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmContainerServiceAgentPoolProfile](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[Get-AzureRmContainerService](./Get-AzureRmContainerService.md)


