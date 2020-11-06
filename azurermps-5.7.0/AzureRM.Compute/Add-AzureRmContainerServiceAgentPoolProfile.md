---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C3C65F3E-1192-4B57-87DB-5D371C8FF68E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmContainerServiceAgentPoolProfile.md
ms.openlocfilehash: 1b3df5b930cd7b30af8fef35735eea56eab7a5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431724"
---
# Add-AzureRmContainerServiceAgentPoolProfile

## Sinopse
Adiciona um perfil de pool de agente de serviço de contêiner.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Add-AzureRmContainerServiceAgentPoolProfile [-ContainerService] <ContainerService> [[-Name] <String>]
 [[-Count] <Int32>] [[-VmSize] <String>] [[-DnsPrefix] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureRmContainerServiceAgentPoolProfile** adiciona um perfil de pool de agente de serviço de contêiner a um objeto de serviço de contêiner local.

## EXEMPLOS

### Exemplo 1: adicionar um perfil
```
PS C:\> Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

Esse comando adiciona um perfil de pool de agente de serviço de contêiner ao objeto de serviço de contêiner local.

## OS

### -ContainerService
Especifica o objeto de serviço de contêiner para o qual esse cmdlet adiciona um perfil de pool do agente.
Para obter um objeto **ContainerService** , use o cmdlet [New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md) .

```yaml
Type: ContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Contagem
Especifica o número de agentes que hospedam contêineres.
Os valores aceitáveis para esse parâmetro são: inteiros de 1 a 100.
O valor padrão é 1.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DnsPrefix
Especifica o prefixo DNS que este cmdlet usa para criar o nome de domínio totalmente qualificado para esse pool de agentes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do perfil do pool do agente.
Esse valor deve ser exclusivo no contexto da assinatura e do grupo de recursos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmSize
Especifica o tamanho das máquinas virtuais para os agentes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmContainerServiceConfig](./New-AzureRmContainerServiceConfig.md)

[Remove-AzureRmContainerServiceAgentPoolProfile](./Remove-AzureRmContainerServiceAgentPoolProfile.md)
