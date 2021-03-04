---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/get-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Get-AzServiceFabricCluster.md
ms.openlocfilehash: 4695502bddb11b1b033b75057ba5ff3d2bf96b74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885841"
---
# <span data-ttu-id="64906-101">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="64906-101">Get-AzServiceFabricCluster</span></span>

## <span data-ttu-id="64906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64906-102">SYNOPSIS</span></span>
<span data-ttu-id="64906-103">Obter os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="64906-103">Get the cluster resource details.</span></span>

## <span data-ttu-id="64906-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="64906-104">SYNTAX</span></span>

### <span data-ttu-id="64906-105">BySubscription (Padrão)</span><span class="sxs-lookup"><span data-stu-id="64906-105">BySubscription (Default)</span></span>
```
Get-AzServiceFabricCluster [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64906-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="64906-106">ByResourceGroup</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64906-107">ByName</span><span class="sxs-lookup"><span data-stu-id="64906-107">ByName</span></span>
```
Get-AzServiceFabricCluster [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64906-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="64906-108">DESCRIPTION</span></span>
<span data-ttu-id="64906-109">O **Get-AzServiceFabricCluster** receberá os detalhes do recurso de cluster.</span><span class="sxs-lookup"><span data-stu-id="64906-109">The **Get-AzServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="64906-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64906-110">EXAMPLES</span></span>

### <span data-ttu-id="64906-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="64906-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="64906-112">Este comando receberá os detalhes do recurso de cluster para o cluster 'myCluster'.</span><span class="sxs-lookup"><span data-stu-id="64906-112">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="64906-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="64906-113">PARAMETERS</span></span>

### <span data-ttu-id="64906-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64906-114">-DefaultProfile</span></span>
<span data-ttu-id="64906-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64906-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64906-116">-Name</span><span class="sxs-lookup"><span data-stu-id="64906-116">-Name</span></span>
<span data-ttu-id="64906-117">Especificar o nome do cluster</span><span class="sxs-lookup"><span data-stu-id="64906-117">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="64906-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64906-118">-ResourceGroupName</span></span>
<span data-ttu-id="64906-119">Especifique o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64906-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="64906-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64906-120">CommonParameters</span></span>
<span data-ttu-id="64906-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64906-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64906-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64906-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64906-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="64906-123">INPUTS</span></span>

### <span data-ttu-id="64906-124">System.String</span><span class="sxs-lookup"><span data-stu-id="64906-124">System.String</span></span>

## <span data-ttu-id="64906-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="64906-125">OUTPUTS</span></span>

### <span data-ttu-id="64906-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="64906-126">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="64906-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="64906-127">NOTES</span></span>

## <span data-ttu-id="64906-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64906-128">RELATED LINKS</span></span>
