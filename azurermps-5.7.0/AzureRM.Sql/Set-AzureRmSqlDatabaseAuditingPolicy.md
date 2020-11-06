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
# <span data-ttu-id="caba4-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="caba4-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="caba4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="caba4-102">SYNOPSIS</span></span>
<span data-ttu-id="caba4-103">Define a política de auditoria para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="caba4-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caba4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="caba4-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caba4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="caba4-105">DESCRIPTION</span></span>
<span data-ttu-id="caba4-106">O cmdlet **set-AzureRmSqlDatabaseAuditingPolicy** altera a política de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="caba4-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="caba4-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="caba4-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="caba4-108">Especifique o parâmetro *StorageAccountName* para especificar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="caba4-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="caba4-109">Você também pode definir a retenção para a tabela de logs de auditoria definindo o valor dos parâmetros *RetentionInDays* e *TableIdentifier* para definir o período e a semente dos nomes de tabela de log de auditoria.</span><span class="sxs-lookup"><span data-stu-id="caba4-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="caba4-110">Especifique o parâmetro *EventType* para definir quais tipos de eventos auditar.</span><span class="sxs-lookup"><span data-stu-id="caba4-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="caba4-111">Depois que o cmdlet é executado com êxito, a auditoria do banco de dados é habilitada.</span><span class="sxs-lookup"><span data-stu-id="caba4-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="caba4-112">Para a auditoria de tabela, se o banco de dados usou a política de seu servidor para auditoria antes de executar esse cmdlet, a auditoria deixará de usar essa política.</span><span class="sxs-lookup"><span data-stu-id="caba4-112">For Table Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span> <span data-ttu-id="caba4-113">Para a auditoria de BLOB, se o banco de dados usou a política de seu servidor para auditoria antes de executar esse cmdlet, ambas as políticas de auditoria serão usadas lado a lado.</span><span class="sxs-lookup"><span data-stu-id="caba4-113">For Blob Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, both auditing policies will exist side-by-side.</span></span>
<span data-ttu-id="caba4-114">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve a política de auditoria atual, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="caba4-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="caba4-115">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="caba4-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="caba4-116">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="caba4-116">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="caba4-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="caba4-117">EXAMPLES</span></span>

### <span data-ttu-id="caba4-118">Exemplo 1: definir a política de auditoria de um banco de dados para usar a auditoria de tabela</span><span class="sxs-lookup"><span data-stu-id="caba4-118">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="caba4-119">Esse comando define a política de auditoria do banco de dados chamada Database01 localizada em Server01 para usar a conta de armazenamento chamada Storage31.</span><span class="sxs-lookup"><span data-stu-id="caba4-119">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="caba4-120">Exemplo 2: definir a chave da conta de armazenamento de uma política de auditoria existente de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="caba4-120">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="caba4-121">Esse comando define a política de auditoria do banco de dados chamada Database01 localizada em Server01 para continuar usando o mesmo nome da conta de armazenamento, mas agora usar a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="caba4-121">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="caba4-122">Exemplo 3: definir a política de auditoria de um banco de dados para usar um tipo de evento específico</span><span class="sxs-lookup"><span data-stu-id="caba4-122">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="caba4-123">Exemplo 4: definir a política de auditoria de um banco de dados para usar a auditoria de BLOB</span><span class="sxs-lookup"><span data-stu-id="caba4-123">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="caba4-124">Esse comando define a política de auditoria do banco de dados chamada Database01 localizada em Server01.</span><span class="sxs-lookup"><span data-stu-id="caba4-124">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="caba4-125">A política registra o tipo de evento Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="caba4-125">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="caba4-126">O comando não altera as configurações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="caba4-126">The command does not change the storage settings.</span></span>

## <span data-ttu-id="caba4-127">OS</span><span class="sxs-lookup"><span data-stu-id="caba4-127">PARAMETERS</span></span>

### <span data-ttu-id="caba4-128">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="caba4-128">-AuditAction</span></span>
<span data-ttu-id="caba4-129">Especifique uma ou mais ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="caba4-129">Specify one or more audit actions.</span></span>
<span data-ttu-id="caba4-130">Esse parâmetro só se aplica a auditoria de BLOB.</span><span class="sxs-lookup"><span data-stu-id="caba4-130">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="caba4-131">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="caba4-131">-AuditActionGroup</span></span>
<span data-ttu-id="caba4-132">Especifique um ou mais grupos de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="caba4-132">Specify one or more audit action groups.</span></span>
<span data-ttu-id="caba4-133">Esse parâmetro só se aplica a auditoria de BLOB.</span><span class="sxs-lookup"><span data-stu-id="caba4-133">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="caba4-134">-Audittype</span><span class="sxs-lookup"><span data-stu-id="caba4-134">-AuditType</span></span>
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

