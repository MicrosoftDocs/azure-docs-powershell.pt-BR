---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117573"
---
# <span data-ttu-id="d69f0-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="d69f0-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="d69f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d69f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d69f0-103">Desvincular serviço para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d69f0-103">Unlink service for workspace</span></span>

## <span data-ttu-id="d69f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d69f0-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d69f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d69f0-105">DESCRIPTION</span></span>
<span data-ttu-id="d69f0-106">Desvincular serviço para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d69f0-106">Unlink service for workspace</span></span>

## <span data-ttu-id="d69f0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d69f0-107">EXAMPLES</span></span>

### <span data-ttu-id="d69f0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d69f0-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="d69f0-109">Desvincular serviço vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="d69f0-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="d69f0-110">OS</span><span class="sxs-lookup"><span data-stu-id="d69f0-110">PARAMETERS</span></span>

### <span data-ttu-id="d69f0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d69f0-111">-AsJob</span></span>
<span data-ttu-id="d69f0-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d69f0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d69f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d69f0-113">-DefaultProfile</span></span>
<span data-ttu-id="d69f0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d69f0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d69f0-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="d69f0-115">-LinkedServiceName</span></span>
<span data-ttu-id="d69f0-116">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d69f0-116">The Workspace name.</span></span>

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

### <span data-ttu-id="d69f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d69f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="d69f0-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d69f0-118">The resource group name.</span></span>

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

### <span data-ttu-id="d69f0-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d69f0-119">-WorkspaceName</span></span>
<span data-ttu-id="d69f0-120">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d69f0-120">The Workspace name.</span></span>

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

### <span data-ttu-id="d69f0-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d69f0-121">-Confirm</span></span>
<span data-ttu-id="d69f0-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d69f0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d69f0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d69f0-123">-WhatIf</span></span>
<span data-ttu-id="d69f0-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d69f0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d69f0-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d69f0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d69f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d69f0-126">CommonParameters</span></span>
<span data-ttu-id="d69f0-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d69f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d69f0-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d69f0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d69f0-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d69f0-129">INPUTS</span></span>

### <span data-ttu-id="d69f0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d69f0-130">System.String</span></span>

## <span data-ttu-id="d69f0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d69f0-131">OUTPUTS</span></span>

### <span data-ttu-id="d69f0-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d69f0-132">System.Boolean</span></span>

## <span data-ttu-id="d69f0-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d69f0-133">NOTES</span></span>

## <span data-ttu-id="d69f0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d69f0-134">RELATED LINKS</span></span>
