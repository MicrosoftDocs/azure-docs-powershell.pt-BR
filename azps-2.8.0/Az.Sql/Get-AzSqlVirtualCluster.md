---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: f5e52938a6d0f618d53621a895aeb7037dc543ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773584"
---
# <span data-ttu-id="df4ab-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="df4ab-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="df4ab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df4ab-102">SYNOPSIS</span></span>
<span data-ttu-id="df4ab-103">Retorna informações sobre o cluster virtual do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="df4ab-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="df4ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df4ab-104">SYNTAX</span></span>

### <span data-ttu-id="df4ab-105">GetVirtualClusterByResourceGroup (padrão)</span><span class="sxs-lookup"><span data-stu-id="df4ab-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="df4ab-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="df4ab-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df4ab-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="df4ab-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df4ab-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df4ab-108">DESCRIPTION</span></span>
<span data-ttu-id="df4ab-109">O cmdlet **Get-AzSqlVirtualCluster** retorna informações sobre um ou mais clusters virtuais do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="df4ab-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="df4ab-110">Especifique o nome de um cluster virtual para ver informações somente para esse cluster.</span><span class="sxs-lookup"><span data-stu-id="df4ab-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="df4ab-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df4ab-111">EXAMPLES</span></span>

### <span data-ttu-id="df4ab-112">Exemplo 1: obter todos os clusters virtuais atribuídos a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="df4ab-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="df4ab-113">Esse comando obtém informações sobre todos os clusters virtuais atribuídos à ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df4ab-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="df4ab-114">Exemplo 2: obter informações sobre um cluster virtual específico</span><span class="sxs-lookup"><span data-stu-id="df4ab-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="df4ab-115">Esse comando obtém informações sobre o cluster virtual VirtualCluster1 na ResourceGroup01 do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df4ab-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="df4ab-116">OS</span><span class="sxs-lookup"><span data-stu-id="df4ab-116">PARAMETERS</span></span>

### <span data-ttu-id="df4ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df4ab-117">-DefaultProfile</span></span>
<span data-ttu-id="df4ab-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df4ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df4ab-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="df4ab-119">-Name</span></span>
<span data-ttu-id="df4ab-120">O nome do cluster virtual.</span><span class="sxs-lookup"><span data-stu-id="df4ab-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4ab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df4ab-121">-ResourceGroupName</span></span>
<span data-ttu-id="df4ab-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="df4ab-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df4ab-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df4ab-123">-ResourceId</span></span>
<span data-ttu-id="df4ab-124">A ID do recurso do objeto de instância a ser obtido</span><span class="sxs-lookup"><span data-stu-id="df4ab-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df4ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df4ab-125">CommonParameters</span></span>
<span data-ttu-id="df4ab-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df4ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df4ab-127">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df4ab-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df4ab-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df4ab-128">INPUTS</span></span>

### <span data-ttu-id="df4ab-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="df4ab-129">None</span></span>

## <span data-ttu-id="df4ab-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df4ab-130">OUTPUTS</span></span>

### <span data-ttu-id="df4ab-131">Microsoft. Azure. Commands. Sql. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="df4ab-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="df4ab-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df4ab-132">NOTES</span></span>

## <span data-ttu-id="df4ab-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df4ab-133">RELATED LINKS</span></span>