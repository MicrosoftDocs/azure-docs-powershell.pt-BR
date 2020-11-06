---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 66da90ea590c4d2359dbe7e703667f9fe7189fba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602207"
---
# <span data-ttu-id="892a3-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="892a3-101">Get-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="892a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="892a3-102">SYNOPSIS</span></span>
<span data-ttu-id="892a3-103">Obtém uma configuração de redirecionamento existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="892a3-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="892a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="892a3-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="892a3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="892a3-105">DESCRIPTION</span></span>
<span data-ttu-id="892a3-106">O cmdlet **Get-AzureRmApplicationGatewayRedirectConfiguration** Obtém uma configuração de redirecionamento existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="892a3-106">The **Get-AzureRmApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="892a3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="892a3-107">EXAMPLES</span></span>

### <span data-ttu-id="892a3-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="892a3-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="892a3-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="892a3-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="892a3-110">O segundo comando obtém a configuração de redirecionamento chamada Redirect01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="892a3-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="892a3-111">OS</span><span class="sxs-lookup"><span data-stu-id="892a3-111">PARAMETERS</span></span>

### <span data-ttu-id="892a3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="892a3-112">-ApplicationGateway</span></span>
<span data-ttu-id="892a3-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="892a3-113">The applicationGateway</span></span>

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

### <span data-ttu-id="892a3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="892a3-114">-Name</span></span>
<span data-ttu-id="892a3-115">O nome da regra de roteamento de solicitação</span><span class="sxs-lookup"><span data-stu-id="892a3-115">The name of the request routing rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="892a3-116">-DefaultProfile</span></span>
<span data-ttu-id="892a3-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="892a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="892a3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="892a3-118">CommonParameters</span></span>
<span data-ttu-id="892a3-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="892a3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="892a3-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="892a3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="892a3-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="892a3-121">INPUTS</span></span>

### <span data-ttu-id="892a3-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="892a3-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="892a3-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="892a3-123">OUTPUTS</span></span>

### <span data-ttu-id="892a3-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="892a3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>
<span data-ttu-id="892a3-125">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands. Network, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="892a3-125">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration, Microsoft.Azure.Commands.Network, Version=4.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="892a3-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="892a3-126">NOTES</span></span>

## <span data-ttu-id="892a3-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="892a3-127">RELATED LINKS</span></span>

