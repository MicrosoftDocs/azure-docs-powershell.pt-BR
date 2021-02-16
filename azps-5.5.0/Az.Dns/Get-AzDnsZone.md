---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117673"
---
# Get-AzDnsZone

## Sinopse
Obtém uma zona DNS.

## Sintaxe

### Padrão (Padrão)
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Grupo de Recursos
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Descrição
O cmdlet **Get-AzDnsZone** obtém uma zona DNS (Sistema de Nomes de Domínio) do grupo de recursos especificado.
Se você especificar o *parâmetro Nome,* um único objeto **DnsZone** será retornado.
Se você não especificar o parâmetro *Nome,* uma matriz que contém todas as zonas no grupo de recursos especificado será retornada.
Você pode usar o **objeto DnsZone** para atualizar a zona, por exemplo, você pode adicionar objetos **RecordSet** a ele.

## Exemplos

### Exemplo 1: Obter uma zona
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

Este exemplo obtém a zona DNS nomeada myzone.com do grupo de recursos especificado e a armazena na variável $Zone dados.

### Exemplo 2: Obter todas as zonas em um grupo de recursos
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

Este exemplo obtém todas as zonas DNS no grupo de recursos especificado e, em seguida, as armazena na variável $Zones dados.

### Exemplo 3: Obter todas as zonas em uma assinatura
```
PS C:\> $Zones = Get-AzDnsZone
```

Este exemplo obtém todas as zonas DNS na assinatura atual do Azure e as armazena na variável $Zones usuário.

## Parâmetros

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure

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
Especifica o nome da zona DNS a ser obter.
Se você não especificar um  valor para o parâmetro Nome, esse cmdlet obtém todas as zonas DNS no grupo de recursos especificado.
Se você também omitir o parâmetro *ResourceGroupName,* esse cmdlet obtém todas as zonas DNS na assinatura atual do Azure.

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
Especifica o nome do grupo de recursos que contém a zona DNS para obter.
Se você não especificar o *ResourceGroupName,* também deverá omitir o *parâmetro* Nome.
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Entradas

### System.String

## Saídas

### Microsoft.Azure.Commands.Dns.DnsZone

## Notas

## LINKS RELACIONADOS

[New-AzDnsZone](./New-AzDnsZone.md)

[Remove-AzDnsZone](./Remove-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
