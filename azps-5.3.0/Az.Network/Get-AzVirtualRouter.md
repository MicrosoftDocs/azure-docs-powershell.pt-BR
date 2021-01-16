---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271837"
---
# <span data-ttu-id="6b471-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6b471-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="6b471-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6b471-102">SYNOPSIS</span></span>
<span data-ttu-id="6b471-103">Obter um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="6b471-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="6b471-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b471-104">SYNTAX</span></span>

### <span data-ttu-id="6b471-105">VirtualRouterSubscriptionIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6b471-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b471-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b471-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b471-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b471-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b471-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6b471-108">DESCRIPTION</span></span>
<span data-ttu-id="6b471-109">O cmdlet **Get-AzVirtualRouter** Obtém um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="6b471-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="6b471-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6b471-110">EXAMPLES</span></span>

### <span data-ttu-id="6b471-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6b471-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="6b471-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6b471-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="6b471-113">OS</span><span class="sxs-lookup"><span data-stu-id="6b471-113">PARAMETERS</span></span>

### <span data-ttu-id="6b471-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b471-114">-DefaultProfile</span></span>
<span data-ttu-id="6b471-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6b471-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b471-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b471-116">-ResourceGroupName</span></span>
<span data-ttu-id="6b471-117">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="6b471-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="6b471-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b471-118">-ResourceId</span></span>
<span data-ttu-id="6b471-119">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="6b471-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="6b471-120">-Roteadorname</span><span class="sxs-lookup"><span data-stu-id="6b471-120">-RouterName</span></span>
<span data-ttu-id="6b471-121">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="6b471-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="6b471-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b471-122">CommonParameters</span></span>
<span data-ttu-id="6b471-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b471-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b471-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b471-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b471-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6b471-125">INPUTS</span></span>

### <span data-ttu-id="6b471-126">System. String</span><span class="sxs-lookup"><span data-stu-id="6b471-126">System.String</span></span>

## <span data-ttu-id="6b471-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6b471-127">OUTPUTS</span></span>

### <span data-ttu-id="6b471-128">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6b471-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="6b471-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6b471-129">NOTES</span></span>

## <span data-ttu-id="6b471-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6b471-130">RELATED LINKS</span></span>
