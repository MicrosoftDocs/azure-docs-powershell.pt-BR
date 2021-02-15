---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112556"
---
# <span data-ttu-id="17464-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="17464-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="17464-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17464-102">SYNOPSIS</span></span>
<span data-ttu-id="17464-103">Obtém uma política de retenção de backup de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="17464-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="17464-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17464-104">SYNTAX</span></span>

### <span data-ttu-id="17464-105">PolicyByResourceServerDatabaseSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17464-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17464-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="17464-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="17464-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="17464-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="17464-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="17464-108">DESCRIPTION</span></span>
<span data-ttu-id="17464-109">O cmdlet **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** obtém a política de retenção de curto prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="17464-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="17464-110">A política é o período de retenção, em dias, para backups de restauração de ponto em tempo.</span><span class="sxs-lookup"><span data-stu-id="17464-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="17464-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17464-111">EXAMPLES</span></span>

### <span data-ttu-id="17464-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17464-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="17464-113">Esse comando obtém a política de retenção de curto prazo para o banco de dados01.</span><span class="sxs-lookup"><span data-stu-id="17464-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="17464-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="17464-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="17464-115">Esse comando obtém a política de retenção de curto prazo para o banco de dados01 por meio de um objeto de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="17464-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="17464-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17464-116">PARAMETERS</span></span>

### <span data-ttu-id="17464-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="17464-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="17464-118">O objeto de banco de dados para o que obter a política.</span><span class="sxs-lookup"><span data-stu-id="17464-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="17464-119">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="17464-119">-DatabaseName</span></span>
<span data-ttu-id="17464-120">O nome do banco de dados SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="17464-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="17464-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17464-121">-DefaultProfile</span></span>
<span data-ttu-id="17464-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17464-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17464-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17464-123">-ResourceGroupName</span></span>
<span data-ttu-id="17464-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17464-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="17464-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17464-125">-ResourceId</span></span>
<span data-ttu-id="17464-126">A ID do recurso de política de retenção de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="17464-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="17464-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="17464-127">-ServerName</span></span>
<span data-ttu-id="17464-128">O nome do SQL Server do Azure no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="17464-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="17464-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17464-129">CommonParameters</span></span>
<span data-ttu-id="17464-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17464-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17464-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17464-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17464-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="17464-132">INPUTS</span></span>

### <span data-ttu-id="17464-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="17464-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="17464-134">System.String</span><span class="sxs-lookup"><span data-stu-id="17464-134">System.String</span></span>

## <span data-ttu-id="17464-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="17464-135">OUTPUTS</span></span>

### <span data-ttu-id="17464-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="17464-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="17464-137">Notas</span><span class="sxs-lookup"><span data-stu-id="17464-137">NOTES</span></span>

## <span data-ttu-id="17464-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17464-138">RELATED LINKS</span></span>
