---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: cbe38933cb4c2c75b5219bf0deccc0b28052a61f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785713"
---
# <span data-ttu-id="fbe60-101">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fbe60-101">Get-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="fbe60-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fbe60-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe60-103">Obtém uma configuração de investigação de integridade existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="fbe60-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbe60-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbe60-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbe60-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fbe60-105">DESCRIPTION</span></span>
<span data-ttu-id="fbe60-106">O cmdlet Get-AzureRmApplicationGatewayProbeConfig Obtém uma configuração de investigação de integridade existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="fbe60-106">The Get-AzureRmApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="fbe60-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fbe60-107">EXAMPLES</span></span>

### <span data-ttu-id="fbe60-108">Exemplo 1: obter um teste existente de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="fbe60-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="fbe60-109">Esse comando obtém o teste de integridade chamado Probe02 do gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="fbe60-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="fbe60-110">OS</span><span class="sxs-lookup"><span data-stu-id="fbe60-110">PARAMETERS</span></span>

### <span data-ttu-id="fbe60-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbe60-111">-ApplicationGateway</span></span>
<span data-ttu-id="fbe60-112">Especifica o gateway do aplicativo para o qual esse cmdlet obtém uma configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="fbe60-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="fbe60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe60-113">-DefaultProfile</span></span>
<span data-ttu-id="fbe60-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe60-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbe60-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbe60-115">-Name</span></span>
<span data-ttu-id="fbe60-116">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="fbe60-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="fbe60-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe60-117">CommonParameters</span></span>
<span data-ttu-id="fbe60-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe60-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe60-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe60-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe60-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fbe60-120">INPUTS</span></span>

### <span data-ttu-id="fbe60-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbe60-121">PSApplicationGateway</span></span>
<span data-ttu-id="fbe60-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="fbe60-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="fbe60-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fbe60-123">OUTPUTS</span></span>

### <span data-ttu-id="fbe60-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="fbe60-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="fbe60-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="fbe60-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="fbe60-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fbe60-126">NOTES</span></span>

## <span data-ttu-id="fbe60-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fbe60-127">RELATED LINKS</span></span>

[<span data-ttu-id="fbe60-128">Adicionar um teste a um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="fbe60-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="fbe60-129">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fbe60-129">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fbe60-130">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fbe60-130">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fbe60-131">Remove-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fbe60-131">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="fbe60-132">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fbe60-132">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

