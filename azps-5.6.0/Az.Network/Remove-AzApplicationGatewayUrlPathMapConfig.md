---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 1d9caf3c95d7f8a508a41b8c047684b86c66227a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891156"
---
# <span data-ttu-id="4c116-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c116-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="4c116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c116-102">SYNOPSIS</span></span>
<span data-ttu-id="4c116-103">Remove mapeamentos de caminho de URL para um pool de servidores de back-end.</span><span class="sxs-lookup"><span data-stu-id="4c116-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4c116-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4c116-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c116-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4c116-105">DESCRIPTION</span></span>
<span data-ttu-id="4c116-106">O cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** remove mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="4c116-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="4c116-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c116-107">EXAMPLES</span></span>

### <span data-ttu-id="4c116-108">Exemplo 1: Remover um mapeamento de caminho de URL de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="4c116-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="4c116-109">O primeiro comando obtém o gateway de aplicativo chamado appGwName e armazena o resultado na $appgw variável.</span><span class="sxs-lookup"><span data-stu-id="4c116-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="4c116-110">O segundo comando remove o mapeamento de caminho da URL chamado map01 do gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4c116-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="4c116-111">O terceiro comando atualiza o gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4c116-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="4c116-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4c116-112">PARAMETERS</span></span>

### <span data-ttu-id="4c116-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c116-113">-ApplicationGateway</span></span>
<span data-ttu-id="4c116-114">Especifica o gateway de aplicativo para o qual este cmdlet remove a configuração do mapa de caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="4c116-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="4c116-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c116-115">-DefaultProfile</span></span>
<span data-ttu-id="4c116-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4c116-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c116-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4c116-117">-Name</span></span>
<span data-ttu-id="4c116-118">Especifica o nome do mapa de caminho da URL que esse cmdlet remove do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="4c116-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="4c116-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c116-119">CommonParameters</span></span>
<span data-ttu-id="4c116-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c116-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c116-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c116-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c116-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c116-122">INPUTS</span></span>

### <span data-ttu-id="4c116-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c116-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c116-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4c116-124">OUTPUTS</span></span>

### <span data-ttu-id="4c116-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c116-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c116-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="4c116-126">NOTES</span></span>

## <span data-ttu-id="4c116-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c116-127">RELATED LINKS</span></span>

[<span data-ttu-id="4c116-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c116-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4c116-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c116-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4c116-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c116-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="4c116-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="4c116-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


