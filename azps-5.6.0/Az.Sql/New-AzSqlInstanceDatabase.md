---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 559e23334f9fc98cd51f296aee243152578ba763
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888602"
---
# <span data-ttu-id="45fee-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="45fee-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="45fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45fee-102">SYNOPSIS</span></span>
<span data-ttu-id="45fee-103">Cria um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="45fee-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="45fee-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="45fee-104">SYNTAX</span></span>

### <span data-ttu-id="45fee-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span><span class="sxs-lookup"><span data-stu-id="45fee-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45fee-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="45fee-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45fee-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="45fee-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45fee-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="45fee-108">DESCRIPTION</span></span>
<span data-ttu-id="45fee-109">O cmdlet **New-AzSqlInstanceDatabase** cria um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="45fee-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="45fee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45fee-110">EXAMPLES</span></span>

### <span data-ttu-id="45fee-111">Exemplo 1: Criar um banco de dados em uma instância especificada</span><span class="sxs-lookup"><span data-stu-id="45fee-111">Example 1: Create a database on a specified instance</span></span>
```
PS C:\>New-AzSqlInstanceDatabase -Name "Database01" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/Database01
Name                     : Database01
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/27/2018 2:30:07 PM
EarliestRestorePoint     : 4/27/2018 2:40:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="45fee-112">Este comando cria um banco de dados de instância chamado Database01 na instância managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="45fee-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="45fee-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="45fee-113">PARAMETERS</span></span>

### <span data-ttu-id="45fee-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45fee-114">-AsJob</span></span>
<span data-ttu-id="45fee-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="45fee-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45fee-116">-Collation</span><span class="sxs-lookup"><span data-stu-id="45fee-116">-Collation</span></span>
<span data-ttu-id="45fee-117">O colamento do Azure SQL De banco de dados de instância a ser usado.</span><span class="sxs-lookup"><span data-stu-id="45fee-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45fee-118">-DefaultProfile</span></span>
<span data-ttu-id="45fee-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45fee-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45fee-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="45fee-120">-InstanceName</span></span>
<span data-ttu-id="45fee-121">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="45fee-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fee-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="45fee-122">-InstanceObject</span></span>
<span data-ttu-id="45fee-123">O objeto instance</span><span class="sxs-lookup"><span data-stu-id="45fee-123">The instance object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45fee-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="45fee-124">-InstanceResourceId</span></span>
<span data-ttu-id="45fee-125">A ID do recurso de instância</span><span class="sxs-lookup"><span data-stu-id="45fee-125">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45fee-126">-Name</span><span class="sxs-lookup"><span data-stu-id="45fee-126">-Name</span></span>
<span data-ttu-id="45fee-127">O nome do Banco de Dados de Instância SQL Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="45fee-127">The name of the Azure SQL Instance Database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45fee-128">-ResourceGroupName</span></span>
<span data-ttu-id="45fee-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="45fee-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateNewInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fee-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="45fee-130">-Tag</span></span>
<span data-ttu-id="45fee-131">As marcas a associar ao Banco de Dados de Instância sql do Azure</span><span class="sxs-lookup"><span data-stu-id="45fee-131">The tags to associate with the Azure Sql Instance Database</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45fee-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45fee-132">-Confirm</span></span>
<span data-ttu-id="45fee-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45fee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45fee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45fee-134">-WhatIf</span></span>
<span data-ttu-id="45fee-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45fee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45fee-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45fee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45fee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45fee-137">CommonParameters</span></span>
<span data-ttu-id="45fee-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45fee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45fee-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45fee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45fee-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45fee-140">INPUTS</span></span>

### <span data-ttu-id="45fee-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="45fee-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="45fee-142">System.String</span><span class="sxs-lookup"><span data-stu-id="45fee-142">System.String</span></span>

## <span data-ttu-id="45fee-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="45fee-143">OUTPUTS</span></span>

### <span data-ttu-id="45fee-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="45fee-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="45fee-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="45fee-145">NOTES</span></span>

## <span data-ttu-id="45fee-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45fee-146">RELATED LINKS</span></span>
