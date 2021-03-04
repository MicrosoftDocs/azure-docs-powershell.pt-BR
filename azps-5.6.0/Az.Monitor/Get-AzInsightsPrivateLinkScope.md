---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 941b60da0282bdad523b06657639a730d1776ce3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888892"
---
# <span data-ttu-id="a262b-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a262b-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="a262b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a262b-102">SYNOPSIS</span></span>
<span data-ttu-id="a262b-103">Obter escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="a262b-103">Get private link scope</span></span>

## <span data-ttu-id="a262b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a262b-104">SYNTAX</span></span>

### <span data-ttu-id="a262b-105">ByResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a262b-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a262b-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a262b-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a262b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a262b-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a262b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a262b-108">DESCRIPTION</span></span>
<span data-ttu-id="a262b-109">Listar ou obter escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="a262b-109">List or get private link scope</span></span> 

## <span data-ttu-id="a262b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a262b-110">EXAMPLES</span></span>

### <span data-ttu-id="a262b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a262b-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="a262b-112">Listar escopos de link privado no grupo de recursos "rg_name"</span><span class="sxs-lookup"><span data-stu-id="a262b-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="a262b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a262b-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="a262b-114">Obter escopo de link privado com o nome "scope_name" no grupo de recursos "rg_name"</span><span class="sxs-lookup"><span data-stu-id="a262b-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="a262b-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a262b-115">PARAMETERS</span></span>

### <span data-ttu-id="a262b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a262b-116">-DefaultProfile</span></span>
<span data-ttu-id="a262b-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a262b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a262b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a262b-118">-Name</span></span>
<span data-ttu-id="a262b-119">Nome do escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="a262b-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="a262b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a262b-120">-ResourceGroupName</span></span>
<span data-ttu-id="a262b-121">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a262b-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="a262b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a262b-122">-ResourceId</span></span>
<span data-ttu-id="a262b-123">ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="a262b-123">Resource Id</span></span>

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

### <span data-ttu-id="a262b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a262b-124">CommonParameters</span></span>
<span data-ttu-id="a262b-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a262b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a262b-126">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a262b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a262b-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a262b-127">INPUTS</span></span>

### <span data-ttu-id="a262b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a262b-128">System.String</span></span>

## <span data-ttu-id="a262b-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a262b-129">OUTPUTS</span></span>

### <span data-ttu-id="a262b-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a262b-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="a262b-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="a262b-131">NOTES</span></span>

## <span data-ttu-id="a262b-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a262b-132">RELATED LINKS</span></span>
