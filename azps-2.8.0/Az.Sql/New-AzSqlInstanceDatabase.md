---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstanceDatabase.md
ms.openlocfilehash: 19f73cf6f2d1906e9390f082bbce7e8000d48515
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773569"
---
# <span data-ttu-id="65afb-101">New-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="65afb-101">New-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="65afb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="65afb-102">SYNOPSIS</span></span>
<span data-ttu-id="65afb-103">Cria um banco de dados de instância gerenciada SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="65afb-103">Creates an Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="65afb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="65afb-104">SYNTAX</span></span>

### <span data-ttu-id="65afb-105">CreateNewInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="65afb-105">CreateNewInstanceDatabaseFromInputParameters (Default)</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-InstanceName] <String> [-ResourceGroupName] <String>
 [-Collation <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65afb-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="65afb-106">CreateNewInstanceDatabaseFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceObject] <AzureSqlManagedInstanceModel> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65afb-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="65afb-107">CreateNewInstanceDatabaseFromAzureSqlInstanceResourceId</span></span>
```
New-AzSqlInstanceDatabase [-Name] <String> [-Collation <String>] [-Tag <Hashtable>]
 [-InstanceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65afb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="65afb-108">DESCRIPTION</span></span>
<span data-ttu-id="65afb-109">O cmdlet **New-AzSqlInstanceDatabase** cria um banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65afb-109">The **New-AzSqlInstanceDatabase** cmdlet creates an Azure SQL Managed instance database.</span></span>

## <span data-ttu-id="65afb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65afb-110">EXAMPLES</span></span>

### <span data-ttu-id="65afb-111">Exemplo 1: criar um banco de dados em uma instância especificada</span><span class="sxs-lookup"><span data-stu-id="65afb-111">Example 1: Create a database on a specified instance</span></span>
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

<span data-ttu-id="65afb-112">Esse comando cria um banco de dados de instância denominado Database01 na instância managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="65afb-112">This command creates a instance database named Database01 on instance managedInstance1.</span></span>

## <span data-ttu-id="65afb-113">OS</span><span class="sxs-lookup"><span data-stu-id="65afb-113">PARAMETERS</span></span>

### <span data-ttu-id="65afb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65afb-114">-AsJob</span></span>
<span data-ttu-id="65afb-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="65afb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65afb-116">-Agrupamento</span><span class="sxs-lookup"><span data-stu-id="65afb-116">-Collation</span></span>
<span data-ttu-id="65afb-117">O agrupamento do agrupamento do banco de dados de instância SQL do Azure a ser usado.</span><span class="sxs-lookup"><span data-stu-id="65afb-117">The collation of the Azure SQL Instance Database collation to use.</span></span>

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

### <span data-ttu-id="65afb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65afb-118">-DefaultProfile</span></span>
<span data-ttu-id="65afb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="65afb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65afb-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="65afb-120">-InstanceName</span></span>
<span data-ttu-id="65afb-121">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="65afb-121">The instance name.</span></span>

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

### <span data-ttu-id="65afb-122">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="65afb-122">-InstanceObject</span></span>
<span data-ttu-id="65afb-123">O objeto de instância</span><span class="sxs-lookup"><span data-stu-id="65afb-123">The instance object</span></span>

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

### <span data-ttu-id="65afb-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="65afb-124">-InstanceResourceId</span></span>
<span data-ttu-id="65afb-125">A ID do recurso da instância</span><span class="sxs-lookup"><span data-stu-id="65afb-125">The instance resource id</span></span>

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

### <span data-ttu-id="65afb-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="65afb-126">-Name</span></span>
<span data-ttu-id="65afb-127">O nome do banco de dados de instância SQL do Azure a ser criado.</span><span class="sxs-lookup"><span data-stu-id="65afb-127">The name of the Azure SQL Instance Database to create.</span></span>

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

### <span data-ttu-id="65afb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65afb-128">-ResourceGroupName</span></span>
<span data-ttu-id="65afb-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="65afb-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="65afb-130">-Marca</span><span class="sxs-lookup"><span data-stu-id="65afb-130">-Tag</span></span>
<span data-ttu-id="65afb-131">As marcas a serem associadas ao banco de dados de instância SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="65afb-131">The tags to associate with the Azure Sql Instance Database</span></span>

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

### <span data-ttu-id="65afb-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="65afb-132">-Confirm</span></span>
<span data-ttu-id="65afb-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65afb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65afb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65afb-134">-WhatIf</span></span>
<span data-ttu-id="65afb-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65afb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65afb-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65afb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65afb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65afb-137">CommonParameters</span></span>
<span data-ttu-id="65afb-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65afb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65afb-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65afb-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65afb-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="65afb-140">INPUTS</span></span>

### <span data-ttu-id="65afb-141">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="65afb-141">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

### <span data-ttu-id="65afb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="65afb-142">System.String</span></span>

## <span data-ttu-id="65afb-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="65afb-143">OUTPUTS</span></span>

### <span data-ttu-id="65afb-144">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="65afb-144">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="65afb-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="65afb-145">NOTES</span></span>

## <span data-ttu-id="65afb-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65afb-146">RELATED LINKS</span></span>