### <span data-ttu-id="caba4-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="caba4-135">-DatabaseName</span></span>
<span data-ttu-id="caba4-136">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="caba4-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="caba4-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caba4-137">-DefaultProfile</span></span>
<span data-ttu-id="caba4-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="caba4-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caba4-139">-EventType</span><span class="sxs-lookup"><span data-stu-id="caba4-139">-EventType</span></span>
<span data-ttu-id="caba4-140">Especifica os tipos de eventos a serem auditados.</span><span class="sxs-lookup"><span data-stu-id="caba4-140">Specifies the event types to audit.</span></span>
<span data-ttu-id="caba4-141">Esse parâmetro só se aplica a auditoria de tabela.</span><span class="sxs-lookup"><span data-stu-id="caba4-141">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="caba4-142">Você pode especificar vários tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="caba4-142">You can specify several event types.</span></span>
<span data-ttu-id="caba4-143">Você pode especificar All para auditar todos os tipos de evento ou nenhum para especificar que nenhum evento será auditado.</span><span class="sxs-lookup"><span data-stu-id="caba4-143">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="caba4-144">Se você especificar All ou None ao mesmo tempo, o cmdlet não será executado.</span><span class="sxs-lookup"><span data-stu-id="caba4-144">If you specify All or None at the same time, the cmdlet does not run.</span></span>

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

### <span data-ttu-id="caba4-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="caba4-145">-PassThru</span></span>
<span data-ttu-id="caba4-146">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="caba4-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="caba4-147">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="caba4-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="caba4-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caba4-148">-ResourceGroupName</span></span>
<span data-ttu-id="caba4-149">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="caba4-149">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="caba4-150">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="caba4-150">-RetentionInDays</span></span>
<span data-ttu-id="caba4-151">Especifica o número de dias de retenção para a tabela de logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="caba4-151">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="caba4-152">Um valor igual a zero (0) significa que a tabela não é mantida.</span><span class="sxs-lookup"><span data-stu-id="caba4-152">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="caba4-153">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="caba4-153">The default value is zero.</span></span>
<span data-ttu-id="caba4-154">Se você especificar um valor maior que zero, você deve especificar um valor para o parâmetro *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="caba4-154">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="caba4-155">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="caba4-155">-ServerName</span></span>
<span data-ttu-id="caba4-156">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="caba4-156">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="caba4-157">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="caba4-157">-StorageAccountName</span></span>
<span data-ttu-id="caba4-158">Especifica o nome da conta de armazenamento para auditar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="caba4-158">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="caba4-159">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="caba4-159">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="caba4-160">Esse parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="caba4-160">This parameter is not required.</span></span>
<span data-ttu-id="caba4-161">Se você não especificar esse parâmetro, o cmdlet usa a conta de armazenamento que foi definida anteriormente como parte da política de auditoria do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="caba4-161">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="caba4-162">Se esta for a primeira vez que uma política de auditoria de banco de dados for definida e você não especificar esse parâmetro, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="caba4-162">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="caba4-163">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="caba4-163">-StorageKeyType</span></span>
<span data-ttu-id="caba4-164">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="caba4-164">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="caba4-165">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="caba4-165">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="caba4-166">Preocupação</span><span class="sxs-lookup"><span data-stu-id="caba4-166">Primary</span></span>
- <span data-ttu-id="caba4-167">Segundo</span><span class="sxs-lookup"><span data-stu-id="caba4-167">Secondary</span></span>

<span data-ttu-id="caba4-168">O valor padrão é principal.</span><span class="sxs-lookup"><span data-stu-id="caba4-168">The default value is Primary.</span></span>

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

### <span data-ttu-id="caba4-169">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="caba4-169">-TableIdentifier</span></span>
<span data-ttu-id="caba4-170">Especifica o nome da tabela de logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="caba4-170">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="caba4-171">Especifique esse valor se você especificar um valor maior que zero para o parâmetro *RetentionInDays* .</span><span class="sxs-lookup"><span data-stu-id="caba4-171">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="caba4-172">-Confirme</span><span class="sxs-lookup"><span data-stu-id="caba4-172">-Confirm</span></span>
<span data-ttu-id="caba4-173">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caba4-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caba4-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caba4-174">-WhatIf</span></span>
<span data-ttu-id="caba4-175">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="caba4-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caba4-176">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="caba4-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caba4-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caba4-177">CommonParameters</span></span>
<span data-ttu-id="caba4-178">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caba4-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caba4-179">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caba4-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caba4-180">SENSORES</span><span class="sxs-lookup"><span data-stu-id="caba4-180">INPUTS</span></span>

### <span data-ttu-id="caba4-181">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="caba4-181">None</span></span>
<span data-ttu-id="caba4-182">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="caba4-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="caba4-183">EXIBE</span><span class="sxs-lookup"><span data-stu-id="caba4-183">OUTPUTS</span></span>

### <span data-ttu-id="caba4-184">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="caba4-184">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="caba4-185">INFORMA</span><span class="sxs-lookup"><span data-stu-id="caba4-185">NOTES</span></span>

## <span data-ttu-id="caba4-186">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="caba4-186">RELATED LINKS</span></span>

[<span data-ttu-id="caba4-187">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="caba4-187">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="caba4-188">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="caba4-188">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="caba4-189">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="caba4-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

