---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b8e74c8630dc7f5ba0cd3633314b416ca9a3e39e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889769"
---
# <span data-ttu-id="65399-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="65399-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="65399-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65399-102">SYNOPSIS</span></span>
<span data-ttu-id="65399-103">Remove um certificado SSL de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="65399-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="65399-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65399-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65399-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65399-105">DESCRIPTION</span></span>
<span data-ttu-id="65399-106">O cmdlet **Remove-AzApplicationGatewaySslCertificate** remove um certificado SSL (Secure Sockets Layer) de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="65399-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="65399-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65399-107">EXAMPLES</span></span>

### <span data-ttu-id="65399-108">Exemplo 1: Remover um certificado SSL de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="65399-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="65399-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="65399-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="65399-110">O segundo comando remove o certificado SSL chamado Cert02 do gateway de aplicativo armazenado na variável $AppGW.</span><span class="sxs-lookup"><span data-stu-id="65399-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="65399-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65399-111">PARAMETERS</span></span>

### <span data-ttu-id="65399-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65399-112">-ApplicationGateway</span></span>
<span data-ttu-id="65399-113">Especifica o gateway de aplicativo do qual este cmdlet remove um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="65399-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="65399-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65399-114">-DefaultProfile</span></span>
<span data-ttu-id="65399-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="65399-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65399-116">-Name</span><span class="sxs-lookup"><span data-stu-id="65399-116">-Name</span></span>
<span data-ttu-id="65399-117">Especifica o nome de um certificado SSL que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="65399-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="65399-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65399-118">CommonParameters</span></span>
<span data-ttu-id="65399-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65399-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65399-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65399-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65399-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65399-121">INPUTS</span></span>

### <span data-ttu-id="65399-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65399-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65399-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65399-123">OUTPUTS</span></span>

### <span data-ttu-id="65399-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="65399-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="65399-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="65399-125">NOTES</span></span>

## <span data-ttu-id="65399-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65399-126">RELATED LINKS</span></span>

[<span data-ttu-id="65399-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="65399-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="65399-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="65399-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="65399-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="65399-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="65399-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="65399-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


