---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 2cccbc06095f9ff71f4b16d40bca16d91e91dda0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891273"
---
# <span data-ttu-id="86a63-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="86a63-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="86a63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86a63-102">SYNOPSIS</span></span>
<span data-ttu-id="86a63-103">Obter um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="86a63-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="86a63-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="86a63-104">SYNTAX</span></span>

### <span data-ttu-id="86a63-105">VirtualRouterSubscriptionIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="86a63-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86a63-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="86a63-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86a63-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="86a63-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86a63-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="86a63-108">DESCRIPTION</span></span>
<span data-ttu-id="86a63-109">O cmdlet **Get-AzVirtualRouter** obtém um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="86a63-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="86a63-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86a63-110">EXAMPLES</span></span>

### <span data-ttu-id="86a63-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="86a63-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="86a63-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="86a63-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="86a63-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="86a63-113">PARAMETERS</span></span>

### <span data-ttu-id="86a63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86a63-114">-DefaultProfile</span></span>
<span data-ttu-id="86a63-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86a63-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86a63-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86a63-116">-ResourceGroupName</span></span>
<span data-ttu-id="86a63-117">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="86a63-117">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86a63-118">-ResourceId</span></span>
<span data-ttu-id="86a63-119">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="86a63-119">ResourceId of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-120">-RouterName</span><span class="sxs-lookup"><span data-stu-id="86a63-120">-RouterName</span></span>
<span data-ttu-id="86a63-121">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="86a63-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86a63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86a63-122">CommonParameters</span></span>
<span data-ttu-id="86a63-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86a63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86a63-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86a63-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86a63-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86a63-125">INPUTS</span></span>

### <span data-ttu-id="86a63-126">System.String</span><span class="sxs-lookup"><span data-stu-id="86a63-126">System.String</span></span>

## <span data-ttu-id="86a63-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="86a63-127">OUTPUTS</span></span>

### <span data-ttu-id="86a63-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="86a63-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="86a63-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="86a63-129">NOTES</span></span>

## <span data-ttu-id="86a63-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86a63-130">RELATED LINKS</span></span>
