---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 6ec4e3163d1bcd388ef0b4b8813ece89a41bfd23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773758"
---
# <span data-ttu-id="33d37-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="33d37-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="33d37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33d37-102">SYNOPSIS</span></span>
<span data-ttu-id="33d37-103">Define uma política de retenção de curto prazo de backup.</span><span class="sxs-lookup"><span data-stu-id="33d37-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="33d37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33d37-104">SYNTAX</span></span>

### <span data-ttu-id="33d37-105">PolicyByResourceInstanceDatabaseSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="33d37-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33d37-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="33d37-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33d37-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="33d37-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33d37-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33d37-108">DESCRIPTION</span></span>
<span data-ttu-id="33d37-109">O cmdlet **set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** Obtém a política de retenção de curto prazo registrada nesse banco de dados.</span><span class="sxs-lookup"><span data-stu-id="33d37-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="33d37-110">A política é o período de retenção, em dias, para backups de restauração point-in-time.</span><span class="sxs-lookup"><span data-stu-id="33d37-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="33d37-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33d37-111">EXAMPLES</span></span>

### <span data-ttu-id="33d37-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33d37-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="33d37-113">Esse comando define a política de retenção de curto prazo para database01 a 35 dias.</span><span class="sxs-lookup"><span data-stu-id="33d37-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="33d37-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="33d37-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="33d37-115">Esse comando define a política de retenção de curto prazo para database01 a 35 dias via tubulação em um objeto de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="33d37-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="33d37-116">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="33d37-116">Example 3</span></span>
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

<span data-ttu-id="33d37-117">Esse comando define a política de retenção de curto prazo para todos os bancos de dados excluídos denominados DB1 via tubulação em um objeto de banco de dados excluído.</span><span class="sxs-lookup"><span data-stu-id="33d37-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="33d37-118">Observação Você só pode reduzir o período de retenção em bancos de dados excluídos.</span><span class="sxs-lookup"><span data-stu-id="33d37-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="33d37-119">OS</span><span class="sxs-lookup"><span data-stu-id="33d37-119">PARAMETERS</span></span>

### <span data-ttu-id="33d37-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="33d37-120">-DatabaseName</span></span>
<span data-ttu-id="33d37-121">O nome do banco de dados de instância SQL do Azure para a recuperação de backups.</span><span class="sxs-lookup"><span data-stu-id="33d37-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="33d37-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d37-122">-DefaultProfile</span></span>
<span data-ttu-id="33d37-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="33d37-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d37-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="33d37-124">-DeletionDate</span></span>
<span data-ttu-id="33d37-125">A data de exclusão do banco de dados de instância SQL do Azure para recuperar backups para, com a precisão de milissegundos (por exemplo, 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="33d37-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="33d37-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33d37-126">-InputObject</span></span>
<span data-ttu-id="33d37-127">O objeto de banco de dados ao vivo ou excluído para obter/definir a política para.</span><span class="sxs-lookup"><span data-stu-id="33d37-127">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="33d37-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="33d37-128">-InstanceName</span></span>
<span data-ttu-id="33d37-129">O nome da instância gerenciada SQL do Azure na qual o banco de dados está.</span><span class="sxs-lookup"><span data-stu-id="33d37-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="33d37-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d37-130">-ResourceGroupName</span></span>
<span data-ttu-id="33d37-131">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="33d37-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="33d37-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33d37-132">-ResourceId</span></span>
<span data-ttu-id="33d37-133">A ID do recurso da política de retenção de curto prazo.</span><span class="sxs-lookup"><span data-stu-id="33d37-133">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="33d37-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="33d37-134">-RetentionDays</span></span>
<span data-ttu-id="33d37-135">Dias de retenção de backup.</span><span class="sxs-lookup"><span data-stu-id="33d37-135">Days of backup retention.</span></span>

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

### <span data-ttu-id="33d37-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="33d37-136">-Confirm</span></span>
<span data-ttu-id="33d37-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33d37-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33d37-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33d37-138">-WhatIf</span></span>
<span data-ttu-id="33d37-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="33d37-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33d37-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="33d37-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33d37-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d37-141">CommonParameters</span></span>
<span data-ttu-id="33d37-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d37-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d37-143">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33d37-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d37-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33d37-144">INPUTS</span></span>

### <span data-ttu-id="33d37-145">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="33d37-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="33d37-146">System. String</span><span class="sxs-lookup"><span data-stu-id="33d37-146">System.String</span></span>

## <span data-ttu-id="33d37-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33d37-147">OUTPUTS</span></span>

### <span data-ttu-id="33d37-148">Microsoft. Azure. Commands. Sql. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="33d37-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="33d37-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33d37-149">NOTES</span></span>

## <span data-ttu-id="33d37-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33d37-150">RELATED LINKS</span></span>