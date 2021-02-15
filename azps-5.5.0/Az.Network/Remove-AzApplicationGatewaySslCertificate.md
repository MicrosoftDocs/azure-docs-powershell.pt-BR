---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: b03d35b511bafefe0ba062eb15a9c1eee8961585
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111602"
---
# <span data-ttu-id="5f62c-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5f62c-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5f62c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f62c-102">SYNOPSIS</span></span>
<span data-ttu-id="5f62c-103">Remove um certificado SSL de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f62c-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="5f62c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f62c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f62c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f62c-105">DESCRIPTION</span></span>
<span data-ttu-id="5f62c-106">O cmdlet **Remove-AzApplicationGatewaySslCertificate** remove um certificado SSL (Secure Sockets Layer) de um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="5f62c-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="5f62c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5f62c-107">EXAMPLES</span></span>

### <span data-ttu-id="5f62c-108">Exemplo 1: Remover um certificado SSL de um gateway de aplicativo</span><span class="sxs-lookup"><span data-stu-id="5f62c-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="5f62c-109">O primeiro comando obtém o gateway de aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5f62c-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5f62c-110">O segundo comando remove o certificado SSL chamado Cert02 do gateway de aplicativo armazenado na variável $AppGW dados.</span><span class="sxs-lookup"><span data-stu-id="5f62c-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="5f62c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f62c-111">PARAMETERS</span></span>

### <span data-ttu-id="5f62c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f62c-112">-ApplicationGateway</span></span>
<span data-ttu-id="5f62c-113">Especifica o gateway de aplicativo do qual este cmdlet remove um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="5f62c-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="5f62c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f62c-114">-DefaultProfile</span></span>
<span data-ttu-id="5f62c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="5f62c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f62c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f62c-116">-Name</span></span>
<span data-ttu-id="5f62c-117">Especifica o nome de um certificado SSL que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="5f62c-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5f62c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f62c-118">CommonParameters</span></span>
<span data-ttu-id="5f62c-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f62c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f62c-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f62c-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f62c-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="5f62c-121">INPUTS</span></span>

### <span data-ttu-id="5f62c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f62c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f62c-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="5f62c-123">OUTPUTS</span></span>

### <span data-ttu-id="5f62c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5f62c-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5f62c-125">Notas</span><span class="sxs-lookup"><span data-stu-id="5f62c-125">NOTES</span></span>

## <span data-ttu-id="5f62c-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f62c-126">RELATED LINKS</span></span>

[<span data-ttu-id="5f62c-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5f62c-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5f62c-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5f62c-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5f62c-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5f62c-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5f62c-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5f62c-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


