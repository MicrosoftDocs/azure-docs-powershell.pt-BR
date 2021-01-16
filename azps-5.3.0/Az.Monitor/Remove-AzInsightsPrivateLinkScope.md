---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428621"
---
# <span data-ttu-id="e19fb-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e19fb-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="e19fb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e19fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e19fb-103">excluir escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="e19fb-103">delete private link scope</span></span>

## <span data-ttu-id="e19fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e19fb-104">SYNTAX</span></span>

### <span data-ttu-id="e19fb-105">ByResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e19fb-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e19fb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e19fb-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e19fb-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e19fb-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e19fb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e19fb-108">DESCRIPTION</span></span>
<span data-ttu-id="e19fb-109">excluir escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="e19fb-109">delete private link scope</span></span>

## <span data-ttu-id="e19fb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e19fb-110">EXAMPLES</span></span>

### <span data-ttu-id="e19fb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e19fb-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="e19fb-112">excluir o escopo do link privado com o nome "scope_name" em grupo de recursos "rg_name"</span><span class="sxs-lookup"><span data-stu-id="e19fb-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="e19fb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e19fb-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="e19fb-114">excluir escopo do link particular com ID do recurso</span><span class="sxs-lookup"><span data-stu-id="e19fb-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="e19fb-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e19fb-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="e19fb-116">excluir escopo do link privado com o objeto de escopo de link particular de entrada</span><span class="sxs-lookup"><span data-stu-id="e19fb-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="e19fb-117">OS</span><span class="sxs-lookup"><span data-stu-id="e19fb-117">PARAMETERS</span></span>

### <span data-ttu-id="e19fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e19fb-118">-DefaultProfile</span></span>
<span data-ttu-id="e19fb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e19fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e19fb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e19fb-120">-InputObject</span></span>
<span data-ttu-id="e19fb-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e19fb-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e19fb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e19fb-122">-Name</span></span>
<span data-ttu-id="e19fb-123">Nome do escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="e19fb-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="e19fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e19fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="e19fb-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e19fb-125">Resource Group Name</span></span>

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

### <span data-ttu-id="e19fb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e19fb-126">-ResourceId</span></span>
<span data-ttu-id="e19fb-127">ID do recurso</span><span class="sxs-lookup"><span data-stu-id="e19fb-127">Resource Id</span></span>

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

### <span data-ttu-id="e19fb-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e19fb-128">-Confirm</span></span>
<span data-ttu-id="e19fb-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e19fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e19fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e19fb-130">-WhatIf</span></span>
<span data-ttu-id="e19fb-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e19fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e19fb-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e19fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e19fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19fb-133">CommonParameters</span></span>
<span data-ttu-id="e19fb-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e19fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19fb-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e19fb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19fb-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e19fb-136">INPUTS</span></span>

### <span data-ttu-id="e19fb-137">Microsoft. Azure. Commands. insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e19fb-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="e19fb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e19fb-138">System.String</span></span>

## <span data-ttu-id="e19fb-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e19fb-139">OUTPUTS</span></span>

### <span data-ttu-id="e19fb-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e19fb-140">System.Boolean</span></span>

## <span data-ttu-id="e19fb-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e19fb-141">NOTES</span></span>

## <span data-ttu-id="e19fb-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e19fb-142">RELATED LINKS</span></span>
