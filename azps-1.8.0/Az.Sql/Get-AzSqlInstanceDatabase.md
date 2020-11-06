---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabase.md
ms.openlocfilehash: 63eb337f4c81658b8263066dd39e1af0634c49e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598976"
---
# <span data-ttu-id="99f6e-101">Get-AzSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="99f6e-101">Get-AzSqlInstanceDatabase</span></span>

## <span data-ttu-id="99f6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="99f6e-103">Retorna informações sobre o banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="99f6e-103">Returns information about Azure SQL Managed Instance database.</span></span>

## <span data-ttu-id="99f6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99f6e-104">SYNTAX</span></span>

### <span data-ttu-id="99f6e-105">GetInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="99f6e-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99f6e-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="99f6e-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99f6e-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="99f6e-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99f6e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99f6e-108">DESCRIPTION</span></span>
<span data-ttu-id="99f6e-109">O cmdlet **Get-AzSqlInstanceDatabase** Obtém um ou mais bancos de dados SQL do Azure de uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="99f6e-109">The **Get-AzSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="99f6e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99f6e-110">EXAMPLES</span></span>

### <span data-ttu-id="99f6e-111">Exemplo 1: obter todos os bancos de dados em uma instância</span><span class="sxs-lookup"><span data-stu-id="99f6e-111">Example 1: Get all databases on a instance</span></span>
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

<span data-ttu-id="99f6e-112">Esse comando obtém todos os bancos de dados na instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="99f6e-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="99f6e-113">Exemplo 2: obter um banco de dados por nome em uma instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="99f6e-113">Example 2: Get a database by name on a Managed instance</span></span>
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

<span data-ttu-id="99f6e-114">Esse comando obtém um banco de dados denominado managedDatabase1 de uma instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="99f6e-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

### <span data-ttu-id="99f6e-115">Exemplo 3: obter todos os bancos de dados em uma instância usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="99f6e-115">Example 3: Get all databases on a instance using filtering</span></span>
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

<span data-ttu-id="99f6e-116">Esse comando obtém todos os bancos de dados na instância chamada managedInstance1 que começam com "managedDatabase".</span><span class="sxs-lookup"><span data-stu-id="99f6e-116">This command gets all databases on the instance named managedInstance1 that start with "managedDatabase".</span></span>

## <span data-ttu-id="99f6e-117">OS</span><span class="sxs-lookup"><span data-stu-id="99f6e-117">PARAMETERS</span></span>

### <span data-ttu-id="99f6e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99f6e-118">-DefaultProfile</span></span>
<span data-ttu-id="99f6e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="99f6e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99f6e-120">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="99f6e-120">-InstanceName</span></span>
<span data-ttu-id="99f6e-121">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="99f6e-121">The instance name.</span></span>

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

### <span data-ttu-id="99f6e-122">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="99f6e-122">-InstanceObject</span></span>
<span data-ttu-id="99f6e-123">O objeto de instância a ser usado para obter o banco de dados de instância</span><span class="sxs-lookup"><span data-stu-id="99f6e-123">The instance object to use for getting instance database</span></span>

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

### <span data-ttu-id="99f6e-124">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="99f6e-124">-InstanceResourceId</span></span>
<span data-ttu-id="99f6e-125">A ID do recurso do objeto de instância a ser obtido</span><span class="sxs-lookup"><span data-stu-id="99f6e-125">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="99f6e-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="99f6e-126">-Name</span></span>
<span data-ttu-id="99f6e-127">O nome do banco de dados de instância SQL do Azure a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="99f6e-127">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="99f6e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99f6e-128">-ResourceGroupName</span></span>
<span data-ttu-id="99f6e-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="99f6e-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="99f6e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99f6e-130">CommonParameters</span></span>
<span data-ttu-id="99f6e-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99f6e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99f6e-132">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99f6e-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99f6e-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99f6e-133">INPUTS</span></span>

### <span data-ttu-id="99f6e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="99f6e-134">System.String</span></span>

### <span data-ttu-id="99f6e-135">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="99f6e-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="99f6e-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99f6e-136">OUTPUTS</span></span>

### <span data-ttu-id="99f6e-137">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="99f6e-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="99f6e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99f6e-138">NOTES</span></span>

## <span data-ttu-id="99f6e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99f6e-139">RELATED LINKS</span></span>
