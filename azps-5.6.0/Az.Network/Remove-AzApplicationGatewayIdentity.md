---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 7d4cce44aa76628011b35d6723b1ae34a869a2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889912"
---
# <span data-ttu-id="a2358-101">Remove-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="a2358-101">Remove-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="a2358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2358-102">SYNOPSIS</span></span>
<span data-ttu-id="a2358-103">Remove uma identidade de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2358-103">Removes a identity from an application gateway.</span></span>

## <span data-ttu-id="a2358-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a2358-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2358-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a2358-105">DESCRIPTION</span></span>
<span data-ttu-id="a2358-106">O cmdlet **Remove-AzApplicationGatewayIdentity** remove a identidade de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2358-106">**Remove-AzApplicationGatewayIdentity** cmdlet removes identity from an application gateway.</span></span>

## <span data-ttu-id="a2358-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a2358-107">EXAMPLES</span></span>

### <span data-ttu-id="a2358-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a2358-108">Example 1</span></span>
```powershell
PS C:\> $appgw = Remove-AzApplicationGatewayIdentity -ApplicationGateway $appgw
PS C:\> $updatedgateway = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="a2358-109">Neste exemplo, removemos a identidade de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="a2358-109">In this example, we remove identity from an existing application gateway.</span></span>
<span data-ttu-id="a2358-110">Observação: se o gateway estiver fazendo referência a um segredo de keyvault, também é importante remover essas referências de certificado ssl ao longo dessa operação.</span><span class="sxs-lookup"><span data-stu-id="a2358-110">Note: If the gateway is referencing a keyvault secret, then it is also important to remove those ssl certificate references along this operation.</span></span>

## <span data-ttu-id="a2358-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a2358-111">PARAMETERS</span></span>

### <span data-ttu-id="a2358-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2358-112">-ApplicationGateway</span></span>
<span data-ttu-id="a2358-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2358-113">The applicationGateway</span></span>

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

### <span data-ttu-id="a2358-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2358-114">-DefaultProfile</span></span>
<span data-ttu-id="a2358-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a2358-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2358-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2358-116">-Confirm</span></span>
<span data-ttu-id="a2358-117">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2358-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2358-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2358-118">-WhatIf</span></span>
<span data-ttu-id="a2358-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a2358-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2358-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a2358-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2358-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2358-121">CommonParameters</span></span>
<span data-ttu-id="a2358-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2358-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2358-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2358-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2358-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a2358-124">INPUTS</span></span>

### <span data-ttu-id="a2358-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2358-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a2358-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a2358-126">OUTPUTS</span></span>

### <span data-ttu-id="a2358-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a2358-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a2358-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="a2358-128">NOTES</span></span>

## <span data-ttu-id="a2358-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a2358-129">RELATED LINKS</span></span>
