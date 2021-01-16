---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262362"
---
# <span data-ttu-id="38bf0-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="38bf0-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="38bf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="38bf0-102">SYNOPSIS</span></span>
<span data-ttu-id="38bf0-103">Excluir cluster</span><span class="sxs-lookup"><span data-stu-id="38bf0-103">Delete cluster</span></span>

## <span data-ttu-id="38bf0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="38bf0-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38bf0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="38bf0-105">DESCRIPTION</span></span>
<span data-ttu-id="38bf0-106">Excluir cluster, aplicar-se somente a clusters com o estado de provisionamento "êxito"</span><span class="sxs-lookup"><span data-stu-id="38bf0-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="38bf0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38bf0-107">EXAMPLES</span></span>

### <span data-ttu-id="38bf0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38bf0-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="38bf0-109">Excluir cluster</span><span class="sxs-lookup"><span data-stu-id="38bf0-109">Delete cluster</span></span>

## <span data-ttu-id="38bf0-110">OS</span><span class="sxs-lookup"><span data-stu-id="38bf0-110">PARAMETERS</span></span>

### <span data-ttu-id="38bf0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38bf0-111">-AsJob</span></span>
<span data-ttu-id="38bf0-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="38bf0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38bf0-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="38bf0-113">-ClusterName</span></span>
<span data-ttu-id="38bf0-114">O nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="38bf0-114">The cluster name.</span></span>

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

### <span data-ttu-id="38bf0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38bf0-115">-DefaultProfile</span></span>
<span data-ttu-id="38bf0-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38bf0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38bf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38bf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="38bf0-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="38bf0-118">The resource group name.</span></span>

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

### <span data-ttu-id="38bf0-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="38bf0-119">-Confirm</span></span>
<span data-ttu-id="38bf0-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38bf0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38bf0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38bf0-121">-WhatIf</span></span>
<span data-ttu-id="38bf0-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38bf0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38bf0-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38bf0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38bf0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38bf0-124">CommonParameters</span></span>
<span data-ttu-id="38bf0-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38bf0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38bf0-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38bf0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38bf0-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="38bf0-127">INPUTS</span></span>

### <span data-ttu-id="38bf0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="38bf0-128">System.String</span></span>

## <span data-ttu-id="38bf0-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="38bf0-129">OUTPUTS</span></span>

### <span data-ttu-id="38bf0-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38bf0-130">System.Boolean</span></span>

## <span data-ttu-id="38bf0-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="38bf0-131">NOTES</span></span>

## <span data-ttu-id="38bf0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38bf0-132">RELATED LINKS</span></span>
