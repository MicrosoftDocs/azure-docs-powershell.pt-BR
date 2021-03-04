---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 45DF71E0-77E1-4D20-AD09-2C06680F659F
online version: https://docs.microsoft.com/powershell/module/az.dns/new-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/New-AzDnsRecordSet.md
ms.openlocfilehash: f1731cb0eceb4474c233db859c3f4edb10461fe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889493"
---
# New-AzDnsRecordSet

## SYNOPSIS
Cria um conjunto de registros DNS.

## SINTAXE

### Campos (Padrão)
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> -Ttl <UInt32>
 -RecordType <RecordType> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasFields
```
New-AzDnsRecordSet -Name <String> -ZoneName <String> -ResourceGroupName <String> [-Ttl <UInt32>]
 -RecordType <RecordType> -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>]
 [-Overwrite] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> -Ttl <UInt32> -RecordType <RecordType>
 [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AliasObject
```
New-AzDnsRecordSet -Name <String> -Zone <DnsZone> [-Ttl <UInt32>] -RecordType <RecordType>
 -TargetResourceId <String> [-Metadata <Hashtable>] [-DnsRecords <DnsRecordBase[]>] [-Overwrite]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **New-AzDnsRecordSet** cria um novo registro DNS (Sistema de Nomes de Domínio) definido com o nome especificado e digite na zona especificada.
Um **objeto RecordSet** é um conjunto de registros DNS com o mesmo nome e tipo.
Observe que o nome é relativo à zona e não ao nome totalmente qualificado.
O *parâmetro DnsRecords* especifica os registros no conjunto de registros.
Esse parâmetro usa uma matriz de registros DNS, construída usando New-AzDnsRecordConfig.
Você pode usar o operador de pipeline para passar um objeto **DnsZone** para esse cmdlet, ou pode passar um **objeto DnsZone** como o parâmetro *Zone* ou, como alternativa, pode especificar a zona pelo nome.
Você pode usar o *parâmetro Confirm* e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.
Se um **RecordSet** correspondente já existir (mesmo nome e tipo de registro), você deverá especificar o parâmetro *Overwrite,* caso contrário, o cmdlet não criará um **novo RecordSet** .

## EXEMPLOS

### Exemplo 1: Criar um RecordSet do tipo A
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records

# When creating a RecordSet containing a single record, the above sequence can also be condensed into a single line:

PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -IPv4Address 1.2.3.4)

# To create a record set containing multiple records, use New-AzDnsRecordConfig to add each record to the $Records array,
# then call New-AzDnsRecordSet, as follows:

PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 1.2.3.4
PS C:\> $Records += New-AzDnsRecordConfig -IPv4Address 5.6.7.8
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este exemplo cria um **RecordSet** denominado www na zona myzone.com.
O conjunto de registros é do tipo A e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.

### Exemplo 2: Criar um RecordSet do tipo AAAA
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv6Address 2001:db8::1
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType AAAA -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este exemplo cria um **RecordSet** denominado www na zona myzone.com.
O conjunto de registros é do tipo AAAA e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.

### Exemplo 3: Criar um RecordSet do tipo CNAME
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Cname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "www" -RecordType CNAME -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este exemplo cria um **RecordSet** denominado www na zona myzone.com.
O conjunto de registros é do tipo CNAME e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.

### Exemplo 4: Criar um RecordSet do tipo MX
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Exchange "mail.microsoft.com" -Preference 5
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "mail" -RecordType MX -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este comando cria um **RecordSet** denominado www na zona myzone.com.
O conjunto de registros é do tipo MX e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.

### Exemplo 5: Criar um RecordSet do tipo NS
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Nsdname ns1-01.azure-dns.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "ns1" -RecordType NS -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este comando cria um **RecordSet** chamado ns1 na zona myzone.com.
O conjunto de registros é do tipo NS e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.

