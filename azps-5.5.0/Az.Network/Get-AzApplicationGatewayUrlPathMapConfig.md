---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114716"
---
# <span data-ttu-id="f958a-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f958a-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="f958a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f958a-102">SYNOPSIS</span></span>
<span data-ttu-id="f958a-103">Obtém uma matriz de mapeamentos de caminho de URL para um pool de servidor de back-end.</span><span class="sxs-lookup"><span data-stu-id="f958a-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f958a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f958a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f958a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f958a-105">DESCRIPTION</span></span>
<span data-ttu-id="f958a-106">O cmdlet **Get-AzApplicationGatewayURLPathMapConfig obtém** uma matriz de mapeamentos de caminho de URL para um pool de servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="f958a-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="f958a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f958a-107">EXAMPLES</span></span>

### <span data-ttu-id="f958a-108">Exemplo 1: Obter uma configuração de mapa de caminho de URL</span><span class="sxs-lookup"><span data-stu-id="f958a-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="f958a-109">Esse comando obtém as configurações de mapa de caminho de URL do servidor back-end localizado no gateway de aplicativo chamado Gateway.</span><span class="sxs-lookup"><span data-stu-id="f958a-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="f958a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f958a-110">PARAMETERS</span></span>

### <span data-ttu-id="f958a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f958a-111">-ApplicationGateway</span></span>
<span data-ttu-id="f958a-112">Especifica o gateway do aplicativo para o qual este cmdlet obtém uma configuração de mapa de caminho de URL.</span><span class="sxs-lookup"><span data-stu-id="f958a-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="f958a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f958a-113">-DefaultProfile</span></span>
<span data-ttu-id="f958a-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f958a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f958a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f958a-115">-Name</span></span>
<span data-ttu-id="f958a-116">Especifica o nome do mapa do caminho da URL no qual este cmdlet obterá a configuração do mapa de caminho.</span><span class="sxs-lookup"><span data-stu-id="f958a-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="f958a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f958a-117">CommonParameters</span></span>
<span data-ttu-id="f958a-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f958a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f958a-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f958a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f958a-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="f958a-120">INPUTS</span></span>

### <span data-ttu-id="f958a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f958a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f958a-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="f958a-122">OUTPUTS</span></span>

### <span data-ttu-id="f958a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="f958a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="f958a-124">Notas</span><span class="sxs-lookup"><span data-stu-id="f958a-124">NOTES</span></span>

## <span data-ttu-id="f958a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f958a-125">RELATED LINKS</span></span>

[<span data-ttu-id="f958a-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f958a-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f958a-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f958a-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f958a-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f958a-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="f958a-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="f958a-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


