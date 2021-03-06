---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786116"
---
# Get-AzureRmDnsZone

## Sinopse
Obtém uma zona DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Padrão (padrão)
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### Resource
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmDnsZone** Obtém uma zona de sistema de nome de domínio (DNS) do grupo de recursos especificado.
Se você especificar o parâmetro *Name* , um único objeto **dnsZone** será retornado.
Se você não especificar o parâmetro *Name* , será retornada uma matriz contendo todas as zonas do grupo de recursos especificado.
Você pode usar o objeto **dnsZone** para atualizar a zona, por exemplo, você pode adicionar objetos **Recordset** a ele.

## EXEMPLOS

### Exemplo 1: obter uma zona
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Este exemplo obtém a zona DNS chamada myzone.com do grupo de recursos especificado e armazena-a na variável $Zone.

### Exemplo 2: obter todas as zonas em um grupo de recursos
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

Este exemplo obtém todas as zonas DNS no grupo de recursos especificado e, em seguida, as armazena na variável $Zones.

### Exemplo 3: obter todas as zonas em uma assinatura
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

Este exemplo obtém todas as zonas DNS na assinatura atual do Azure e as armazena na variável $Zones.

## OS

### -Nome
Especifica o nome da zona DNS a ser obtida.

Se você não especificar um valor para o parâmetro *Name* , esse cmdlet obtém todas as zonas DNS no grupo de recursos especificado.
Se você também omitir o parâmetro *ResourceGroupName* , esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a zona DNS a ser obtida.

Se você não especificar o *ResourceGroupName* , também deverá omitir o parâmetro *Name* .
Nesse caso, esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Este cmdlet não permite que você entre na entrada de pipe.

## EXIBE

### Microsoft. Azure. Commands. DNS. DnsZone
Esse cmdlet retorna um objeto que representa a zona DNS.
Se o nome da zona não for especificado, uma matriz de objetos de zona será retornada.

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)

[Set-AzureRmDnsZone](./Set-AzureRmDnsZone.md)
