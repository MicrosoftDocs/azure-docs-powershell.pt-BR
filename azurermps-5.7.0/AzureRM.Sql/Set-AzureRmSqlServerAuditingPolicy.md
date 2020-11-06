---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: ee54928b1f32c726bc2847eace77e6ccbe48c4d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429652"
---
# <span data-ttu-id="db789-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="db789-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="db789-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db789-102">SYNOPSIS</span></span>
<span data-ttu-id="db789-103">Altera a política de auditoria de um servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="db789-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db789-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db789-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db789-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db789-105">DESCRIPTION</span></span>
<span data-ttu-id="db789-106">O cmdlet **set-AzureRmSqlServerAuditingPolicy** altera a política de auditoria de um servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="db789-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="db789-107">Especifique os parâmetros *ResourceGroupName* e *nomedoservidor* para identificar o servidor, o parâmetro *StorageAccountName* para especificar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="db789-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>

<span data-ttu-id="db789-108">Você também pode definir a retenção para a tabela de logs de auditoria definindo o valor dos parâmetros *RetentionInDays* e *TableIdentifier* para definir o período e a semente dos nomes de tabela de log de auditoria.</span><span class="sxs-lookup"><span data-stu-id="db789-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="db789-109">Especifique o parâmetro *EventType* para definir quais tipos de eventos auditar.</span><span class="sxs-lookup"><span data-stu-id="db789-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="db789-110">Depois que você executar esse cmdlet, a auditoria dos bancos de dados que usam a política deste servidor será habilitada.</span><span class="sxs-lookup"><span data-stu-id="db789-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="db789-111">Se o cmdlet for bem-sucedido e você especificar o parâmetro *PassThru* , o cmdlet retornará um objeto que descreve a política de auditoria atual e os identificadores do servidor.</span><span class="sxs-lookup"><span data-stu-id="db789-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="db789-112">Os identificadores de servidor incluem **ResourceGroupName** e **nomedoservidor**.</span><span class="sxs-lookup"><span data-stu-id="db789-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="db789-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db789-113">EXAMPLES</span></span>

### <span data-ttu-id="db789-114">Exemplo 1: definir a política de auditoria de um SQL Server do Azure usar a auditoria de tabela</span><span class="sxs-lookup"><span data-stu-id="db789-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="db789-115">Esse comando define a política de auditoria do servidor chamado Server01 para usar uma conta de armazenamento chamada Storage22.</span><span class="sxs-lookup"><span data-stu-id="db789-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="db789-116">Exemplo 2: definir a chave da conta de armazenamento de uma política de auditoria existente de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="db789-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="db789-117">Este comando define a política de auditoria do servidor chamado Server01 para usar a chave secundária.</span><span class="sxs-lookup"><span data-stu-id="db789-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="db789-118">O comando não modifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="db789-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="db789-119">Exemplo 3: definir a política de auditoria de um SQL Server do Azure para usar um tipo de evento específico</span><span class="sxs-lookup"><span data-stu-id="db789-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="db789-120">Exemplo 4: definir a política de auditoria de um banco de dados para usar a auditoria de BLOB</span><span class="sxs-lookup"><span data-stu-id="db789-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="db789-121">Esse comando define a política de auditoria do servidor chamado Server01 para usar o tipo de evento Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="db789-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="db789-122">Esse comando não modifica nenhuma outra configuração.</span><span class="sxs-lookup"><span data-stu-id="db789-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="db789-123">OS</span><span class="sxs-lookup"><span data-stu-id="db789-123">PARAMETERS</span></span>

### <span data-ttu-id="db789-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="db789-124">-AuditActionGroup</span></span>
<span data-ttu-id="db789-125">Especifique um ou mais grupos de ações de auditoria.</span><span class="sxs-lookup"><span data-stu-id="db789-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="db789-126">Esse parâmetro só se aplica a auditoria de BLOB.</span><span class="sxs-lookup"><span data-stu-id="db789-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="db789-127">-Audittype</span><span class="sxs-lookup"><span data-stu-id="db789-127">-AuditType</span></span>
<span data-ttu-id="db789-128">Especifique o tipo de auditoria.</span><span class="sxs-lookup"><span data-stu-id="db789-128">Specify the audit type.</span></span> <span data-ttu-id="db789-129">Os logs de auditoria podem ser gravados no armazenamento de tabelas ou no armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="db789-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="db789-130">A auditoria de blob oferece maior desempenho e dá suporte à auditoria em nível de objeto.</span><span class="sxs-lookup"><span data-stu-id="db789-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

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

