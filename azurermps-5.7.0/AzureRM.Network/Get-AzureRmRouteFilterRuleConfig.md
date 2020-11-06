---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: d5acd58d9b36e3a581ec025b06e256652a9c4eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428175"
---
# <span data-ttu-id="629c2-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="629c2-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="629c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="629c2-102">SYNOPSIS</span></span>
<span data-ttu-id="629c2-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="629c2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="629c2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="629c2-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="629c2-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="629c2-105">DESCRIPTION</span></span>
<span data-ttu-id="629c2-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="629c2-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="629c2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="629c2-107">EXAMPLES</span></span>

### <span data-ttu-id="629c2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="629c2-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="629c2-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="629c2-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="629c2-110">OS</span><span class="sxs-lookup"><span data-stu-id="629c2-110">PARAMETERS</span></span>

### <span data-ttu-id="629c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="629c2-111">-DefaultProfile</span></span>
<span data-ttu-id="629c2-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="629c2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="629c2-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="629c2-113">-Name</span></span>
<span data-ttu-id="629c2-114">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="629c2-114">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="629c2-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="629c2-115">-RouteFilter</span></span>
<span data-ttu-id="629c2-116">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="629c2-116">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="629c2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="629c2-117">CommonParameters</span></span>
<span data-ttu-id="629c2-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="629c2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="629c2-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="629c2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="629c2-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="629c2-120">INPUTS</span></span>

### <span data-ttu-id="629c2-121">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="629c2-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="629c2-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="629c2-122">OUTPUTS</span></span>

### <span data-ttu-id="629c2-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="629c2-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="629c2-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="629c2-124">NOTES</span></span>

## <span data-ttu-id="629c2-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="629c2-125">RELATED LINKS</span></span>

