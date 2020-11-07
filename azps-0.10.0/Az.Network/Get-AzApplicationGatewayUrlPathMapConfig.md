---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 92d970d87b79b1a392b6da73c567d6e8445cfd90
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775568"
---
# <span data-ttu-id="309c1-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="309c1-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="309c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="309c1-102">SYNOPSIS</span></span>
<span data-ttu-id="309c1-103">Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="309c1-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="309c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="309c1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="309c1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="309c1-105">DESCRIPTION</span></span>
<span data-ttu-id="309c1-106">O cmdlet **Get-AzApplicationGatewayURLPathMapConfig** Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="309c1-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="309c1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="309c1-107">EXAMPLES</span></span>

### <span data-ttu-id="309c1-108">Exemplo 1: obter uma configuração de mapa de caminho de URL</span><span class="sxs-lookup"><span data-stu-id="309c1-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="309c1-109">Esse comando obtém as configurações de mapa de caminho de URL do servidor back-end localizado no gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="309c1-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="309c1-110">OS</span><span class="sxs-lookup"><span data-stu-id="309c1-110">PARAMETERS</span></span>

### <span data-ttu-id="309c1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="309c1-111">-ApplicationGateway</span></span>
<span data-ttu-id="309c1-112">Especifica o gateway do aplicativo para o qual esse cmdlet obtém uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="309c1-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="309c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="309c1-113">-DefaultProfile</span></span>
<span data-ttu-id="309c1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="309c1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="309c1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="309c1-115">-Name</span></span>
<span data-ttu-id="309c1-116">Especifica o nome do mapa de caminho da URL em que esse cmdlet obtém a configuração do mapa de caminho.</span><span class="sxs-lookup"><span data-stu-id="309c1-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="309c1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="309c1-117">CommonParameters</span></span>
<span data-ttu-id="309c1-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="309c1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="309c1-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="309c1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="309c1-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="309c1-120">INPUTS</span></span>

### <span data-ttu-id="309c1-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="309c1-121">PSApplicationGateway</span></span>
<span data-ttu-id="309c1-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="309c1-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="309c1-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="309c1-123">OUTPUTS</span></span>

### <span data-ttu-id="309c1-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="309c1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

### <span data-ttu-id="309c1-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap]</span><span class="sxs-lookup"><span data-stu-id="309c1-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap]</span></span>

## <span data-ttu-id="309c1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="309c1-126">NOTES</span></span>

## <span data-ttu-id="309c1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="309c1-127">RELATED LINKS</span></span>

[<span data-ttu-id="309c1-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="309c1-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="309c1-129">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="309c1-129">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="309c1-130">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="309c1-130">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="309c1-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="309c1-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


