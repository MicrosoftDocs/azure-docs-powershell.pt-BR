---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111324"
---
# <span data-ttu-id="86e82-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="86e82-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="86e82-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86e82-102">SYNOPSIS</span></span>
<span data-ttu-id="86e82-103">Retorna informações sobre o Cluster Virtual SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="86e82-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="86e82-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86e82-104">SYNTAX</span></span>

### <span data-ttu-id="86e82-105">GetVirtualClusterByResourceGroup (Padrão)</span><span class="sxs-lookup"><span data-stu-id="86e82-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="86e82-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="86e82-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86e82-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="86e82-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86e82-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="86e82-108">DESCRIPTION</span></span>
<span data-ttu-id="86e82-109">O cmdlet **Get-AzSqlVirtualCluster** retorna informações sobre um ou mais Clusters Virtuais do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="86e82-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="86e82-110">Especifique o nome de um cluster virtual para ver informações somente para esse cluster.</span><span class="sxs-lookup"><span data-stu-id="86e82-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="86e82-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="86e82-111">EXAMPLES</span></span>

### <span data-ttu-id="86e82-112">Exemplo 1: Obter todos os clusters virtuais atribuídos a um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="86e82-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="86e82-113">Esse comando obtém informações sobre todos os Clusters Virtuais atribuídos ao grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="86e82-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="86e82-114">Exemplo 2: Obter informações sobre cluster virtual específico</span><span class="sxs-lookup"><span data-stu-id="86e82-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="86e82-115">Este comando obtém informações sobre o cluster virtual VirtualCluster1 no grupo de recursos ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="86e82-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="86e82-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86e82-116">PARAMETERS</span></span>

### <span data-ttu-id="86e82-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e82-117">-DefaultProfile</span></span>
<span data-ttu-id="86e82-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86e82-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86e82-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="86e82-119">-Name</span></span>
<span data-ttu-id="86e82-120">O nome do cluster virtual.</span><span class="sxs-lookup"><span data-stu-id="86e82-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="86e82-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e82-121">-ResourceGroupName</span></span>
<span data-ttu-id="86e82-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="86e82-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="86e82-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86e82-123">-ResourceId</span></span>
<span data-ttu-id="86e82-124">A ID do recurso do objeto de instância para obter</span><span class="sxs-lookup"><span data-stu-id="86e82-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="86e82-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e82-125">CommonParameters</span></span>
<span data-ttu-id="86e82-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e82-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e82-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86e82-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e82-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="86e82-128">INPUTS</span></span>

### <span data-ttu-id="86e82-129">Nenhum</span><span class="sxs-lookup"><span data-stu-id="86e82-129">None</span></span>

## <span data-ttu-id="86e82-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="86e82-130">OUTPUTS</span></span>

### <span data-ttu-id="86e82-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="86e82-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="86e82-132">Notas</span><span class="sxs-lookup"><span data-stu-id="86e82-132">NOTES</span></span>

## <span data-ttu-id="86e82-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86e82-133">RELATED LINKS</span></span>
