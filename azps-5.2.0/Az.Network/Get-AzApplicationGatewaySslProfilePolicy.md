---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: a1e6bd507b7ddcc0a70405136cb76bba9231a7f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259020"
---
# <span data-ttu-id="615b3-101">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="615b3-101">Get-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="615b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="615b3-102">SYNOPSIS</span></span>
<span data-ttu-id="615b3-103">Obtém a política SSL de um perfil de SSL do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="615b3-103">Gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="615b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="615b3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="615b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="615b3-105">DESCRIPTION</span></span>
<span data-ttu-id="615b3-106">O cmdlet **Get-AzApplicationGatewaySslProfilePolicy** Obtém a política SSL de um perfil SSL do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="615b3-106">The **Get-AzApplicationGatewaySslProfilePolicy** cmdlet gets the SSL policy of an application gateway SSL profile.</span></span>

## <span data-ttu-id="615b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="615b3-107">EXAMPLES</span></span>

### <span data-ttu-id="615b3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="615b3-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SslProfile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> $sslpolicy = Get-AzApplicationGatewaySslProfilePolicy -SslProfile $SslProfile
```

<span data-ttu-id="615b3-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 no grupo de recursos chamado ResourceGroup01 e o armazena na variável $AppGw.</span><span class="sxs-lookup"><span data-stu-id="615b3-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="615b3-110">O segundo comando obtém o perfil SSL chamado SslProfile01 para $AppGw e o armazena $SslProfile variável.</span><span class="sxs-lookup"><span data-stu-id="615b3-110">The second command gets the SSL profile named SslProfile01 for $AppGw and stores it $SslProfile variable.</span></span> <span data-ttu-id="615b3-111">O último comando obtém a política SSL do perfil SSL $SslProfile e a armazena na variável $sslpolicy.</span><span class="sxs-lookup"><span data-stu-id="615b3-111">The last command gets the SSL policy from the SSL profile $SslProfile and stores it in the $sslpolicy variable.</span></span>

## <span data-ttu-id="615b3-112">OS</span><span class="sxs-lookup"><span data-stu-id="615b3-112">PARAMETERS</span></span>

### <span data-ttu-id="615b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="615b3-113">-DefaultProfile</span></span>
<span data-ttu-id="615b3-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="615b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="615b3-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="615b3-115">-SslProfile</span></span>
<span data-ttu-id="615b3-116">O perfil SSL do Application Gateway</span><span class="sxs-lookup"><span data-stu-id="615b3-116">The application Gateway SSL profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="615b3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="615b3-117">CommonParameters</span></span>
<span data-ttu-id="615b3-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="615b3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="615b3-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="615b3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="615b3-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="615b3-120">INPUTS</span></span>

### <span data-ttu-id="615b3-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="615b3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="615b3-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="615b3-122">OUTPUTS</span></span>

### <span data-ttu-id="615b3-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslPolicy</span><span class="sxs-lookup"><span data-stu-id="615b3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslPolicy</span></span>

## <span data-ttu-id="615b3-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="615b3-124">NOTES</span></span>

## <span data-ttu-id="615b3-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="615b3-125">RELATED LINKS</span></span>

[<span data-ttu-id="615b3-126">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="615b3-126">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="615b3-127">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="615b3-127">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="615b3-128">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="615b3-128">Remove-AzApplicationGatewaySslProfilePolicy</span></span>](./Remove-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="615b3-129">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="615b3-129">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)