### <span data-ttu-id="db789-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db789-131">-DefaultProfile</span></span>
<span data-ttu-id="db789-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="db789-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db789-133">-EventType</span><span class="sxs-lookup"><span data-stu-id="db789-133">-EventType</span></span>
<span data-ttu-id="db789-134">Especifica os tipos de eventos a serem auditados.</span><span class="sxs-lookup"><span data-stu-id="db789-134">Specifies the event types to audit.</span></span>
<span data-ttu-id="db789-135">Esse parâmetro só se aplica a auditoria de tabela.</span><span class="sxs-lookup"><span data-stu-id="db789-135">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="db789-136">Você pode especificar vários tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="db789-136">You can specify several event types.</span></span>
<span data-ttu-id="db789-137">Você pode especificar All para auditar todos os tipos de evento ou nenhum para especificar que nenhum evento será auditado.</span><span class="sxs-lookup"><span data-stu-id="db789-137">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="db789-138">Se você especificar All ou None ao mesmo tempo, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="db789-138">If you specify All or None at the same time, the command fails.</span></span>

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

### <span data-ttu-id="db789-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db789-139">-PassThru</span></span>
<span data-ttu-id="db789-140">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="db789-140">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="db789-141">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="db789-141">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="db789-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db789-142">-ResourceGroupName</span></span>
<span data-ttu-id="db789-143">Especifica o nome do grupo de recursos que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="db789-143">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="db789-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="db789-144">-RetentionInDays</span></span>
<span data-ttu-id="db789-145">Especifica o número de dias de retenção para a tabela de logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="db789-145">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="db789-146">Um valor igual a zero (0) significa que a tabela não é mantida.</span><span class="sxs-lookup"><span data-stu-id="db789-146">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="db789-147">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="db789-147">this is the default.</span></span>
<span data-ttu-id="db789-148">Se você especificar um valor maior que zero, também deverá especificar um valor para o parâmetro *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="db789-148">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="db789-149">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="db789-149">-ServerName</span></span>
<span data-ttu-id="db789-150">Especifica o nome do servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="db789-150">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db789-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="db789-151">-StorageAccountName</span></span>
<span data-ttu-id="db789-152">Especifica o nome da conta de armazenamento para auditar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="db789-152">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="db789-153">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="db789-153">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="db789-154">Se você não especificar esse parâmetro, o cmdlet usa a conta de armazenamento que foi definida anteriormente como parte da política de auditoria do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="db789-154">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="db789-155">Se esta for a primeira vez que uma política de auditoria de banco de dados for definida e você não especificar esse parâmetro, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="db789-155">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="db789-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="db789-156">-StorageKeyType</span></span>
<span data-ttu-id="db789-157">Especifica quais das chaves de acesso de armazenamento usar.</span><span class="sxs-lookup"><span data-stu-id="db789-157">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="db789-158">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="db789-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="db789-159">Preocupação</span><span class="sxs-lookup"><span data-stu-id="db789-159">Primary</span></span>
- <span data-ttu-id="db789-160">Segundo</span><span class="sxs-lookup"><span data-stu-id="db789-160">Secondary</span></span>

<span data-ttu-id="db789-161">O valor padrão é principal.</span><span class="sxs-lookup"><span data-stu-id="db789-161">The default value is Primary.</span></span>

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

### <span data-ttu-id="db789-162">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="db789-162">-TableIdentifier</span></span>
<span data-ttu-id="db789-163">Especifica o nome da tabela de logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="db789-163">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="db789-164">Especifique esse valor se você especificar um valor maior que zero para o parâmetro *RetentionInDays* .</span><span class="sxs-lookup"><span data-stu-id="db789-164">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="db789-165">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db789-165">-Confirm</span></span>
<span data-ttu-id="db789-166">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db789-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db789-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db789-167">-WhatIf</span></span>
<span data-ttu-id="db789-168">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="db789-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db789-169">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="db789-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db789-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db789-170">CommonParameters</span></span>
<span data-ttu-id="db789-171">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db789-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db789-172">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db789-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db789-173">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db789-173">INPUTS</span></span>

### <span data-ttu-id="db789-174">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="db789-174">None</span></span>
<span data-ttu-id="db789-175">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="db789-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db789-176">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db789-176">OUTPUTS</span></span>

### <span data-ttu-id="db789-177">Microsoft. Azure. Commands. Sql. Security. Model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="db789-177">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="db789-178">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db789-178">NOTES</span></span>

## <span data-ttu-id="db789-179">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db789-179">RELATED LINKS</span></span>

[<span data-ttu-id="db789-180">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="db789-180">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="db789-181">Use-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="db789-181">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="db789-182">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="db789-182">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


