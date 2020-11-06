---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpPrefix.md
ms.openlocfilehash: 7b60c157f3e86e72461c82f34a2d23dcb5eb0b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426317"
---
# Set-AzureRmPublicIpPrefix

## Sinopse
Define as marcas para um PublicIpPrefix existente

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmPublicIpPrefix -PublicIpPrefix <PSPublicIpPrefix> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmPublicIpPrefix** define as marcas para um prefixo de IP público.

## EXEMPLOS

### Definir as marcas do prefixo de IP público
```powershell
PS C:\> $publicIpPrefix = Get-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName

PS C:\> $publicIpPrefix.Tags = "TestTag"

PS C:\> Set-AzureRmPublicIpPrefix -PublicIpPrefix $publicIpPrefix
```

O primeiro comando obtém um prefixo de IP público existente, o segundo comando define a propriedade Tags e o terceiro comando atualiza o objeto existente.

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

### -PublicIpPrefix
O PublicIpPrefix

```yaml
Type: PSPublicIpPrefix
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.
Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix


## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix


## INFORMA

## LINKS RELACIONADOS
