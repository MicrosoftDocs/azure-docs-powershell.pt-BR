---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: b3e2b3ea03ca0bae0db1bea1606e4ae6b94a597e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775584"
---
# <span data-ttu-id="262b1-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="262b1-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="262b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="262b1-102">SYNOPSIS</span></span>
<span data-ttu-id="262b1-103">Obtém uma configuração de investigação de integridade existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="262b1-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="262b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="262b1-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="262b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="262b1-105">DESCRIPTION</span></span>
<span data-ttu-id="262b1-106">O cmdlet Get-AzApplicationGatewayProbeConfig Obtém uma configuração de investigação de integridade existente de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="262b1-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="262b1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="262b1-107">EXAMPLES</span></span>

### <span data-ttu-id="262b1-108">Exemplo 1: obter um teste existente de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="262b1-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="262b1-109">Esse comando obtém o teste de integridade chamado Probe02 do gateway do aplicativo chamado gateway.</span><span class="sxs-lookup"><span data-stu-id="262b1-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="262b1-110">OS</span><span class="sxs-lookup"><span data-stu-id="262b1-110">PARAMETERS</span></span>

### <span data-ttu-id="262b1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="262b1-111">-ApplicationGateway</span></span>
<span data-ttu-id="262b1-112">Especifica o gateway do aplicativo para o qual esse cmdlet obtém uma configuração de sondagem.</span><span class="sxs-lookup"><span data-stu-id="262b1-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="262b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="262b1-113">-DefaultProfile</span></span>
<span data-ttu-id="262b1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="262b1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="262b1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="262b1-115">-Name</span></span>
<span data-ttu-id="262b1-116">Especifica o nome do teste.</span><span class="sxs-lookup"><span data-stu-id="262b1-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="262b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="262b1-117">CommonParameters</span></span>
<span data-ttu-id="262b1-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="262b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="262b1-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="262b1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="262b1-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="262b1-120">INPUTS</span></span>

### <span data-ttu-id="262b1-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="262b1-121">PSApplicationGateway</span></span>
<span data-ttu-id="262b1-122">O parâmetro ' ApplicationGateway ' aceita o valor do tipo ' PSApplicationGateway ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="262b1-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="262b1-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="262b1-123">OUTPUTS</span></span>

### <span data-ttu-id="262b1-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="262b1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

### <span data-ttu-id="262b1-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe]</span><span class="sxs-lookup"><span data-stu-id="262b1-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe]</span></span>

## <span data-ttu-id="262b1-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="262b1-126">NOTES</span></span>

## <span data-ttu-id="262b1-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="262b1-127">RELATED LINKS</span></span>

[<span data-ttu-id="262b1-128">Adicionar um teste a um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="262b1-128">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="262b1-129">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="262b1-129">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="262b1-130">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="262b1-130">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="262b1-131">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="262b1-131">Remove-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="262b1-132">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="262b1-132">Set-AzApplicationGatewayProbeConfig</span></span>]()

