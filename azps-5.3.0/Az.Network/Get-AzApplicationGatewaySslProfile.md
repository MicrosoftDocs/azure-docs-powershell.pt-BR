---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 6d4bab8f7c4c766730dd6fb09f0d0a011d5d3739
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428549"
---
# <span data-ttu-id="6064a-101">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6064a-101">Get-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="6064a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6064a-102">SYNOPSIS</span></span>
<span data-ttu-id="6064a-103">Obtém o perfil SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6064a-103">Gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="6064a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6064a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfile [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6064a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6064a-105">DESCRIPTION</span></span>
<span data-ttu-id="6064a-106">O cmdlet **Get-AzApplicationGatewaySslProfile** Obtém o perfil SSL de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6064a-106">The **Get-AzApplicationGatewaySslProfile** cmdlet gets the SSL profile of an application gateway.</span></span>

## <span data-ttu-id="6064a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6064a-107">EXAMPLES</span></span>

### <span data-ttu-id="6064a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6064a-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
```

<span data-ttu-id="6064a-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw. O segundo comando obtém o perfil SSL SslProfile01 para $AppGw e o armazena na variável $profile.</span><span class="sxs-lookup"><span data-stu-id="6064a-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command gets the SSL profile SslProfile01 for $AppGw and stores it in the $profile variable.</span></span>

## <span data-ttu-id="6064a-110">OS</span><span class="sxs-lookup"><span data-stu-id="6064a-110">PARAMETERS</span></span>

### <span data-ttu-id="6064a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6064a-111">-ApplicationGateway</span></span>
<span data-ttu-id="6064a-112">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="6064a-112">The applicationGateway</span></span>

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

### <span data-ttu-id="6064a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6064a-113">-DefaultProfile</span></span>
<span data-ttu-id="6064a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6064a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6064a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6064a-115">-Name</span></span>
<span data-ttu-id="6064a-116">O nome do perfil SSL</span><span class="sxs-lookup"><span data-stu-id="6064a-116">The name of the ssl profile</span></span>

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

### <span data-ttu-id="6064a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6064a-117">CommonParameters</span></span>
<span data-ttu-id="6064a-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6064a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6064a-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6064a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6064a-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6064a-120">INPUTS</span></span>

### <span data-ttu-id="6064a-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6064a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6064a-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6064a-122">OUTPUTS</span></span>

### <span data-ttu-id="6064a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6064a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="6064a-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6064a-124">NOTES</span></span>

## <span data-ttu-id="6064a-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6064a-125">RELATED LINKS</span></span>

[<span data-ttu-id="6064a-126">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6064a-126">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="6064a-127">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6064a-127">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="6064a-128">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6064a-128">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="6064a-129">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6064a-129">Set-AzApplicationGatewaySslProfile</span></span>](./Set-AzApplicationGatewaySslProfile.md)