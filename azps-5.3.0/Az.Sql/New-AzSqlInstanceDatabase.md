---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 6c8fdc5b54ca802c8c23df577fc0e0e39de0ba16
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427951"
---
# <span data-ttu-id="21c83-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="21c83-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="21c83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21c83-102">SYNOPSIS</span></span>
<span data-ttu-id="21c83-103">Cria um banco de dados de instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="21c83-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="21c83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21c83-104">SYNTAX</span></span>

### <span data-ttu-id="21c83-105">CreateNewInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="21c83-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c83-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="21c83-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21c83-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="21c83-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21c83-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21c83-108">DESCRIPTION</span></span>
<span data-ttu-id="21c83-109">O cmdlet **New-AzSqlInstanceDatabase** cria um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="21c83-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="21c83-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21c83-110">EXAMPLES</span></span>

### <span data-ttu-id="21c83-111">Exemplo 1: criar um banco de dados em uma instância especificada</span><span class="sxs-lookup"><span data-stu-id="21c83-111">Example 1: Create a database on a specified instance</span></span>
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

<span data-ttu-id="21c83-112">Esse comando cria um banco de dados de instância denominado Database01 na instância managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="21c83-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="21c83-113">OS</span><span class="sxs-lookup"><span data-stu-id="21c83-113">PARAMETERS</span></span>

### <span data-ttu-id="21c83-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="21c83-114">-AsJob</span></span>
<span data-ttu-id="21c83-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="21c83-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="21c83-116">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="21c83-116">-Collation</span></span>
<span data-ttu-id="21c83-117">O agrupamento do agrupamento do banco de dados de instância SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="21c83-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="21c83-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c83-118">-DefaultProfile</span></span>
<span data-ttu-id="21c83-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21c83-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21c83-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="21c83-120">-InstanceName</span></span>
<span data-ttu-id="21c83-121">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="21c83-121">The instance name.</span></span>

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

### <span data-ttu-id="21c83-122">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="21c83-122">-InstanceObject</span></span>
<span data-ttu-id="21c83-123">O objeto de instância</span><span class="sxs-lookup"><span data-stu-id="21c83-123">The instance object</span></span>

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

### <span data-ttu-id="21c83-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="21c83-124">-InstanceResourceId</span></span>
<span data-ttu-id="21c83-125">A ID do recurso da instância</span><span class="sxs-lookup"><span data-stu-id="21c83-125">The instance resource id</span></span>

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

### <span data-ttu-id="21c83-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="21c83-126">-Name</span></span>
<span data-ttu-id="21c83-127">O nome do banco de dados de instância SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="21c83-127">The name of the Azure SQL Instance Database to create.</span></span>

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

### <span data-ttu-id="21c83-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c83-128">-ResourceGroupName</span></span>
<span data-ttu-id="21c83-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="21c83-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="21c83-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="21c83-130">-Tag</span></span>
<span data-ttu-id="21c83-131">As marcas a serem associadas ao banco de dados de instância SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="21c83-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="21c83-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="21c83-132">-Confirm</span></span>
<span data-ttu-id="21c83-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21c83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c83-134">-WhatIf</span></span>
<span data-ttu-id="21c83-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="21c83-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21c83-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="21c83-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c83-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c83-137">CommonParameters</span></span>
<span data-ttu-id="21c83-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c83-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c83-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21c83-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c83-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21c83-140">INPUTS</span></span>

### <span data-ttu-id="21c83-141">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="21c83-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="21c83-142">System. String</span><span class="sxs-lookup"><span data-stu-id="21c83-142">System.String</span></span>

## <span data-ttu-id="21c83-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21c83-143">OUTPUTS</span></span>

### <span data-ttu-id="21c83-144">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="21c83-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="21c83-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21c83-145">NOTES</span></span>

## <span data-ttu-id="21c83-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21c83-146">RELATED LINKS</span></span>
