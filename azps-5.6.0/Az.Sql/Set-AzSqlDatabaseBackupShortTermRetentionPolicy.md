---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: ccdcf55b61b57b54848f3310d7366bb76e0f6805
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890944"
---
# <span data-ttu-id="f6024-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f6024-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="f6024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6024-102">SYNOPSIS</span></span>
<span data-ttu-id="f6024-103">Define uma política de retenção de curto prazo de backup.</span><span class="sxs-lookup"><span data-stu-id="f6024-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="f6024-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f6024-104">SYNTAX</span></span>

### <span data-ttu-id="f6024-105">PolicyByResourceServerDatabaseSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f6024-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6024-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f6024-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6024-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f6024-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6024-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f6024-108">DESCRIPTION</span></span>
<span data-ttu-id="f6024-109">O cmdlet **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** obtém a política de retenção de curto prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f6024-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="f6024-110">A política é o período de retenção, em dias, para backups de restauração point-in-time.</span><span class="sxs-lookup"><span data-stu-id="f6024-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="f6024-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6024-111">EXAMPLES</span></span>

### <span data-ttu-id="f6024-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6024-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="f6024-113">Este comando define a política de retenção de curto prazo para database01 como 35 dias.</span><span class="sxs-lookup"><span data-stu-id="f6024-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="f6024-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f6024-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="f6024-115">Este comando define a política de retenção de curto prazo para database01 como 35 dias por meio da canalização em um objeto de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f6024-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="f6024-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f6024-116">PARAMETERS</span></span>

### <span data-ttu-id="f6024-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f6024-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="f6024-118">O objeto database para o que obter a política.</span><span class="sxs-lookup"><span data-stu-id="f6024-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6024-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6024-119">-DatabaseName</span></span>
<span data-ttu-id="f6024-120">O nome do banco de dados do Azure SQL a ser usado.</span><span class="sxs-lookup"><span data-stu-id="f6024-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6024-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6024-121">-DefaultProfile</span></span>
<span data-ttu-id="f6024-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6024-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6024-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6024-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6024-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f6024-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6024-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6024-125">-ResourceId</span></span>
<span data-ttu-id="f6024-126">A ID do recurso de política de retenção de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="f6024-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6024-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="f6024-127">-RetentionDays</span></span>
<span data-ttu-id="f6024-128">A configuração de retenção de backup, em dias.</span><span class="sxs-lookup"><span data-stu-id="f6024-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="f6024-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f6024-129">-ServerName</span></span>
<span data-ttu-id="f6024-130">O nome do Azure SQL Server o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="f6024-130">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6024-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6024-131">-Confirm</span></span>
<span data-ttu-id="f6024-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6024-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6024-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6024-133">-WhatIf</span></span>
<span data-ttu-id="f6024-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6024-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6024-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6024-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6024-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6024-136">CommonParameters</span></span>
<span data-ttu-id="f6024-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6024-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6024-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6024-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6024-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6024-139">INPUTS</span></span>

### <span data-ttu-id="f6024-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f6024-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="f6024-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f6024-141">System.String</span></span>

## <span data-ttu-id="f6024-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f6024-142">OUTPUTS</span></span>

### <span data-ttu-id="f6024-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f6024-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="f6024-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="f6024-144">NOTES</span></span>

## <span data-ttu-id="f6024-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6024-145">RELATED LINKS</span></span>
