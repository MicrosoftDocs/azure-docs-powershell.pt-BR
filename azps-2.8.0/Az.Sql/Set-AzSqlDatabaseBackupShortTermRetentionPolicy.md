---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: ac63ae50893ec54a2d14431c55229fad71c80c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773780"
---
# <span data-ttu-id="cd157-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cd157-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="cd157-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd157-102">SYNOPSIS</span></span>
<span data-ttu-id="cd157-103">Define uma política de retenção de curto prazo de backup.</span><span class="sxs-lookup"><span data-stu-id="cd157-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="cd157-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd157-104">SYNTAX</span></span>

### <span data-ttu-id="cd157-105">PolicyByResourceServerDatabaseSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="cd157-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd157-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cd157-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd157-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cd157-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd157-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cd157-108">DESCRIPTION</span></span>
<span data-ttu-id="cd157-109">O cmdlet **set-AzSqlDatabaseBackupShortTermRetentionPolicy** Obtém a política de retenção de curto prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cd157-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="cd157-110">A política é o período de retenção, em dias, para backups de restauração point-in-time.</span><span class="sxs-lookup"><span data-stu-id="cd157-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="cd157-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cd157-111">EXAMPLES</span></span>

### <span data-ttu-id="cd157-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cd157-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="cd157-113">Esse comando define a política de retenção de curto prazo para database01 a 35 dias.</span><span class="sxs-lookup"><span data-stu-id="cd157-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="cd157-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cd157-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="cd157-115">Esse comando define a política de retenção de curto prazo para database01 a 35 dias via tubulação em um objeto de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="cd157-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="cd157-116">OS</span><span class="sxs-lookup"><span data-stu-id="cd157-116">PARAMETERS</span></span>

### <span data-ttu-id="cd157-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="cd157-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="cd157-118">O objeto de banco de dados para o qual obter a política.</span><span class="sxs-lookup"><span data-stu-id="cd157-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="cd157-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cd157-119">-DatabaseName</span></span>
<span data-ttu-id="cd157-120">O nome do banco de dados SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="cd157-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="cd157-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd157-121">-DefaultProfile</span></span>
<span data-ttu-id="cd157-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd157-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd157-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd157-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd157-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd157-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="cd157-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd157-125">-ResourceId</span></span>
<span data-ttu-id="cd157-126">A ID do recurso da política de retenção de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="cd157-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="cd157-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="cd157-127">-RetentionDays</span></span>
<span data-ttu-id="cd157-128">A configuração de retenção de backup em dias.</span><span class="sxs-lookup"><span data-stu-id="cd157-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="cd157-129">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="cd157-129">-ServerName</span></span>
<span data-ttu-id="cd157-130">O nome do Azure SQL Server no qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="cd157-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="cd157-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cd157-131">-Confirm</span></span>
<span data-ttu-id="cd157-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd157-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd157-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd157-133">-WhatIf</span></span>
<span data-ttu-id="cd157-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cd157-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd157-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd157-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd157-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd157-136">CommonParameters</span></span>
<span data-ttu-id="cd157-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd157-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd157-138">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd157-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd157-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cd157-139">INPUTS</span></span>

### <span data-ttu-id="cd157-140">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cd157-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="cd157-141">System. String</span><span class="sxs-lookup"><span data-stu-id="cd157-141">System.String</span></span>

## <span data-ttu-id="cd157-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cd157-142">OUTPUTS</span></span>

### <span data-ttu-id="cd157-143">Microsoft. Azure. Commands. Sql. backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="cd157-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="cd157-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cd157-144">NOTES</span></span>

## <span data-ttu-id="cd157-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd157-145">RELATED LINKS</span></span>