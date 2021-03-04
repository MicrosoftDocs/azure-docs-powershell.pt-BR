---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: ec9245c15a0c07da92874daa42c387e4109258c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889453"
---
# <span data-ttu-id="bc33b-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bc33b-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="bc33b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc33b-102">SYNOPSIS</span></span>
<span data-ttu-id="bc33b-103">criar escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="bc33b-103">create private link scope</span></span>

## <span data-ttu-id="bc33b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bc33b-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc33b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bc33b-105">DESCRIPTION</span></span>
<span data-ttu-id="bc33b-106">criar escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="bc33b-106">create private link scope</span></span>

## <span data-ttu-id="bc33b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc33b-107">EXAMPLES</span></span>

### <span data-ttu-id="bc33b-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bc33b-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="bc33b-109">criar escopo de link privado com o nome "scope_name" no grupo de recursos "rg_name" no local "eastus"</span><span class="sxs-lookup"><span data-stu-id="bc33b-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="bc33b-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bc33b-110">PARAMETERS</span></span>

### <span data-ttu-id="bc33b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc33b-111">-DefaultProfile</span></span>
<span data-ttu-id="bc33b-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc33b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc33b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="bc33b-113">-Location</span></span>
<span data-ttu-id="bc33b-114">Local</span><span class="sxs-lookup"><span data-stu-id="bc33b-114">Location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc33b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bc33b-115">-Name</span></span>
<span data-ttu-id="bc33b-116">Nome do escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="bc33b-116">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc33b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc33b-117">-ResourceGroupName</span></span>
<span data-ttu-id="bc33b-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="bc33b-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc33b-119">-Tags</span><span class="sxs-lookup"><span data-stu-id="bc33b-119">-Tags</span></span>
<span data-ttu-id="bc33b-120">Tags</span><span class="sxs-lookup"><span data-stu-id="bc33b-120">Tags</span></span>

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

### <span data-ttu-id="bc33b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc33b-121">-Confirm</span></span>
<span data-ttu-id="bc33b-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc33b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc33b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc33b-123">-WhatIf</span></span>
<span data-ttu-id="bc33b-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc33b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc33b-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc33b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc33b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc33b-126">CommonParameters</span></span>
<span data-ttu-id="bc33b-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc33b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc33b-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc33b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc33b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc33b-129">INPUTS</span></span>

### <span data-ttu-id="bc33b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bc33b-130">System.String</span></span>

## <span data-ttu-id="bc33b-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bc33b-131">OUTPUTS</span></span>

### <span data-ttu-id="bc33b-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bc33b-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="bc33b-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="bc33b-133">NOTES</span></span>

## <span data-ttu-id="bc33b-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc33b-134">RELATED LINKS</span></span>
