---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: 1ab2d10800648d04c9e8dcb2cf8907d426bd2d48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889485"
---
# Set-AzDnsRecordSet

## SYNOPSIS
Atualiza um conjunto de registros DNS.

## SINTAXE

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Set-AzDnsRecordSet** atualiza um registro definido no serviço DNS do Azure a partir de um **objeto RecordSet** local.
Você pode passar um **objeto RecordSet** como parâmetro ou usando o operador de pipeline.
Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.
O conjunto de registros não será atualizado se tiver sido alterado no DNS do Azure desde que o **objeto RecordSet** local foi recuperado.
Isso fornece proteção para alterações simultâneas.
Você pode suprimir esse comportamento usando o parâmetro *Overwrite,* que atualiza o conjunto de registros independentemente de alterações simultâneas.

## EXEMPLOS

### Exemplo 1: Atualizar um conjunto de registros
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

O primeiro comando usa o cmdlet Get-AzDnsRecordSet para obter o conjunto de registros especificado e o armazena na variável $RecordSet.
O segundo e o terceiro comandos são operações off-line para adicionar dois registros A ao conjunto de registros.
O comando final usa o cmdlet **Set-AzDnsRecordSet** para confirmação da atualização.

### Exemplo 2: atualizar um registro SOA
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

O primeiro comando usa o cmdlet **Get-AzDnsRecordset** para obter o conjunto de registros especificado e o armazena na variável $RecordSet.
O segundo comando atualiza o registro SOA especificado $RecordSet.
O comando final usa o cmdlet **Set-AzDnsRecordSet** para propagar a atualização no $RecordSet.

## PARÂMETROS

### -DefaultProfile
As credenciais, conta, locatário e assinatura usadas para comunicação com o azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
Indica atualizar o conjunto de registros independentemente das alterações simultâneas.
O conjunto de registros não será atualizado se tiver sido alterado no DNS do Azure desde que o **objeto RecordSet** local foi recuperado.
Isso fornece proteção para alterações simultâneas.
Para suprimir esse comportamento, você pode usar o parâmetro *Overwrite,* que resulta no conjunto de registros sendo atualizado independentemente de alterações simultâneas.

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

### -RecordSet
Especifica o **RecordSet** a ser atualizado.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Solicita a confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## SAÍDAS

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTES
Você pode usar o *parâmetro Confirm* para controlar se esse cmdlet solicita a confirmação.
Por padrão, o cmdlet solicita que você confirme se a variável $ConfirmPreference Windows PowerShell tem um valor médio ou inferior.
Se você especificar *Confirm* ou *Confirm:$True*, este cmdlet solicitará confirmação antes de ser executado.
Se você especificar *Confirm:$False*, o cmdlet não solicitará confirmação. 

## LINKS RELACIONADOS

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
