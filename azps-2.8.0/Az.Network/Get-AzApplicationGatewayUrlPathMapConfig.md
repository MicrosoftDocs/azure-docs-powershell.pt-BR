---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ac85a308b73d822846a2f2a0a7b9ddf9ccc05cbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771791"
---
# <span data-ttu-id="55cab-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="55cab-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="55cab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="55cab-102">SYNOPSIS</span></span>
<span data-ttu-id="55cab-103">Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="55cab-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="55cab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="55cab-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55cab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="55cab-105">DESCRIPTION</span></span>
<span data-ttu-id="55cab-106">O cmdlet **Get-AzApplicationGatewayURLPathMapConfig** Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="55cab-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="55cab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="55cab-107">EXAMPLES</span></span>

### <span data-ttu-id="55cab-108">Exemplo 1: obter uma configuração de mapa de caminho de URL</span><span class="sxs-lookup"><span data-stu-id="55cab-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="55cab-109">Esse comando obtém as configurações de mapa de caminho de URL do servidor back-end localizado no gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="55cab-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="55cab-110">OS</span><span class="sxs-lookup"><span data-stu-id="55cab-110">PARAMETERS</span></span>

### <span data-ttu-id="55cab-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="55cab-111">-ApplicationGateway</span></span>
<span data-ttu-id="55cab-112">Especifica o gateway do aplicativo para o qual esse cmdlet obtém uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="55cab-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="55cab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55cab-113">-DefaultProfile</span></span>
<span data-ttu-id="55cab-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="55cab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55cab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="55cab-115">-Name</span></span>
<span data-ttu-id="55cab-116">Especifica o nome do mapa de caminho da URL em que esse cmdlet obtém a configuração do mapa de caminho.</span><span class="sxs-lookup"><span data-stu-id="55cab-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="55cab-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55cab-117">CommonParameters</span></span>
<span data-ttu-id="55cab-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55cab-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55cab-119">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55cab-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55cab-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="55cab-120">INPUTS</span></span>

### <span data-ttu-id="55cab-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="55cab-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="55cab-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="55cab-122">OUTPUTS</span></span>

### <span data-ttu-id="55cab-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="55cab-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="55cab-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="55cab-124">NOTES</span></span>

## <span data-ttu-id="55cab-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="55cab-125">RELATED LINKS</span></span>

[<span data-ttu-id="55cab-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="55cab-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="55cab-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="55cab-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="55cab-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="55cab-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="55cab-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="55cab-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


