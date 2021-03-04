---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 5a67faaf48d96a93fe1bc3e6380abb4fe6d03d98
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885840"
---
# <span data-ttu-id="2aaf3-101">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2aaf3-101">Get-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="2aaf3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2aaf3-102">SYNOPSIS</span></span>
<span data-ttu-id="2aaf3-103">Obter os detalhes do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2aaf3-103">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="2aaf3-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2aaf3-104">SYNTAX</span></span>

### <span data-ttu-id="2aaf3-105">BySubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2aaf3-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricManagedCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2aaf3-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2aaf3-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2aaf3-107">ByName</span><span class="sxs-lookup"><span data-stu-id="2aaf3-107">ByName</span></span>
```
Get-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aaf3-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2aaf3-108">DESCRIPTION</span></span>
<span data-ttu-id="2aaf3-109">Obter os detalhes do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2aaf3-109">Get the managed cluster resource details.</span></span>

## <span data-ttu-id="2aaf3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2aaf3-110">EXAMPLES</span></span>

### <span data-ttu-id="2aaf3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2aaf3-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName
```

<span data-ttu-id="2aaf3-112">Obter detalhes do cluster.</span><span class="sxs-lookup"><span data-stu-id="2aaf3-112">Get cluster details.</span></span>

### <span data-ttu-id="2aaf3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="2aaf3-113">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName
```

<span data-ttu-id="2aaf3-114">Obter lista de clusters no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2aaf3-114">Get list of clusters under the specified resource group.</span></span>

### <span data-ttu-id="2aaf3-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2aaf3-115">Example 3</span></span>
```powershell
Get-AzServiceFabricManagedCluster
```

<span data-ttu-id="2aaf3-116">Obter lista de clusters na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="2aaf3-116">Get list of clusters under the current subscription.</span></span>

## <span data-ttu-id="2aaf3-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2aaf3-117">PARAMETERS</span></span>

### <span data-ttu-id="2aaf3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aaf3-118">-DefaultProfile</span></span>
<span data-ttu-id="2aaf3-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2aaf3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aaf3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2aaf3-120">-Name</span></span>
<span data-ttu-id="2aaf3-121">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="2aaf3-121">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aaf3-122">-ResourceGroupName</span></span>
<span data-ttu-id="2aaf3-123">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2aaf3-123">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup, ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aaf3-124">CommonParameters</span></span>
<span data-ttu-id="2aaf3-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aaf3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aaf3-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aaf3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aaf3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2aaf3-127">INPUTS</span></span>

### <span data-ttu-id="2aaf3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2aaf3-128">System.String</span></span>

## <span data-ttu-id="2aaf3-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2aaf3-129">OUTPUTS</span></span>

### <span data-ttu-id="2aaf3-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2aaf3-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="2aaf3-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="2aaf3-131">NOTES</span></span>

## <span data-ttu-id="2aaf3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2aaf3-132">RELATED LINKS</span></span>
