---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 9a199a0aa0e31cf8bc57585d4825a33e10b5bfc1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786540"
---
# Update-AzureRmContainerService

## Sinopse
Atualiza o estado de um serviço de contêiner.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzureRmContainerService** atualiza o estado de um serviço de contêiner para corresponder a uma instância local do serviço.

## EXEMPLOS

### Exemplo 1: atualizar um serviço de contêiner
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

Esse comando obtém o serviço de contêiner chamado CSResourceGroup17 usando o cmdlet Get-AzureRmContainerService.
O comando passa esse objeto para o cmdlet Remove-AzureRmContainerServiceAgentPoolProfile usando o operador pipeline.

**Remove-AzureRmContainerServiceAgentPoolProfile** remove o perfil chamado AgentPool01.
O comando passa o resultado para o cmdlet Add-AzureRmContainerServiceAgentPoolProfile.

**Add-AzureRmContainerServiceAgentPoolProfile** adiciona um perfil que tem o nome AgentPool01 e tem as propriedades especificadas.
O comando passa o resultado para o cmdlet atual.

O cmdlet atual atualiza o serviço de contêiner para refletir as alterações feitas neste comando.

## OS

### -AsJob
Executar o cmdlet em segundo plano

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

### -ContainerService
Especifica um objeto **ContainerService** local que contém alterações.

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
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
Especifica o nome do serviço de contêiner que este cmdlet atualiza.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o grupo de recursos do serviço de contêiner em que este cmdlet é atualizado.

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.

O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

[New-AzureRmContainerService](./New-AzureRmContainerService.md)

[Remove-AzureRmContainerService](./Remove-AzureRmContainerService.md)

[Remove-AzureRmContainerServiceAgentPoolProfile](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


