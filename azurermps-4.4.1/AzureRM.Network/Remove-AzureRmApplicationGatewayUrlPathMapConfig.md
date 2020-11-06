---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 2297eb3d1734938f6c04b22472b02add19f634f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602564"
---
# <span data-ttu-id="15c26-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15c26-101">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="15c26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15c26-102">SYNOPSIS</span></span>
<span data-ttu-id="15c26-103">Remove os mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="15c26-103">Removes URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15c26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15c26-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15c26-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15c26-105">DESCRIPTION</span></span>
<span data-ttu-id="15c26-106">O cmdlet **Remove-AzureRmApplicationGatewayUrlPathMapConfig** remove mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="15c26-106">The **Remove-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="15c26-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15c26-107">EXAMPLES</span></span>

## <span data-ttu-id="15c26-108">OS</span><span class="sxs-lookup"><span data-stu-id="15c26-108">PARAMETERS</span></span>

### <span data-ttu-id="15c26-109">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15c26-109">-ApplicationGateway</span></span>
<span data-ttu-id="15c26-110">Especifica o gateway do aplicativo para o qual esse cmdlet Remove a configuração do mapa de caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="15c26-110">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15c26-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="15c26-111">-Name</span></span>
<span data-ttu-id="15c26-112">Especifica o nome do mapa de caminho de URL que este cmdlet Remove do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="15c26-112">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15c26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c26-113">-DefaultProfile</span></span>
<span data-ttu-id="15c26-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15c26-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15c26-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c26-115">CommonParameters</span></span>
<span data-ttu-id="15c26-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15c26-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c26-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15c26-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c26-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15c26-118">INPUTS</span></span>

### <span data-ttu-id="15c26-119">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15c26-119">PSApplicationGateway</span></span>
<span data-ttu-id="15c26-120">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="15c26-120">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="15c26-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15c26-121">OUTPUTS</span></span>

### <span data-ttu-id="15c26-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="15c26-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="15c26-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15c26-123">NOTES</span></span>

## <span data-ttu-id="15c26-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15c26-124">RELATED LINKS</span></span>

[<span data-ttu-id="15c26-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15c26-125">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="15c26-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15c26-126">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="15c26-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15c26-127">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="15c26-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="15c26-128">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


