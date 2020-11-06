---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431759"
---
# <span data-ttu-id="b89c9-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="b89c9-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="b89c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b89c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b89c9-103">Altera as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="b89c9-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b89c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b89c9-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b89c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b89c9-105">DESCRIPTION</span></span>
<span data-ttu-id="b89c9-106">O cmdlet **set-AzureRmSqlServerAuditing** altera as configurações de auditoria de um SQL Server do Azure.</span><span class="sxs-lookup"><span data-stu-id="b89c9-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="b89c9-107">Para usar o cmdlet, use os parâmetros *ResourceGroupName* e *ServerName* para identificar o servidor.</span><span class="sxs-lookup"><span data-stu-id="b89c9-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="b89c9-108">Especifique o parâmetro *StorageAccountName* para especificar a conta de armazenamento para os logs de auditoria e o parâmetro *StorageKeyType* para definir as chaves de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b89c9-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="b89c9-109">Use o parâmetro *State* para habilitar/desabilitar a política.</span><span class="sxs-lookup"><span data-stu-id="b89c9-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="b89c9-110">Você também pode definir a retenção para os logs de auditoria definindo o valor do parâmetro *RetentionInDays* para definir o período para os logs de auditoria.</span><span class="sxs-lookup"><span data-stu-id="b89c9-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="b89c9-111">Após a execução bem-sucedida do cmdlet, a auditoria dos bancos de dados SQL do Azure definidos no Azure SQL Server especificado está habilitada.</span><span class="sxs-lookup"><span data-stu-id="b89c9-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="b89c9-112">Se o cmdlet for bem-sucedido e você usar o parâmetro *PassThru* , ele retornará um objeto que descreve a política de auditoria de blob atual, além dos identificadores de servidor.</span><span class="sxs-lookup"><span data-stu-id="b89c9-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="b89c9-113">Os identificadores de servidor incluem, entre outros, **ResourceGroupName** e **nomedoservidor**.</span><span class="sxs-lookup"><span data-stu-id="b89c9-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="b89c9-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b89c9-114">EXAMPLES</span></span>

### <span data-ttu-id="b89c9-115">Exemplo 1: habilitar a política de auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="b89c9-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="b89c9-116">Exemplo 2: desabilitar a política de auditoria de um SQL Server do Azure</span><span class="sxs-lookup"><span data-stu-id="b89c9-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="b89c9-117">OS</span><span class="sxs-lookup"><span data-stu-id="b89c9-117">PARAMETERS</span></span>

### <span data-ttu-id="b89c9-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="b89c9-118">-AuditActionGroup</span></span>
<span data-ttu-id="b89c9-119">O conjunto dos grupos de ação de auditoria</span><span class="sxs-lookup"><span data-stu-id="b89c9-119">The set of the audit action groups</span></span>

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

### <span data-ttu-id="b89c9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b89c9-120">-PassThru</span></span>
<span data-ttu-id="b89c9-121">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="b89c9-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b89c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b89c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="b89c9-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b89c9-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="b89c9-124">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="b89c9-124">-RetentionInDays</span></span>
<span data-ttu-id="b89c9-125">O número de dias de retenção para os logs de auditoria</span><span class="sxs-lookup"><span data-stu-id="b89c9-125">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="b89c9-126">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="b89c9-126">-ServerName</span></span>
<span data-ttu-id="b89c9-127">Nome do SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b89c9-127">SQL server name.</span></span>

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

### <span data-ttu-id="b89c9-128">-Estado</span><span class="sxs-lookup"><span data-stu-id="b89c9-128">-State</span></span>
<span data-ttu-id="b89c9-129">O estado da política de auditoria</span><span class="sxs-lookup"><span data-stu-id="b89c9-129">The state of the auditing policy</span></span>

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

### <span data-ttu-id="b89c9-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b89c9-130">-StorageAccountName</span></span>
<span data-ttu-id="b89c9-131">O nome da conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b89c9-131">The name of the storage account</span></span>

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

### <span data-ttu-id="b89c9-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="b89c9-132">-StorageKeyType</span></span>
<span data-ttu-id="b89c9-133">O tipo da chave de armazenamento</span><span class="sxs-lookup"><span data-stu-id="b89c9-133">The type of the storage key</span></span>

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

### <span data-ttu-id="b89c9-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b89c9-134">-Confirm</span></span>
<span data-ttu-id="b89c9-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b89c9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b89c9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b89c9-136">-WhatIf</span></span>
<span data-ttu-id="b89c9-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b89c9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b89c9-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b89c9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b89c9-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89c9-139">-DefaultProfile</span></span>
<span data-ttu-id="b89c9-140">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b89c9-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b89c9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89c9-141">CommonParameters</span></span>
<span data-ttu-id="b89c9-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b89c9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89c9-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89c9-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89c9-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b89c9-144">INPUTS</span></span>

## <span data-ttu-id="b89c9-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b89c9-145">OUTPUTS</span></span>

### <span data-ttu-id="b89c9-146">Microsoft. Azure. Commands. Sql. Security. Model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="b89c9-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="b89c9-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b89c9-147">NOTES</span></span>

## <span data-ttu-id="b89c9-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b89c9-148">RELATED LINKS</span></span>

