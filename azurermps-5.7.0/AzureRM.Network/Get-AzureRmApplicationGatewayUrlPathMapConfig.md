---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 7aa38014487221e3a18600650757c2001e5e9928
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603027"
---
# <span data-ttu-id="4dd6d-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4dd6d-101">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4dd6d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4dd6d-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd6d-103">Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-103">Gets an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4dd6d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dd6d-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dd6d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4dd6d-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd6d-106">O cmdlet **Get-AzureRmApplicationGatewayURLPathMapConfig** Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-106">The **Get-AzureRmApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4dd6d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4dd6d-107">EXAMPLES</span></span>

### <span data-ttu-id="4dd6d-108">Exemplo 1: obter uma configuração de mapa de caminho de URL</span><span class="sxs-lookup"><span data-stu-id="4dd6d-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="4dd6d-109">Esse comando obtém as configurações de mapa de caminho de URL do servidor back-end localizado no gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="4dd6d-110">OS</span><span class="sxs-lookup"><span data-stu-id="4dd6d-110">PARAMETERS</span></span>

### <span data-ttu-id="4dd6d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dd6d-111">-ApplicationGateway</span></span>
<span data-ttu-id="4dd6d-112">Especifica o gateway do aplicativo para o qual esse cmdlet obtém uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="4dd6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd6d-113">-DefaultProfile</span></span>
<span data-ttu-id="4dd6d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dd6d-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4dd6d-115">-Name</span></span>
<span data-ttu-id="4dd6d-116">Especifica o nome do mapa de caminho da URL em que esse cmdlet obtém a configuração do mapa de caminho.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="4dd6d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd6d-117">CommonParameters</span></span>
<span data-ttu-id="4dd6d-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd6d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd6d-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd6d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd6d-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4dd6d-120">INPUTS</span></span>

### <span data-ttu-id="4dd6d-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4dd6d-121">PSApplicationGateway</span></span>
<span data-ttu-id="4dd6d-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="4dd6d-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="4dd6d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4dd6d-123">OUTPUTS</span></span>

### <span data-ttu-id="4dd6d-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="4dd6d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="4dd6d-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="4dd6d-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="4dd6d-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4dd6d-126">NOTES</span></span>

## <span data-ttu-id="4dd6d-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4dd6d-127">RELATED LINKS</span></span>

[<span data-ttu-id="4dd6d-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4dd6d-128">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4dd6d-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4dd6d-129">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4dd6d-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4dd6d-130">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4dd6d-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4dd6d-131">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


