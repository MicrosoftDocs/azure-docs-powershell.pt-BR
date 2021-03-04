---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: b2cb61ff6b80cb6e0325f006d063d7e0a8971a4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890218"
---
# <span data-ttu-id="4e1e0-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="4e1e0-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="4e1e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="4e1e0-103">Excluir cluster</span><span class="sxs-lookup"><span data-stu-id="4e1e0-103">Delete cluster</span></span>

## <span data-ttu-id="4e1e0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4e1e0-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e1e0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4e1e0-105">DESCRIPTION</span></span>
<span data-ttu-id="4e1e0-106">Excluir cluster, aplicar somente a clusters com estado de provisionamento "Bem-sucedido"</span><span class="sxs-lookup"><span data-stu-id="4e1e0-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="4e1e0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4e1e0-107">EXAMPLES</span></span>

### <span data-ttu-id="4e1e0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4e1e0-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="4e1e0-109">Excluir cluster</span><span class="sxs-lookup"><span data-stu-id="4e1e0-109">Delete cluster</span></span>

## <span data-ttu-id="4e1e0-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4e1e0-110">PARAMETERS</span></span>

### <span data-ttu-id="4e1e0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e1e0-111">-AsJob</span></span>
<span data-ttu-id="4e1e0-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="4e1e0-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1e0-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4e1e0-113">-ClusterName</span></span>
<span data-ttu-id="4e1e0-114">O nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1e0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e1e0-115">-DefaultProfile</span></span>
<span data-ttu-id="4e1e0-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1e0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e1e0-117">-ResourceGroupName</span></span>
<span data-ttu-id="4e1e0-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1e0-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e1e0-119">-Confirm</span></span>
<span data-ttu-id="4e1e0-120">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1e0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e1e0-121">-WhatIf</span></span>
<span data-ttu-id="4e1e0-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e1e0-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e1e0-124">CommonParameters</span></span>
<span data-ttu-id="4e1e0-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e1e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e1e0-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e1e0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e1e0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e1e0-127">INPUTS</span></span>

### <span data-ttu-id="4e1e0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4e1e0-128">System.String</span></span>

## <span data-ttu-id="4e1e0-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4e1e0-129">OUTPUTS</span></span>

### <span data-ttu-id="4e1e0-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4e1e0-130">System.Boolean</span></span>

## <span data-ttu-id="4e1e0-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="4e1e0-131">NOTES</span></span>

## <span data-ttu-id="4e1e0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e1e0-132">RELATED LINKS</span></span>
