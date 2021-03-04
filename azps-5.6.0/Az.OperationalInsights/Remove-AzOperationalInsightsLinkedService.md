---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 8a78fc36e13360babc43b512dccee80550b3fbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890215"
---
# <span data-ttu-id="61a73-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="61a73-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="61a73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61a73-102">SYNOPSIS</span></span>
<span data-ttu-id="61a73-103">Desvincular serviço para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="61a73-103">Unlink service for workspace</span></span>

## <span data-ttu-id="61a73-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="61a73-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61a73-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="61a73-105">DESCRIPTION</span></span>
<span data-ttu-id="61a73-106">Desvincular serviço para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="61a73-106">Unlink service for workspace</span></span>

## <span data-ttu-id="61a73-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="61a73-107">EXAMPLES</span></span>

### <span data-ttu-id="61a73-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="61a73-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="61a73-109">Desvincular serviço vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="61a73-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="61a73-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="61a73-110">PARAMETERS</span></span>

### <span data-ttu-id="61a73-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61a73-111">-AsJob</span></span>
<span data-ttu-id="61a73-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="61a73-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61a73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a73-113">-DefaultProfile</span></span>
<span data-ttu-id="61a73-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="61a73-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61a73-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="61a73-115">-LinkedServiceName</span></span>
<span data-ttu-id="61a73-116">O nome do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="61a73-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61a73-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61a73-117">-ResourceGroupName</span></span>
<span data-ttu-id="61a73-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="61a73-118">The resource group name.</span></span>

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

### <span data-ttu-id="61a73-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="61a73-119">-WorkspaceName</span></span>
<span data-ttu-id="61a73-120">O nome do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="61a73-120">The Workspace name.</span></span>

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

### <span data-ttu-id="61a73-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61a73-121">-Confirm</span></span>
<span data-ttu-id="61a73-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61a73-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a73-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a73-123">-WhatIf</span></span>
<span data-ttu-id="61a73-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="61a73-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a73-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="61a73-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61a73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a73-126">CommonParameters</span></span>
<span data-ttu-id="61a73-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61a73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a73-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61a73-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a73-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61a73-129">INPUTS</span></span>

### <span data-ttu-id="61a73-130">System.String</span><span class="sxs-lookup"><span data-stu-id="61a73-130">System.String</span></span>

## <span data-ttu-id="61a73-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="61a73-131">OUTPUTS</span></span>

### <span data-ttu-id="61a73-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61a73-132">System.Boolean</span></span>

## <span data-ttu-id="61a73-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="61a73-133">NOTES</span></span>

## <span data-ttu-id="61a73-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="61a73-134">RELATED LINKS</span></span>
