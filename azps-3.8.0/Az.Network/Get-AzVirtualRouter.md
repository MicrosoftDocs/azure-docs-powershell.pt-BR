---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualRouter.md
ms.openlocfilehash: dc568657feb5f86cf7cfaa21042e03f8470a9caa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941364"
---
# <span data-ttu-id="8b4ff-101">Get-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8b4ff-101">Get-AzVirtualRouter</span></span>

## <span data-ttu-id="8b4ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8b4ff-103">Obter um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="8b4ff-103">Get an Azure VirtualRouter</span></span>

## <span data-ttu-id="8b4ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b4ff-104">SYNTAX</span></span>

### <span data-ttu-id="8b4ff-105">VirtualRouterNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8b4ff-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Get-AzVirtualRouter -ResourceGroupName <String> [-RouterName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b4ff-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b4ff-106">VirtualRouterResourceIdParameterSet</span></span>
```
Get-AzVirtualRouter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b4ff-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b4ff-107">DESCRIPTION</span></span>
<span data-ttu-id="8b4ff-108">O cmdlet **Get-AzVirtualRouter** Obtém um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="8b4ff-108">The **Get-AzVirtualRouter** cmdlet gets an Azure VirtualRouter</span></span>

## <span data-ttu-id="8b4ff-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b4ff-109">EXAMPLES</span></span>

### <span data-ttu-id="8b4ff-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8b4ff-110">Example 1</span></span>
```powershell
Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="8b4ff-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8b4ff-111">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Get-AzVirtualRouter -ResourceId $virtualRouterId
```

## <span data-ttu-id="8b4ff-112">OS</span><span class="sxs-lookup"><span data-stu-id="8b4ff-112">PARAMETERS</span></span>

### <span data-ttu-id="8b4ff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b4ff-113">-DefaultProfile</span></span>
<span data-ttu-id="8b4ff-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b4ff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b4ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b4ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="8b4ff-116">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="8b4ff-116">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4ff-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b4ff-117">-ResourceId</span></span>
<span data-ttu-id="8b4ff-118">ResourceId do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="8b4ff-118">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4ff-119">-Roteadorname</span><span class="sxs-lookup"><span data-stu-id="8b4ff-119">-RouterName</span></span>
<span data-ttu-id="8b4ff-120">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="8b4ff-120">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b4ff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b4ff-121">CommonParameters</span></span>
<span data-ttu-id="8b4ff-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b4ff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b4ff-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b4ff-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b4ff-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b4ff-124">INPUTS</span></span>

### <span data-ttu-id="8b4ff-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8b4ff-125">System.String</span></span>

## <span data-ttu-id="8b4ff-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b4ff-126">OUTPUTS</span></span>

### <span data-ttu-id="8b4ff-127">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="8b4ff-127">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="8b4ff-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b4ff-128">NOTES</span></span>

## <span data-ttu-id="8b4ff-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b4ff-129">RELATED LINKS</span></span>
