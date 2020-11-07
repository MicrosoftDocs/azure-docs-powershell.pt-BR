---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: c52b0a9cafbb5a3e61af3a044ef834e499e88bc5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942810"
---
# <span data-ttu-id="7fa55-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7fa55-101">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>

## <span data-ttu-id="7fa55-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fa55-102">SYNOPSIS</span></span>
<span data-ttu-id="7fa55-103">Exclui um backup de retenção de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="7fa55-103">Deletes a long term retention backup.</span></span>

## <span data-ttu-id="7fa55-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fa55-104">SYNTAX</span></span>

### <span data-ttu-id="7fa55-105">RemoveBackupDefault (padrão)</span><span class="sxs-lookup"><span data-stu-id="7fa55-105">RemoveBackupDefault (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa55-106">RemoveBackupByInputObject</span><span class="sxs-lookup"><span data-stu-id="7fa55-106">RemoveBackupByInputObject</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fa55-107">RemoveBackupByResourceId</span><span class="sxs-lookup"><span data-stu-id="7fa55-107">RemoveBackupByResourceId</span></span>
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fa55-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fa55-108">DESCRIPTION</span></span>
<span data-ttu-id="7fa55-109">O cmdlet **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** exclui o backup especificado.</span><span class="sxs-lookup"><span data-stu-id="7fa55-109">The **Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** cmdlet deletes the backup specified.</span></span>

## <span data-ttu-id="7fa55-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fa55-110">EXAMPLES</span></span>

### <span data-ttu-id="7fa55-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7fa55-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

<span data-ttu-id="7fa55-112">Exclui o backup com o nome 15be823c-7e2c-49d8-819f-a3fdcad92215; 132268250550000000</span><span class="sxs-lookup"><span data-stu-id="7fa55-112">Deletes the backup with name 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000</span></span>

## <span data-ttu-id="7fa55-113">OS</span><span class="sxs-lookup"><span data-stu-id="7fa55-113">PARAMETERS</span></span>

### <span data-ttu-id="7fa55-114">-Backupname</span><span class="sxs-lookup"><span data-stu-id="7fa55-114">-BackupName</span></span>
<span data-ttu-id="7fa55-115">O nome do backup.</span><span class="sxs-lookup"><span data-stu-id="7fa55-115">The name of the backup.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fa55-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7fa55-116">-DatabaseName</span></span>
<span data-ttu-id="7fa55-117">O nome do banco de dados gerenciado do qual o backup se encontra.</span><span class="sxs-lookup"><span data-stu-id="7fa55-117">The name of the Managed Database the backup is from.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fa55-118">-DefaultProfile</span></span>
<span data-ttu-id="7fa55-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fa55-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa55-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7fa55-120">-Force</span></span>
<span data-ttu-id="7fa55-121">Ignorar a mensagem de confirmação para executar a ação</span><span class="sxs-lookup"><span data-stu-id="7fa55-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="7fa55-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fa55-122">-InputObject</span></span>
<span data-ttu-id="7fa55-123">O objeto de backup de retenção de longo prazo do banco de dados a ser removido.</span><span class="sxs-lookup"><span data-stu-id="7fa55-123">The Database Long Term Retention Backup object to remove.</span></span>

```yaml
Type: AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fa55-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7fa55-124">-InstanceName</span></span>
<span data-ttu-id="7fa55-125">O nome da instância gerenciada na qual o backup se encontra.</span><span class="sxs-lookup"><span data-stu-id="7fa55-125">The name of the Managed Instance the backup is under.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa55-126">-Local</span><span class="sxs-lookup"><span data-stu-id="7fa55-126">-Location</span></span>
<span data-ttu-id="7fa55-127">O local da instância gerenciada de origem dos backups.</span><span class="sxs-lookup"><span data-stu-id="7fa55-127">The location of the backups' source Managed Instance.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa55-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fa55-128">-ResourceGroupName</span></span>
<span data-ttu-id="7fa55-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fa55-129">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fa55-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fa55-130">-ResourceId</span></span>
<span data-ttu-id="7fa55-131">A ID do recurso do backup de retenção de longo prazo do banco de dados a ser removida.</span><span class="sxs-lookup"><span data-stu-id="7fa55-131">The Resource ID of the Database Long Term Retention Backup to remove.</span></span>

```yaml
Type: String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fa55-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7fa55-132">-Confirm</span></span>
<span data-ttu-id="7fa55-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fa55-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fa55-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fa55-134">-WhatIf</span></span>
<span data-ttu-id="7fa55-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7fa55-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fa55-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7fa55-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fa55-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fa55-137">CommonParameters</span></span>
<span data-ttu-id="7fa55-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fa55-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fa55-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fa55-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fa55-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fa55-140">INPUTS</span></span>

### <span data-ttu-id="7fa55-141">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="7fa55-141">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

### <span data-ttu-id="7fa55-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7fa55-142">System.String</span></span>

## <span data-ttu-id="7fa55-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fa55-143">OUTPUTS</span></span>

### <span data-ttu-id="7fa55-144">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseLongTermRetentionBackupModel</span><span class="sxs-lookup"><span data-stu-id="7fa55-144">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel</span></span>

## <span data-ttu-id="7fa55-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fa55-145">NOTES</span></span>

## <span data-ttu-id="7fa55-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fa55-146">RELATED LINKS</span></span>

[<span data-ttu-id="7fa55-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="7fa55-147">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="7fa55-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7fa55-148">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="7fa55-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7fa55-149">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="7fa55-150">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="7fa55-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)