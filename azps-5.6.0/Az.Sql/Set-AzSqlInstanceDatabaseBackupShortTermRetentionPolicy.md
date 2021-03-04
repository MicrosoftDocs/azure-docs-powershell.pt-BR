---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 0a08176dab2d4bb40d25f11574850d584981063c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889079"
---
# <span data-ttu-id="65ccc-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="65ccc-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="65ccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="65ccc-103">Define uma política de retenção de curto prazo de backup.</span><span class="sxs-lookup"><span data-stu-id="65ccc-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="65ccc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65ccc-104">SYNTAX</span></span>

### <span data-ttu-id="65ccc-105">PolicyByResourceInstanceDatabaseSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65ccc-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65ccc-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="65ccc-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65ccc-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="65ccc-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65ccc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65ccc-108">DESCRIPTION</span></span>
<span data-ttu-id="65ccc-109">O cmdlet **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** obtém a política de retenção de curto prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="65ccc-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="65ccc-110">A política é o período de retenção, em dias, para backups de restauração point-in-time.</span><span class="sxs-lookup"><span data-stu-id="65ccc-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="65ccc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65ccc-111">EXAMPLES</span></span>

### <span data-ttu-id="65ccc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="65ccc-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="65ccc-113">Este comando define a política de retenção de curto prazo para database01 como 35 dias.</span><span class="sxs-lookup"><span data-stu-id="65ccc-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="65ccc-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="65ccc-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="65ccc-115">Este comando define a política de retenção de curto prazo para database01 como 35 dias por meio da canalização em um objeto de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="65ccc-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="65ccc-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="65ccc-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="65ccc-117">Este comando define a política de retenção de curto prazo para todos os bancos de dados excluídos denominados DB1 por meio de canalização em um objeto de banco de dados excluído.</span><span class="sxs-lookup"><span data-stu-id="65ccc-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="65ccc-118">Observe que você só pode reduzir o período de retenção em bancos de dados excluídos.</span><span class="sxs-lookup"><span data-stu-id="65ccc-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="65ccc-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65ccc-119">PARAMETERS</span></span>

### <span data-ttu-id="65ccc-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="65ccc-120">-DatabaseName</span></span>
<span data-ttu-id="65ccc-121">O nome do Banco de Dados SQL instância do Azure para o que recuperar backups.</span><span class="sxs-lookup"><span data-stu-id="65ccc-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ccc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65ccc-122">-DefaultProfile</span></span>
<span data-ttu-id="65ccc-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65ccc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ccc-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="65ccc-124">-DeletionDate</span></span>
<span data-ttu-id="65ccc-125">A data de exclusão do Banco de Dados de Instância do Azure SQL para recuperar backups, com precisão de milissegundos (por exemplo, 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="65ccc-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ccc-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65ccc-126">-InputObject</span></span>
<span data-ttu-id="65ccc-127">O objeto de banco de dados ao vivo ou excluído para obter/definir a política.</span><span class="sxs-lookup"><span data-stu-id="65ccc-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65ccc-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="65ccc-128">-InstanceName</span></span>
<span data-ttu-id="65ccc-129">O nome da Instância Gerenciada do Azure SQL em que o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="65ccc-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ccc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65ccc-130">-ResourceGroupName</span></span>
<span data-ttu-id="65ccc-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65ccc-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ccc-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65ccc-132">-ResourceId</span></span>
<span data-ttu-id="65ccc-133">A ID do recurso de política de retenção de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="65ccc-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65ccc-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="65ccc-134">-RetentionDays</span></span>
<span data-ttu-id="65ccc-135">Dias de retenção de backup.</span><span class="sxs-lookup"><span data-stu-id="65ccc-135">Days of backup retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65ccc-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65ccc-136">-Confirm</span></span>
<span data-ttu-id="65ccc-137">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65ccc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65ccc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65ccc-138">-WhatIf</span></span>
<span data-ttu-id="65ccc-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65ccc-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65ccc-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65ccc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65ccc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65ccc-141">CommonParameters</span></span>
<span data-ttu-id="65ccc-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65ccc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65ccc-143">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65ccc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65ccc-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65ccc-144">INPUTS</span></span>

### <span data-ttu-id="65ccc-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="65ccc-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="65ccc-146">System.String</span><span class="sxs-lookup"><span data-stu-id="65ccc-146">System.String</span></span>

## <span data-ttu-id="65ccc-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65ccc-147">OUTPUTS</span></span>

### <span data-ttu-id="65ccc-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="65ccc-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="65ccc-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="65ccc-149">NOTES</span></span>

## <span data-ttu-id="65ccc-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65ccc-150">RELATED LINKS</span></span>
