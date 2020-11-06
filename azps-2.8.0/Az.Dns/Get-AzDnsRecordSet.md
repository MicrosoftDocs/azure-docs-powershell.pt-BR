---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsRecordSet.md
ms.openlocfilehash: 37cd1f7b00cbfae6421b5dab06ce87c0f462434c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596563"
---
# Get-AzDnsRecordSet

## Sinopse
Obtém um conjunto de registros DNS.

## SYNTAX

### Campos
```
Get-AzDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Objeto
```
Get-AzDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzDnsRecordSet** Obtém o conjunto de registros DNS (Domain Name System) com o nome e o tipo especificados, na zona especificada.
Se você não especificar os parâmetros *Name* ou *RecordType* , esse cmdlet retornará todos os conjuntos de registros do tipo especificado na zona.
Se você especificar o parâmetro *RecordType* , mas não o parâmetro *Name* , esse cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.
Você pode usar o operador de pipeline para passar um objeto **dnsZone** para esse cmdlet, ou pode passar um objeto **dnsZone** como o parâmetro de *zona* ou também pode especificar a zona e o grupo de recursos por nome.

## EXEMPLOS

### Exemplo 1: obter conjuntos de registros com um nome e tipo especificados
```
PS C:\>$RecordSet = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Esse comando obtém o conjunto de registros do tipo de registro um chamado www no grupo de recursos e zona especificados e, em seguida, armazena-o na variável $RecordSet.
Como os parâmetros *Name* e *RecordType* são especificados, apenas um objeto **Recordset** é retornado.

### Exemplo 2: obter conjuntos de registros de um tipo especificado
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Esse comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.

### Exemplo 3: obter todos os conjuntos de registros em uma zona
```
PS C:\>$RecordSets = Get-AzDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Esse comando obtém uma matriz de todos os conjuntos de registros na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.

### Exemplo 4: obter todos os conjuntos de registros em uma zona usando um objeto DnsZone
```
PS C:\> $Zone = Get-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzDnsRecordSet -Zone $Zone
```

Este exemplo é equivalente ao exemplo 3 acima.
Neste momento, a região é especificada usando um objeto Zone.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -Nome
Especifica o nome do **conjunto de registros** a ser obtido.
Se você não especificar o parâmetro *Name* , todos os conjuntos de registros do tipo especificado serão retornados.

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
Especifica o tipo de registro DNS que este cmdlet obtém.
Os valores válidos são: 
- Um
- AAAA
- CNAME
- MX
- SÉRIE
- PTR
- SOA
- SRV
- TXT se você não especificar o parâmetro *RecordType* , também deverá omitir o parâmetro *Name* . Em seguida, esse cmdlet retorna todos os conjuntos de registros na zona (de todos os nomes e tipos).

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
O nome da zona também deve ser especificado, usando o parâmetro *zonename* .
Você também pode especificar a zona e o grupo de recursos passando um objeto **dnsZone** usando o parâmetro *Zone* .

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
Especifica a zona DNS que contém o conjunto de registros que esse cmdlet obtém.
Você também pode especificar a zona usando os parâmetros *zonename* e *ResourceGroupName* .

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

### -Zonename
Especifica o nome da zona DNS que contém o conjunto de registros a obter.
O grupo de recursos que contém a zona também deve ser especificado, usando o parâmetro *ResourceGroupName* .
Você também pode especificar a zona e o grupo de recursos, passando um objeto de zona DNS usando o parâmetro *Zone* .

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### Microsoft. Azure. Commands. DNS. DnsZone

### System. Nullable ' 1 [[Microsoft. Azure. Management. DNS. Models. RecordType, Microsoft. Azure. Management. DNS, Version = 3.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## EXIBE

### Microsoft. Azure. Commands. DNS. DnsRecordSet

## INFORMA

## LINKS RELACIONADOS

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Remove-AzDnsRecordSet](./Remove-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)


