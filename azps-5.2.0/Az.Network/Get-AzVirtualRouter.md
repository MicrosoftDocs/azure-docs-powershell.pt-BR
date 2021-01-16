---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: 26e919935a65a486252cac234450adf214992b36
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262780"
---
# <span data-ttu-id="3f3ee-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3f3ee-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="3f3ee-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3f3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="3f3ee-103">Obter um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="3f3ee-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="3f3ee-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f3ee-104">SYNTAX</span></span>

### <span data-ttu-id="3f3ee-105">VirtualRouterSubscriptionIdParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3f3ee-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f3ee-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f3ee-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f3ee-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f3ee-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f3ee-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3f3ee-108">DESCRIPTION</span></span>
<span data-ttu-id="3f3ee-109">O cmdlet **Get-AzVirtualRouter** Obtém um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="3f3ee-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="3f3ee-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3f3ee-110">EXAMPLES</span></span>

### <span data-ttu-id="3f3ee-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3f3ee-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="3f3ee-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3f3ee-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="3f3ee-113">OS</span><span class="sxs-lookup"><span data-stu-id="3f3ee-113">PARAMETERS</span></span>

### <span data-ttu-id="3f3ee-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f3ee-114">-DefaultProfile</span></span>
<span data-ttu-id="3f3ee-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f3ee-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f3ee-116">-ResourceGroupName</span></span>
<span data-ttu-id="3f3ee-117">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="3f3ee-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f3ee-118">-ResourceId</span></span>
<span data-ttu-id="3f3ee-119">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="3f3ee-120">-Roteadorname</span><span class="sxs-lookup"><span data-stu-id="3f3ee-120">-RouterName</span></span>
<span data-ttu-id="3f3ee-121">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="3f3ee-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f3ee-122">CommonParameters</span></span>
<span data-ttu-id="3f3ee-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f3ee-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f3ee-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f3ee-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3f3ee-125">INPUTS</span></span>

### <span data-ttu-id="3f3ee-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3f3ee-126">System.String</span></span>

## <span data-ttu-id="3f3ee-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3f3ee-127">OUTPUTS</span></span>

### <span data-ttu-id="3f3ee-128">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="3f3ee-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="3f3ee-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3f3ee-129">NOTES</span></span>

## <span data-ttu-id="3f3ee-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3f3ee-130">RELATED LINKS</span></span>
