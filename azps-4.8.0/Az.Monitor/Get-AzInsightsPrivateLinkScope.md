---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114439"
---
# <span data-ttu-id="bd33c-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bd33c-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="bd33c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bd33c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd33c-103">Obter escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="bd33c-103">Get private link scope</span></span>

## <span data-ttu-id="bd33c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bd33c-104">SYNTAX</span></span>

### <span data-ttu-id="bd33c-105">ByResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bd33c-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd33c-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd33c-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bd33c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd33c-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd33c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bd33c-108">DESCRIPTION</span></span>
<span data-ttu-id="bd33c-109">Lista ou obter escopo de link privado</span><span class="sxs-lookup"><span data-stu-id="bd33c-109">List or get private link scope</span></span> 

## <span data-ttu-id="bd33c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bd33c-110">EXAMPLES</span></span>

### <span data-ttu-id="bd33c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bd33c-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="bd33c-112">Listar escopos do link privado no grupo de recursos "rg_name"</span><span class="sxs-lookup"><span data-stu-id="bd33c-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="bd33c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bd33c-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="bd33c-114">Obter o escopo do link privado com o nome "scope_name" em grupo de recursos "rg_name"</span><span class="sxs-lookup"><span data-stu-id="bd33c-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="bd33c-115">OS</span><span class="sxs-lookup"><span data-stu-id="bd33c-115">PARAMETERS</span></span>

### <span data-ttu-id="bd33c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd33c-116">-DefaultProfile</span></span>
<span data-ttu-id="bd33c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bd33c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd33c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="bd33c-118">-Name</span></span>
<span data-ttu-id="bd33c-119">Nome do escopo do link privado</span><span class="sxs-lookup"><span data-stu-id="bd33c-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="bd33c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd33c-120">-ResourceGroupName</span></span>
<span data-ttu-id="bd33c-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bd33c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="bd33c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd33c-122">-ResourceId</span></span>
<span data-ttu-id="bd33c-123">ID do recurso</span><span class="sxs-lookup"><span data-stu-id="bd33c-123">Resource Id</span></span>

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

### <span data-ttu-id="bd33c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd33c-124">CommonParameters</span></span>
<span data-ttu-id="bd33c-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd33c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd33c-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bd33c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd33c-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bd33c-127">INPUTS</span></span>

### <span data-ttu-id="bd33c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bd33c-128">System.String</span></span>

## <span data-ttu-id="bd33c-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bd33c-129">OUTPUTS</span></span>

### <span data-ttu-id="bd33c-130">Microsoft. Azure. Commands. insights. OutputClasses. PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bd33c-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="bd33c-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bd33c-131">NOTES</span></span>

## <span data-ttu-id="bd33c-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bd33c-132">RELATED LINKS</span></span>
