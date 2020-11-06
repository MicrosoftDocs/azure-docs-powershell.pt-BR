---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 99fb9bf57f056a869310de2fe27d00a72ce5d8c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427740"
---
# <span data-ttu-id="71f0f-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="71f0f-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="71f0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="71f0f-103">Define a política de auditoria para um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71f0f-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71f0f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71f0f-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71f0f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="71f0f-106">O cmdlet **set-AzureRmSqlDatabaseAuditingPolicy** altera a política de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="71f0f-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="71f0f-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71f0f-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="71f0f-108">Especifique o parâmetro *StorageAccountName* para especificar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="71f0f-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="71f0f-109">Você também pode definir a retenção para a tabela de logs de auditoria definindo o valor dos parâmetros *RetentionInDays* e *TableIdentifier* para definir o período e a semente dos nomes de tabela de log de auditoria.</span><span class="sxs-lookup"><span data-stu-id="71f0f-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="71f0f-110">Especifique o parâmetro *EventType* para definir quais tipos de eventos auditar.</span><span class="sxs-lookup"><span data-stu-id="71f0f-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="71f0f-111">Depois que o cmdlet é executado com êxito, a auditoria do banco de dados é habilitada.</span><span class="sxs-lookup"><span data-stu-id="71f0f-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="71f0f-112">Se o banco de dados usou a política de seu servidor para auditoria antes de executar esse cmdlet, a auditoria deixará de usar essa política.</span><span class="sxs-lookup"><span data-stu-id="71f0f-112">If the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span>
<span data-ttu-id="71f0f-113">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve a política de auditoria atual, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71f0f-113">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="71f0f-114">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="71f0f-114">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="71f0f-115">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="71f0f-115">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="71f0f-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71f0f-116">EXAMPLES</span></span>

### <span data-ttu-id="71f0f-117">Exemplo 1: definir a política de auditoria de um banco de dados para usar a auditoria de tabela</span><span class="sxs-lookup"><span data-stu-id="71f0f-117">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="71f0f-118">Esse comando define a política de auditoria do banco de dados chamada Database01 localizada em Server01 para usar a conta de armazenamento chamada Storage31.</span><span class="sxs-lookup"><span data-stu-id="71f0f-118">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="71f0f-119">Exemplo 2: definir a chave da conta de armazenamento de uma política de auditoria existente de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="71f0f-119">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="71f0f-120">Esse comando define a política de auditoria do banco de dados chamada Database01 localizada em Server01 para continuar usando o mesmo nome da conta de armazenamento, mas agora usar a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="71f0f-120">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="71f0f-121">Exemplo 3: definir a política de auditoria de um banco de dados para usar um tipo de evento específico</span><span class="sxs-lookup"><span data-stu-id="71f0f-121">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="71f0f-122">Exemplo 4: definir a política de auditoria de um banco de dados para usar a auditoria de BLOB</span><span class="sxs-lookup"><span data-stu-id="71f0f-122">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="71f0f-123">Esse comando define a política de auditoria do banco de dados chamada Database01 localizada em Server01.</span><span class="sxs-lookup"><span data-stu-id="71f0f-123">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="71f0f-124">A política registra o tipo de evento Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="71f0f-124">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="71f0f-125">O comando não altera as configurações de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="71f0f-125">The command does not change the storage settings.</span></span>

## <span data-ttu-id="71f0f-126">OS</span><span class="sxs-lookup"><span data-stu-id="71f0f-126">PARAMETERS</span></span>

