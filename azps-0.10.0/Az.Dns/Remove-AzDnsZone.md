---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: bc77e2c69f285f0acab0bed8e6a40592374ebd18
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775916"
---
# Remove-AzDnsZone

## Sinopse
Remove uma zona DNS de um grupo de recursos.

## SYNTAX

### Campos
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Objeto
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-Force] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzDnsZone** exclui permanentemente uma zona de sistema de nomes de domínio (DNS) de um grupo de recursos especificado.
Todos os conjuntos de registros contidos na zona também são excluídos.

Você pode passar um objeto **dnsZone** usando o parâmetro *Name* ou usando o operador pipeline ou, como alternativa, pode especificar os parâmetros *zonename* e *ResourceGroupName* .

Você pode usar o parâmetro Confirm e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.

Ao especificar a zona usando um objeto **dnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não é excluída se foi alterada no Azure DNS, pois o objeto **dnsZone** local foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.

## EXEMPLOS

### Exemplo 1: remover uma zona
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Esse comando Remove a zona chamada myzone.com do grupo de recursos chamado MyResource Group.

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
Especifica o nome da zona DNS que este cmdlet Remove.
Você também deve especificar o parâmetro *ResourceGroupName* .

Você também pode especificar a zona DNS usando o parâmetro *Zone* .

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

### -Substituir
Ao especificar a zona usando um objeto **dnsZone** (passado por meio do parâmetro pipeline ou *Zone* ), a zona não é excluída se foi alterada no Azure DNS, pois o objeto **dnsZone** local foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, operações em conjuntos de registros dentro da zona não).
Isso fornece proteção para alterações de zona simultâneas.

Isso pode ser suprimido usando o parâmetro *overwrite* , que exclui a zona independentemente das alterações simultâneas.

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

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a zona a ser removida.
Você também deve especificar o parâmetro *zonename* .

Como alternativa, você pode especificar a zona DNS usando um objeto **dnsZone** , passado pelo pipeline ou pelo parâmetro *Zone* .

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
Especifica a zona DNS a ser excluída.
O objeto **dnsZone** aprovado também pode ser passado pelo pipeline.

Você também pode especificar a zona DNS a ser excluída usando os parâmetros *zonename* e *ResourceGroupName* .

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Microsoft. Azure. Commands. DNS. DnsZone
Você pode canalizar um objeto **dnsZone** para este cmdlet.

## EXIBE

### Nenhuma
Esse cmdlet não gera nenhuma saída.

## INFORMA
Devido ao impacto potencialmente alto na exclusão de uma zona DNS, por padrão, esse cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem qualquer valor diferente de None.

Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.
Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação. 

## LINKS RELACIONADOS

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
