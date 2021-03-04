---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 4cb97982ed3649502bcf11ce471cef0231ae3058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887324"
---
# <span data-ttu-id="314f9-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="314f9-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="314f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="314f9-102">SYNOPSIS</span></span>
<span data-ttu-id="314f9-103">Obtém uma política de retenção de curto prazo de backup.</span><span class="sxs-lookup"><span data-stu-id="314f9-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="314f9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="314f9-104">SYNTAX</span></span>

### <span data-ttu-id="314f9-105">PolicyByResourceServerDatabaseSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="314f9-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="314f9-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="314f9-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="314f9-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="314f9-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="314f9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="314f9-108">DESCRIPTION</span></span>
<span data-ttu-id="314f9-109">O cmdlet **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** obtém a política de retenção de curto prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="314f9-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="314f9-110">A política é o período de retenção, em dias, para backups de restauração point-in-time.</span><span class="sxs-lookup"><span data-stu-id="314f9-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="314f9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="314f9-111">EXAMPLES</span></span>

### <span data-ttu-id="314f9-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="314f9-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="314f9-113">Este comando obtém a política de retenção de curto prazo para database01.</span><span class="sxs-lookup"><span data-stu-id="314f9-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="314f9-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="314f9-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="314f9-115">Este comando obtém a política de retenção de curto prazo para database01 por meio de canalização em um objeto de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="314f9-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="314f9-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="314f9-116">PARAMETERS</span></span>

### <span data-ttu-id="314f9-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="314f9-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="314f9-118">O objeto database para o que obter a política.</span><span class="sxs-lookup"><span data-stu-id="314f9-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="314f9-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="314f9-119">-DatabaseName</span></span>
<span data-ttu-id="314f9-120">O nome do banco de dados do Azure SQL a ser usado.</span><span class="sxs-lookup"><span data-stu-id="314f9-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="314f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314f9-121">-DefaultProfile</span></span>
<span data-ttu-id="314f9-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="314f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="314f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="314f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="314f9-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="314f9-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="314f9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="314f9-125">-ResourceId</span></span>
<span data-ttu-id="314f9-126">A ID do recurso de política de retenção de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="314f9-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="314f9-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="314f9-127">-ServerName</span></span>
<span data-ttu-id="314f9-128">O nome do Azure SQL Server o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="314f9-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="314f9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314f9-129">CommonParameters</span></span>
<span data-ttu-id="314f9-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314f9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314f9-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="314f9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314f9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="314f9-132">INPUTS</span></span>

### <span data-ttu-id="314f9-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="314f9-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="314f9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="314f9-134">System.String</span></span>

## <span data-ttu-id="314f9-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="314f9-135">OUTPUTS</span></span>

### <span data-ttu-id="314f9-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="314f9-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="314f9-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="314f9-137">NOTES</span></span>

## <span data-ttu-id="314f9-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="314f9-138">RELATED LINKS</span></span>
