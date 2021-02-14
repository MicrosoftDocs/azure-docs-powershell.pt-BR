---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117300"
---
# <span data-ttu-id="0c608-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="0c608-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="0c608-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0c608-102">SYNOPSIS</span></span>
<span data-ttu-id="0c608-103">Excluir cluster</span><span class="sxs-lookup"><span data-stu-id="0c608-103">Delete cluster</span></span>

## <span data-ttu-id="0c608-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c608-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c608-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c608-105">DESCRIPTION</span></span>
<span data-ttu-id="0c608-106">Excluir cluster, aplicar somente a clusters com o estado de provisionamento "Bem-sucedido"</span><span class="sxs-lookup"><span data-stu-id="0c608-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="0c608-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0c608-107">EXAMPLES</span></span>

### <span data-ttu-id="0c608-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c608-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="0c608-109">Excluir cluster</span><span class="sxs-lookup"><span data-stu-id="0c608-109">Delete cluster</span></span>

## <span data-ttu-id="0c608-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c608-110">PARAMETERS</span></span>

### <span data-ttu-id="0c608-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c608-111">-AsJob</span></span>
<span data-ttu-id="0c608-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0c608-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0c608-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0c608-113">-ClusterName</span></span>
<span data-ttu-id="0c608-114">O nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="0c608-114">The cluster name.</span></span>

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

### <span data-ttu-id="0c608-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c608-115">-DefaultProfile</span></span>
<span data-ttu-id="0c608-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c608-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c608-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c608-117">-ResourceGroupName</span></span>
<span data-ttu-id="0c608-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="0c608-118">The resource group name.</span></span>

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

### <span data-ttu-id="0c608-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0c608-119">-Confirm</span></span>
<span data-ttu-id="0c608-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c608-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c608-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c608-121">-WhatIf</span></span>
<span data-ttu-id="0c608-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0c608-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c608-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c608-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c608-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c608-124">CommonParameters</span></span>
<span data-ttu-id="0c608-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c608-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c608-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c608-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c608-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="0c608-127">INPUTS</span></span>

### <span data-ttu-id="0c608-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0c608-128">System.String</span></span>

## <span data-ttu-id="0c608-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="0c608-129">OUTPUTS</span></span>

### <span data-ttu-id="0c608-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c608-130">System.Boolean</span></span>

## <span data-ttu-id="0c608-131">Notas</span><span class="sxs-lookup"><span data-stu-id="0c608-131">NOTES</span></span>

## <span data-ttu-id="0c608-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c608-132">RELATED LINKS</span></span>
