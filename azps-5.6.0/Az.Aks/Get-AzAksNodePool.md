---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 4d6fab247a56054b8c78914f5e47bc5737f8828f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887249"
---
# <span data-ttu-id="2b7e5-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="2b7e5-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="2b7e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b7e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7e5-103">Criar pool de anotações no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="2b7e5-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="2b7e5-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2b7e5-104">SYNTAX</span></span>

### <span data-ttu-id="2b7e5-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2b7e5-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b7e5-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b7e5-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b7e5-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b7e5-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b7e5-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2b7e5-108">DESCRIPTION</span></span>
<span data-ttu-id="2b7e5-109">Criar pool de anotações no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="2b7e5-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="2b7e5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b7e5-110">EXAMPLES</span></span>

### <span data-ttu-id="2b7e5-111">Obter todos os pools de nós dentro do cluster especificado</span><span class="sxs-lookup"><span data-stu-id="2b7e5-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="2b7e5-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2b7e5-112">PARAMETERS</span></span>

### <span data-ttu-id="2b7e5-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2b7e5-113">-ClusterName</span></span>
<span data-ttu-id="2b7e5-114">O nome do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2b7e5-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7e5-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="2b7e5-115">-ClusterObject</span></span>
<span data-ttu-id="2b7e5-116">O objeto cluster.</span><span class="sxs-lookup"><span data-stu-id="2b7e5-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7e5-117">-DefaultProfile</span></span>
<span data-ttu-id="2b7e5-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2b7e5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b7e5-119">-Id</span><span class="sxs-lookup"><span data-stu-id="2b7e5-119">-Id</span></span>
<span data-ttu-id="2b7e5-120">ID de um pool de nós no cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="2b7e5-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7e5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2b7e5-121">-Name</span></span>
<span data-ttu-id="2b7e5-122">O nome do pool de nós.</span><span class="sxs-lookup"><span data-stu-id="2b7e5-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b7e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b7e5-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2b7e5-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7e5-125">CommonParameters</span></span>
<span data-ttu-id="2b7e5-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b7e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7e5-127">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b7e5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7e5-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b7e5-128">INPUTS</span></span>

### <span data-ttu-id="2b7e5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2b7e5-129">System.String</span></span>

## <span data-ttu-id="2b7e5-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2b7e5-130">OUTPUTS</span></span>

### <span data-ttu-id="2b7e5-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="2b7e5-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="2b7e5-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="2b7e5-132">NOTES</span></span>

## <span data-ttu-id="2b7e5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b7e5-133">RELATED LINKS</span></span>
