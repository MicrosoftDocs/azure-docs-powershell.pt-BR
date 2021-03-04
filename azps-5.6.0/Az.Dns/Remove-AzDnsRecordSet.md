---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: 505562A4-30BC-44E7-94EF-579763B8D794
online version: https://docs.microsoft.com/powershell/module/az.dns/remove-azdnsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Remove-AzDnsRecordSet.md
ms.openlocfilehash: ab4f7bf6693eda413587b572832706d617b3e683
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889490"
---
# Remove-AzDnsRecordSet

## SYNOPSIS
Exclui um conjunto de registros.

## SINTAXE

### Fields
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -ZoneName <String> -ResourceGroupName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Mixed
```
Remove-AzDnsRecordSet -Name <String> -RecordType <RecordType> -Zone <DnsZone> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Objeto
```
Remove-AzDnsRecordSet -RecordSet <DnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Remove-AzDnsRecordSet** exclui o conjunto de registros especificado da zona especificada.
Não é possível excluir registros SOA ou NS (servidor de nomes) que são criados automaticamente no apex de zona.
Você pode passar um **objeto RecordSet** para esse cmdlet usando o operador de pipeline ou como parâmetro.
Para identificar um registro definido por nome e tipo sem usar um **objeto RecordSet,** você deve passar a zona como um **objeto DnsZone** para esse cmdlet usando o operador de pipeline ou como parâmetro ou, como alternativa, você pode especificar os parâmetros *ZoneName* e *ResourceGroupName.*
Você pode usar o parâmetro Confirm e $ConfirmPreference Windows PowerShell para controlar se o cmdlet solicita a confirmação.
Ao especificar o conjunto de registros usando um **objeto RecordSet,** o conjunto de registros não será excluído se tiver sido alterado no DNS do Azure desde que o objeto **RecordSet** local foi recuperado.
Isso fornece proteção para alterações simultâneas.
Você pode suprimir isso usando o parâmetro *Overwrite,* que exclui o conjunto de registros independentemente de alterações simultâneas.

## EXEMPLOS

### Exemplo 1: Remover um conjunto de registros
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet
```

O primeiro comando obtém o conjunto de registros especificado e o armazena na variável $RecordSet. O segundo comando remove o conjunto de registros em $RecordSet.

### Exemplo 2: remover um conjunto de registros e suprimir toda a confirmação
```
PS C:\> $RecordSet = Get-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

O primeiro comando obtém o conjunto de registros especificado.
O segundo comando exclui o conjunto de registros, mesmo que tenha sido alterado enquanto isso.
Os prompts de confirmação são suprimidos.

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
Especifica o nome do **RecordSet** a ser removido.
Ao especificar o registro definido pelo nome, a zona DNS deve ser especificada usando o parâmetro *Zone* ou os parâmetros *ZoneName* e *ResourceGroupName.*
Como alternativa, o conjunto de registros pode ser especificado usando um **objeto RecordSet,** passado usando o *parâmetro RecordSet.*

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Overwrite
Ao especificar o conjunto de registros usando um **objeto RecordSet,** o conjunto de registros não será excluído se tiver sido alterado no DNS do Azure desde que o objeto **RecordSet** local foi recuperado.
Isso fornece proteção para alterações simultâneas.
Isso pode ser suprimido usando o parâmetro *Overwrite,* que exclui o conjunto de registros independentemente de alterações simultâneas.

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

### -RecordSet
Especifica o **objeto RecordSet** a ser removido.
Como alternativa, o conjunto de registros pode ser especificado usando os parâmetros *Name* e *Zone* ou usando os parâmetros *Name,* *ZoneName* e *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsRecordSet
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
- A
- AAAA
- CNAME
- MX
- NS
- PTR
- SRV
- Os registros SOA TXT são excluídos automaticamente quando a zona é excluída.
Não é possível excluir manualmente os registros SOA.

```yaml
Type: Microsoft.Azure.Management.Dns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CAA, CNAME, MX, NS, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o grupo de recursos que contém a zona DNS que contém **o RecordSet** a ser excluído.
Esse parâmetro só é aplicável quando o conjunto de registros e a zona DNS são especificados usando os parâmetros *Name* e *ZoneName.*
Como alternativa, você pode especificar o conjunto de registros usando o *parâmetro RecordSet* ou os *parâmetros Name* e *Zone.*

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
Especifica a zona DNS que contém **o RecordSet** a ser excluído.
Esse parâmetro só é aplicável ao especificar o conjunto de registros usando o *parâmetro* Name.
Como alternativa, você pode especificar o conjunto de registros usando o parâmetro *RecordSet* ou os parâmetros *Name*, *ZoneName* e *ResourceGroupName.*

```yaml
Type: Microsoft.Azure.Commands.Dns.DnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ZoneName
Especifica o nome da zona que contém **o RecordSet** a ser excluído.
Você também deve especificar os parâmetros *Name* e *ResourceGroupName.*
Como alternativa, o conjunto de registros pode ser especificado usando o parâmetro *RecordSet* ou os *parâmetros Name* e *Zone.*

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

### Microsoft.Azure.Management.Dns.Models.RecordType

### System.String

### Microsoft.Azure.Commands.Dns.DnsZone

### Microsoft.Azure.Commands.Dns.DnsRecordSet

## SAÍDAS

### System.Boolean

## NOTES
Você pode usar o *parâmetro Confirm* para controlar se esse cmdlet solicita a confirmação.
Por padrão, o cmdlet solicita que você confirme se a variável $ConfirmPreference Windows PowerShell tem um valor médio ou inferior.
Se você especificar *Confirm* ou *Confirm:$True*, este cmdlet solicitará confirmação antes de ser executado.
Se você especificar *Confirm:$False*, o cmdlet não solicitará confirmação.

## LINKS RELACIONADOS

[Get-AzDnsRecordSet](./Get-AzDnsRecordSet.md)

[New-AzDnsRecordSet](./New-AzDnsRecordSet.md)

[Set-AzDnsRecordSet](./Set-AzDnsRecordSet.md)
