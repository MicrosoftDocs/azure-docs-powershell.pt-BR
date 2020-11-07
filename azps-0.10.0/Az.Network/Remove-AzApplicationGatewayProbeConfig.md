---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 320588b81791c033b94a07261f769fa0886d2f2c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775321"
---
# <span data-ttu-id="80b65-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80b65-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="80b65-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80b65-102">SYNOPSIS</span></span>
<span data-ttu-id="80b65-103">Remove uma investigação de integridade de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="80b65-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="80b65-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="80b65-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80b65-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="80b65-105">DESCRIPTION</span></span>
<span data-ttu-id="80b65-106">O cmdlet Remove-AzApplicationGatewayProbeConfig remove um teste Heath de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="80b65-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="80b65-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="80b65-107">EXAMPLES</span></span>

### <span data-ttu-id="80b65-108">Exemplo 1: remover um teste de integridade de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="80b65-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="80b65-109">Esse comando Remove o teste de integridade chamado Probe04 do gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="80b65-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="80b65-110">OS</span><span class="sxs-lookup"><span data-stu-id="80b65-110">PARAMETERS</span></span>

### <span data-ttu-id="80b65-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80b65-111">-ApplicationGateway</span></span>
<span data-ttu-id="80b65-112">Especifica o gateway do aplicativo para o qual esse cmdlet Remove um teste.</span><span class="sxs-lookup"><span data-stu-id="80b65-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="80b65-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80b65-113">-DefaultProfile</span></span>
<span data-ttu-id="80b65-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80b65-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80b65-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="80b65-115">-Name</span></span>
<span data-ttu-id="80b65-116">Especifica o nome do teste para o qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="80b65-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80b65-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80b65-117">CommonParameters</span></span>
<span data-ttu-id="80b65-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80b65-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80b65-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80b65-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80b65-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="80b65-120">INPUTS</span></span>

### <span data-ttu-id="80b65-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80b65-121">PSApplicationGateway</span></span>
<span data-ttu-id="80b65-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="80b65-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="80b65-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="80b65-123">OUTPUTS</span></span>

### <span data-ttu-id="80b65-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="80b65-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="80b65-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="80b65-125">NOTES</span></span>

## <span data-ttu-id="80b65-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80b65-126">RELATED LINKS</span></span>

[<span data-ttu-id="80b65-127">Remover um teste de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="80b65-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="80b65-128">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80b65-128">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="80b65-129">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80b65-129">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="80b65-130">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80b65-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="80b65-131">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="80b65-131">Set-AzApplicationGatewayProbeConfig</span></span>]()

