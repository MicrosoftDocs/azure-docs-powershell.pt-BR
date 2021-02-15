---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: e99df2f29781281ee0293f4cf52715153ff0d0cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112870"
---
# <span data-ttu-id="361a1-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="361a1-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="361a1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="361a1-102">SYNOPSIS</span></span>
<span data-ttu-id="361a1-103">Obter uma Rota Virtual do Azure</span><span class="sxs-lookup"><span data-stu-id="361a1-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="361a1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="361a1-104">SYNTAX</span></span>

### <span data-ttu-id="361a1-105">VirtualRouterSubscriptionIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="361a1-105">VirtualRouterSubscriptionIdParameterSet (Default)</span></span>
```
Get-AzVirtualRouter [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="361a1-106">VirtualRouterNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="361a1-106">VirtualRouterNameParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="361a1-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="361a1-107">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="361a1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="361a1-108">DESCRIPTION</span></span>
<span data-ttu-id="361a1-109">O cmdlet **Get-AzVirtualRouter** obtém um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="361a1-109">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="361a1-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="361a1-110">EXAMPLES</span></span>

### <span data-ttu-id="361a1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="361a1-111">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="361a1-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="361a1-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="361a1-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="361a1-113">PARAMETERS</span></span>

### <span data-ttu-id="361a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="361a1-114">-DefaultProfile</span></span>
<span data-ttu-id="361a1-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="361a1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="361a1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="361a1-116">-ResourceGroupName</span></span>
<span data-ttu-id="361a1-117">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="361a1-117">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="361a1-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="361a1-118">-ResourceId</span></span>
<span data-ttu-id="361a1-119">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="361a1-119">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="361a1-120">-Nomedo Roteador</span><span class="sxs-lookup"><span data-stu-id="361a1-120">-RouterName</span></span>
<span data-ttu-id="361a1-121">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="361a1-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="361a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="361a1-122">CommonParameters</span></span>
<span data-ttu-id="361a1-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="361a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="361a1-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="361a1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="361a1-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="361a1-125">INPUTS</span></span>

### <span data-ttu-id="361a1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="361a1-126">System.String</span></span>

## <span data-ttu-id="361a1-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="361a1-127">OUTPUTS</span></span>

### <span data-ttu-id="361a1-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="361a1-128">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="361a1-129">Notas</span><span class="sxs-lookup"><span data-stu-id="361a1-129">NOTES</span></span>

## <span data-ttu-id="361a1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="361a1-130">RELATED LINKS</span></span>
