---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281594"
---
# <span data-ttu-id="e8ecd-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e8ecd-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="e8ecd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e8ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ecd-103">Obter os detalhes do recurso de tipo de nó gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e8ecd-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="e8ecd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8ecd-104">SYNTAX</span></span>

### <span data-ttu-id="e8ecd-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e8ecd-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8ecd-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8ecd-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8ecd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e8ecd-107">DESCRIPTION</span></span>
<span data-ttu-id="e8ecd-108">Obter os detalhes do recurso de tipo de nó gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e8ecd-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="e8ecd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e8ecd-109">EXAMPLES</span></span>

### <span data-ttu-id="e8ecd-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8ecd-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="e8ecd-111">Obter detalhes do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="e8ecd-111">Get node type details.</span></span>

### <span data-ttu-id="e8ecd-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e8ecd-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="e8ecd-113">Obter a lista de tipos de nós no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="e8ecd-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="e8ecd-114">OS</span><span class="sxs-lookup"><span data-stu-id="e8ecd-114">PARAMETERS</span></span>

### <span data-ttu-id="e8ecd-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e8ecd-115">-ClusterName</span></span>
<span data-ttu-id="e8ecd-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="e8ecd-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e8ecd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ecd-117">-DefaultProfile</span></span>
<span data-ttu-id="e8ecd-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e8ecd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ecd-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8ecd-119">-Name</span></span>
<span data-ttu-id="e8ecd-120">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="e8ecd-120">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="e8ecd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ecd-121">-ResourceGroupName</span></span>
<span data-ttu-id="e8ecd-122">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e8ecd-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e8ecd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ecd-123">CommonParameters</span></span>
<span data-ttu-id="e8ecd-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8ecd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ecd-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8ecd-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ecd-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e8ecd-126">INPUTS</span></span>

### <span data-ttu-id="e8ecd-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e8ecd-127">System.String</span></span>

## <span data-ttu-id="e8ecd-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e8ecd-128">OUTPUTS</span></span>

### <span data-ttu-id="e8ecd-129">Microsoft. Azure. Commands. imfabric. Models. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="e8ecd-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="e8ecd-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e8ecd-130">NOTES</span></span>

## <span data-ttu-id="e8ecd-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e8ecd-131">RELATED LINKS</span></span>
