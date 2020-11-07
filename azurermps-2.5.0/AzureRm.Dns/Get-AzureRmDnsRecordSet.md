---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 40179CF3-7896-4C45-BC18-4CB653B245B6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4027b13fb398d69bee09be5c0a939ff86a099e39
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786118"
---
# Get-AzureRmDnsRecordSet

## Sinopse
Obtém um conjunto de registros DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Campos
```
Get-AzureRmDnsRecordSet [-Name <String>] -ZoneName <String> -ResourceGroupName <String>
 [-RecordType <RecordType>] [<CommonParameters>]
```

### Objeto
```
Get-AzureRmDnsRecordSet [-Name <String>] -Zone <DnsZone> [-RecordType <RecordType>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRmDnsRecordSet** Obtém o conjunto de registros DNS (Domain Name System) com o nome e o tipo especificados, na zona especificada.

Se você não especificar os parâmetros *Name* ou *RecordType* , esse cmdlet retornará todos os conjuntos de registros do tipo especificado na zona.
Se você especificar o parâmetro *RecordType* , mas não o parâmetro *Name* , esse cmdlet retornará todos os conjuntos de registros do tipo de registro especificado.

Você pode usar o operador de pipeline para passar um objeto **dnsZone** para esse cmdlet, ou pode passar um objeto **dnsZone** como o parâmetro de *zona* ou também pode especificar a zona e o grupo de recursos por nome.

## EXEMPLOS

### Exemplo 1: obter conjuntos de registros com um nome e tipo especificados
```
PS C:\>$RecordSet = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -Name "www" -RecordType A
```

Esse comando obtém o conjunto de registros do tipo de registro um chamado www no grupo de recursos e zona especificados e, em seguida, armazena-o na variável $RecordSet.
Como os parâmetros *Name* e *RecordType* são especificados, apenas um objeto **Recordset** é retornado.

### Exemplo 2: obter conjuntos de registros de um tipo especificado
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com" -RecordType A
```

Esse comando obtém uma matriz de todos os conjuntos de registros do tipo de registro A na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.

### Exemplo 3: obter todos os conjuntos de registros em uma zona
```
PS C:\>$RecordSets = Get-AzureRmDnsRecordSet -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
```

Esse comando obtém uma matriz de todos os conjuntos de registros na zona chamada myzone.com no grupo de recursos chamado MyResource Group e, em seguida, os armazena na variável $RecordSets.

### Exemplo 4: obter todos os conjuntos de registros em uma zona usando um objeto DnsZone
```
PS C:\> $Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $RecordSets = Get-AzureRmDnsRecordSet -Zone $Zone
```

Este exemplo é equivalente ao exemplo 3 acima.
Neste momento, a região é especificada usando um objeto Zone.

## OS

### -Nome
Especifica o nome do **conjunto de registros** a ser obtido.
Se você não especificar o parâmetro *Name* , todos os conjuntos de registros do tipo especificado serão retornados.

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
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
- LOCALIZADO

Se você não especificar o parâmetro *RecordType* , também deverá omitir o parâmetro *Name* . Em seguida, esse cmdlet retorna todos os conjuntos de registros na zona (de todos os nomes e tipos).

```yaml
Type: RecordType
Parameter Sets: (All)
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

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
Type: String
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
Especifica o nome da zona DNS que contém o conjunto de registros a obter.
O grupo de recursos que contém a zona também deve ser especificado, usando o parâmetro *ResourceGroupName* .

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. DNS. DnsZone
Você pode canalizar um objeto **dnsZone** para este cmdlet.
O objeto **dnsZone** representa a zona na qual procurar o objeto **Recordset** .

## EXIBE

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Esse cmdlet retorna um ou mais objetos que representam os conjuntos de registros que são encontrados.
Haverá no máximo um conjunto de **registros** retornado se os parâmetros *Name* e *RecordType* forem especificados; caso contrário, vários objetos **Recordset** serão retornados como uma matriz.

## INFORMA

## LINKS RELACIONADOS

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Remove-AzureRmDnsRecordSet](./Remove-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)


