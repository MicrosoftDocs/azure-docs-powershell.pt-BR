---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 80887d1c3cfc91c9eba23f686deac071660cf852
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432707"
---
# <span data-ttu-id="7ca37-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="7ca37-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="7ca37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ca37-102">SYNOPSIS</span></span>
<span data-ttu-id="7ca37-103">Altera as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca37-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ca37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ca37-104">SYNTAX</span></span>

### <span data-ttu-id="7ca37-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ca37-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-PredicateExpression <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ca37-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="7ca37-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ca37-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ca37-107">DESCRIPTION</span></span>
<span data-ttu-id="7ca37-108">O cmdlet **set-AzureRmSqlServerAuditing** altera as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca37-108">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="7ca37-109">Para usar o cmdlet, use os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="7ca37-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="7ca37-110">Especifique o parâmetro *StorageAccountName* para especificar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7ca37-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="7ca37-111">Use o parâmetro *State* para habilitar/desabilitar a política.</span><span class="sxs-lookup"><span data-stu-id="7ca37-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="7ca37-112">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7ca37-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="7ca37-113">Após a execução bem-sucedida do cmdlet, a auditoria dos bancos de dados SQL do Azure definidos no Azure SQL Server especificado está habilitada.</span><span class="sxs-lookup"><span data-stu-id="7ca37-113">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="7ca37-114">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve a política de auditoria de blob atual, além dos identificadores de servidor.</span><span class="sxs-lookup"><span data-stu-id="7ca37-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="7ca37-115">Os identificadores de servidor incluem, entre outros, **ResourceGroupName** e **nomedoservidor**.</span><span class="sxs-lookup"><span data-stu-id="7ca37-115">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="7ca37-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ca37-116">EXAMPLES</span></span>

### <span data-ttu-id="7ca37-117">Exemplo 1: habilitar a política de auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="7ca37-117">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="7ca37-118">Exemplo 2: desabilitar a política de auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="7ca37-118">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="7ca37-119">Exemplo 3: habilitar a política de auditoria de um SQL Server do Azure usando uma conta de armazenamento de uma assinatura diferente</span><span class="sxs-lookup"><span data-stu-id="7ca37-119">Example 3: Enable the auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="7ca37-120">Exemplo 4: habilitar a política de auditoria estendida de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="7ca37-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="7ca37-121">Exemplo 5: remover a política de auditoria estendida de um banco de dados SQL do Azure e definir uma política de auditoria em vez disso.</span><span class="sxs-lookup"><span data-stu-id="7ca37-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="7ca37-122">OS</span><span class="sxs-lookup"><span data-stu-id="7ca37-122">PARAMETERS</span></span>

### <span data-ttu-id="7ca37-123">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="7ca37-123">-AuditActionGroup</span></span>
<span data-ttu-id="7ca37-124">O conjunto recomendado de grupos de ação a ser usado é a seguinte combinação-isso fará a auditoria de todas as consultas e procedimentos armazenados executados no banco de dados, bem como dos logons com falha e com falha: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" essa combinação acima também é o conjunto que é configurado por padrão.</span><span class="sxs-lookup"><span data-stu-id="7ca37-124">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="7ca37-125">Esses grupos abrangem todas as instruções SQL e procedimentos armazenados executados em relação ao banco de dados e não devem ser usados em combinação com outros grupos, pois isso resultará em logs de auditoria duplicados.</span><span class="sxs-lookup"><span data-stu-id="7ca37-125">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="7ca37-126">Para obter mais informações, consulte https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="7ca37-126">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="7ca37-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ca37-127">-DefaultProfile</span></span>
<span data-ttu-id="7ca37-128">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7ca37-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ca37-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ca37-129">-PassThru</span></span>
<span data-ttu-id="7ca37-130">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="7ca37-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7ca37-131">-Predicateie</span><span class="sxs-lookup"><span data-stu-id="7ca37-131">-PredicateExpression</span></span>
<span data-ttu-id="7ca37-132">A instrução da cláusula WHERE usada para filtrar logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7ca37-132">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="7ca37-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ca37-133">-ResourceGroupName</span></span>
<span data-ttu-id="7ca37-134">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7ca37-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="7ca37-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="7ca37-135">-RetentionInDays</span></span>
<span data-ttu-id="7ca37-136">O número de dias de retenção para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7ca37-136">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="7ca37-137">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="7ca37-137">-ServerName</span></span>
<span data-ttu-id="7ca37-138">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="7ca37-138">SQL server name.</span></span>

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

### <span data-ttu-id="7ca37-139">-Estado</span><span class="sxs-lookup"><span data-stu-id="7ca37-139">-State</span></span>
<span data-ttu-id="7ca37-140">O estado da política.</span><span class="sxs-lookup"><span data-stu-id="7ca37-140">The state of the policy.</span></span>

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

### <span data-ttu-id="7ca37-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="7ca37-141">-StorageAccountName</span></span>
<span data-ttu-id="7ca37-142">O nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="7ca37-142">The name of the storage account.</span></span> <span data-ttu-id="7ca37-143">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="7ca37-143">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="7ca37-144">Esse parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="7ca37-144">This parameter is not required.</span></span>
<span data-ttu-id="7ca37-145">Se você não especificar esse parâmetro, o cmdlet usa a conta de armazenamento que foi definida anteriormente como parte da política de auditoria.</span><span class="sxs-lookup"><span data-stu-id="7ca37-145">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="7ca37-146">Se esta for a primeira vez que uma política de auditoria for definida e você não especificar esse parâmetro, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="7ca37-146">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="7ca37-147">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7ca37-147">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="7ca37-148">Especifica a ID da assinatura da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="7ca37-148">Specifies storage account subscription id</span></span>

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

### <span data-ttu-id="7ca37-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="7ca37-149">-StorageKeyType</span></span>
<span data-ttu-id="7ca37-150">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="7ca37-150">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="7ca37-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ca37-151">-Confirm</span></span>
<span data-ttu-id="7ca37-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ca37-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ca37-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ca37-153">-WhatIf</span></span>
<span data-ttu-id="7ca37-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ca37-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ca37-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ca37-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ca37-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ca37-156">CommonParameters</span></span>
<span data-ttu-id="7ca37-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ca37-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ca37-158">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ca37-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ca37-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ca37-159">INPUTS</span></span>

## <span data-ttu-id="7ca37-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ca37-160">OUTPUTS</span></span>

## <span data-ttu-id="7ca37-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ca37-161">NOTES</span></span>

## <span data-ttu-id="7ca37-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ca37-162">RELATED LINKS</span></span>
