---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: ''
schema: 2.0.0
ms.openlocfilehash: b86ad0382fa7f87ac8aabb6b026b84d5a879f8ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786110"
---
# Remove-AzureRmDnsRecordSet

## Sinopse
Exclui um conjunto de registros.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Campos
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String>
 -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Misto
```
Remove-AzureRmDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-Force] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
Remove-AzureRmDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureRmDnsRecordSet** exclui o conjunto de registros especificado da zona especificada.
Não é possível excluir registros de SOA ou de servidor de nomes (NS) criados automaticamente na zona Apex.

Você pode passar um objeto **Recordset** para esse cmdlet usando o operador pipeline ou como um parâmetro.
Para identificar um registro definido por nome e tipo sem usar um objeto **Recordset** , você deve passar a zona como um objeto **dnsZone** para esse cmdlet usando o operador pipeline ou como um parâmetro ou, como alternativa, você pode especificar os parâmetros *zonename* e *ResourceGroupName* .

Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.

Ao especificar o conjunto de registros usando um objeto **Recordset** , o conjunto de registros não é excluído se foi alterado no Azure DNS desde que o objeto **Recordset** local foi recuperado.
Isso fornece proteção para alterações simultâneas.
Você pode suprimir isso usando o parâmetro *overwrite* , que exclui o conjunto de registros independentemente de alterações simultâneas.

## EXEMPLOS

### Exemplo 1: remover um conjunto de registros
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet
```

O primeiro comando obtém o conjunto de registros especificado e, em seguida, armazena-o na variável $RecordSet. O segundo comando Remove o conjunto de registros no $RecordSet.

### Exemplo 2: remover um conjunto de registros e suprimir todas as confirmações
```
PS C:\> $RecordSet = Get-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzureRmDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzureRmDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

O primeiro comando obtém o conjunto de registros especificado.

O segundo comando exclui o conjunto de registros, mesmo que ele tenha sido alterado enquanto isso.
As solicitações de confirmação são suprimidas.

## OS

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

### -Nome
Especifica o nome do **conjunto de registros** a ser removido.
Ao especificar o registro definido por nome, a zona de DNS deve ser especificada usando o parâmetro de *zona* ou os parâmetros *zonename* e *ResourceGroupName* .

Como alternativa, o conjunto de registros pode ser especificado usando um objeto **Recordset** , passado usando o parâmetro *Recordset* .

```yaml
Type: String
Parameter Sets: Fields, Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Substituir
Ao especificar o conjunto de registros usando um objeto **Recordset** , o conjunto de registros não é excluído se foi alterado no Azure DNS desde que o objeto **Recordset** local foi recuperado.
Isso fornece proteção para alterações simultâneas.
Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui o conjunto de registros independentemente das alterações simultâneas.

```yaml
Type: SwitchParameter
Parameter Sets: Object
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
PassThru

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
Especifica o objeto **Recordset** a ser removido.

Como alternativa, o conjunto de registros pode ser especificado usando os parâmetros *Name* e *Zone* ou usando os parâmetros *Name* , *zonename* e *ResourceGroupName* .

```yaml
Type: DnsRecordSet
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecordType
Especifica o tipo de registro DNS.

Os valores válidos são:

- Um
- AAAA
- CNAME
- MX
- SÉRIE
- PTR
- SRV
- LOCALIZADO

Os registros SOA são excluídos automaticamente quando a zona é excluída.
Não é possível excluir manualmente os registros SOA.

```yaml
Type: RecordType
Parameter Sets: Fields, Mixed
Aliases: 
Accepted values: A, AAAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o grupo de recursos que contém a zona DNS que contém o **conjunto de registros** a ser excluído.
Esse parâmetro é aplicável somente quando o conjunto de registros e a zona DNS são especificados usando os parâmetros *Name* e *zonename* .

Como alternativa, você pode especificar o conjunto de registros usando o parâmetro *Recordset* ou os parâmetros *Name* e *Zone* .

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
Especifica a zona DNS que contém o **conjunto de registros** a ser excluído.
Esse parâmetro é aplicável somente quando se especifica o conjunto de registros usando o parâmetro *Name* .

Como alternativa, você pode especificar o conjunto de registros usando o parâmetro *Recordset* ou os parâmetros *Name* , *zonename* e *ResourceGroupName* .

```yaml
Type: DnsZone
Parameter Sets: Mixed
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Zonename
Especifica o nome da zona que contém o **conjunto de registros** a ser excluído.
Você também deve especificar os parâmetros *Name* e *ResourceGroupName* .

Como alternativa, o conjunto de registros pode ser especificado usando o parâmetro *Recordset* ou os parâmetros *Name* e *Zone* .

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

### Microsoft. Azure. Commands. DNS. DnsRecordSet
Você pode canalizar um objeto **Recordset** para este cmdlet.

## EXIBE

### Nenhuma
Esse cmdlet não gera nenhuma saída.

## INFORMA
Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.
Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.

Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.
Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.

## LINKS RELACIONADOS

[Get-AzureRmDnsRecordSet](./Get-AzureRmDnsRecordSet.md)

[New-AzureRmDnsRecordSet](./New-AzureRmDnsRecordSet.md)

[Set-AzureRmDnsRecordSet](./Set-AzureRmDnsRecordSet.md)
