---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 105097f30ea87637cd0ad4bd16e0b8da922c2f4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891798"
---
# <span data-ttu-id="02380-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="02380-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="02380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02380-102">SYNOPSIS</span></span>
<span data-ttu-id="02380-103">Obter identidade atribuída ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="02380-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="02380-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="02380-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02380-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="02380-105">DESCRIPTION</span></span>
<span data-ttu-id="02380-106">O cmdlet **Get-AzApplicationGatewayIdentity** recebe a identidade atribuída ao gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="02380-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="02380-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="02380-107">EXAMPLES</span></span>

### <span data-ttu-id="02380-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="02380-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="02380-109">Este exemplo mostra como obter a identidade do gateway de aplicativo do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="02380-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="02380-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="02380-110">PARAMETERS</span></span>

### <span data-ttu-id="02380-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02380-111">-ApplicationGateway</span></span>
<span data-ttu-id="02380-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02380-112">The applicationGateway</span></span>

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

### <span data-ttu-id="02380-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02380-113">-DefaultProfile</span></span>
<span data-ttu-id="02380-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02380-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02380-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02380-115">CommonParameters</span></span>
<span data-ttu-id="02380-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02380-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02380-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02380-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02380-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02380-118">INPUTS</span></span>

### <span data-ttu-id="02380-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="02380-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="02380-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="02380-120">OUTPUTS</span></span>

### <span data-ttu-id="02380-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="02380-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="02380-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="02380-122">NOTES</span></span>

## <span data-ttu-id="02380-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02380-123">RELATED LINKS</span></span>
