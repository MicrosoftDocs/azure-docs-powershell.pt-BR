---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 2490896fa66a3d06a8887e386c2bf6db6ff2f829
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890806"
---
# <span data-ttu-id="69f29-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="69f29-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="69f29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69f29-102">SYNOPSIS</span></span>
<span data-ttu-id="69f29-103">Obtém o perfil SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69f29-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="69f29-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="69f29-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69f29-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="69f29-105">DESCRIPTION</span></span>
<span data-ttu-id="69f29-106">O cmdlet **Get-AzApplicationGatewaySslProfile** obtém o perfil SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69f29-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="69f29-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69f29-107">EXAMPLES</span></span>

### <span data-ttu-id="69f29-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69f29-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="69f29-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém o SslProfile01 de perfil SSL para $AppGw e o armazena na variável $profile.</span><span class="sxs-lookup"><span data-stu-id="69f29-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="69f29-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="69f29-110">PARAMETERS</span></span>

### <span data-ttu-id="69f29-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69f29-111">-ApplicationGateway</span></span>
<span data-ttu-id="69f29-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69f29-112">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69f29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f29-113">-DefaultProfile</span></span>
<span data-ttu-id="69f29-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69f29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f29-115">-Name</span><span class="sxs-lookup"><span data-stu-id="69f29-115">-Name</span></span>
<span data-ttu-id="69f29-116">O nome do perfil ssl</span><span class="sxs-lookup"><span data-stu-id="69f29-116">The name of the ssl profile</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f29-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f29-117">CommonParameters</span></span>
<span data-ttu-id="69f29-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f29-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f29-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69f29-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f29-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69f29-120">INPUTS</span></span>

### <span data-ttu-id="69f29-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="69f29-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="69f29-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="69f29-122">OUTPUTS</span></span>

### <span data-ttu-id="69f29-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="69f29-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="69f29-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="69f29-124">NOTES</span></span>

## <span data-ttu-id="69f29-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69f29-125">RELATED LINKS</span></span>

[<span data-ttu-id="69f29-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="69f29-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="69f29-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="69f29-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="69f29-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="69f29-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="69f29-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="69f29-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)