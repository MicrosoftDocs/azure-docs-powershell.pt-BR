---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: E37ADC54-A37B-41BF-BE94-9E4052C234BB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 347f590ecd6e2825264e6bb0b980dd94450b0f06
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785773"
---
# Set-AzureRmDnsZone

## Sinopse
Atualiza as propriedades de uma zona DNS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### Campos
```
Set-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Objeto
```
Set-AzureRmDnsZone -Zone <DnsZone> [-Overwrite] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmDnsZone** atualiza a zona DNS especificada no serviço DNS do Azure.
Esse cmdlet não atualiza os conjuntos de registros na zona.

Você pode passar um objeto **dnsZone** como um parâmetro ou usar o operador pipeline ou, como alternativa, pode especificar os parâmetros *zonename* e *ResourceGroupName* .

Você pode usar o parâmetro *Confirm* e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.

Ao passar uma zona DNS como um objeto (usando o objeto Zone ou via pipeline), ele não será atualizado se ele tiver sido alterado no Azure DNS desde que o objeto DnsZone local foi recuperado. Isso fornece proteção para alterações simultâneas. Você pode suprimir esse comportamento com o parâmetro *overwrite* , que atualiza a zona independentemente das alterações simultâneas.

## EXEMPLOS

### Exemplo 1: atualizar uma zona DNS
```
PS C:\>$Zone = Get-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> $Zone.Tags = @(@{"Name"="Dept"; "Value"="Electrical"})
PS C:\> Set-AzureRmDnsZone -Zone $Zone
```

O primeiro comando obtém a zona chamada myzone.com do grupo de recursos especificado e, em seguida, armazena-a na variável $Zone.

O segundo comando atualiza as marcas para $Zone.

O comando final confirma a alteração.

### Exemplo 2: atualizar marcas para uma zona
```
PS C:\>Set-AzureRmDNSZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com" -Tag @(@{"Name"="Dept"; "Value"="Electrical"})
```

Esse comando atualiza as marcas da zona chamada myzone.com sem primeiro obter a zona explicitamente.

## OS

### -Nome
Especifica o nome da zona DNS a ser atualizada.

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
Ao passar uma zona DNS como um objeto (usando o objeto Zone ou via pipeline), ele não será atualizado se ele tiver sido alterado no Azure DNS desde que o objeto DnsZone local foi recuperado. Isso fornece proteção para alterações simultâneas. Você pode suprimir esse comportamento com o parâmetro *overwrite* , que atualiza a zona independentemente das alterações simultâneas.

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

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a zona a ser atualizada.
Você também deve especificar o parâmetro zonename.

Você também pode especificar a zona usando um objeto DnsZone com o parâmetro *Zone* ou o pipeline.

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

### -Marca
Pares de valores chave na forma de uma tabela de hash. Por exemplo:

@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: Fields
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Zone
Especifica a zona DNS a ser atualizada.

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
Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado. O cmdlet não é executado.

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

### Microsoft. Azure. Commands. DNS. DnsZone
Esse cmdlet retorna um objeto DnsZone que representa a zona DNS atualizada com um novo ETag.

## INFORMA
Você pode usar o parâmetro *Confirm* para controlar se esse cmdlet solicita confirmação.
Por padrão, o cmdlet solicita confirmação se a variável $ConfirmPreference do Windows PowerShell tem um valor médio ou menor.

Se você especificar *Confirm* ou *Confirm: $true* , esse cmdlet solicitará confirmação antes de ser executado.
Se você especificar *Confirm: $false* , o cmdlet não solicitará confirmação.

## LINKS RELACIONADOS

[Get-AzureRmDnsZone](./Get-AzureRmDnsZone.md)

[New-AzureRmDnsZone](./New-AzureRmDnsZone.md)

[Remove-AzureRmDnsZone](./Remove-AzureRmDnsZone.md)
