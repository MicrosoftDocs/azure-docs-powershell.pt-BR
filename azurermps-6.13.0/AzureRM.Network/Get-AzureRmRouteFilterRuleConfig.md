---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 96122c68317166f078d40be8cee9d0124c4d713e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602598"
---
# <span data-ttu-id="d7471-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="d7471-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="d7471-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7471-102">SYNOPSIS</span></span>
<span data-ttu-id="d7471-103">{{Preencher o resumo}}</span><span class="sxs-lookup"><span data-stu-id="d7471-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7471-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7471-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7471-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7471-105">DESCRIPTION</span></span>
<span data-ttu-id="d7471-106">{{Preencher a descrição}}</span><span class="sxs-lookup"><span data-stu-id="d7471-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="d7471-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7471-107">EXAMPLES</span></span>

### <span data-ttu-id="d7471-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7471-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="d7471-109">{{Adicionar exemplo de descrição aqui}}</span><span class="sxs-lookup"><span data-stu-id="d7471-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="d7471-110">OS</span><span class="sxs-lookup"><span data-stu-id="d7471-110">PARAMETERS</span></span>

### <span data-ttu-id="d7471-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7471-111">-DefaultProfile</span></span>
<span data-ttu-id="d7471-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7471-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7471-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7471-113">-Name</span></span>
<span data-ttu-id="d7471-114">O nome da regra de filtro de rota</span><span class="sxs-lookup"><span data-stu-id="d7471-114">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7471-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d7471-115">-RouteFilter</span></span>
<span data-ttu-id="d7471-116">O RouteFilter</span><span class="sxs-lookup"><span data-stu-id="d7471-116">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7471-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7471-117">CommonParameters</span></span>
<span data-ttu-id="d7471-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7471-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7471-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7471-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7471-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7471-120">INPUTS</span></span>

### <span data-ttu-id="d7471-121">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="d7471-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="d7471-122">Parâmetros: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d7471-122">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="d7471-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7471-123">OUTPUTS</span></span>

### <span data-ttu-id="d7471-124">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="d7471-124">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="d7471-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7471-125">NOTES</span></span>

## <span data-ttu-id="d7471-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7471-126">RELATED LINKS</span></span>
