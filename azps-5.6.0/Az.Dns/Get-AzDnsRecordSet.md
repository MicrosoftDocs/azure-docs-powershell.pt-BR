---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 447b1e32473d00504446478a9efaa5634e3b1c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889498"
---
# Get-AzDnsRecordSet

## SYNOPSIS
Obtém um conjunto de registros DNS.

## SINTAXE

### Fields
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objeto
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Get-AzDnsRecordSet** obtém o registro DNS (Sistema de Nomes de Domínio) definido com o nome e o tipo especificados, na zona especificada.
Se você não especificar os parâmetros *Name* ou *RecordType,* este cmdlet retornará todos os conjuntos de registros do tipo especificado na zona.
Se você especificar o *parâmetro RecordType,* mas não o parâmetro *Name,* este cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.
Você pode usar o operador de pipeline para passar um objeto **DnsZone** para esse cmdlet, ou pode passar um **objeto DnsZone** como o parâmetro *Zone* ou, como alternativa, pode especificar a zona e o grupo de recursos pelo nome.

## EXEMPLOS

### Exemplo 1: Obter conjuntos de registros com um nome e tipo especificados
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Este comando obtém o conjunto de registros do tipo de registro A denominado www no grupo de recursos especificado e zona e o armazena na variável $RecordSet.
Como os *parâmetros Name* e *RecordType* são especificados, apenas um **objeto RecordSet** é retornado.

### Exemplo 2: Obter conjuntos de registros de um tipo especificado
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Este comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona chamada myzone.com no grupo de recursos chamado MyResourceGroup e os armazena na variável $RecordSets.

### Exemplo 3: Obter todos os conjuntos de registros em uma zona
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Esse comando obtém uma matriz de todos os conjuntos de registros na zona chamada myzone.com no grupo de recursos chamado MyResourceGroup e os armazena na variável $RecordSets.

### Exemplo 4: Obter todos os conjuntos de registros em uma zona usando um objeto DnsZone
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Este exemplo equivale ao Exemplo 3 acima.
Desta vez, a zona é especificada usando um objeto zone.

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

### -Name
Especifica o nome do **RecordSet** a ser definido.
Se você não especificar o parâmetro *Name,* todos os conjuntos de registros do tipo especificado serão retornados.

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecordType
Especifica o tipo de registro DNS que esse cmdlet obtém.
Os valores válidos são: 
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SOA
- SRV
- TXT Se você não especificar o parâmetro *RecordType,* também deverá omitir o *parâmetro Name.* Em seguida, este cmdlet retorna todos os conjuntos de registros na zona (de todos os nomes e tipos).

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Dns.Models.RecordType]
Parameter Sets: (All)
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o grupo de recursos que contém a zona DNS.
O nome da zona também deve ser especificado, usando o *parâmetro ZoneName.*
Como alternativa, você pode especificar a zona e o grupo de recursos passando um **objeto DnsZone** usando o *parâmetro Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Especifica a zona DNS que contém o conjunto de registros que este cmdlet obtém.
Como alternativa, você pode especificar a zona usando os *parâmetros ZoneName* e *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Especifica o nome da zona DNS que contém o conjunto de registros a ser definido.
O grupo de recursos que contém a zona também deve ser especificado, usando o *parâmetro ResourceGroupName.*
Como alternativa, você pode especificar a zona e o grupo de recursos passando um objeto Zona DNS usando o *parâmetro Zone.*

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUTS

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### System.Nullable'1[[Microsoft.Azure.Management.Dns.Models.RecordType, Microsoft.Azure.Management.Dns, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## SAÍDAS

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## NOTES

## LINKS RELACIONADOS

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


