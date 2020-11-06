---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 9be5ca678b690400e044b9627fd455ea2cbc29c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596560"
---
# Get-AzDnsZone

## Sinopse
Obtém uma zona DNS.

## SYNTAX

### Padrão (padrão)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resource
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzDnsZone** Obtém uma zona de sistema de nome de domínio (DNS) do grupo de recursos especificado.
Se você especificar o parâmetro *Name* , um único objeto **dnsZone** será retornado.
Se você não especificar o parâmetro *Name* , será retornada uma matriz contendo todas as zonas do grupo de recursos especificado.
Você pode usar o objeto **dnsZone** para atualizar a zona, por exemplo, você pode adicionar objetos **Recordset** a ele.

## EXEMPLOS

### Exemplo 1: obter uma zona
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Este exemplo obtém a zona DNS chamada myzone.com do grupo de recursos especificado e armazena-a na variável $Zone.

### Exemplo 2: obter todas as zonas em um grupo de recursos
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

Este exemplo obtém todas as zonas DNS no grupo de recursos especificado e, em seguida, as armazena na variável $Zones.

### Exemplo 3: obter todas as zonas em uma assinatura
```
PS C:\> $Zones = Get-AzDnsZone
```

Este exemplo obtém todas as zonas DNS na assinatura atual do Azure e as armazena na variável $Zones.

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
Especifica o nome da zona DNS a ser obtida.
Se você não especificar um valor para o parâmetro *Name* , esse cmdlet obtém todas as zonas DNS no grupo de recursos especificado.
Se você também omitir o parâmetro *ResourceGroupName* , esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a zona DNS a ser obtida.
Se você não especificar o *ResourceGroupName* , também deverá omitir o parâmetro *Name* .
Nesse caso, esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.

```yaml
Type: System.String
Parameter Sets: ResourceGroup
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

## EXIBE

### Microsoft. Azure. Commands. DNS. DnsZone

## INFORMA

## LINKS RELACIONADOS

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
