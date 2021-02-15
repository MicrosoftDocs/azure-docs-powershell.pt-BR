---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111690"
---
# <span data-ttu-id="16766-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16766-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="16766-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="16766-102">SYNOPSIS</span></span>
<span data-ttu-id="16766-103">Obtém uma configuração de configuração de configuração de saúde existente de um Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16766-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="16766-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16766-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16766-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="16766-105">DESCRIPTION</span></span>
<span data-ttu-id="16766-106">O Get-AzApplicationGatewayProbeConfig cmdlet obtém uma configuração de configuração de problemas de saúde existente de um Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="16766-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="16766-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="16766-107">EXAMPLES</span></span>

### <span data-ttu-id="16766-108">Exemplo 1: Obter uma confirmação existente de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="16766-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="16766-109">Esse comando obtém a confirmação de saúde chamada " Sor02 " do gateway de aplicativo chamado Gateway.</span><span class="sxs-lookup"><span data-stu-id="16766-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="16766-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="16766-110">PARAMETERS</span></span>

### <span data-ttu-id="16766-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16766-111">-ApplicationGateway</span></span>
<span data-ttu-id="16766-112">Especifica o gateway do aplicativo para o qual este cmdlet obtém uma configuração de configuração de configuração.</span><span class="sxs-lookup"><span data-stu-id="16766-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="16766-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16766-113">-DefaultProfile</span></span>
<span data-ttu-id="16766-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="16766-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16766-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="16766-115">-Name</span></span>
<span data-ttu-id="16766-116">Especifica o nome da sonda.</span><span class="sxs-lookup"><span data-stu-id="16766-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="16766-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16766-117">CommonParameters</span></span>
<span data-ttu-id="16766-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16766-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16766-119">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16766-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16766-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="16766-120">INPUTS</span></span>

### <span data-ttu-id="16766-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="16766-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="16766-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="16766-122">OUTPUTS</span></span>

### <span data-ttu-id="16766-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="16766-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="16766-124">Notas</span><span class="sxs-lookup"><span data-stu-id="16766-124">NOTES</span></span>

## <span data-ttu-id="16766-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="16766-125">RELATED LINKS</span></span>

[<span data-ttu-id="16766-126">Adicionar um problema a um gateway de aplicativo existente</span><span class="sxs-lookup"><span data-stu-id="16766-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="16766-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16766-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="16766-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16766-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="16766-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16766-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="16766-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="16766-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