### Exemplo 6: Criar um RecordSet do tipo PTR
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ptrdname www.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "4" -RecordType PTR -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "3.2.1.in-addr.arpa" -DnsRecords $Records
```

Este comando cria um **RecordSet** chamado 4 na zona 3.2.1.in-addr.arpa.
O conjunto de registros é do tipo PTR e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.

### Exemplo 7: Criar um RecordSet do tipo SRV
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Priority 0 -Weight 5 -Port 8080 -Target sipservice.contoso.com
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "_sip._tcp" -RecordType SRV -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este comando cria um **RecordSet** chamado _sip._tcp na zona myzone.com.
O conjunto de registros é do tipo SRV e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS, apontando para o endereço IP 2001.2.3.4.
O serviço (sip) e o protocolo (tcp) são especificados como parte do nome do conjunto de registros, não como parte dos dados do registro.
Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.

### Exemplo 8: Criar um RecordSet do tipo TXT
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Value "This is a TXT Record"
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "text" -RecordType TXT -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este comando cria um **texto chamado RecordSet** na zona myzone.com.
O conjunto de registros é do tipo TXT e tem um TTL de 1 hora (3600 segundos).
Ele contém um único registro DNS.
Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.

### Exemplo 9: Criar um RecordSet no véreo de zona
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "@" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este comando cria um **RecordSet** no véreo (ou raiz) da zona myzone.com.
Para fazer isso, o nome do conjunto de registros é especificado como "@" (incluindo aspas duplas).
Não é possível criar registros CNAME no vérme de uma zona.
Essa é uma restrição dos padrões DNS; não é uma limitação do DNS do Azure.
Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.

### Exemplo 10: Criar um conjunto de registros curinga
```
PS C:\> $Records = @()
PS C:\> $Records += New-AzDnsRecordConfig -Ipv4Address 1.2.3.4
PS C:\> $RecordSet = New-AzDnsRecordSet -Name "*" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords $Records
```

Este comando cria um **RecordSet** chamado * na zona myzone.com.
Este é um conjunto de registros curinga.
Para criar um **RecordSet** usando apenas uma linha de pn_PowerShell_short ou para criar um conjunto de registros com vários registros, consulte o Exemplo 1.

### Exemplo 11: Criar um conjunto de registros vazio
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords @()
```

Este comando cria um **RecordSet** denominado www na zona myzone.com.
O conjunto de registros é do tipo A e tem um TTL de 1 hora (3600 segundos).
Este é um conjunto de registros vazio, que atua como um espaço reservado para o qual você pode adicionar registros posteriormente.

### Exemplo 12: Criar um conjunto de registros e suprimir toda a confirmação
```
PS C:\>$RecordSet = New-AzDnsRecordSet -Name "www" -RecordType A -ResourceGroupName "MyResourceGroup" -TTL 3600 -ZoneName "myzone.com" -DnsRecords (New-AzDnsRecordConfig -Ipv4Address 1.2.3.4) -Confirm:$False -Overwrite
```

Este comando cria um **RecordSet**.
O *parâmetro Overwrite* garante que esse conjunto de registros sobrescreva qualquer conjunto de registros pré-existentes com o mesmo nome e tipo (os registros existentes nesse conjunto de registros são perdidos).
O *parâmetro Confirm* com um valor de $False suprime o prompt de confirmação.

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

### -DnsRecords
Especifica a matriz de registros DNS a incluir no conjunto de registros.
Você pode usar o cmdlet New-AzDnsRecordConfig para criar objetos de registro DNS.
Confira os exemplos para obter mais informações.

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordBase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Metadados
Especifica uma matriz de metadados a ser associada ao RecordSet.
Os metadados são especificados usando pares de valores de nome representados como tabelas de hash, por exemplo @{"dept"="shopping";" env"="production"}.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Especifica o nome do **RecordSet** a ser criado.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
Indica que esse cmdlet substitui o **RecordSet** especificado se ele já existir.

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

### -RecordType
Especifica o tipo de registro DNS a ser criado.
Os valores válidos são:
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- Os registros SOA TXT são criados automaticamente quando a zona é criada e não podem ser criados manualmente.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o grupo de recursos que contém a zona DNS.
Você também deve especificar o parâmetro *ZoneName* para especificar o nome da zona.
Como alternativa, você pode especificar a zona e o grupo de recursos passando um objeto Zona DNS usando o *parâmetro Zone.*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
ID do Recurso de Destino de Alias.

```yaml
Type: System.String
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ttl
Especifica o TTL (Time to Live) para o DNS RecordSet.

```yaml
Type: System.UInt32
Parameter Sets: Fields, Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.UInt32
Parameter Sets: AliasFields, AliasObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Especifica o DnsZone no qual criar o **RecordSet**.
Como alternativa, você pode especificar a zona usando os *parâmetros ZoneName* e *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object, AliasObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Especifica o nome da zona na qual criar o **RecordSet**.
Você também deve especificar o grupo de recursos que contém a zona usando o *parâmetro ResourceGroupName.*
Como alternativa, você pode especificar a zona e o grupo de recursos passando um objeto Zona DNS usando o *parâmetro Zone.*

```yaml
Type: System.String
Parameter Sets: Fields, AliasFields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

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

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.UInt32

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.Collections.Hashtable

### Microsoft.Azure.Commands.Dns.DnsRecordBase[]

## SAÍDAS

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTES
Você pode usar o *parâmetro Confirm* para controlar se esse cmdlet solicita a confirmação.
Por padrão, o cmdlet solicita que você confirme se a variável $ConfirmPreference Windows PowerShell tem um valor médio ou inferior.
Se você especificar *Confirm* ou *Confirm:$True*, este cmdlet solicitará confirmação antes de ser executado.
Se você especificar *Confirm:$False*, o cmdlet não solicitará confirmação.

## LINKS RELACIONADOS

[Add-AzDnsRecordConfig](./Add-AzDnsRecordConfig.md)

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordConfig](./New-AzDnsRecordConfig.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
