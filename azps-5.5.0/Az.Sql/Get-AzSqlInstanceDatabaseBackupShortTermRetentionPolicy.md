---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116359"
---
# <span data-ttu-id="c5125-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c5125-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="c5125-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5125-102">SYNOPSIS</span></span>
<span data-ttu-id="c5125-103">Obtém uma política de retenção de backup de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="c5125-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="c5125-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5125-104">SYNTAX</span></span>

### <span data-ttu-id="c5125-105">PolicyByResourceInstanceDatabaseSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c5125-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5125-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c5125-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5125-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c5125-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5125-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5125-108">DESCRIPTION</span></span>
<span data-ttu-id="c5125-109">O cmdlet **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** obtém a política de retenção de curto prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c5125-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="c5125-110">A política é o período de retenção, em dias, para backups de restauração de ponto em tempo.</span><span class="sxs-lookup"><span data-stu-id="c5125-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="c5125-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c5125-111">EXAMPLES</span></span>

### <span data-ttu-id="c5125-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5125-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="c5125-113">Esse comando obtém a política de retenção de curto prazo para o banco de dados01.</span><span class="sxs-lookup"><span data-stu-id="c5125-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="c5125-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c5125-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="c5125-115">Esse comando obtém a política de retenção de curto prazo para o banco de dados01 por meio de um objeto de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c5125-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="c5125-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c5125-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="c5125-117">Esse comando obtém a política de retenção de curto prazo para todos os bancos de dados excluídos denominados banco de dados01 por meio de um objeto de banco de dados excluído.</span><span class="sxs-lookup"><span data-stu-id="c5125-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="c5125-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5125-118">PARAMETERS</span></span>

### <span data-ttu-id="c5125-119">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="c5125-119">-DatabaseName</span></span>
<span data-ttu-id="c5125-120">O nome do Banco de Dados de Instância SQL do Azure para o que recuperar backups.</span><span class="sxs-lookup"><span data-stu-id="c5125-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="c5125-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5125-121">-DefaultProfile</span></span>
<span data-ttu-id="c5125-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5125-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5125-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="c5125-123">-DeletionDate</span></span>
<span data-ttu-id="c5125-124">A data de exclusão do Banco de Dados de Instância SQL do Azure para recuperar backups para, com precisão de milissegundos (por exemplo, 2016-02-23T00:21:22,847Z)</span><span class="sxs-lookup"><span data-stu-id="c5125-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="c5125-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5125-125">-InputObject</span></span>
<span data-ttu-id="c5125-126">O objeto de banco de dados ao vivo ou excluído para obter/definir a política.</span><span class="sxs-lookup"><span data-stu-id="c5125-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5125-127">-NomedaE ocorrência</span><span class="sxs-lookup"><span data-stu-id="c5125-127">-InstanceName</span></span>
<span data-ttu-id="c5125-128">O nome da Instância Gerenciada do SQL do Azure no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="c5125-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="c5125-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5125-129">-ResourceGroupName</span></span>
<span data-ttu-id="c5125-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c5125-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c5125-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5125-131">-ResourceId</span></span>
<span data-ttu-id="c5125-132">A ID do recurso de política de retenção de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="c5125-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="c5125-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5125-133">CommonParameters</span></span>
<span data-ttu-id="c5125-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5125-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5125-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5125-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5125-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="c5125-136">INPUTS</span></span>

### <span data-ttu-id="c5125-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="c5125-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="c5125-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c5125-138">System.String</span></span>

## <span data-ttu-id="c5125-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="c5125-139">OUTPUTS</span></span>

### <span data-ttu-id="c5125-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c5125-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="c5125-141">Notas</span><span class="sxs-lookup"><span data-stu-id="c5125-141">NOTES</span></span>

## <span data-ttu-id="c5125-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5125-142">RELATED LINKS</span></span>
