---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: a21b2436f44cb2df5f9984e70ccecf6c1d9c306a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598979"
---
# <span data-ttu-id="7c229-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="7c229-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="7c229-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c229-102">SYNOPSIS</span></span>
<span data-ttu-id="7c229-103">Retorna informações sobre a instância de banco de dados gerenciado do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7c229-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="7c229-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c229-104">SYNTAX</span></span>

```
Get-AzSqlInstance [[-Name] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c229-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c229-105">DESCRIPTION</span></span>
<span data-ttu-id="7c229-106">O cmdlet **Get-AzSqlInstance** retorna informações sobre uma ou mais instâncias gerenciadas do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="7c229-106">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="7c229-107">Especifique o nome de uma instância para ver informações somente para essa instância.</span><span class="sxs-lookup"><span data-stu-id="7c229-107">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="7c229-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c229-108">EXAMPLES</span></span>

### <span data-ttu-id="7c229-109">Exemplo 1: obter todas as instâncias atribuídas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7c229-109">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="7c229-110">Esse comando obtém informações sobre todas as instâncias atribuídas à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c229-110">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="7c229-111">Exemplo 2: obter informações sobre uma instância</span><span class="sxs-lookup"><span data-stu-id="7c229-111">Example 2: Get information about an  instance</span></span>
```
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="7c229-112">Esse comando obtém informações sobre a instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="7c229-112">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="7c229-113">Exemplo 3: obter todas as instâncias atribuídas a um grupo de recursos usando a filtragem</span><span class="sxs-lookup"><span data-stu-id="7c229-113">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="7c229-114">Esse comando obtém informações sobre todas as instâncias atribuídas ao grupo de recursos ResourceGroup01 que começam com "managedInstance".</span><span class="sxs-lookup"><span data-stu-id="7c229-114">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

## <span data-ttu-id="7c229-115">OS</span><span class="sxs-lookup"><span data-stu-id="7c229-115">PARAMETERS</span></span>

### <span data-ttu-id="7c229-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c229-116">-DefaultProfile</span></span>
<span data-ttu-id="7c229-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7c229-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c229-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c229-118">-Name</span></span>
<span data-ttu-id="7c229-119">Nome da instância SQL.</span><span class="sxs-lookup"><span data-stu-id="7c229-119">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7c229-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c229-120">-ResourceGroupName</span></span>
<span data-ttu-id="7c229-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7c229-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7c229-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c229-122">CommonParameters</span></span>
<span data-ttu-id="7c229-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c229-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c229-124">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c229-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c229-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c229-125">INPUTS</span></span>

### <span data-ttu-id="7c229-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7c229-126">None</span></span>

## <span data-ttu-id="7c229-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c229-127">OUTPUTS</span></span>

### <span data-ttu-id="7c229-128">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7c229-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="7c229-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c229-129">NOTES</span></span>

## <span data-ttu-id="7c229-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c229-130">RELATED LINKS</span></span>
