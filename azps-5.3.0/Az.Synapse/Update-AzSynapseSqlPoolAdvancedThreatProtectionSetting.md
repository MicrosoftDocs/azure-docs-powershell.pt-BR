---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpooladvancedthreatprotectionsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 87c3f0e2e86f2867d659b26b5acc9df5a6dfe8c7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271268"
---
# Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting

## Sinopse
Define as configurações avançadas de proteção contra ameaças em um pool do SQL.

## SYNTAX

### UpdateByNameParameterSet (padrão)
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>]
 [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateByParentObjectParameterSet
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateByInputObjectParameterSet
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -InputObject <PSSynapseSqlPool>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateByResourceIdParameterSet
```
Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -ResourceId <String>
 [-NotificationRecipientsEmail <String>] [-EmailAdmin <Boolean>] [-ExcludedDetectionType <String[]>]
 [-StorageAccountName <String>] [-RetentionInDays <UInt32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting** define as configurações avançadas de proteção contra ameaças em um pool SQL do Azure Synapse Analytics.
Para habilitar a proteção avançada contra ameaças em um pool SQL, as configurações de auditoria devem estar habilitadas nesse pool do SQL.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Update-AzSynapseSqlPoolAdvancedThreatProtectionSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

Esse comando define as configurações avançadas de proteção contra ameaças para um pool SQL chamado ContosoSqlPool no espaço de trabalho chamado ContosoWorkspace.

## OS

### -AsJob
Executar o cmdlet em segundo plano

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

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

### -EmailAdmin
Define se os administradores de email devem ser enviados.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: EmailAdmins

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedDetectionType
Tipos de detecção a serem excluídos.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Objeto de entrada de pool SQL, geralmente passado pelo pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
Nome do pool do SQL Synapse.

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotificationRecipientsEmail
Uma lista de endereços de email separados por ponto-e-vírgula para enviar os alertas.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NotificationRecipientsEmails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identificador de recurso do pool do SQL Synapse.

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionInDays
O número de dias de retenção para os logs de auditoria.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
O nome da conta de armazenamento.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkspaceName
Nome do espaço de trabalho do Synapse.

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Workspaceobject
objeto de entrada do espaço de trabalho, geralmente passado pelo pipeline.

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace

### Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool

## EXIBE

### Microsoft. Azure. Commands. Synapse. Models. PSSqlPoolSecurityAlertPolicy

## INFORMA

## LINKS RELACIONADOS
