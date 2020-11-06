---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 6583856eb6d44fa170b53a855e43db71602534a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427865"
---
# <span data-ttu-id="0d69f-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d69f-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="0d69f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0d69f-102">SYNOPSIS</span></span>
<span data-ttu-id="0d69f-103">Obtém uma configuração de investigação de integridade existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="0d69f-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d69f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0d69f-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d69f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0d69f-105">DESCRIPTION</span></span>
<span data-ttu-id="0d69f-106">O cmdlet Get-AzureRmApplicationGatewayProbeConfig Obtém uma configuração de investigação de integridade existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="0d69f-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="0d69f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0d69f-107">EXAMPLES</span></span>

### <span data-ttu-id="0d69f-108">Exemplo 1: obter um teste existente de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="0d69f-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="0d69f-109">Esse comando obtém o teste de integridade chamado Probe02 do gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="0d69f-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="0d69f-110">OS</span><span class="sxs-lookup"><span data-stu-id="0d69f-110">PARAMETERS</span></span>

### <span data-ttu-id="0d69f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d69f-111">-ApplicationGateway</span></span>
<span data-ttu-id="0d69f-112">Especifica o gateway do aplicativo para o qual esse cmdlet obtém uma configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="0d69f-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="0d69f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d69f-113">-Name</span></span>
<span data-ttu-id="0d69f-114">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="0d69f-114">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="0d69f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d69f-115">-DefaultProfile</span></span>
<span data-ttu-id="0d69f-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0d69f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d69f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d69f-117">CommonParameters</span></span>
<span data-ttu-id="0d69f-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d69f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d69f-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d69f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d69f-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0d69f-120">INPUTS</span></span>

### <span data-ttu-id="0d69f-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0d69f-121">PSApplicationGateway</span></span>
<span data-ttu-id="0d69f-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0d69f-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="0d69f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0d69f-123">OUTPUTS</span></span>

### <span data-ttu-id="0d69f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="0d69f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="0d69f-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="0d69f-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="0d69f-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0d69f-126">NOTES</span></span>

## <span data-ttu-id="0d69f-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0d69f-127">RELATED LINKS</span></span>

[<span data-ttu-id="0d69f-128">Adicionar um teste a um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="0d69f-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="0d69f-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d69f-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0d69f-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d69f-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0d69f-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d69f-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="0d69f-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="0d69f-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

