---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c6479f9358322ae76eeb2fdf3cb9f2bb922e462
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785530"
---
# Set-AzureRmDnsRecordSet

## Sinopse
Atualiza um conjunto de registros DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmDnsRecordSet** atualiza um conjunto de registros no serviço DNS do Azure a partir de um objeto **Recordset** local.

Você pode passar um objeto **Recordset** como um parâmetro ou usando o operador pipeline.

Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.

O conjunto de registros não será atualizado se tiver sido alterado no Azure DNS desde a recuperação do objeto **Recordset** local.
Isso fornece proteção para alterações simultâneas.
Você pode suprimir esse comportamento usando o parâmetro *overwrite* , que atualiza o conjunto de registros independentemente das alterações simultâneas.

## EXEMPLOS

### Exemplo 1: atualizar um conjunto de registros
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzureRmDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzureRmDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzureRmDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzureRmDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzureRmDnsRecordSet
```

O primeiro comando usa o cmdlet Get-AzureRmDnsRecordSet para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet.

O segundo e o terceiro comandos são operações off-line para adicionar dois registros a ao conjunto de registros.

O comando final usa o cmdlet **set-AzureRmDnsRecordSet** para confirmar a atualização.

### Exemplo 2: atualizar um registro SOA
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzureRmDnsRecordSet -RecordSet $RecordSet
```

O primeiro comando usa o cmdlet **Get-AzureRmDnsRecordset** para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $Recordset.

O segundo comando atualiza o registro SOA especificado em $RecordSet.

O comando final usa o cmdlet **set-AzureRmDnsRecordSet** para propagar a atualização em $Recordset.

## OS

### -Substituir
Indica a atualização do conjunto de registros independentemente das alterações simultâneas.

O conjunto de registros não será atualizado se tiver sido alterado no Azure DNS desde que o objeto **Recordset** local foi recuperado.
Isso fornece proteção para alterações simultâneas.
Para suprimir esse comportamento, você pode usar o parâmetro *overwrite* , que faz com que o conjunto de registros seja atualizado independentemente das alterações simultâneas.

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

### -RecordSet
Especifica o **conjunto de registros** a ser atualizado.

```yaml
Type: DnsRecordSet
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Você pode passar um objeto **Recordset** para este cmdlet.

## EXIBE

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Esse cmdlet retorna um objeto que representa o objeto **Recordset** atualizado.

## INFORMA
Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.
Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.

Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.
Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação. 

## LINKS RELACIONADOS

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)
