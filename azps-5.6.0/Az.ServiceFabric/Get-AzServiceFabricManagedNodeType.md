---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 15ba499908a4a631a22f9064b1938d3b32fdafd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885839"
---
# <span data-ttu-id="a9eaa-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a9eaa-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="a9eaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="a9eaa-103">Obter os detalhes do recurso de tipo de nó gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a9eaa-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="a9eaa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a9eaa-104">SYNTAX</span></span>

### <span data-ttu-id="a9eaa-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a9eaa-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9eaa-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a9eaa-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9eaa-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a9eaa-107">DESCRIPTION</span></span>
<span data-ttu-id="a9eaa-108">Obter os detalhes do recurso de tipo de nó gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a9eaa-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="a9eaa-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9eaa-109">EXAMPLES</span></span>

### <span data-ttu-id="a9eaa-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9eaa-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="a9eaa-111">Obter detalhes do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a9eaa-111">Get node type details.</span></span>

### <span data-ttu-id="a9eaa-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a9eaa-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="a9eaa-113">Obter lista de tipos de nó no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="a9eaa-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="a9eaa-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a9eaa-114">PARAMETERS</span></span>

### <span data-ttu-id="a9eaa-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a9eaa-115">-ClusterName</span></span>
<span data-ttu-id="a9eaa-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="a9eaa-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eaa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9eaa-117">-DefaultProfile</span></span>
<span data-ttu-id="a9eaa-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9eaa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9eaa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a9eaa-119">-Name</span></span>
<span data-ttu-id="a9eaa-120">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="a9eaa-120">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eaa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9eaa-121">-ResourceGroupName</span></span>
<span data-ttu-id="a9eaa-122">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a9eaa-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9eaa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9eaa-123">CommonParameters</span></span>
<span data-ttu-id="a9eaa-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9eaa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9eaa-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9eaa-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9eaa-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a9eaa-126">INPUTS</span></span>

### <span data-ttu-id="a9eaa-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a9eaa-127">System.String</span></span>

## <span data-ttu-id="a9eaa-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a9eaa-128">OUTPUTS</span></span>

### <span data-ttu-id="a9eaa-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a9eaa-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="a9eaa-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="a9eaa-130">NOTES</span></span>

## <span data-ttu-id="a9eaa-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9eaa-131">RELATED LINKS</span></span>
