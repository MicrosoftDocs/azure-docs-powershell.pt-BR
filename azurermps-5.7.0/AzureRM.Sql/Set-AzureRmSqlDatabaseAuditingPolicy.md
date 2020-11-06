---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 9f551b5b334f6151b42faebf8b60d2939a0680d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428712"
---
# Set-AzureRmSqlDatabaseAuditingPolicy

## Sinopse
Define a política de auditoria para um banco de dados.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmSqlDatabaseAuditingPolicy** altera a política de auditoria de um banco de dados SQL do Azure.
Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.
Especifique o parâmetro *StorageAccountName* para especificar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.

Você também pode definir a retenção para a tabela de logs de auditoria definindo o valor dos parâmetros *RetentionInDays* e *TableIdentifier* para definir o período e a semente dos nomes de tabela de log de auditoria.
Especifique o parâmetro *EventType* para definir quais tipos de eventos auditar.

Depois que o cmdlet é executado com êxito, a auditoria do banco de dados é habilitada.
Para a auditoria de tabela, se o banco de dados usou a política de seu servidor para auditoria antes de executar esse cmdlet, a auditoria deixará de usar essa política. Para a auditoria de BLOB, se o banco de dados usou a política de seu servidor para auditoria antes de executar esse cmdlet, ambas as políticas de auditoria serão usadas lado a lado.
Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve a política de auditoria atual, além dos identificadores de banco de dados.
Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.

Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.

## EXEMPLOS

### Exemplo 1: definir a política de auditoria de um banco de dados para usar a auditoria de tabela
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

Esse comando define a política de auditoria do banco de dados chamada Database01 localizada em Server01 para usar a conta de armazenamento chamada Storage31.

### Exemplo 2: definir a chave da conta de armazenamento de uma política de auditoria existente de um banco de dados
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

Esse comando define a política de auditoria do banco de dados chamada Database01 localizada em Server01 para continuar usando o mesmo nome da conta de armazenamento, mas agora usar a chave secundária.

### Exemplo 3: definir a política de auditoria de um banco de dados para usar um tipo de evento específico
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### Exemplo 4: definir a política de auditoria de um banco de dados para usar a auditoria de BLOB
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

Esse comando define a política de auditoria do banco de dados chamada Database01 localizada em Server01.
A política registra o tipo de evento Login_Failure.
O comando não altera as configurações de armazenamento.

## OS

### -AuditAction
Especifique uma ou mais ações de auditoria.
Esse parâmetro só se aplica a auditoria de BLOB.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditActionGroup
Especifique um ou mais grupos de ações de auditoria.
Esse parâmetro só se aplica a auditoria de BLOB.

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Audittype
```yaml
Type: AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Especifica o nome do banco de dados.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EventType
Especifica os tipos de eventos a serem auditados.
Esse parâmetro só se aplica a auditoria de tabela.

Você pode especificar vários tipos de eventos.
Você pode especificar All para auditar todos os tipos de evento ou nenhum para especificar que nenhum evento será auditado.
Se você especificar All ou None ao mesmo tempo, o cmdlet não será executado.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

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
Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Especifica o número de dias de retenção para a tabela de logs de auditoria.
Um valor igual a zero (0) significa que a tabela não é mantida.
O valor padrão é zero.
Se você especificar um valor maior que zero, você deve especificar um valor para o parâmetro *TableIdentifer* .

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomedoservidor
Especifica o nome do servidor que hospeda o banco de dados.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Especifica o nome da conta de armazenamento para auditar o banco de dados.
Caracteres curinga não são permitidos.
Esse parâmetro não é necessário.
Se você não especificar esse parâmetro, o cmdlet usa a conta de armazenamento que foi definida anteriormente como parte da política de auditoria do banco de dados.
Se esta for a primeira vez que uma política de auditoria de banco de dados for definida e você não especificar esse parâmetro, o cmdlet falhará.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKeyType
Especifica quais das chaves de acesso de armazenamento usar.
Os valores aceitáveis para esse parâmetro são:

- Preocupação
- Segundo

O valor padrão é principal.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableIdentifier
Especifica o nome da tabela de logs de auditoria.
Especifique esse valor se você especificar um valor maior que zero para o parâmetro *RetentionInDays* .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

### Microsoft. Azure. Commands. Sql. Security. Model. DatabaseAuditingPolicyModel

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSqlDatabaseAuditingPolicy](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[Remove-AzureRmSqlDatabaseAuditing](./Remove-AzureRmSqlDatabaseAuditing.md)

[Documentação do banco de dados SQL](https://docs.microsoft.com/azure/sql-database/)


