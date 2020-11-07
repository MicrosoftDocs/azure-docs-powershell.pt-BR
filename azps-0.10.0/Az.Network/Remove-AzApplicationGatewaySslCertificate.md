---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 9b90dc354a62c6f6d69e1e6dbd8bf18ecc0fa4f7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775318"
---
# <span data-ttu-id="23e0d-101">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="23e0d-101">Remove-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="23e0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="23e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="23e0d-103">Remove um certificado SSL de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="23e0d-103">Removes an SSL certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="23e0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23e0d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23e0d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="23e0d-105">DESCRIPTION</span></span>
<span data-ttu-id="23e0d-106">O cmdlet **Remove-AzApplicationGatewaySslCertificate** remove um certificado Secure Sockets Layer (SSL) de um Application Gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="23e0d-106">The **Remove-AzApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="23e0d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="23e0d-107">EXAMPLES</span></span>

### <span data-ttu-id="23e0d-108">Exemplo 1: remover um certificado SSL de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="23e0d-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="23e0d-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="23e0d-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="23e0d-110">O segundo comando Remove o certificado SSL chamado Cert02 do gateway do aplicativo armazenado na variável $AppGW.</span><span class="sxs-lookup"><span data-stu-id="23e0d-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="23e0d-111">OS</span><span class="sxs-lookup"><span data-stu-id="23e0d-111">PARAMETERS</span></span>

### <span data-ttu-id="23e0d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23e0d-112">-ApplicationGateway</span></span>
<span data-ttu-id="23e0d-113">Especifica o Application Gateway do qual esse cmdlet Remove um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="23e0d-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="23e0d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e0d-114">-DefaultProfile</span></span>
<span data-ttu-id="23e0d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="23e0d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23e0d-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="23e0d-116">-Name</span></span>
<span data-ttu-id="23e0d-117">Especifica o nome de um certificado SSL que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="23e0d-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="23e0d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e0d-118">CommonParameters</span></span>
<span data-ttu-id="23e0d-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e0d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e0d-120">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e0d-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e0d-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="23e0d-121">INPUTS</span></span>

### <span data-ttu-id="23e0d-122">System. String</span><span class="sxs-lookup"><span data-stu-id="23e0d-122">System.String</span></span>

## <span data-ttu-id="23e0d-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="23e0d-123">OUTPUTS</span></span>

### <span data-ttu-id="23e0d-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23e0d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="23e0d-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="23e0d-125">NOTES</span></span>

## <span data-ttu-id="23e0d-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="23e0d-126">RELATED LINKS</span></span>

[<span data-ttu-id="23e0d-127">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="23e0d-127">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="23e0d-128">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="23e0d-128">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="23e0d-129">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="23e0d-129">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="23e0d-130">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="23e0d-130">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


