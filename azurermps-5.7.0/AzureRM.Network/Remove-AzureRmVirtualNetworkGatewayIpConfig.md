---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkGatewayIpConfig.md
ms.openlocfilehash: 6be6c0d7993b44d807cad5bf8c06a203fe8ff7a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610107"
---
# <span data-ttu-id="05a85-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="05a85-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="05a85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="05a85-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05a85-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="05a85-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05a85-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="05a85-104">DESCRIPTION</span></span>

## <span data-ttu-id="05a85-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05a85-105">EXAMPLES</span></span>

### <span data-ttu-id="05a85-106">1:</span><span class="sxs-lookup"><span data-stu-id="05a85-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="05a85-107">OS</span><span class="sxs-lookup"><span data-stu-id="05a85-107">PARAMETERS</span></span>

### <span data-ttu-id="05a85-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05a85-108">-DefaultProfile</span></span>
<span data-ttu-id="05a85-109">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05a85-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05a85-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="05a85-110">-Name</span></span>
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

### <span data-ttu-id="05a85-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05a85-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="05a85-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="05a85-112">-Confirm</span></span>
<span data-ttu-id="05a85-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05a85-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05a85-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05a85-114">-WhatIf</span></span>
<span data-ttu-id="05a85-115">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="05a85-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05a85-116">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="05a85-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05a85-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05a85-117">CommonParameters</span></span>
<span data-ttu-id="05a85-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05a85-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05a85-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05a85-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05a85-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="05a85-120">INPUTS</span></span>

### <span data-ttu-id="05a85-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05a85-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="05a85-122">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="05a85-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="05a85-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="05a85-123">OUTPUTS</span></span>

### <span data-ttu-id="05a85-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05a85-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="05a85-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="05a85-125">NOTES</span></span>

## <span data-ttu-id="05a85-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05a85-126">RELATED LINKS</span></span>

