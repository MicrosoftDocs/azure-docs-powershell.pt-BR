---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: ''
schema: 2.0.0
ms.openlocfilehash: ce82a1bae63fafcf0d221d0c2ce6d8e82e8e8e12
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785531"
---
# New-AzureRmDnsRecordSet

## Sinopse
Cria um conjunto de registros DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Campos
```
New-AzureRmDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
New-AzureRmDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureRmDnsRecordSet** cria um novo conjunto de registros DNS (sistema de nomes de domínio) com o nome e o tipo especificados na zona especificada.
Um objeto **Recordset** é um conjunto de registros DNS com o mesmo nome e tipo.
Observe que o nome é relativo à zona e não o nome totalmente qualificado.

O parâmetro *DnsRecords* especifica os registros no conjunto de registros.
Esse parâmetro usa uma matriz de registros DNS, construídos usando New-AzureRmDnsRecordConfig.

Você pode usar o operador de pipeline para passar um objeto **dnsZone** para esse cmdlet, ou pode passar um objeto **dnsZone** como o parâmetro de *zona* ou, como alternativa, pode especificar a zona por nome.

Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.

Se um **conjunto de registros** correspondente já existir (mesmo nome e tipo de registro), você deverá especificar o parâmetro *overwrite* , caso contrário, o cmdlet não criará um novo **conjunto de registros** .

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

### Exemplo 9: criar um conjunto de registros na zona Apex
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Esse comando cria um **conjunto de registros** no Apex (ou raiz) da região MyZone.com.
Para fazer isso, o nome do conjunto de registros é especificado como "@" (incluindo as aspas duplas).

Não é possível criar registros CNAME na Apex de uma zona.
Isso é uma restrição dos padrões de DNS; Ele não é uma limitação do Azure DNS.

Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.

### Exemplo 10: criar um conjunto de registros curinga
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzureRmDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Esse comando cria um **conjunto de registros** chamado * na região MyZone.com.
Este é um conjunto de registros curinga.

Para criar um **conjunto de registros** usando apenas uma linha de pn_PowerShell_short ou criar um conjunto de registros com vários registros, consulte o exemplo 1.

### Exemplo 11: criar um conjunto de registros vazio
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

Esse comando cria um **conjunto de registros** chamado www na região MyZone.com.
O conjunto de registros é do tipo A e tem uma TTL de 1 hora (3600 segundos).
Esse é um conjunto de registros vazio, que atua como um espaço reservado para o qual você pode adicionar registros mais tarde.

### Exemplo 12: criar um conjunto de registros e suprimir todas as confirmações
```
PS C:\>$RecordSet = New-AzureRmDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzureRmDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

Esse comando cria um **conjunto de registros**.
O parâmetro overwrite garante que esse registro *substitua* o conjunto de registros preexistentes com o mesmo nome e tipo (os registros existentes nesse conjunto de registros são perdidos).
O parâmetro *Confirm* com um valor de $false suprime o prompt de confirmação.

## OS

### -DnsRecords
Especifica a matriz de registros DNS a serem incluídos no conjunto de registros.
Você pode usar o cmdlet New-AzureRmDnsRecordConfig para criar objetos de registro DNS.
Consulte os exemplos para obter mais informações.

```yaml
Type: DnsRecordBase[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
Esse parâmetro é preterido para esse cmdlet.
Ela será removida em uma versão futura.

Para controlar se esse cmdlet solicita confirmação, use o parâmetro *Confirm* .

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

### -Metadados
Especifica uma matriz de metadados a serem associados ao conjunto de registros.
Os metadados são especificados usando pares de nome-valor representados como tabelas de hash, por exemplo, @ (@ {"Name" = "Dept"; "Valor" = "compra"}, @ {"nome" = "env"; "Valor" = "produção"}).

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Especifica o nome do **conjunto de registros** a ser criado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Substituir
Indica que esse cmdlet substitui o **conjunto de registros** especificado se ele já existir.

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

### -RecordType
Especifica o tipo de registro DNS a ser criado.

Os valores válidos são:

- Um
- AAAA
- CNAME
- MX
- SÉRIE
- PTR
- SRV
- LOCALIZADO

Os registros SOA são criados automaticamente quando a zona é criada e não podem ser criadas manualmente.

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o grupo de recursos que contém a zona DNS.
Você também deve especificar o parâmetro *zonename* para especificar o nome da zona.

Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TTL
Especifica o tempo de vida útil (TTL) do conjunto de registros DNS.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Especifica o DnsZone no qual criar o **conjunto de registros**.
Você também pode especificar a zona usando os parâmetros *zonename* e *ResourceGroupName* .

```yaml
Type: DnsZone
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Zonename
Especifica o nome da zona na qual criar o conjunto de **registros**.
Você também deve especificar o grupo de recursos que contém a zona usando o parâmetro *ResourceGroupName* .

Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
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

### Microsoft. Azure. Commands. DNS. DnsZone
Você pode canalizar um objeto DnsZone para este cmdlet.

## EXIBE

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Esse cmdlet retorna um objeto **Recordset** .

## INFORMA
Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.
Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.

Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.
Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.

## LINKS RELACIONADOS

[Add-AzureRmDnsRecordConfig](./Add-AzureRmDnsRecordConfig.md)

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[New-AzureRmDnsRecordConfig](./New-AzureRmDnsRecordConfig.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
