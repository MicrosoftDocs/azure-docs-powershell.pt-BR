---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 39ce61f4a1e973dfdac8104a6364bdd3d8b9151a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786283"
---
# <span data-ttu-id="470da-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="470da-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="470da-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="470da-102">SYNOPSIS</span></span>
<span data-ttu-id="470da-103">Remove uma investigação de integridade de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="470da-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="470da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="470da-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="470da-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="470da-105">DESCRIPTION</span></span>
<span data-ttu-id="470da-106">O cmdlet Remove-AzureRmApplicationGatewayProbeConfig remove um teste Heath de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="470da-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="470da-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="470da-107">EXAMPLES</span></span>

### <span data-ttu-id="470da-108">Exemplo 1: remover um teste de integridade de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="470da-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="470da-109">Esse comando Remove o teste de integridade chamado Probe04 do gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="470da-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="470da-110">OS</span><span class="sxs-lookup"><span data-stu-id="470da-110">PARAMETERS</span></span>

### <span data-ttu-id="470da-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="470da-111">-ApplicationGateway</span></span>
<span data-ttu-id="470da-112">Especifica o gateway do aplicativo para o qual esse cmdlet Remove um teste.</span><span class="sxs-lookup"><span data-stu-id="470da-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="470da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="470da-113">-DefaultProfile</span></span>
<span data-ttu-id="470da-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="470da-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="470da-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="470da-115">-Name</span></span>
<span data-ttu-id="470da-116">Especifica o nome do teste para o qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="470da-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="470da-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="470da-117">CommonParameters</span></span>
<span data-ttu-id="470da-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="470da-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="470da-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="470da-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="470da-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="470da-120">INPUTS</span></span>

### <span data-ttu-id="470da-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="470da-121">PSApplicationGateway</span></span>
<span data-ttu-id="470da-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="470da-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="470da-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="470da-123">OUTPUTS</span></span>

### <span data-ttu-id="470da-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="470da-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="470da-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="470da-125">NOTES</span></span>

## <span data-ttu-id="470da-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="470da-126">RELATED LINKS</span></span>

[<span data-ttu-id="470da-127">Remover um teste de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="470da-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="470da-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="470da-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="470da-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="470da-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="470da-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="470da-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="470da-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="470da-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

