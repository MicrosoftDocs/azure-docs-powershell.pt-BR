---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116685"
---
# <span data-ttu-id="9287f-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="9287f-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="9287f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9287f-102">SYNOPSIS</span></span>
<span data-ttu-id="9287f-103">Criar pool de anotações no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="9287f-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="9287f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9287f-104">SYNTAX</span></span>

### <span data-ttu-id="9287f-105">NameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9287f-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9287f-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9287f-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9287f-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9287f-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9287f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9287f-108">DESCRIPTION</span></span>
<span data-ttu-id="9287f-109">Criar pool de anotações no cluster especificado.</span><span class="sxs-lookup"><span data-stu-id="9287f-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="9287f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9287f-110">EXAMPLES</span></span>

### <span data-ttu-id="9287f-111">Obter todos os pools de nó dentro do cluster especificado</span><span class="sxs-lookup"><span data-stu-id="9287f-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="9287f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9287f-112">PARAMETERS</span></span>

### <span data-ttu-id="9287f-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9287f-113">-ClusterName</span></span>
<span data-ttu-id="9287f-114">O nome do recurso de cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="9287f-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="9287f-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="9287f-115">-ClusterObject</span></span>
<span data-ttu-id="9287f-116">O objeto de cluster.</span><span class="sxs-lookup"><span data-stu-id="9287f-116">The cluster object.</span></span>

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

### <span data-ttu-id="9287f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9287f-117">-DefaultProfile</span></span>
<span data-ttu-id="9287f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9287f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9287f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="9287f-119">-Id</span></span>
<span data-ttu-id="9287f-120">ID de um pool de nó no cluster Desernetes gerenciados</span><span class="sxs-lookup"><span data-stu-id="9287f-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="9287f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9287f-121">-Name</span></span>
<span data-ttu-id="9287f-122">O nome do pool de nó.</span><span class="sxs-lookup"><span data-stu-id="9287f-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="9287f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9287f-123">-ResourceGroupName</span></span>
<span data-ttu-id="9287f-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9287f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9287f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9287f-125">CommonParameters</span></span>
<span data-ttu-id="9287f-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9287f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9287f-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9287f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9287f-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="9287f-128">INPUTS</span></span>

### <span data-ttu-id="9287f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="9287f-129">System.String</span></span>

## <span data-ttu-id="9287f-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="9287f-130">OUTPUTS</span></span>

### <span data-ttu-id="9287f-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="9287f-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="9287f-132">Notas</span><span class="sxs-lookup"><span data-stu-id="9287f-132">NOTES</span></span>

## <span data-ttu-id="9287f-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9287f-133">RELATED LINKS</span></span>
