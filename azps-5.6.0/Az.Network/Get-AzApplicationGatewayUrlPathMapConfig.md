---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: f82882a4975c2f873362ece62f6eac9e6b7a53a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890799"
---
# <span data-ttu-id="adc89-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="adc89-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="adc89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc89-102">SYNOPSIS</span></span>
<span data-ttu-id="adc89-103">Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="adc89-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="adc89-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="adc89-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adc89-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="adc89-105">DESCRIPTION</span></span>
<span data-ttu-id="adc89-106">O cmdlet **Get-AzApplicationGatewayURLPathMapConfig obtém** uma matriz de mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="adc89-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="adc89-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="adc89-107">EXAMPLES</span></span>

### <span data-ttu-id="adc89-108">Exemplo 1: Obter uma configuração de mapa de caminho de URL</span><span class="sxs-lookup"><span data-stu-id="adc89-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="adc89-109">Este comando obtém as configurações de mapa de caminho da URL do servidor back-end localizado no gateway de aplicativo chamado Gateway.</span><span class="sxs-lookup"><span data-stu-id="adc89-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="adc89-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="adc89-110">PARAMETERS</span></span>

### <span data-ttu-id="adc89-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adc89-111">-ApplicationGateway</span></span>
<span data-ttu-id="adc89-112">Especifica o gateway de aplicativo para o qual esse cmdlet obtém uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="adc89-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="adc89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc89-113">-DefaultProfile</span></span>
<span data-ttu-id="adc89-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="adc89-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="adc89-115">-Name</span><span class="sxs-lookup"><span data-stu-id="adc89-115">-Name</span></span>
<span data-ttu-id="adc89-116">Especifica o nome do mapa do caminho da URL no qual esse cmdlet obterá a configuração do mapa de caminho.</span><span class="sxs-lookup"><span data-stu-id="adc89-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="adc89-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc89-117">CommonParameters</span></span>
<span data-ttu-id="adc89-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc89-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc89-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adc89-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc89-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adc89-120">INPUTS</span></span>

### <span data-ttu-id="adc89-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="adc89-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="adc89-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="adc89-122">OUTPUTS</span></span>

### <span data-ttu-id="adc89-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="adc89-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="adc89-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="adc89-124">NOTES</span></span>

## <span data-ttu-id="adc89-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="adc89-125">RELATED LINKS</span></span>

[<span data-ttu-id="adc89-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="adc89-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="adc89-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="adc89-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="adc89-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="adc89-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="adc89-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="adc89-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


