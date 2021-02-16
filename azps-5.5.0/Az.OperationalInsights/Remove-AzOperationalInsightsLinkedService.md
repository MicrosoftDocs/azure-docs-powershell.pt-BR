---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113395"
---
# <span data-ttu-id="9eaf0-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="9eaf0-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="9eaf0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9eaf0-102">SYNOPSIS</span></span>
<span data-ttu-id="9eaf0-103">Desvincular o serviço para o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="9eaf0-103">Unlink service for workspace</span></span>

## <span data-ttu-id="9eaf0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9eaf0-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9eaf0-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9eaf0-105">DESCRIPTION</span></span>
<span data-ttu-id="9eaf0-106">Desvincular o serviço para o espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="9eaf0-106">Unlink service for workspace</span></span>

## <span data-ttu-id="9eaf0-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9eaf0-107">EXAMPLES</span></span>

### <span data-ttu-id="9eaf0-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9eaf0-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="9eaf0-109">Desvincular serviço vinculado para espaço de trabalho</span><span class="sxs-lookup"><span data-stu-id="9eaf0-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="9eaf0-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9eaf0-110">PARAMETERS</span></span>

### <span data-ttu-id="9eaf0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9eaf0-111">-AsJob</span></span>
<span data-ttu-id="9eaf0-112">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9eaf0-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9eaf0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eaf0-113">-DefaultProfile</span></span>
<span data-ttu-id="9eaf0-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eaf0-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="9eaf0-115">-LinkedServiceName</span></span>
<span data-ttu-id="9eaf0-116">O nome do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-116">The Workspace name.</span></span>

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

### <span data-ttu-id="9eaf0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eaf0-117">-ResourceGroupName</span></span>
<span data-ttu-id="9eaf0-118">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-118">The resource group name.</span></span>

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

### <span data-ttu-id="9eaf0-119">-NomedoEspacial de Trabalho</span><span class="sxs-lookup"><span data-stu-id="9eaf0-119">-WorkspaceName</span></span>
<span data-ttu-id="9eaf0-120">O nome do Espaço de Trabalho.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-120">The Workspace name.</span></span>

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

### <span data-ttu-id="9eaf0-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9eaf0-121">-Confirm</span></span>
<span data-ttu-id="9eaf0-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eaf0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eaf0-123">-WhatIf</span></span>
<span data-ttu-id="9eaf0-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eaf0-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eaf0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eaf0-126">CommonParameters</span></span>
<span data-ttu-id="9eaf0-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eaf0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eaf0-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9eaf0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eaf0-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="9eaf0-129">INPUTS</span></span>

### <span data-ttu-id="9eaf0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9eaf0-130">System.String</span></span>

## <span data-ttu-id="9eaf0-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="9eaf0-131">OUTPUTS</span></span>

### <span data-ttu-id="9eaf0-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9eaf0-132">System.Boolean</span></span>

## <span data-ttu-id="9eaf0-133">Notas</span><span class="sxs-lookup"><span data-stu-id="9eaf0-133">NOTES</span></span>

## <span data-ttu-id="9eaf0-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9eaf0-134">RELATED LINKS</span></span>
