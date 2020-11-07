---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777263"
---
# <span data-ttu-id="1f26f-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="1f26f-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="1f26f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f26f-102">SYNOPSIS</span></span>
<span data-ttu-id="1f26f-103">Atualização do escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="1f26f-103">Update for private link scope</span></span>

## <span data-ttu-id="1f26f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f26f-104">SYNTAX</span></span>

### <span data-ttu-id="1f26f-105">ByResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f26f-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f26f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f26f-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f26f-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f26f-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f26f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f26f-108">DESCRIPTION</span></span>
<span data-ttu-id="1f26f-109">Atualização do escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="1f26f-109">Update for private link scope</span></span>

## <span data-ttu-id="1f26f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f26f-110">EXAMPLES</span></span>

### <span data-ttu-id="1f26f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f26f-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="1f26f-112">Atualize o escopo do link privado com o nome "scope_name" em grupo de recursos "rg_name" para usar a marca "chave: valor"</span><span class="sxs-lookup"><span data-stu-id="1f26f-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="1f26f-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1f26f-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="1f26f-114">Atualize o escopo do link particular com ID do recurso para usar a marca "chave: valor"</span><span class="sxs-lookup"><span data-stu-id="1f26f-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="1f26f-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="1f26f-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="1f26f-116">Atualize o escopo do link privado com objeto de escopo de link privado de entrada para usar a marca "chave: valor"</span><span class="sxs-lookup"><span data-stu-id="1f26f-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="1f26f-117">OS</span><span class="sxs-lookup"><span data-stu-id="1f26f-117">PARAMETERS</span></span>

### <span data-ttu-id="1f26f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f26f-118">-DefaultProfile</span></span>
<span data-ttu-id="1f26f-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f26f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f26f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f26f-120">-InputObject</span></span>
<span data-ttu-id="1f26f-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="1f26f-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="1f26f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f26f-122">-Name</span></span>
<span data-ttu-id="1f26f-123">Nome do escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="1f26f-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="1f26f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f26f-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f26f-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1f26f-125">Resource Group Name</span></span>

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

### <span data-ttu-id="1f26f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f26f-126">-ResourceId</span></span>
<span data-ttu-id="1f26f-127">ID do recurso</span><span class="sxs-lookup"><span data-stu-id="1f26f-127">Resource Id</span></span>

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

### <span data-ttu-id="1f26f-128">-Marcas</span><span class="sxs-lookup"><span data-stu-id="1f26f-128">-Tags</span></span>
<span data-ttu-id="1f26f-129">Marcas</span><span class="sxs-lookup"><span data-stu-id="1f26f-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f26f-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f26f-130">-Confirm</span></span>
<span data-ttu-id="1f26f-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f26f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f26f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f26f-132">-WhatIf</span></span>
<span data-ttu-id="1f26f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f26f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f26f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f26f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f26f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f26f-135">CommonParameters</span></span>
<span data-ttu-id="1f26f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f26f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f26f-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f26f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f26f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f26f-138">INPUTS</span></span>

### <span data-ttu-id="1f26f-139">Microsoft. Azure. Commands. insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="1f26f-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="1f26f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1f26f-140">System.String</span></span>

## <span data-ttu-id="1f26f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f26f-141">OUTPUTS</span></span>

### <span data-ttu-id="1f26f-142">Microsoft. Azure. Commands. insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="1f26f-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="1f26f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f26f-143">NOTES</span></span>

## <span data-ttu-id="1f26f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f26f-144">RELATED LINKS</span></span>
