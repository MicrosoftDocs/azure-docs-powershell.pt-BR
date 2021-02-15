---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: A8E230A0-5057-40BC-81CD-6D397A503A84
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/remove-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsZone.md
ms.openlocfilehash: 633a71788bb9578438053f7a296422e99e7c488e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111903"
---
# Remove-AzDnsZone

## Sinopse
Remove uma zona DNS de um grupo de recursos.

## Sintaxe

### Campos
```
Remove-AzDnsZone -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
Remove-AzDnsZone -Zone <DnsZone> [-Overwrite] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Descrição
O cmdlet **Remove-AzDnsZone** exclui permanentemente uma zona DNS (Sistema de Nomes de Domínio) de um grupo de recursos especificado.
Todos os conjuntos de registros contidos na zona também são excluídos.
Você pode passar um objeto  **DnsZone** usando o parâmetro Nome ou usando o operador de pipeline ou, alternativamente, pode especificar os parâmetros *ZoneName* e *ResourceGroupName.*
Você pode usar o parâmetro Confirmar e $ConfirmPreference variável do Windows PowerShell para controlar se o cmdlet solicita confirmação.
Ao especificar a zona usando um objeto **DnsZone** (passado pelo parâmetro pipeline ou Zona), a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **DnsZone** local foi recuperado (somente as operações diretamente na contagem de recursos de zona DNS como alterações, as operações em conjuntos de registros dentro da zona não o fazem). 
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *Substituir,* que exclui a zona independentemente das alterações simultâneas.

## Exemplos

### Exemplo 1: Remover uma zona
```
PS C:\>Remove-AzDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

Esse comando remove a zona chamada myzone.com do grupo de recursos chamado MyResourceGroup.

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
Especifica o nome da zona DNS que este cmdlet remove.
Você também deve especificar o parâmetro *ResourceGroupName.*
Como alternativa, você pode especificar a zona DNS usando o *parâmetro* Zona.

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

### -Substituir
Ao especificar a zona usando um objeto **DnsZone** (passado pelo parâmetro pipeline ou Zona), a zona não será excluída se tiver sido alterada no DNS do Azure desde que o objeto **DnsZone** local foi recuperado (somente as operações diretamente na contagem de recursos de zona DNS como alterações, as operações em conjuntos de registros dentro da zona não o fazem). 
Isso fornece proteção para alterações de zona simultâneas.
Isso pode ser suprimido usando o parâmetro *Substituir,* que exclui a zona independentemente das alterações simultâneas.

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
Passthru

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
Você também deve especificar o parâmetro *ZoneName.*
Como alternativa, você pode especificar a zona DNS usando um objeto **DnsZone,** passado pelo pipeline ou pelo parâmetro *Zona.*

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

### -Zona
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

### -Confirmar
Solicita confirmação antes de executar o cmdlet.

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
Mostra o que acontece se o cmdlet for executado.
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

## Entradas

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

## Saídas

### System.Boolean

## Notas
Devido ao potencialmente alto impacto da exclusão de uma zona DNS, por padrão, esse cmdlet solicita confirmação se a variável $ConfirmPreference Windows PowerShell tiver algum valor diferente de Nenhum.
Se você especificar *Confirmar* ou *Confirmar:$True,* este cmdlet solicitará que você confirme antes de ser executado.
Se você especificar *Confirm:$False,* o cmdlet não solicitará confirmação. 

## LINKS RELACIONADOS

[Get-AzDnsZone](./Get-AzDnsZone.md)

[New-AzDnsZone](./New-AzDnsZone.md)

[Set-AzDnsZone](./Set-AzDnsZone.md)
