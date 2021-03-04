---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 8c1058345d78289a7601fa390e202e428554b50c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889486"
---
# Remove-AzDnsZone

## SYNOPSIS
Remove uma zona DNS de um grupo de recursos.

## SINTAXE

### Fields
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Remove-AzDnsZone** exclui permanentemente uma zona DNS (Sistema de Nomes de Domínio) de um grupo de recursos especificado.
Todos os conjuntos de registros contidos na zona também são excluídos.
Você pode passar um **objeto DnsZone** usando o parâmetro *Name* ou usando o operador de pipeline ou, como alternativa, pode especificar os parâmetros *ZoneName* e *ResourceGroupName.*
Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.
Ao especificar a zona usando um objeto **DnsZone** (passado por meio do pipeline ou do parâmetro *Zone),* a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **DnsZone** local foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, as operações nos conjuntos de registros dentro da zona não.
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *Overwrite,* que exclui a zona independentemente de alterações simultâneas.

## EXEMPLOS

### Exemplo 1: Remover uma zona
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Este comando remove a zona denominada myzone.com do grupo de recursos chamado MyResourceGroup.

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
Especifica o nome da zona DNS que esse cmdlet remove.
Você também deve especificar o *parâmetro ResourceGroupName.*
Como alternativa, você pode especificar a zona DNS usando o *parâmetro Zone.*

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

### -Overwrite
Ao especificar a zona usando um objeto **DnsZone** (passado por meio do pipeline ou do parâmetro *Zone),* a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **DnsZone** local foi recuperado (somente operações diretamente na contagem de recursos de zona DNS como alterações, as operações nos conjuntos de registros dentro da zona não.
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *Overwrite,* que exclui a zona independentemente de alterações simultâneas.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
passthru

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

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a zona a ser removido.
Você também deve especificar o *parâmetro ZoneName.*
Como alternativa, você pode especificar a zona DNS usando um **objeto DnsZone,** passado pelo pipeline ou pelo *parâmetro Zone.*

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
Especifica a zona DNS a ser excluído.
O **objeto DnsZone** passado também pode ser passado por meio do pipeline.
Como alternativa, você pode especificar a zona DNS a ser excluído usando os parâmetros *ZoneName* e *ResourceGroupName.*

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

## SAÍDAS

### System.Boolean

## NOTES
Devido ao impacto potencialmente alto da exclusão de uma zona DNS, por padrão, esse cmdlet solicita a confirmação se a variável $ConfirmPreference Windows PowerShell tiver qualquer valor diferente de None.
Se você especificar *Confirm* ou *Confirm:$True*, este cmdlet solicitará confirmação antes de ser executado.
Se você especificar *Confirm:$False*, o cmdlet não solicitará confirmação. 

## LINKS RELACIONADOS

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
