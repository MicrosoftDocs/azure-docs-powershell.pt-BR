---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 60DA2175-7970-410C-A13C-B1314716AD8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworkgatewayipconfig
schema: 2.0.0
ms.openlocfilehash: f68709cad84adb6904e509472b1c960d6134144c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785455"
---
# <span data-ttu-id="353ef-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="353ef-101">Remove-AzureRmVirtualNetworkGatewayIpConfig</span></span>

## <span data-ttu-id="353ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="353ef-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="353ef-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="353ef-103">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkGatewayIpConfig -VirtualNetworkGateway <PSVirtualNetworkGateway> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="353ef-104">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="353ef-104">DESCRIPTION</span></span>

## <span data-ttu-id="353ef-105">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="353ef-105">EXAMPLES</span></span>

### <span data-ttu-id="353ef-106">1:</span><span class="sxs-lookup"><span data-stu-id="353ef-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="353ef-107">OS</span><span class="sxs-lookup"><span data-stu-id="353ef-107">PARAMETERS</span></span>

### <span data-ttu-id="353ef-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="353ef-108">-DefaultProfile</span></span>
<span data-ttu-id="353ef-109">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="353ef-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="353ef-110">-Nome</span><span class="sxs-lookup"><span data-stu-id="353ef-110">-Name</span></span>
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

### <span data-ttu-id="353ef-111">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="353ef-111">-VirtualNetworkGateway</span></span>
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

### <span data-ttu-id="353ef-112">-Confirme</span><span class="sxs-lookup"><span data-stu-id="353ef-112">-Confirm</span></span>
<span data-ttu-id="353ef-113">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="353ef-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="353ef-114">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="353ef-114">-WhatIf</span></span>
<span data-ttu-id="353ef-115">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="353ef-115">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="353ef-116">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="353ef-116">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="353ef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="353ef-117">CommonParameters</span></span>
<span data-ttu-id="353ef-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="353ef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="353ef-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="353ef-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="353ef-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="353ef-120">INPUTS</span></span>

### <span data-ttu-id="353ef-121">PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="353ef-121">PSVirtualNetworkGateway</span></span>
<span data-ttu-id="353ef-122">O parâmetro ' VirtualNetworkGateway ' aceita o valor do tipo ' PSVirtualNetworkGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="353ef-122">Parameter 'VirtualNetworkGateway' accepts value of type 'PSVirtualNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="353ef-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="353ef-123">OUTPUTS</span></span>

### <span data-ttu-id="353ef-124">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="353ef-124">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="353ef-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="353ef-125">NOTES</span></span>

## <span data-ttu-id="353ef-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="353ef-126">RELATED LINKS</span></span>

