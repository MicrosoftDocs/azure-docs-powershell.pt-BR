---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777281"
---
# <span data-ttu-id="85180-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="85180-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="85180-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85180-102">SYNOPSIS</span></span>
<span data-ttu-id="85180-103">excluir do recurso escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="85180-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="85180-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85180-104">SYNTAX</span></span>

### <span data-ttu-id="85180-105">ByScopeParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="85180-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85180-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85180-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85180-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85180-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85180-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85180-108">DESCRIPTION</span></span>
<span data-ttu-id="85180-109">excluir do recurso escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="85180-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="85180-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85180-110">EXAMPLES</span></span>

### <span data-ttu-id="85180-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="85180-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="85180-112">excluir recurso escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="85180-112">delete private link scoped resource</span></span>

## <span data-ttu-id="85180-113">OS</span><span class="sxs-lookup"><span data-stu-id="85180-113">PARAMETERS</span></span>

### <span data-ttu-id="85180-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85180-114">-DefaultProfile</span></span>
<span data-ttu-id="85180-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85180-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85180-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85180-116">-InputObject</span></span>
<span data-ttu-id="85180-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="85180-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="85180-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="85180-118">-Name</span></span>
<span data-ttu-id="85180-119">Nome do recurso com escopo</span><span class="sxs-lookup"><span data-stu-id="85180-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85180-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85180-120">-ResourceGroupName</span></span>
<span data-ttu-id="85180-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="85180-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85180-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85180-122">-ResourceId</span></span>
<span data-ttu-id="85180-123">ID do recurso</span><span class="sxs-lookup"><span data-stu-id="85180-123">Resource Id</span></span>

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

### <span data-ttu-id="85180-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="85180-124">-ScopeName</span></span>
<span data-ttu-id="85180-125">Nome do escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="85180-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85180-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85180-126">-Confirm</span></span>
<span data-ttu-id="85180-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85180-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85180-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85180-128">-WhatIf</span></span>
<span data-ttu-id="85180-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85180-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85180-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85180-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85180-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85180-131">CommonParameters</span></span>
<span data-ttu-id="85180-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85180-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85180-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85180-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85180-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85180-134">INPUTS</span></span>

### <span data-ttu-id="85180-135">Microsoft. Azure. Commands. insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="85180-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="85180-136">System. String</span><span class="sxs-lookup"><span data-stu-id="85180-136">System.String</span></span>

## <span data-ttu-id="85180-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85180-137">OUTPUTS</span></span>

### <span data-ttu-id="85180-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85180-138">System.Boolean</span></span>

## <span data-ttu-id="85180-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85180-139">NOTES</span></span>

## <span data-ttu-id="85180-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85180-140">RELATED LINKS</span></span>
