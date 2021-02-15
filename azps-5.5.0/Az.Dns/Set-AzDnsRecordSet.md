---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 99E6C4DD-11AF-4DC0-848B-39811240BE06
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/set-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Set-AzDnsRecordSet.md
ms.openlocfilehash: e75d394596b85c75dc79b0eb0d2b19525aa9c7c4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111902"
---
# Set-AzDnsRecordSet

## Sinopse
Atualiza um conjunto de registros DNS.

## Sintaxe

```
Set-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Set-AzDnsRecordSet** atualiza um conjunto de registros no serviço DNS do Azure de um objeto **local RecordSet.**
Você pode passar um objeto **RecordSet** como parâmetro ou usando o operador de pipeline.
Você pode usar o *parâmetro Confirmar* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.
O conjunto de registros não será atualizado se tiver sido alterado no DNS do Azure desde que o objeto **local RecordSet** foi recuperado.
Isso fornece proteção para alterações simultâneas.
Você pode suprimir esse comportamento usando o parâmetro *Substituir,* que atualiza o conjunto de registros independentemente de alterações simultâneas.

## Exemplos

### Exemplo 1: Atualizar um conjunto de registros
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.16.0.0
PS C:\> Add-AzDnsRecordConfig -RecordSet $RecordSet -Ipv4Address 172.31.255.255
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet

# These cmdlets can also be piped:

PS C:\> Get-AzDnsRecordSet -ResourceGroupName MyResourceGroup -ZoneName myzone.com -Name www -RecordType A | Add-AzDnsRecordConfig -Ipv4Address 172.16.0.0 | Add-AzDnsRecordConfig -Ipv4Address 172.31.255.255 | Set-AzDnsRecordSet
```

O primeiro comando usa o cmdlet Get-AzDnsRecordSet para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet dados.
O segundo e o terceiro comandos são operações fora de linha para adicionar dois registros A ao conjunto de registros.
O comando final usa **o cmdlet Set-AzDnsRecordSet** para confirmação da atualização.

### Exemplo 2: Atualizar um registro SOA
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -Name "@" -RecordType SOA -Zone $Zone
PS C:\> $RecordSet.Records[0].Email = "admin.myzone.com"
PS C:\> Set-AzDnsRecordSet -RecordSet $RecordSet
```

O primeiro comando usa o cmdlet **Get-AzDnsRecordset** para obter o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet dados.
O segundo comando atualiza o registro SOA especificado no $RecordSet.
O comando final usa **o cmdlet Set-AzDnsRecordSet** para propagar a atualização no $RecordSet.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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

### -Substituir
Indica atualizar o conjunto de registros independentemente de alterações simultâneas.
O conjunto de registros não será atualizado se tiver sido alterado no DNS do Azure desde que o objeto **local RecordSet** foi recuperado.
Isso fornece proteção para alterações simultâneas.
Para suprimir esse comportamento, você pode usar o parâmetro *Substituir,* que faz com que o conjunto de registros seja atualizado independentemente de alterações simultâneas.

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
Especifica o **RecordSet a** ser atualizado.

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

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

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
Mostra o que acontece se o cmdlet for executado. O cmdlet não é executado. Mostra o que acontece se o cmdlet for executado. O cmdlet não é executado.

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

## Entradas

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## Saídas

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## Notas
Você pode usar o *parâmetro Confirmar* para controlar se esse cmdlet solicita confirmação.
Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference Windows PowerShell tem um valor médio ou inferior.
Se você especificar *Confirmar* ou *Confirmar:$True,* este cmdlet solicitará que você confirme antes de ser executado.
Se você especificar *Confirm:$False,* o cmdlet não solicitará confirmação. 

## LINKS RELACIONADOS

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)
