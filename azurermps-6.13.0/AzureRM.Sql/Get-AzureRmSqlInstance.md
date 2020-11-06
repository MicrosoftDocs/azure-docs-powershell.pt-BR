---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
ms.openlocfilehash: 72e3b740a84a46da094208b941e8b68173133e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431880"
---
# <span data-ttu-id="51877-101">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="51877-101">Get-AzureRmSqlInstance</span></span>

## <span data-ttu-id="51877-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51877-102">SYNOPSIS</span></span>
<span data-ttu-id="51877-103">Retorna informações sobre a instância de banco de dados gerenciado do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="51877-103">Returns information about Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51877-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51877-104">SYNTAX</span></span>

### <span data-ttu-id="51877-105">GetInstanceByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="51877-105">GetInstanceByResourceGroup (Default)</span></span>
```
Get-AzureRmSqlInstance [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="51877-106">GetInstanceByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="51877-106">GetInstanceByNameAndResourceGroup</span></span>
```
Get-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51877-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51877-107">DESCRIPTION</span></span>
<span data-ttu-id="51877-108">O cmdlet **Get-AzureRmSqlInstance** retorna informações sobre uma ou mais instâncias gerenciadas do SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="51877-108">The **Get-AzureRmSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="51877-109">Especifique o nome de uma instância para ver informações somente para essa instância.</span><span class="sxs-lookup"><span data-stu-id="51877-109">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="51877-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51877-110">EXAMPLES</span></span>

### <span data-ttu-id="51877-111">Exemplo 1: obter todas as instâncias atribuídas a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="51877-111">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlInstance -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="51877-112">Esse comando obtém informações sobre todas as instâncias atribuídas à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51877-112">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="51877-113">Exemplo 2: obter informações sobre uma instância</span><span class="sxs-lookup"><span data-stu-id="51877-113">Example 2: Get information about an  instance</span></span>
```
PS C:\>Get-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="51877-114">Esse comando obtém informações sobre a instância chamada managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="51877-114">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="51877-115">OS</span><span class="sxs-lookup"><span data-stu-id="51877-115">PARAMETERS</span></span>

### <span data-ttu-id="51877-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51877-116">-DefaultProfile</span></span>
<span data-ttu-id="51877-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51877-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51877-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="51877-118">-Name</span></span>
<span data-ttu-id="51877-119">Nome da instância SQL.</span><span class="sxs-lookup"><span data-stu-id="51877-119">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51877-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51877-120">-ResourceGroupName</span></span>
<span data-ttu-id="51877-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="51877-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51877-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51877-122">CommonParameters</span></span>
<span data-ttu-id="51877-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51877-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51877-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51877-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51877-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51877-125">INPUTS</span></span>

### <span data-ttu-id="51877-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="51877-126">None</span></span>

## <span data-ttu-id="51877-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51877-127">OUTPUTS</span></span>

### <span data-ttu-id="51877-128">Microsoft. Azure. Commands. Sql. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="51877-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="51877-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51877-129">NOTES</span></span>

## <span data-ttu-id="51877-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51877-130">RELATED LINKS</span></span>
