---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 4385b231a5346af6b49ad3a74c6c984f2f94c416
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891589"
---
# <span data-ttu-id="3c9af-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="3c9af-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="3c9af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c9af-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9af-103">Retorna informações sobre o banco de dados SQL Instância Gerenciada do Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9af-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="3c9af-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3c9af-104">SYNTAX</span></span>

### <span data-ttu-id="3c9af-105">GetInstanceDatabaseFromInputParameters (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3c9af-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c9af-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="3c9af-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c9af-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="3c9af-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c9af-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3c9af-108">DESCRIPTION</span></span>
<span data-ttu-id="3c9af-109">O cmdlet **Get-AzSqlInstanceDatabase** obtém um ou mais bancos de dados do Azure SQL de uma Instância Gerenciada de Banco de Dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3c9af-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="3c9af-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c9af-110">EXAMPLES</span></span>

### <span data-ttu-id="3c9af-111">Exemplo 1: Obter todos os bancos de dados em uma instância</span><span class="sxs-lookup"><span data-stu-id="3c9af-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
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

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="3c9af-112">Esse comando obtém todos os bancos de dados na instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="3c9af-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="3c9af-113">Exemplo 2: Obter um banco de dados pelo nome em uma instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="3c9af-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
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

<span data-ttu-id="3c9af-114">Esse comando obtém um banco de dados chamado managedDatabase1 de uma instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="3c9af-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="3c9af-115">Exemplo 3: Obter todos os bancos de dados em uma instância usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="3c9af-115">Example 3: Get all databases on a instance using filtering</span></span>
```
PS C:\> Get-AzSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01" -Name "managedDatabase*"
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase1
Name                     : managedDatabase1
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

ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1/databases/managedDatabase2
Name                     : managedDatabase2
Tags                     :
Collation                : SQL_Latin1_General_CP1_CI_AS
Status                   : Online
CreationDate             : 4/23/2018 5:21:07 PM
EarliestRestorePoint     : 4/23/2018 5:31:47 PM
RestorePointInTime       :
DefaultSecondaryLocation : West US 2
CatalogCollation         :
CreateMode               :
StorageContainerUri      :
StorageContainerSasToken :
SourceDatabaseId         :
FailoverGroupId          :
```

<span data-ttu-id="3c9af-116">Esse comando obtém todos os bancos de dados na instância denominada managedInstance1 que começam com "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="3c9af-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="3c9af-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3c9af-117">PARAMETERS</span></span>

### <span data-ttu-id="3c9af-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9af-118">-DefaultProfile</span></span>
<span data-ttu-id="3c9af-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9af-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c9af-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="3c9af-120">-InstanceName</span></span>
<span data-ttu-id="3c9af-121">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="3c9af-121">The instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c9af-122">-InstanceObject</span><span class="sxs-lookup"><span data-stu-id="3c9af-122">-InstanceObject</span></span>
<span data-ttu-id="3c9af-123">O objeto instance a ser usado para obter o banco de dados de instância</span><span class="sxs-lookup"><span data-stu-id="3c9af-123">The instance object to use for getting instance database</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c9af-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="3c9af-124">-InstanceResourceId</span></span>
<span data-ttu-id="3c9af-125">A id de recurso do objeto instance a ser obter</span><span class="sxs-lookup"><span data-stu-id="3c9af-125">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c9af-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3c9af-126">-Name</span></span>
<span data-ttu-id="3c9af-127">O nome do Banco de Dados de Instância do Azure SQL a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="3c9af-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c9af-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c9af-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c9af-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="3c9af-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c9af-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9af-130">CommonParameters</span></span>
<span data-ttu-id="3c9af-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c9af-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9af-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c9af-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9af-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c9af-133">INPUTS</span></span>

### <span data-ttu-id="3c9af-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3c9af-134">System.String</span></span>

### <span data-ttu-id="3c9af-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="3c9af-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="3c9af-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3c9af-136">OUTPUTS</span></span>

### <span data-ttu-id="3c9af-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="3c9af-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="3c9af-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="3c9af-138">NOTES</span></span>

## <span data-ttu-id="3c9af-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c9af-139">RELATED LINKS</span></span>
