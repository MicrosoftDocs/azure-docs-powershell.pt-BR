---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118381"
---
# <span data-ttu-id="21146-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="21146-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="21146-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21146-102">SYNOPSIS</span></span>
<span data-ttu-id="21146-103">Obter identidade atribuída ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21146-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="21146-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21146-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21146-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="21146-105">DESCRIPTION</span></span>
<span data-ttu-id="21146-106">O cmdlet **Get-AzApplicationGatewayIdentity** recebe a identidade atribuída ao gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21146-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="21146-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="21146-107">EXAMPLES</span></span>

### <span data-ttu-id="21146-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="21146-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="21146-109">Este exemplo mostra como obter a identidade do gateway de aplicativo do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="21146-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="21146-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21146-110">PARAMETERS</span></span>

### <span data-ttu-id="21146-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21146-111">-ApplicationGateway</span></span>
<span data-ttu-id="21146-112">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="21146-112">The applicationGateway</span></span>

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

### <span data-ttu-id="21146-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21146-113">-DefaultProfile</span></span>
<span data-ttu-id="21146-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="21146-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21146-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21146-115">CommonParameters</span></span>
<span data-ttu-id="21146-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21146-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21146-117">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="21146-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21146-118">Entradas</span><span class="sxs-lookup"><span data-stu-id="21146-118">INPUTS</span></span>

### <span data-ttu-id="21146-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21146-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="21146-120">Saídas</span><span class="sxs-lookup"><span data-stu-id="21146-120">OUTPUTS</span></span>

### <span data-ttu-id="21146-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="21146-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="21146-122">Notas</span><span class="sxs-lookup"><span data-stu-id="21146-122">NOTES</span></span>

## <span data-ttu-id="21146-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21146-123">RELATED LINKS</span></span>
