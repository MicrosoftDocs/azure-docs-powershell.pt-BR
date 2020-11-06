---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 40a7e63150384ac3fa2c330c079d5377c836d52e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429456"
---
# <span data-ttu-id="9b3cd-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b3cd-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="9b3cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9b3cd-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3cd-103">Remove uma investigação de integridade de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="9b3cd-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b3cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9b3cd-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b3cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9b3cd-105">DESCRIPTION</span></span>
<span data-ttu-id="9b3cd-106">O cmdlet Remove-AzureRmApplicationGatewayProbeConfig remove um teste Heath de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="9b3cd-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="9b3cd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9b3cd-107">EXAMPLES</span></span>

### <span data-ttu-id="9b3cd-108">Exemplo 1: remover um teste de integridade de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="9b3cd-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="9b3cd-109">Esse comando Remove o teste de integridade chamado Probe04 do gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="9b3cd-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="9b3cd-110">OS</span><span class="sxs-lookup"><span data-stu-id="9b3cd-110">PARAMETERS</span></span>

### <span data-ttu-id="9b3cd-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b3cd-111">-ApplicationGateway</span></span>
<span data-ttu-id="9b3cd-112">Especifica o gateway do aplicativo para o qual esse cmdlet Remove um teste.</span><span class="sxs-lookup"><span data-stu-id="9b3cd-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="9b3cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3cd-113">-DefaultProfile</span></span>
<span data-ttu-id="9b3cd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9b3cd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b3cd-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b3cd-115">-Name</span></span>
<span data-ttu-id="9b3cd-116">Especifica o nome do teste para o qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="9b3cd-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="9b3cd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3cd-117">CommonParameters</span></span>
<span data-ttu-id="9b3cd-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b3cd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3cd-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b3cd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3cd-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9b3cd-120">INPUTS</span></span>

### <span data-ttu-id="9b3cd-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b3cd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="9b3cd-122">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b3cd-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="9b3cd-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9b3cd-123">OUTPUTS</span></span>

### <span data-ttu-id="9b3cd-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b3cd-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b3cd-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9b3cd-125">NOTES</span></span>

## <span data-ttu-id="9b3cd-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9b3cd-126">RELATED LINKS</span></span>

[<span data-ttu-id="9b3cd-127">Remover um teste de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="9b3cd-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="9b3cd-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b3cd-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="9b3cd-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b3cd-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="9b3cd-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b3cd-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="9b3cd-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="9b3cd-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