### <span data-ttu-id="71f0f-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="71f0f-127">-AuditAction</span></span>
<span data-ttu-id="71f0f-128">Especifique uma ou mais ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="71f0f-128">Specify one or more audit actions.</span></span>
<span data-ttu-id="71f0f-129">Esse parâmetro só se aplica a auditoria de BLOB.</span><span class="sxs-lookup"><span data-stu-id="71f0f-129">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="71f0f-130">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="71f0f-130">-AuditActionGroup</span></span>
<span data-ttu-id="71f0f-131">Especifique um ou mais grupos de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="71f0f-131">Specify one or more audit action groups.</span></span>
<span data-ttu-id="71f0f-132">Esse parâmetro só se aplica a auditoria de BLOB.</span><span class="sxs-lookup"><span data-stu-id="71f0f-132">This parameter is only applicable to Blob auditing.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases: 
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71f0f-133">-Audittype</span><span class="sxs-lookup"><span data-stu-id="71f0f-133">-AuditType</span></span>
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases: 
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71f0f-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71f0f-134">-DatabaseName</span></span>
<span data-ttu-id="71f0f-135">Especifica o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71f0f-135">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="71f0f-136">-EventType</span><span class="sxs-lookup"><span data-stu-id="71f0f-136">-EventType</span></span>
<span data-ttu-id="71f0f-137">Especifica os tipos de eventos a serem auditados.</span><span class="sxs-lookup"><span data-stu-id="71f0f-137">Specifies the event types to audit.</span></span>
<span data-ttu-id="71f0f-138">Esse parâmetro só se aplica a auditoria de tabela.</span><span class="sxs-lookup"><span data-stu-id="71f0f-138">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="71f0f-139">Você pode especificar vários tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="71f0f-139">You can specify several event types.</span></span>
<span data-ttu-id="71f0f-140">Você pode especificar All para auditar todos os tipos de evento ou nenhum para especificar que nenhum evento será auditado.</span><span class="sxs-lookup"><span data-stu-id="71f0f-140">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="71f0f-141">Se você especificar All ou None ao mesmo tempo, o cmdlet não será executado.</span><span class="sxs-lookup"><span data-stu-id="71f0f-141">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71f0f-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71f0f-142">-PassThru</span></span>
<span data-ttu-id="71f0f-143">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="71f0f-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="71f0f-144">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="71f0f-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71f0f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71f0f-145">-ResourceGroupName</span></span>
<span data-ttu-id="71f0f-146">Especifica o nome do grupo de recursos ao qual o banco de dados está atribuído.</span><span class="sxs-lookup"><span data-stu-id="71f0f-146">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="71f0f-147">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="71f0f-147">-RetentionInDays</span></span>
<span data-ttu-id="71f0f-148">Especifica o número de dias de retenção para a tabela de logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="71f0f-148">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="71f0f-149">Um valor igual a zero (0) significa que a tabela não é mantida.</span><span class="sxs-lookup"><span data-stu-id="71f0f-149">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="71f0f-150">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="71f0f-150">The default value is zero.</span></span>
<span data-ttu-id="71f0f-151">Se você especificar um valor maior que zero, você deve especificar um valor para o parâmetro *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="71f0f-151">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="71f0f-152">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="71f0f-152">-ServerName</span></span>
<span data-ttu-id="71f0f-153">Especifica o nome do servidor que hospeda o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71f0f-153">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="71f0f-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="71f0f-154">-StorageAccountName</span></span>
<span data-ttu-id="71f0f-155">Especifica o nome da conta de armazenamento para auditar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71f0f-155">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="71f0f-156">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="71f0f-156">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="71f0f-157">Esse parâmetro não é necessário.</span><span class="sxs-lookup"><span data-stu-id="71f0f-157">This parameter is not required.</span></span>
<span data-ttu-id="71f0f-158">Se você não especificar esse parâmetro, o cmdlet usa a conta de armazenamento que foi definida anteriormente como parte da política de auditoria do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71f0f-158">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="71f0f-159">Se esta for a primeira vez que uma política de auditoria de banco de dados for definida e você não especificar esse parâmetro, o cmdlet falhará.</span><span class="sxs-lookup"><span data-stu-id="71f0f-159">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="71f0f-160">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="71f0f-160">-StorageKeyType</span></span>
<span data-ttu-id="71f0f-161">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="71f0f-161">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="71f0f-162">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="71f0f-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71f0f-163">Preocupação</span><span class="sxs-lookup"><span data-stu-id="71f0f-163">Primary</span></span>
- <span data-ttu-id="71f0f-164">Segundo</span><span class="sxs-lookup"><span data-stu-id="71f0f-164">Secondary</span></span>

<span data-ttu-id="71f0f-165">O valor padrão é principal.</span><span class="sxs-lookup"><span data-stu-id="71f0f-165">The default value is Primary.</span></span>

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

### <span data-ttu-id="71f0f-166">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="71f0f-166">-TableIdentifier</span></span>
<span data-ttu-id="71f0f-167">Especifica o nome da tabela de logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="71f0f-167">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="71f0f-168">Especifique esse valor se você especificar um valor maior que zero para o parâmetro *RetentionInDays* .</span><span class="sxs-lookup"><span data-stu-id="71f0f-168">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="71f0f-169">-Confirme</span><span class="sxs-lookup"><span data-stu-id="71f0f-169">-Confirm</span></span>
<span data-ttu-id="71f0f-170">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71f0f-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71f0f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71f0f-171">-WhatIf</span></span>
<span data-ttu-id="71f0f-172">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="71f0f-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71f0f-173">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71f0f-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71f0f-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71f0f-174">-DefaultProfile</span></span>
<span data-ttu-id="71f0f-175">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71f0f-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71f0f-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71f0f-176">CommonParameters</span></span>
<span data-ttu-id="71f0f-177">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71f0f-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71f0f-178">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71f0f-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71f0f-179">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71f0f-179">INPUTS</span></span>

## <span data-ttu-id="71f0f-180">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71f0f-180">OUTPUTS</span></span>

### <span data-ttu-id="71f0f-181">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="71f0f-181">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="71f0f-182">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71f0f-182">NOTES</span></span>

## <span data-ttu-id="71f0f-183">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71f0f-183">RELATED LINKS</span></span>

[<span data-ttu-id="71f0f-184">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="71f0f-184">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="71f0f-185">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="71f0f-185">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="71f0f-186">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="71f0f-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


