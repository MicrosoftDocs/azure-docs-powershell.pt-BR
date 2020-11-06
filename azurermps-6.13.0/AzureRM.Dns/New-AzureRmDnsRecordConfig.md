---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: AD97BCAF-69BA-4C16-8B57-AB243D796B71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnsrecordconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsRecordConfig.md
ms.openlocfilehash: 6c2acfe611a8b2c5ef9ecb11173ca9e5210e00e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426352"
---
# New-AzureRmDnsRecordConfig

## Sinopse
Cria um novo objeto local de registro DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Um
```
New-AzureRmDnsRecordConfig -Ipv4Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Aaaa
```
New-AzureRmDnsRecordConfig -Ipv6Address <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Série
```
New-AzureRmDnsRecordConfig -Nsdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### MX
```
New-AzureRmDnsRecordConfig -Exchange <String> -Preference <UInt16> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PTR
```
New-AzureRmDnsRecordConfig -Ptrdname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Localizado
```
New-AzureRmDnsRecordConfig -Value <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SRV
```
New-AzureRmDnsRecordConfig -Priority <UInt16> -Target <String> -Port <UInt16> -Weight <UInt16>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### CName
```
New-AzureRmDnsRecordConfig -Cname <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Caa
```
New-AzureRmDnsRecordConfig -CaaFlags <Byte> -CaaTag <String> -CaaValue <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmDnsRecordConfig** cria um objeto **DnsRecord** local.
Uma matriz desses objetos é passada para o cmdlet New-AzureRmDnsRecordSet usando o parâmetro *DnsRecords* para especificar os registros a serem criados no conjunto de registros.

## EXEMPLOS

### Exemplo 1: criar um conjunto de registros do tipo A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzureRmDnsRecordConfig to add each record to the $Records array,
# then call New-AzureRmDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzureRmDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.
O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.

### Exemplo 2: criar um conjunto de registros do tipo AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.
O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.

### Exemplo 3: criar um conjunto de registros do tipo CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este exemplo cria um **conjunto de registros** chamado www na região MyZone.com.
O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.

### Exemplo 4: criar um conjunto de registros do tipo MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Esse comando cria um **conjunto de registros** chamado www na região MyZone.com.
O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.

### Exemplo 5: criar um conjunto de registros do tipo NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Esse comando cria um **conjunto de registros** chamado ns1 na zona MyZone.com.
O conjunto de registros é do tipo NS e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.

### Exemplo 6: criar um conjunto de registros do tipo PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Esse comando cria um **conjunto de registros** chamado 4 na zona 3.2.1.in-addr. arpa.
O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.

### Exemplo 7: criar um conjunto de registros do tipo SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Esse comando cria um **conjunto de registros** chamado _sip. _ TCP na zona MyZone.com.
O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS, apontando para o endereço de IP 2001.2.3.4.
O serviço (SIP) e o protocolo (TCP) são especificados como parte do nome do conjunto de registros, não como parte dos dados do registro.
Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.

### Exemplo 8: criar um conjunto de registros do tipo TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Esse comando cria um **conjunto de registros** chamado texto na zona MyZone.com.
O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.

## OS

### -CaaFlags
Os sinalizadores para o registro CAA a ser adicionado. Deve ser um número entre 0 e 255.

```yaml
Type: System.Byte
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaTag
O campo de marca do registro CAA a ser adicionado.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CaaValue
O campo de valor do registro CAA a ser adicionado.

```yaml
Type: System.String
Parameter Sets: Caa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CNAME
Especifica o nome de domínio para um registro de nome canônico (CNAME).

```yaml
Type: System.String
Parameter Sets: CName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Exchange
Especifica o nome do servidor do servidor de mensagens para um registro de troca de email (MX).

```yaml
Type: System.String
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv4Address
Especifica um endereço IPv4 para um registro A.

```yaml
Type: System.String
Parameter Sets: A
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ipv6Address
Especifica um endereço IPv6 para um registro AAAA.

```yaml
Type: System.String
Parameter Sets: Aaaa
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nsdname
Especifica o nome do servidor de nomes para um registro de servidor de nomes (NS).

```yaml
Type: System.String
Parameter Sets: Ns
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Porta
Especifica a porta para um registro de serviço (SRV).

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Preferência
Especifica a preferência para um registro MX.

```yaml
Type: System.UInt16
Parameter Sets: Mx
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Priority
Especifica a prioridade para um registro SRV.

```yaml
Type: System.UInt16
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ptrdname
Especifica o nome de domínio de destino de um registro de recurso de ponteiro (PTR).

```yaml
Type: System.String
Parameter Sets: Ptr
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Destino
Especifica o destino para um registro SRV.

```yaml
Type: System.String
Parameter Sets: Srv
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Valor
Especifica o valor de um registro TXT.

```yaml
Type: System.String
Parameter Sets: Txt
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Weight
Especifica o peso para um registro SRV.

```yaml
Type: System.UInt16
Parameter Sets: Srv
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

### System. String

### System. UInt16

### System. byte

## EXIBE

### Microsoft. Azure. Commands. DNS. DnsRecordBase

## INFORMA

## LINKS RELACIONADOS

[Add-AzureRmDnsRecordConfig](./Add-AzureRmDnsRecordConfig.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordConfig](./Remove-AzureRmDnsRecordConfig.md)
