---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
ms.openlocfilehash: d78e4d8e84508e9a737bb15dc31b0dad1c9bdedc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785637"
---
# Set-AzureRmPublicIpAddress

## Sinopse
Define o estado da meta para um endereço IP público.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmPublicIpAddress** define o estado da meta para um endereço IP público.

## EXEMPLOS

### 1: alterar o método de alocação de um endereço IP público
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.
Segundo comando define o método de alocação do objeto de endereço IP público como "estático".
Set-AzureRmPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado e modifica o método de alocação para ' estático '. Um endereço IP público é alocado imediatamente.

### 2: alterar o rótulo de domínio DNS de um endereço IP público
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

Primeiro comando obtém o recurso de endereço IP público com o nome $publicIPName no $rgName do grupo de recursos.
Segundo comando define a propriedade DomainNameLabel para o prefixo DNS obrigatório.
Set-AzureRmPublicIPAddress comando atualiza o recurso de endereço IP público com o objeto atualizado. DomainNameLabel & FQDN são modificados como esperado.

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

### -PublicIpAddress
Especifica um objeto **PublicIpAddress** que representa o estado da meta para o qual o endereço IP público deve ser definido.

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSPublicIpAddress
O parâmetro ' PublicIpAddress ' aceita o valor do tipo ' PSPublicIpAddress ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmPublicIpAddress](./Get-AzureRmPublicIpAddress.md)

[New-AzureRmPublicIpAddress](./New-AzureRmPublicIpAddress.md)

[Remove-AzureRmPublicIpAddress](./Remove-AzureRmPublicIpAddress.md)


