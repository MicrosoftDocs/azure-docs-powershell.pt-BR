---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: c9443c93745c1f6db9372b8f845f3ac399e51398
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775580"
---
# <span data-ttu-id="39585-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="39585-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="39585-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39585-102">SYNOPSIS</span></span>
<span data-ttu-id="39585-103">Obtém uma configuração de redirecionamento existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="39585-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="39585-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39585-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39585-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="39585-105">DESCRIPTION</span></span>
<span data-ttu-id="39585-106">O cmdlet **Get-AzApplicationGatewayRedirectConfiguration** Obtém uma configuração de redirecionamento existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="39585-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="39585-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="39585-107">EXAMPLES</span></span>

### <span data-ttu-id="39585-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39585-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="39585-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="39585-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="39585-110">O segundo comando obtém a configuração de redirecionamento chamada Redirect01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="39585-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="39585-111">OS</span><span class="sxs-lookup"><span data-stu-id="39585-111">PARAMETERS</span></span>

### <span data-ttu-id="39585-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39585-112">-ApplicationGateway</span></span>
<span data-ttu-id="39585-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="39585-113">The applicationGateway</span></span>

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

### <span data-ttu-id="39585-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39585-114">-DefaultProfile</span></span>
<span data-ttu-id="39585-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="39585-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39585-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="39585-116">-Name</span></span>
<span data-ttu-id="39585-117">O nome da regra de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="39585-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="39585-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39585-118">CommonParameters</span></span>
<span data-ttu-id="39585-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39585-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39585-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39585-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39585-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="39585-121">INPUTS</span></span>

### <span data-ttu-id="39585-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="39585-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="39585-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="39585-123">OUTPUTS</span></span>

### <span data-ttu-id="39585-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="39585-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="39585-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="39585-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="39585-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="39585-126">NOTES</span></span>

## <span data-ttu-id="39585-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39585-127">RELATED LINKS</span></span>

