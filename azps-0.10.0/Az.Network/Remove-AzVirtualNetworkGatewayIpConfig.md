---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: b4503c94b750763fa7371f1c5297b0c181e32054
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776595"
---
# <span data-ttu-id="7f9a5-101">Remove-AzVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="7f9a5-101">Remove-AzVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="7f9a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f9a5-102">SYNOPSIS</span></span>

## <span data-ttu-id="7f9a5-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f9a5-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f9a5-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f9a5-104">DESCRIPTION</span></span>

## <span data-ttu-id="7f9a5-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f9a5-105">EXAMPLES</span></span>

### <span data-ttu-id="7f9a5-106">1:</span><span class="sxs-lookup"><span data-stu-id="7f9a5-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="7f9a5-107">OS</span><span class="sxs-lookup"><span data-stu-id="7f9a5-107">PARAMETERS</span></span>

### <span data-ttu-id="7f9a5-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f9a5-108">-DefaultProfile</span></span>
<span data-ttu-id="7f9a5-109">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f9a5-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f9a5-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f9a5-110">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a5-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7f9a5-111">-VirtualNetworkGateway</span></span>
```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a5-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7f9a5-112">-Confirm</span></span>
<span data-ttu-id="7f9a5-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f9a5-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a5-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f9a5-114">-WhatIf</span></span>
<span data-ttu-id="7f9a5-115">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7f9a5-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f9a5-116">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7f9a5-116">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f9a5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f9a5-117">CommonParameters</span></span>
<span data-ttu-id="7f9a5-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f9a5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f9a5-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f9a5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f9a5-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f9a5-120">INPUTS</span></span>

### <span data-ttu-id="7f9a5-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7f9a5-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="7f9a5-122">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7f9a5-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="7f9a5-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f9a5-123">OUTPUTS</span></span>

### <span data-ttu-id="7f9a5-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="7f9a5-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="7f9a5-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f9a5-125">NOTES</span></span>

## <span data-ttu-id="7f9a5-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f9a5-126">RELATED LINKS</span></span>

