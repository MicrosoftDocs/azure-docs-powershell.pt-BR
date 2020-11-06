---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 14d1aea928923d9da4eee089ae1e95c75289eb3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610645"
---
# <span data-ttu-id="ff30f-101">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff30f-101">Remove-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ff30f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff30f-102">SYNOPSIS</span></span>
<span data-ttu-id="ff30f-103">Remove uma investigação de integridade de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="ff30f-103">Removes a health probe from an existing application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff30f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff30f-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff30f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff30f-105">DESCRIPTION</span></span>
<span data-ttu-id="ff30f-106">O cmdlet Remove-AzureRmApplicationGatewayProbeConfig remove um teste Heath de um gateway de aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="ff30f-106">The Remove-AzureRmApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="ff30f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff30f-107">EXAMPLES</span></span>

### <span data-ttu-id="ff30f-108">Exemplo 1: remover um teste de integridade de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="ff30f-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="ff30f-109">Esse comando Remove o teste de integridade chamado Probe04 do gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="ff30f-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="ff30f-110">OS</span><span class="sxs-lookup"><span data-stu-id="ff30f-110">PARAMETERS</span></span>

### <span data-ttu-id="ff30f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff30f-111">-ApplicationGateway</span></span>
<span data-ttu-id="ff30f-112">Especifica o gateway do aplicativo para o qual esse cmdlet Remove um teste.</span><span class="sxs-lookup"><span data-stu-id="ff30f-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="ff30f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff30f-113">-DefaultProfile</span></span>
<span data-ttu-id="ff30f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ff30f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff30f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff30f-115">-Name</span></span>
<span data-ttu-id="ff30f-116">Especifica o nome do teste para o qual esse cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="ff30f-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="ff30f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff30f-117">CommonParameters</span></span>
<span data-ttu-id="ff30f-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff30f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff30f-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff30f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff30f-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff30f-120">INPUTS</span></span>

### <span data-ttu-id="ff30f-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff30f-121">PSApplicationGateway</span></span>
<span data-ttu-id="ff30f-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="ff30f-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ff30f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff30f-123">OUTPUTS</span></span>

### <span data-ttu-id="ff30f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff30f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ff30f-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff30f-125">NOTES</span></span>

## <span data-ttu-id="ff30f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff30f-126">RELATED LINKS</span></span>

[<span data-ttu-id="ff30f-127">Remover um teste de um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="ff30f-127">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="ff30f-128">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff30f-128">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ff30f-129">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff30f-129">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ff30f-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff30f-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ff30f-131">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ff30f-131">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

