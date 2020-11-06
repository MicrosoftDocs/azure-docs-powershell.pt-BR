---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428033"
---
# <span data-ttu-id="b4888-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="b4888-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="b4888-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b4888-102">SYNOPSIS</span></span>
<span data-ttu-id="b4888-103">Altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4888-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b4888-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4888-104">SYNTAX</span></span>

### <span data-ttu-id="b4888-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b4888-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4888-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="b4888-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4888-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b4888-107">DESCRIPTION</span></span>
<span data-ttu-id="b4888-108">O cmdlet **set-AzureRmSqlDatabaseAuditing** altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="b4888-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="b4888-109">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b4888-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="b4888-110">Especifique o parâmetro *StorageAccountName* para especificar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b4888-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="b4888-111">Use o parâmetro *State* para habilitar/desabilitar a política.</span><span class="sxs-lookup"><span data-stu-id="b4888-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="b4888-112">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b4888-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="b4888-113">Depois que o cmdlet é executado com êxito, a auditoria do banco de dados é habilitada.</span><span class="sxs-lookup"><span data-stu-id="b4888-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="b4888-114">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve a política de auditoria de blob atual, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="b4888-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="b4888-115">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="b4888-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="b4888-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b4888-116">EXAMPLES</span></span>

### <span data-ttu-id="b4888-117">Exemplo 1: habilitar a política de auditoria de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="b4888-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="b4888-118">Exemplo 2: desabilitar a política de auditoria de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="b4888-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="b4888-119">Exemplo 3: habilitar a política de auditoria de um banco de dados SQL do Azure usando uma conta de armazenamento de uma assinatura diferente</span><span class="sxs-lookup"><span data-stu-id="b4888-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="b4888-120">Exemplo 4: habilitar a política de auditoria estendida de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="b4888-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="b4888-121">Exemplo 5: remover a política de auditoria estendida de um banco de dados SQL do Azure e definir uma política de auditoria em vez disso.</span><span class="sxs-lookup"><span data-stu-id="b4888-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="b4888-122">OS</span><span class="sxs-lookup"><span data-stu-id="b4888-122">PARAMETERS</span></span>

### <span data-ttu-id="b4888-123">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="b4888-123">-AuditAction</span></span>
<span data-ttu-id="b4888-124">O conjunto de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b4888-124">The set of audit actions.</span></span>
<span data-ttu-id="b4888-125">As ações com suporte a auditoria são: selecionar atualizar inserir excluir executar como referências o formato geral para definir uma ação a ser auditada é: [ação] em [objeto] por [principal] Observe que [objeto] no formato acima pode se referir a um objeto, como uma tabela, um modo de exibição ou um procedimento armazenado ou um esquema ou banco de dados inteiro.</span><span class="sxs-lookup"><span data-stu-id="b4888-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="b4888-126">Para os últimos casos, o banco de dados de formulários:: [dbname] e esquema:: [SchemaName] são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b4888-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="b4888-127">Por exemplo: selecionar em dbo. myTable por público selecionar no banco de dados:: MyDatabase por público selecione em esquema:: MySchema by Public para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="b4888-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="b4888-128">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="b4888-128">-AuditActionGroup</span></span>
<span data-ttu-id="b4888-129">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" essa combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="b4888-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="b4888-130">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="b4888-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="b4888-131">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="b4888-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4888-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b4888-132">-DatabaseName</span></span>
<span data-ttu-id="b4888-133">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="b4888-133">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4888-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4888-134">-DefaultProfile</span></span>
<span data-ttu-id="b4888-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b4888-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4888-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4888-136">-PassThru</span></span>
<span data-ttu-id="b4888-137">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="b4888-137">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4888-138">-Predicateie</span><span class="sxs-lookup"><span data-stu-id="b4888-138">-PredicateExpression</span></span>
<span data-ttu-id="b4888-139">A instrução da cláusula WHERE usada para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b4888-139">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="b4888-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4888-140">-ResourceGroupName</span></span>
<span data-ttu-id="b4888-141">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4888-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="b4888-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b4888-142">-RetentionInDays</span></span>
<span data-ttu-id="b4888-143">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b4888-143">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="b4888-144">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b4888-144">-ServerName</span></span>
<span data-ttu-id="b4888-145">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="b4888-145">SQL Database server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4888-146">-Estado</span><span class="sxs-lookup"><span data-stu-id="b4888-146">-State</span></span>
<span data-ttu-id="b4888-147">O estado da política.</span><span class="sxs-lookup"><span data-stu-id="b4888-147">The state of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4888-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4888-148">-StorageAccountName</span></span>
<span data-ttu-id="b4888-149">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b4888-149">The name of the storage account.</span></span> <span data-ttu-id="b4888-150">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="b4888-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="b4888-151">Esse parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="b4888-151">This parameter is not required.</span></span>
<span data-ttu-id="b4888-152">Se você não especificar esse parâmetro, o cmdlet usa a conta de armazenamento que foi definida anteriormente como parte da política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b4888-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="b4888-153">Se esta for a primeira vez que uma política de auditoria for definida e você não especificar esse parâmetro, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="b4888-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4888-154">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b4888-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="b4888-155">Especifica a ID da assinatura da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b4888-155">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4888-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="b4888-156">-StorageKeyType</span></span>
<span data-ttu-id="b4888-157">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="b4888-157">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4888-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b4888-158">-Confirm</span></span>
<span data-ttu-id="b4888-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4888-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4888-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4888-160">-WhatIf</span></span>
<span data-ttu-id="b4888-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b4888-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4888-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b4888-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4888-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4888-163">CommonParameters</span></span>
<span data-ttu-id="b4888-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4888-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4888-165">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4888-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4888-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b4888-166">INPUTS</span></span>

## <span data-ttu-id="b4888-167">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b4888-167">OUTPUTS</span></span>

## <span data-ttu-id="b4888-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b4888-168">NOTES</span></span>

## <span data-ttu-id="b4888-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b4888-169">RELATED LINKS</span></span>
