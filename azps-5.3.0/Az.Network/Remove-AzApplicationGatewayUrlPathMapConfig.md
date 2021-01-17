---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433446"
---
# <span data-ttu-id="b36db-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b36db-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="b36db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b36db-102">SYNOPSIS</span></span>
<span data-ttu-id="b36db-103">Remove os mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="b36db-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b36db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b36db-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b36db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b36db-105">DESCRIPTION</span></span>
<span data-ttu-id="b36db-106">O cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** remove mapeamentos de caminho de URL para um pool de servidores back-end.</span><span class="sxs-lookup"><span data-stu-id="b36db-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="b36db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b36db-107">EXAMPLES</span></span>

### <span data-ttu-id="b36db-108">Exemplo 1: remover um mapeamento de caminho de URL de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="b36db-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="b36db-109">O primeiro comando obtém o gateway do aplicativo chamado appGwName e armazena o resultado na variável $appgw.</span><span class="sxs-lookup"><span data-stu-id="b36db-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="b36db-110">O segundo comando Remove o mapeamento de caminho de URL chamado map01 do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b36db-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="b36db-111">O terceiro comando atualiza o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b36db-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="b36db-112">OS</span><span class="sxs-lookup"><span data-stu-id="b36db-112">PARAMETERS</span></span>

### <span data-ttu-id="b36db-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b36db-113">-ApplicationGateway</span></span>
<span data-ttu-id="b36db-114">Especifica o gateway do aplicativo para o qual esse cmdlet Remove a configuração do mapa de caminho da URL.</span><span class="sxs-lookup"><span data-stu-id="b36db-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="b36db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b36db-115">-DefaultProfile</span></span>
<span data-ttu-id="b36db-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b36db-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b36db-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b36db-117">-Name</span></span>
<span data-ttu-id="b36db-118">Especifica o nome do mapa de caminho de URL que este cmdlet Remove do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="b36db-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="b36db-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b36db-119">CommonParameters</span></span>
<span data-ttu-id="b36db-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b36db-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b36db-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b36db-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b36db-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b36db-122">INPUTS</span></span>

### <span data-ttu-id="b36db-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b36db-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b36db-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b36db-124">OUTPUTS</span></span>

### <span data-ttu-id="b36db-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b36db-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b36db-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b36db-126">NOTES</span></span>

## <span data-ttu-id="b36db-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b36db-127">RELATED LINKS</span></span>

[<span data-ttu-id="b36db-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b36db-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b36db-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b36db-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b36db-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b36db-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="b36db-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="b36db-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


