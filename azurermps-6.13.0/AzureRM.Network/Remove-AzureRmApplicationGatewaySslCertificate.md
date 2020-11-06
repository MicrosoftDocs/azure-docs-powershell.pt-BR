---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: 865b9a576219cbaf7d938094baf923c497436e07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429451"
---
# <span data-ttu-id="2f1ae-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1ae-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="2f1ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2f1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="2f1ae-103">Remove um certificado SSL de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1ae-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2f1ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2f1ae-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f1ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2f1ae-105">DESCRIPTION</span></span>
<span data-ttu-id="2f1ae-106">O cmdlet **Remove-AzureRmApplicationGatewaySslCertificate** remove um certificado Secure Sockets Layer (SSL) de um Application Gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1ae-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="2f1ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f1ae-107">EXAMPLES</span></span>

### <span data-ttu-id="2f1ae-108">Exemplo 1: remover um certificado SSL de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="2f1ae-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="2f1ae-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="2f1ae-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="2f1ae-110">O segundo comando Remove o certificado SSL chamado Cert02 do gateway do aplicativo armazenado na variável $AppGW.</span><span class="sxs-lookup"><span data-stu-id="2f1ae-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="2f1ae-111">OS</span><span class="sxs-lookup"><span data-stu-id="2f1ae-111">PARAMETERS</span></span>

### <span data-ttu-id="2f1ae-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f1ae-112">-ApplicationGateway</span></span>
<span data-ttu-id="2f1ae-113">Especifica o Application Gateway do qual esse cmdlet Remove um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="2f1ae-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="2f1ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f1ae-114">-DefaultProfile</span></span>
<span data-ttu-id="2f1ae-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2f1ae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f1ae-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2f1ae-116">-Name</span></span>
<span data-ttu-id="2f1ae-117">Especifica o nome de um certificado SSL que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="2f1ae-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f1ae-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f1ae-118">CommonParameters</span></span>
<span data-ttu-id="2f1ae-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f1ae-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f1ae-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f1ae-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f1ae-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2f1ae-121">INPUTS</span></span>

### <span data-ttu-id="2f1ae-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f1ae-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="2f1ae-123">Parâmetros: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f1ae-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="2f1ae-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2f1ae-124">OUTPUTS</span></span>

### <span data-ttu-id="2f1ae-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2f1ae-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2f1ae-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2f1ae-126">NOTES</span></span>

## <span data-ttu-id="2f1ae-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f1ae-127">RELATED LINKS</span></span>

[<span data-ttu-id="2f1ae-128">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1ae-128">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2f1ae-129">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1ae-129">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2f1ae-130">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1ae-130">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="2f1ae-131">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2f1ae-131">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)

