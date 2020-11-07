---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: a0885534311dfef4498c9fc71be7f82d16b05277
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785473"
---
# <span data-ttu-id="7e8fc-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e8fc-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="7e8fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e8fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7e8fc-103">Remove os mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="7e8fc-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e8fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e8fc-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e8fc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e8fc-105">DESCRIPTION</span></span>
<span data-ttu-id="7e8fc-106">O cmdlet **Remove-AzureRmApplicationGatewayUrlPathMapConfig** remove mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="7e8fc-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="7e8fc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e8fc-107">EXAMPLES</span></span>

### <span data-ttu-id="7e8fc-108">1:</span><span class="sxs-lookup"><span data-stu-id="7e8fc-108">1:</span></span>
```

```

## <span data-ttu-id="7e8fc-109">OS</span><span class="sxs-lookup"><span data-stu-id="7e8fc-109">PARAMETERS</span></span>

### <span data-ttu-id="7e8fc-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e8fc-110">-ApplicationGateway</span></span>
<span data-ttu-id="7e8fc-111">Especifica o gateway do aplicativo para o qual esse cmdlet Remove a configuração do mapa de caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="7e8fc-111">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e8fc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e8fc-112">-DefaultProfile</span></span>
<span data-ttu-id="7e8fc-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e8fc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e8fc-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e8fc-114">-Name</span></span>
<span data-ttu-id="7e8fc-115">Especifica o nome do mapa de caminho de URL que este cmdlet Remove do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="7e8fc-115">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="7e8fc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e8fc-116">CommonParameters</span></span>
<span data-ttu-id="7e8fc-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e8fc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e8fc-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e8fc-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e8fc-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e8fc-119">INPUTS</span></span>

### <span data-ttu-id="7e8fc-120">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e8fc-120">PSApplicationGateway</span></span>
<span data-ttu-id="7e8fc-121">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7e8fc-121">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="7e8fc-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e8fc-122">OUTPUTS</span></span>

### <span data-ttu-id="7e8fc-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7e8fc-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7e8fc-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e8fc-124">NOTES</span></span>

## <span data-ttu-id="7e8fc-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e8fc-125">RELATED LINKS</span></span>

[<span data-ttu-id="7e8fc-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e8fc-126">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7e8fc-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e8fc-127">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7e8fc-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e8fc-128">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="7e8fc-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7e8fc-129">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


