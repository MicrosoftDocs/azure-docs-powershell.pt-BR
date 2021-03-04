---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 377a2b967058de9c0cdae1d4c07ceffc73b1bfec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891888"
---
# <span data-ttu-id="a5e1b-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a5e1b-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a5e1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a5e1b-103">Excluir conta de armazenamento vinculada de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a5e1b-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="a5e1b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a5e1b-104">SYNTAX</span></span>

### <span data-ttu-id="a5e1b-105">ByResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a5e1b-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e1b-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e1b-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5e1b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5e1b-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5e1b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a5e1b-108">DESCRIPTION</span></span>
<span data-ttu-id="a5e1b-109">Excluir conta de armazenamento vinculada de insights de aplicativo</span><span class="sxs-lookup"><span data-stu-id="a5e1b-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="a5e1b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5e1b-110">EXAMPLES</span></span>

### <span data-ttu-id="a5e1b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5e1b-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="a5e1b-112">Excluir conta de armazenamento vinculada associada ao componente de insights do aplicativo "componentName"</span><span class="sxs-lookup"><span data-stu-id="a5e1b-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="a5e1b-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a5e1b-113">PARAMETERS</span></span>

### <span data-ttu-id="a5e1b-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="a5e1b-114">-ComponentName</span></span>
<span data-ttu-id="a5e1b-115">Nome do componente</span><span class="sxs-lookup"><span data-stu-id="a5e1b-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5e1b-116">-DefaultProfile</span></span>
<span data-ttu-id="a5e1b-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5e1b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5e1b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5e1b-118">-InputObject</span></span>
<span data-ttu-id="a5e1b-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a5e1b-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5e1b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5e1b-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5e1b-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a5e1b-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e1b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5e1b-122">-ResourceId</span></span>
<span data-ttu-id="a5e1b-123">ResourceId de componente</span><span class="sxs-lookup"><span data-stu-id="a5e1b-123">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e1b-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5e1b-124">-Confirm</span></span>
<span data-ttu-id="a5e1b-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5e1b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e1b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5e1b-126">-WhatIf</span></span>
<span data-ttu-id="a5e1b-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5e1b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5e1b-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5e1b-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5e1b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5e1b-129">CommonParameters</span></span>
<span data-ttu-id="a5e1b-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5e1b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5e1b-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5e1b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5e1b-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5e1b-132">INPUTS</span></span>

### <span data-ttu-id="a5e1b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a5e1b-133">System.String</span></span>

### <span data-ttu-id="a5e1b-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a5e1b-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a5e1b-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a5e1b-135">OUTPUTS</span></span>

### <span data-ttu-id="a5e1b-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5e1b-136">System.Boolean</span></span>

## <span data-ttu-id="a5e1b-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="a5e1b-137">NOTES</span></span>

## <span data-ttu-id="a5e1b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5e1b-138">RELATED LINKS</span></span>
