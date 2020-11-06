---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428713"
---
# <span data-ttu-id="d7584-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d7584-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="d7584-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7584-102">SYNOPSIS</span></span>
<span data-ttu-id="d7584-103">Altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7584-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7584-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7584-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7584-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7584-105">DESCRIPTION</span></span>
<span data-ttu-id="d7584-106">O cmdlet **set-AzureRmSqlDatabaseAuditing** altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="d7584-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="d7584-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d7584-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d7584-108">Especifique o parâmetro *StorageAccountName* para especificar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7584-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="d7584-109">Use o parâmetro *State* para habilitar/desabilitar a política.</span><span class="sxs-lookup"><span data-stu-id="d7584-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="d7584-110">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d7584-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="d7584-111">Depois que o cmdlet é executado com êxito, a auditoria do banco de dados é habilitada.</span><span class="sxs-lookup"><span data-stu-id="d7584-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="d7584-112">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve a política de auditoria de blob atual, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="d7584-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="d7584-113">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="d7584-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="d7584-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7584-114">EXAMPLES</span></span>

### <span data-ttu-id="d7584-115">Exemplo 1: habilitar a política de auditoria de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="d7584-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="d7584-116">Exemplo 2: desabilitar a política de auditoria de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="d7584-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="d7584-117">OS</span><span class="sxs-lookup"><span data-stu-id="d7584-117">PARAMETERS</span></span>

### <span data-ttu-id="d7584-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="d7584-118">-AuditAction</span></span>
<span data-ttu-id="d7584-119">O conjunto de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d7584-119">The set of audit actions.</span></span>  
<span data-ttu-id="d7584-120">As ações com suporte para auditoria são:</span><span class="sxs-lookup"><span data-stu-id="d7584-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="d7584-121">SELECIONADA</span><span class="sxs-lookup"><span data-stu-id="d7584-121">SELECT</span></span>  
<span data-ttu-id="d7584-122">ATUALIZAÇÃO</span><span class="sxs-lookup"><span data-stu-id="d7584-122">UPDATE</span></span>  
<span data-ttu-id="d7584-123">NSERIR</span><span class="sxs-lookup"><span data-stu-id="d7584-123">INSERT</span></span>  
<span data-ttu-id="d7584-124">REMOVER</span><span class="sxs-lookup"><span data-stu-id="d7584-124">DELETE</span></span>  
<span data-ttu-id="d7584-125">NOVAMENTE</span><span class="sxs-lookup"><span data-stu-id="d7584-125">EXECUTE</span></span>  
<span data-ttu-id="d7584-126">Recebi</span><span class="sxs-lookup"><span data-stu-id="d7584-126">RECEIVE</span></span>  
<span data-ttu-id="d7584-127">REFERE</span><span class="sxs-lookup"><span data-stu-id="d7584-127">REFERENCES</span></span>  

<span data-ttu-id="d7584-128">A forma geral para definir uma ação a ser auditada é:</span><span class="sxs-lookup"><span data-stu-id="d7584-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="d7584-129">ação EM [objeto] por [principal]</span><span class="sxs-lookup"><span data-stu-id="d7584-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="d7584-130">Observe que [objeto] no formato acima pode se referir a um objeto, como uma tabela, um modo de exibição ou um procedimento armazenado ou um esquema ou banco de dados inteiro.</span><span class="sxs-lookup"><span data-stu-id="d7584-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="d7584-131">Para os últimos casos, o banco de dados de formulários:: [dbname] e esquema:: [SchemaName] são usados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d7584-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="d7584-132">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="d7584-132">For example:</span></span>  
<span data-ttu-id="d7584-133">SELECIONAR em dbo. myTable por público</span><span class="sxs-lookup"><span data-stu-id="d7584-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="d7584-134">SELECIONAR no banco de dados:: MyDatabase por público</span><span class="sxs-lookup"><span data-stu-id="d7584-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="d7584-135">SELECIONAR no esquema:: MySchema by Public</span><span class="sxs-lookup"><span data-stu-id="d7584-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="d7584-136">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="d7584-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="d7584-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d7584-137">-AuditActionGroup</span></span>
<span data-ttu-id="d7584-138">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha:</span><span class="sxs-lookup"><span data-stu-id="d7584-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="d7584-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="d7584-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="d7584-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="d7584-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="d7584-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="d7584-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="d7584-142">Esta combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="d7584-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="d7584-143">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="d7584-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="d7584-144">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="d7584-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="d7584-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d7584-145">-DatabaseName</span></span>
<span data-ttu-id="d7584-146">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="d7584-146">SQL Database name.</span></span>

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

### <span data-ttu-id="d7584-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7584-147">-DefaultProfile</span></span>
<span data-ttu-id="d7584-148">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7584-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7584-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7584-149">-PassThru</span></span>
<span data-ttu-id="d7584-150">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="d7584-150">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d7584-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7584-151">-ResourceGroupName</span></span>
<span data-ttu-id="d7584-152">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7584-152">The name of the resource group.</span></span>

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

### <span data-ttu-id="d7584-153">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d7584-153">-RetentionInDays</span></span>
<span data-ttu-id="d7584-154">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d7584-154">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="d7584-155">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="d7584-155">-ServerName</span></span>
<span data-ttu-id="d7584-156">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="d7584-156">SQL Database server name.</span></span>

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

### <span data-ttu-id="d7584-157">-Estado</span><span class="sxs-lookup"><span data-stu-id="d7584-157">-State</span></span>
<span data-ttu-id="d7584-158">O estado da política.</span><span class="sxs-lookup"><span data-stu-id="d7584-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7584-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d7584-159">-StorageAccountName</span></span>
<span data-ttu-id="d7584-160">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="d7584-160">The name of the storage account.</span></span> <span data-ttu-id="d7584-161">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="d7584-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="d7584-162">Esse parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="d7584-162">This parameter is not required.</span></span>  
<span data-ttu-id="d7584-163">Se você não especificar esse parâmetro, o cmdlet usa a conta de armazenamento que foi definida anteriormente como parte da política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="d7584-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="d7584-164">Se esta for a primeira vez que uma política de auditoria for definida e você não especificar esse parâmetro, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="d7584-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="d7584-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d7584-165">-StorageKeyType</span></span>
<span data-ttu-id="d7584-166">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="d7584-166">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="d7584-167">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7584-167">-Confirm</span></span>
<span data-ttu-id="d7584-168">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7584-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7584-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7584-169">-WhatIf</span></span>
<span data-ttu-id="d7584-170">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7584-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7584-171">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7584-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7584-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7584-172">CommonParameters</span></span>
<span data-ttu-id="d7584-173">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7584-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7584-174">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7584-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7584-175">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7584-175">INPUTS</span></span>

### <span data-ttu-id="d7584-176">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d7584-176">None</span></span>
<span data-ttu-id="d7584-177">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="d7584-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d7584-178">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7584-178">OUTPUTS</span></span>

### <span data-ttu-id="d7584-179">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="d7584-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="d7584-180">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7584-180">NOTES</span></span>

## <span data-ttu-id="d7584-181">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7584-181">RELATED LINKS</span></span>
