---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a6d09b573225efa5f8467e9ca02edb65a87ebe10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429946"
---
# <span data-ttu-id="ef902-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="ef902-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="ef902-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef902-102">SYNOPSIS</span></span>
<span data-ttu-id="ef902-103">Altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef902-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef902-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef902-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef902-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef902-105">DESCRIPTION</span></span>
<span data-ttu-id="ef902-106">O cmdlet **set-AzureRmSqlDatabaseAuditing** altera as configurações de auditoria de um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef902-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="ef902-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* , *ServerName* e *DatabaseName* para identificar o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ef902-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ef902-108">Especifique o parâmetro *StorageAccountName* para especificar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="ef902-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="ef902-109">Use o parâmetro *State* para habilitar/desabilitar a política.</span><span class="sxs-lookup"><span data-stu-id="ef902-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="ef902-110">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="ef902-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="ef902-111">Depois que o cmdlet é executado com êxito, a auditoria do banco de dados é habilitada.</span><span class="sxs-lookup"><span data-stu-id="ef902-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="ef902-112">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve a política de auditoria de blob atual, além dos identificadores de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ef902-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="ef902-113">Os identificadores de banco de dados incluem, entre outros, **ResourceGroupName** , **nomedoservidor** e **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="ef902-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="ef902-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef902-114">EXAMPLES</span></span>

### <span data-ttu-id="ef902-115">Exemplo 1: habilitar a política de auditoria de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ef902-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="ef902-116">Exemplo 2: desabilitar a política de auditoria de blob de um banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="ef902-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="ef902-117">OS</span><span class="sxs-lookup"><span data-stu-id="ef902-117">PARAMETERS</span></span>

### <span data-ttu-id="ef902-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="ef902-118">-AuditAction</span></span>
<span data-ttu-id="ef902-119">O conjunto de ações de auditoria</span><span class="sxs-lookup"><span data-stu-id="ef902-119">The set of the audit actions</span></span>

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

### <span data-ttu-id="ef902-120">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="ef902-120">-AuditActionGroup</span></span>
<span data-ttu-id="ef902-121">O conjunto dos grupos de ação de auditoria</span><span class="sxs-lookup"><span data-stu-id="ef902-121">The set of the audit action groups</span></span>

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

### <span data-ttu-id="ef902-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef902-122">-DatabaseName</span></span>
<span data-ttu-id="ef902-123">Nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="ef902-123">SQL Database name.</span></span>

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

### <span data-ttu-id="ef902-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef902-124">-PassThru</span></span>
<span data-ttu-id="ef902-125">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="ef902-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ef902-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef902-126">-ResourceGroupName</span></span>
<span data-ttu-id="ef902-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ef902-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef902-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ef902-128">-RetentionInDays</span></span>
<span data-ttu-id="ef902-129">O número de dias de retenção para os logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="ef902-129">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="ef902-130">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="ef902-130">-ServerName</span></span>
<span data-ttu-id="ef902-131">Nome do servidor do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="ef902-131">SQL Database server name.</span></span>

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

### <span data-ttu-id="ef902-132">-Estado</span><span class="sxs-lookup"><span data-stu-id="ef902-132">-State</span></span>
<span data-ttu-id="ef902-133">O estado da política de auditoria</span><span class="sxs-lookup"><span data-stu-id="ef902-133">The state of the auditing policy</span></span>

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

### <span data-ttu-id="ef902-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ef902-134">-StorageAccountName</span></span>
<span data-ttu-id="ef902-135">O nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ef902-135">The name of the storage account</span></span>

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

### <span data-ttu-id="ef902-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="ef902-136">-StorageKeyType</span></span>
<span data-ttu-id="ef902-137">O tipo da chave de armazenamento</span><span class="sxs-lookup"><span data-stu-id="ef902-137">The type of the storage key</span></span>

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

### <span data-ttu-id="ef902-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ef902-138">-Confirm</span></span>
<span data-ttu-id="ef902-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef902-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef902-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef902-140">-WhatIf</span></span>
<span data-ttu-id="ef902-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ef902-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef902-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ef902-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef902-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef902-143">-DefaultProfile</span></span>
<span data-ttu-id="ef902-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef902-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef902-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef902-145">CommonParameters</span></span>
<span data-ttu-id="ef902-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef902-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef902-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef902-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef902-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef902-148">INPUTS</span></span>

## <span data-ttu-id="ef902-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef902-149">OUTPUTS</span></span>

### <span data-ttu-id="ef902-150">Microsoft. Azure. Commands. Sql. Security. Model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="ef902-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="ef902-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef902-151">NOTES</span></span>

## <span data-ttu-id="ef902-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef902-152">RELATED LINKS</span></span>

