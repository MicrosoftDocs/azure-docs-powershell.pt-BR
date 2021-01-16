---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263997"
---
# Remove-AzSqlInstanceDatabaseLongTermRetentionBackup

## Sinopse
Exclui um backup de retenção de longo prazo.

## SYNTAX

### RemoveBackupDefault (padrão)
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBackupByInputObject
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBackupByResourceId
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** exclui o backup especificado.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

Exclui o backup com o nome 15be823c-7e2c-49d8-819f-a3fdcad92215; 132268250550000000

## OS

### -Backupname
O nome do backup.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
O nome do banco de dados gerenciado do qual o backup se encontra.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
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

### -Force
Ignorar a mensagem de confirmação para executar a ação

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

### -InputObject
O objeto de backup de retenção de longo prazo do banco de dados a ser removido.

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstanceName
O nome da instância gerenciada na qual o backup se encontra.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Local
O local da instância gerenciada de origem dos backups.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
A ID do recurso do backup de retenção de longo prazo do banco de dados a ser removida.

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel

### System. String

## EXIBE

### Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel

## INFORMA

## LINKS RELACIONADOS

[Get-AzSqlInstanceDatabaseLongTermRetentionBackup](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)