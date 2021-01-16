---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257163"
---
# <span data-ttu-id="9fda4-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="9fda4-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="9fda4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fda4-102">SYNOPSIS</span></span>
<span data-ttu-id="9fda4-103">Obter identidade atribuída ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9fda4-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="9fda4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fda4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fda4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fda4-105">DESCRIPTION</span></span>
<span data-ttu-id="9fda4-106">O cmdlet **Get-AzApplicationGatewayIdentity** Obtém a identidade atribuída ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9fda4-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="9fda4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fda4-107">EXAMPLES</span></span>

### <span data-ttu-id="9fda4-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9fda4-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="9fda4-109">Este exemplo mostra como obter identidade do Application Gateway do Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9fda4-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="9fda4-110">OS</span><span class="sxs-lookup"><span data-stu-id="9fda4-110">PARAMETERS</span></span>

### <span data-ttu-id="9fda4-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fda4-111">-ApplicationGateway</span></span>
<span data-ttu-id="9fda4-112">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fda4-112">The applicationGateway</span></span>

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

### <span data-ttu-id="9fda4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fda4-113">-DefaultProfile</span></span>
<span data-ttu-id="9fda4-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9fda4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fda4-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fda4-115">CommonParameters</span></span>
<span data-ttu-id="9fda4-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fda4-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fda4-117">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fda4-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fda4-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fda4-118">INPUTS</span></span>

### <span data-ttu-id="9fda4-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9fda4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9fda4-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fda4-120">OUTPUTS</span></span>

### <span data-ttu-id="9fda4-121">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="9fda4-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="9fda4-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fda4-122">NOTES</span></span>

## <span data-ttu-id="9fda4-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fda4-123">RELATED LINKS</span></span>
