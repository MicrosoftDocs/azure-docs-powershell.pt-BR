---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: dd7ad8110afad4302c393295599ed1ef9d6fd4bf
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785337"
---
# <span data-ttu-id="2e5d6-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2e5d6-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="2e5d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2e5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5d6-103">Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e5d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2e5d6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e5d6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2e5d6-105">DESCRIPTION</span></span>
<span data-ttu-id="2e5d6-106">O cmdlet **Get-AzureRmApplicationGatewayURLPathMapConfig** Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2e5d6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2e5d6-107">EXAMPLES</span></span>

### <span data-ttu-id="2e5d6-108">Exemplo 1: obter uma configuração de mapa de caminho de URL</span><span class="sxs-lookup"><span data-stu-id="2e5d6-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="2e5d6-109">Esse comando obtém as configurações de mapa de caminho de URL do servidor back-end localizado no gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="2e5d6-110">OS</span><span class="sxs-lookup"><span data-stu-id="2e5d6-110">PARAMETERS</span></span>

### <span data-ttu-id="2e5d6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e5d6-111">-ApplicationGateway</span></span>
<span data-ttu-id="2e5d6-112">Especifica o gateway do aplicativo para o qual esse cmdlet obtém uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="2e5d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5d6-113">-DefaultProfile</span></span>
<span data-ttu-id="2e5d6-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e5d6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="2e5d6-115">-Name</span></span>
<span data-ttu-id="2e5d6-116">Especifica o nome do mapa de caminho da URL em que esse cmdlet obtém a configuração do mapa de caminho.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="2e5d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5d6-117">CommonParameters</span></span>
<span data-ttu-id="2e5d6-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e5d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5d6-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e5d6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5d6-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2e5d6-120">INPUTS</span></span>

### <span data-ttu-id="2e5d6-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2e5d6-121">PSApplicationGateway</span></span>
<span data-ttu-id="2e5d6-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2e5d6-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="2e5d6-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2e5d6-123">OUTPUTS</span></span>

### <span data-ttu-id="2e5d6-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="2e5d6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="2e5d6-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="2e5d6-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="2e5d6-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2e5d6-126">NOTES</span></span>

## <span data-ttu-id="2e5d6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2e5d6-127">RELATED LINKS</span></span>

[<span data-ttu-id="2e5d6-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2e5d6-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2e5d6-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2e5d6-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2e5d6-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2e5d6-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2e5d6-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2e5d6-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


