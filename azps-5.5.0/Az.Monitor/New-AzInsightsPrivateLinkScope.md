---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111749"
---
# <span data-ttu-id="c5fab-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="c5fab-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="c5fab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5fab-102">SYNOPSIS</span></span>
<span data-ttu-id="c5fab-103">criar escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="c5fab-103">create private link scope</span></span>

## <span data-ttu-id="c5fab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5fab-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5fab-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5fab-105">DESCRIPTION</span></span>
<span data-ttu-id="c5fab-106">criar escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="c5fab-106">create private link scope</span></span>

## <span data-ttu-id="c5fab-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c5fab-107">EXAMPLES</span></span>

### <span data-ttu-id="c5fab-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5fab-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="c5fab-109">criar escopo de link privado com o nome "scope_name" no grupo de recursos "rg_name" no local "eastus"</span><span class="sxs-lookup"><span data-stu-id="c5fab-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="c5fab-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5fab-110">PARAMETERS</span></span>

### <span data-ttu-id="c5fab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5fab-111">-DefaultProfile</span></span>
<span data-ttu-id="c5fab-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5fab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5fab-113">-Local</span><span class="sxs-lookup"><span data-stu-id="c5fab-113">-Location</span></span>
<span data-ttu-id="c5fab-114">Localização</span><span class="sxs-lookup"><span data-stu-id="c5fab-114">Location</span></span>

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

### <span data-ttu-id="c5fab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c5fab-115">-Name</span></span>
<span data-ttu-id="c5fab-116">Nome do escopo do link particular</span><span class="sxs-lookup"><span data-stu-id="c5fab-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="c5fab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5fab-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5fab-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="c5fab-118">Resource Group Name</span></span>

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

### <span data-ttu-id="c5fab-119">-Marcas</span><span class="sxs-lookup"><span data-stu-id="c5fab-119">-Tags</span></span>
<span data-ttu-id="c5fab-120">Tags</span><span class="sxs-lookup"><span data-stu-id="c5fab-120">Tags</span></span>

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

### <span data-ttu-id="c5fab-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c5fab-121">-Confirm</span></span>
<span data-ttu-id="c5fab-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5fab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5fab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5fab-123">-WhatIf</span></span>
<span data-ttu-id="c5fab-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c5fab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5fab-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5fab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5fab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5fab-126">CommonParameters</span></span>
<span data-ttu-id="c5fab-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5fab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5fab-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5fab-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5fab-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="c5fab-129">INPUTS</span></span>

### <span data-ttu-id="c5fab-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c5fab-130">System.String</span></span>

## <span data-ttu-id="c5fab-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="c5fab-131">OUTPUTS</span></span>

### <span data-ttu-id="c5fab-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="c5fab-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="c5fab-133">Notas</span><span class="sxs-lookup"><span data-stu-id="c5fab-133">NOTES</span></span>

## <span data-ttu-id="c5fab-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5fab-134">RELATED LINKS</span></span>
