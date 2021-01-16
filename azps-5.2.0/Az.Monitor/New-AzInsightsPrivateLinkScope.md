---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258706"
---
# <span data-ttu-id="4d084-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4d084-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="4d084-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d084-102">SYNOPSIS</span></span>
<span data-ttu-id="4d084-103">criar escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="4d084-103">create private link scope</span></span>

## <span data-ttu-id="4d084-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d084-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d084-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4d084-105">DESCRIPTION</span></span>
<span data-ttu-id="4d084-106">criar escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="4d084-106">create private link scope</span></span>

## <span data-ttu-id="4d084-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4d084-107">EXAMPLES</span></span>

### <span data-ttu-id="4d084-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d084-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="4d084-109">criar um escopo de link privado com o nome "scope_name" no grupo de recursos "rg_name" no local "eastus"</span><span class="sxs-lookup"><span data-stu-id="4d084-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="4d084-110">OS</span><span class="sxs-lookup"><span data-stu-id="4d084-110">PARAMETERS</span></span>

### <span data-ttu-id="4d084-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d084-111">-DefaultProfile</span></span>
<span data-ttu-id="4d084-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4d084-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d084-113">-Local</span><span class="sxs-lookup"><span data-stu-id="4d084-113">-Location</span></span>
<span data-ttu-id="4d084-114">Ponto</span><span class="sxs-lookup"><span data-stu-id="4d084-114">Location</span></span>

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

### <span data-ttu-id="4d084-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d084-115">-Name</span></span>
<span data-ttu-id="4d084-116">Nome do escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="4d084-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="4d084-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d084-117">-ResourceGroupName</span></span>
<span data-ttu-id="4d084-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4d084-118">Resource Group Name</span></span>

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

### <span data-ttu-id="4d084-119">-Marcas</span><span class="sxs-lookup"><span data-stu-id="4d084-119">-Tags</span></span>
<span data-ttu-id="4d084-120">Marcas</span><span class="sxs-lookup"><span data-stu-id="4d084-120">Tags</span></span>

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

### <span data-ttu-id="4d084-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4d084-121">-Confirm</span></span>
<span data-ttu-id="4d084-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d084-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d084-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d084-123">-WhatIf</span></span>
<span data-ttu-id="4d084-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4d084-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d084-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d084-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d084-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d084-126">CommonParameters</span></span>
<span data-ttu-id="4d084-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d084-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d084-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d084-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d084-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4d084-129">INPUTS</span></span>

### <span data-ttu-id="4d084-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4d084-130">System.String</span></span>

## <span data-ttu-id="4d084-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4d084-131">OUTPUTS</span></span>

### <span data-ttu-id="4d084-132">Microsoft. Azure. Commands. insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4d084-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="4d084-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4d084-133">NOTES</span></span>

## <span data-ttu-id="4d084-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d084-134">RELATED LINKS</span></span>
