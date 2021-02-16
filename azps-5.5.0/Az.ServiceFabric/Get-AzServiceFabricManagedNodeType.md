---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/get-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 6cca65a061e54bbd08327fc054a0c6b55d8c98f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118643"
---
# <span data-ttu-id="92f10-101">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="92f10-101">Get-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="92f10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92f10-102">SYNOPSIS</span></span>
<span data-ttu-id="92f10-103">Obter detalhes do recurso de tipo de nó gerenciado.</span><span class="sxs-lookup"><span data-stu-id="92f10-103">Get the managed node type resource details.</span></span>

## <span data-ttu-id="92f10-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92f10-104">SYNTAX</span></span>

### <span data-ttu-id="92f10-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="92f10-105">ByName (Default)</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92f10-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92f10-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92f10-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="92f10-107">DESCRIPTION</span></span>
<span data-ttu-id="92f10-108">Obter detalhes do recurso de tipo de nó gerenciado.</span><span class="sxs-lookup"><span data-stu-id="92f10-108">Get the managed node type resource details.</span></span>

## <span data-ttu-id="92f10-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="92f10-109">EXAMPLES</span></span>

### <span data-ttu-id="92f10-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="92f10-110">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName
```

<span data-ttu-id="92f10-111">Obter detalhes do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="92f10-111">Get node type details.</span></span>

### <span data-ttu-id="92f10-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="92f10-112">Example 2</span></span>
```powershell
$rgName = "testRG"
Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName
```

<span data-ttu-id="92f10-113">Obter lista de tipos de nó sob o cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="92f10-113">Get list of node types under the specified cluster.</span></span>

## <span data-ttu-id="92f10-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92f10-114">PARAMETERS</span></span>

### <span data-ttu-id="92f10-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="92f10-115">-ClusterName</span></span>
<span data-ttu-id="92f10-116">Especifique o nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="92f10-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="92f10-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f10-117">-DefaultProfile</span></span>
<span data-ttu-id="92f10-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="92f10-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92f10-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="92f10-119">-Name</span></span>
<span data-ttu-id="92f10-120">Especifique o nome do tipo de nó.</span><span class="sxs-lookup"><span data-stu-id="92f10-120">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="92f10-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92f10-121">-ResourceGroupName</span></span>
<span data-ttu-id="92f10-122">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92f10-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="92f10-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f10-123">CommonParameters</span></span>
<span data-ttu-id="92f10-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92f10-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f10-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="92f10-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f10-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="92f10-126">INPUTS</span></span>

### <span data-ttu-id="92f10-127">System.String</span><span class="sxs-lookup"><span data-stu-id="92f10-127">System.String</span></span>

## <span data-ttu-id="92f10-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="92f10-128">OUTPUTS</span></span>

### <span data-ttu-id="92f10-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="92f10-129">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="92f10-130">Notas</span><span class="sxs-lookup"><span data-stu-id="92f10-130">NOTES</span></span>

## <span data-ttu-id="92f10-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92f10-131">RELATED LINKS</span></span>
