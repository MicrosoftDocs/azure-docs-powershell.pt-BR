---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: f6f117b5a748df9f235d1ba3413306c067db4e67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892700"
---
# Update-AzSqlServerAdvancedThreatProtectionSetting

## SYNOPSIS
Define configurações avançadas de proteção contra ameaças em um servidor.

## SINTAXE

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
O cmdlet **Update-AzSqlServerAdvancedThreatProtectionSetting** define uma configuração avançada de proteção contra ameaças em um servidor do Azure SQL.
Para habilitar a proteção avançada contra ameaças em um servidor, as configurações de auditoria devem ser habilitadas nesse servidor.
Para usar esse cmdlet, especifique os *parâmetros ResourceGroupName* e ServerName para identificar o servidor.

## EXEMPLOS

### Exemplo 1: definir as configurações avançadas de proteção contra ameaças para um banco de dados
```powershell
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

Este comando define as configurações avançadas de proteção contra ameaças para um servidor chamado Server01.

### Exemplo 2

Define configurações avançadas de proteção contra ameaças em um servidor. (gerado automaticamente)

```powershell
<!-- Aladdin Generated Example --> 
Update-AzSqlServerAdvancedThreatProtectionSetting -EmailAdmins $false -ResourceGroupName 'ResourceGroup11' -RetentionInDays <UInt32> -ServerName 'Server01' -StorageAccountName 'mystorageAccount'
```

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

### -EmailAdmins
Especifica se as configurações avançadas de proteção contra ameaças contatarão administradores usando email.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExcludedDetectionType
Especifica uma matriz de tipos de detecção a ser excluída das configurações.
Os valores aceitáveis para este parâmetro são:
- Sql_Injection
- Sql_Injection_Vulnerability
- Access_Anomaly
- Nenhum

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotificationRecipientsEmails
Especifica uma lista separada por ponto-e-vírgula de endereços de email para os quais as configurações enviam alertas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Retorna um objeto que representa o item com o qual você está trabalhando.
Por padrão, esse cmdlet não gera nenhuma saída.

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
Especifica o nome do grupo de recursos ao qual o servidor pertence.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
O número de dias de retenção para os logs de auditoria

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Especifica o nome do servidor.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Especifica o nome da conta de armazenamento a ser usada. Caracteres curinga não são permitidos. Esse parâmetro não é necessário. Quando esse parâmetro não for fornecido, o cmdlet usará a conta de armazenamento que foi definida anteriormente como parte das configurações avançadas de proteção contra ameaças do banco de dados. Se essa for a primeira vez que as configurações de detecção de ameaças de banco de dados são definidas e esse parâmetro não é fornecido, o cmdlet falhará.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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
Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]

### System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## SAÍDAS

### Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel

## NOTES

## LINKS RELACIONADOS

[Get-AzSqlServerThreatDetectionsettings](./Get-AzSqlServerThreatDetectionsettings.md)

[Remove-AzSqlServerThreatDetectionsettings](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[SQL documentação do banco de dados](https://docs.microsoft.com/azure/sql-database/)
