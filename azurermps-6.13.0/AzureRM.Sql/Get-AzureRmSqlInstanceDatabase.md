---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstancedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstanceDatabase.md
ms.openlocfilehash: fe6779c64a3cbc5a484dd4a3ee3662bcdaf59059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430009"
---
# <span data-ttu-id="effff-101">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="effff-101">Get-AzureRmSqlInstanceDatabase</span></span>

## <span data-ttu-id="effff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="effff-102">SYNOPSIS</span></span>
<span data-ttu-id="effff-103">Retorna informações sobre o banco de dados de instância gerenciada do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="effff-103">Returns information about Azure SQL Managed Instance database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="effff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="effff-104">SYNTAX</span></span>

### <span data-ttu-id="effff-105">GetInstanceDatabaseFromInputParameters (padrão)</span><span class="sxs-lookup"><span data-stu-id="effff-105">GetInstanceDatabaseFromInputParameters (Default)</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="effff-106">GetInstanceDatabaseFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="effff-106">GetInstanceDatabaseFromAzureResourceId</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="effff-107">GetInstanceDatabaseFromInstanceObject</span><span class="sxs-lookup"><span data-stu-id="effff-107">GetInstanceDatabaseFromInstanceObject</span></span>
```
Get-AzureRmSqlInstanceDatabase [[-Name] <String>] [-InstanceObject] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="effff-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="effff-108">DESCRIPTION</span></span>
<span data-ttu-id="effff-109">O cmdlet **Get-AzureRmSqlInstanceDatabase** Obtém um ou mais bancos de dados SQL do Azure de uma instância gerenciada do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="effff-109">The **Get-AzureRmSqlInstanceDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="effff-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="effff-110">EXAMPLES</span></span>

### <span data-ttu-id="effff-111">Exemplo 1: obter todos os bancos de dados em uma instância</span><span class="sxs-lookup"><span data-stu-id="effff-111">Example 1: Get all databases on a instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -InstanceName "managedInstance1" -ResourceGroupName "resourcegroup01"
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

<span data-ttu-id="effff-112">Esse comando obtém todos os bancos de dados na instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="effff-112">This command gets all databases on the instance named managedInstance1.</span></span>

### <span data-ttu-id="effff-113">Exemplo 2: obter um banco de dados por nome em uma instância gerenciada</span><span class="sxs-lookup"><span data-stu-id="effff-113">Example 2: Get a database by name on a Managed instance</span></span>
```
PS C:\>Get-AzureRmSqlInstanceDatabase -Name "managedDatabase1" -InstanceName "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="effff-114">Esse comando obtém um banco de dados denominado managedDatabase1 de uma instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="effff-114">This command gets a database named managedDatabase1 from a instance named managedInstance1.</span></span>

## <span data-ttu-id="effff-115">OS</span><span class="sxs-lookup"><span data-stu-id="effff-115">PARAMETERS</span></span>

### <span data-ttu-id="effff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="effff-116">-DefaultProfile</span></span>
<span data-ttu-id="effff-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="effff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="effff-118">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="effff-118">-InstanceName</span></span>
<span data-ttu-id="effff-119">O nome da instância.</span><span class="sxs-lookup"><span data-stu-id="effff-119">The instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="effff-120">-Instanceobject</span><span class="sxs-lookup"><span data-stu-id="effff-120">-InstanceObject</span></span>
<span data-ttu-id="effff-121">O objeto de instância a ser usado para obter o banco de dados de instância</span><span class="sxs-lookup"><span data-stu-id="effff-121">The instance object to use for getting instance database</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: GetInstanceDatabaseFromInstanceObject
Aliases: ParentObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="effff-122">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="effff-122">-InstanceResourceId</span></span>
<span data-ttu-id="effff-123">A ID do recurso do objeto de instância a ser obtido</span><span class="sxs-lookup"><span data-stu-id="effff-123">The resource id of instance object to get</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromAzureResourceId
Aliases: ParentResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="effff-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="effff-124">-Name</span></span>
<span data-ttu-id="effff-125">O nome do banco de dados de instância SQL do Azure a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="effff-125">The name of the Azure SQL Instance Database to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="effff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="effff-126">-ResourceGroupName</span></span>
<span data-ttu-id="effff-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="effff-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceDatabaseFromInputParameters
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="effff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="effff-128">CommonParameters</span></span>
<span data-ttu-id="effff-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="effff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="effff-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="effff-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="effff-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="effff-131">INPUTS</span></span>

### <span data-ttu-id="effff-132">System. String</span><span class="sxs-lookup"><span data-stu-id="effff-132">System.String</span></span>
<span data-ttu-id="effff-133">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="effff-133">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="effff-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="effff-134">OUTPUTS</span></span>

### <span data-ttu-id="effff-135">Microsoft. Azure. Commands. Sql. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="effff-135">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="effff-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="effff-136">NOTES</span></span>

## <span data-ttu-id="effff-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="effff-137">RELATED LINKS</span></span>
