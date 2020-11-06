---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440761"
---
# <span data-ttu-id="eb02b-101">Get-AzureRmExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="eb02b-101">Get-AzureRmExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="eb02b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb02b-102">SYNOPSIS</span></span>
<span data-ttu-id="eb02b-103">Obtém uma configuração de link ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="eb02b-103">Gets an ExpressRoutePort link configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb02b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb02b-104">SYNTAX</span></span>

### <span data-ttu-id="eb02b-105">ResourceNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb02b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb02b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb02b-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb02b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb02b-107">DESCRIPTION</span></span>
<span data-ttu-id="eb02b-108">O cmdlet **Get-AzureRmExpressRoutePortLinkConfig** recupera a configuração de um link de um ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="eb02b-108">The **Get-AzureRmExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="eb02b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb02b-109">EXAMPLES</span></span>

### <span data-ttu-id="eb02b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb02b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="eb02b-111">Obtém a configuração LINK1 do ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="eb02b-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="eb02b-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eb02b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="eb02b-113">Obtém a configuração do link com o ResourceId $id em ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="eb02b-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="eb02b-114">OS</span><span class="sxs-lookup"><span data-stu-id="eb02b-114">PARAMETERS</span></span>

### <span data-ttu-id="eb02b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb02b-115">-DefaultProfile</span></span>
<span data-ttu-id="eb02b-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb02b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb02b-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="eb02b-117">-ExpressRoutePort</span></span>
<span data-ttu-id="eb02b-118">A referência do recurso ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="eb02b-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb02b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb02b-119">-Name</span></span>
<span data-ttu-id="eb02b-120">Nome do link.</span><span class="sxs-lookup"><span data-stu-id="eb02b-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb02b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb02b-121">-ResourceId</span></span>
<span data-ttu-id="eb02b-122">ResourceId do link.</span><span class="sxs-lookup"><span data-stu-id="eb02b-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb02b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb02b-123">CommonParameters</span></span>
<span data-ttu-id="eb02b-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb02b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb02b-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb02b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb02b-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb02b-126">INPUTS</span></span>

### <span data-ttu-id="eb02b-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="eb02b-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="eb02b-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb02b-128">OUTPUTS</span></span>

### <span data-ttu-id="eb02b-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="eb02b-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="eb02b-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb02b-130">NOTES</span></span>

## <span data-ttu-id="eb02b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb02b-131">RELATED LINKS</span></span>
