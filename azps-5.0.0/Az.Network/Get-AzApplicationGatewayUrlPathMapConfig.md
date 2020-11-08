---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125917"
---
# <span data-ttu-id="028ea-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="028ea-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="028ea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="028ea-102">SYNOPSIS</span></span>
<span data-ttu-id="028ea-103">Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="028ea-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="028ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="028ea-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="028ea-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="028ea-105">DESCRIPTION</span></span>
<span data-ttu-id="028ea-106">O cmdlet **Get-AzApplicationGatewayURLPathMapConfig** Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="028ea-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="028ea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="028ea-107">EXAMPLES</span></span>

### <span data-ttu-id="028ea-108">Exemplo 1: obter uma configuração de mapa de caminho de URL</span><span class="sxs-lookup"><span data-stu-id="028ea-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="028ea-109">Esse comando obtém as configurações de mapa de caminho de URL do servidor back-end localizado no gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="028ea-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="028ea-110">OS</span><span class="sxs-lookup"><span data-stu-id="028ea-110">PARAMETERS</span></span>

### <span data-ttu-id="028ea-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="028ea-111">-ApplicationGateway</span></span>
<span data-ttu-id="028ea-112">Especifica o gateway do aplicativo para o qual esse cmdlet obtém uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="028ea-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="028ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="028ea-113">-DefaultProfile</span></span>
<span data-ttu-id="028ea-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="028ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="028ea-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="028ea-115">-Name</span></span>
<span data-ttu-id="028ea-116">Especifica o nome do mapa de caminho da URL em que esse cmdlet obtém a configuração do mapa de caminho.</span><span class="sxs-lookup"><span data-stu-id="028ea-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="028ea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="028ea-117">CommonParameters</span></span>
<span data-ttu-id="028ea-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="028ea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="028ea-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="028ea-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="028ea-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="028ea-120">INPUTS</span></span>

### <span data-ttu-id="028ea-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="028ea-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="028ea-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="028ea-122">OUTPUTS</span></span>

### <span data-ttu-id="028ea-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="028ea-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="028ea-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="028ea-124">NOTES</span></span>

## <span data-ttu-id="028ea-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="028ea-125">RELATED LINKS</span></span>

[<span data-ttu-id="028ea-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="028ea-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="028ea-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="028ea-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="028ea-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="028ea-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="028ea-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="028ea-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


