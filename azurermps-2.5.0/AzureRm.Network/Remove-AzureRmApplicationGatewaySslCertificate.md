---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D788B84-0179-4A35-AC35-27C6F5FECB39
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: eeab1f5699af5de737bc1e0390c35d387acfdd98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785475"
---
# <span data-ttu-id="c05b3-101">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c05b3-101">Remove-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="c05b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c05b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c05b3-103">Remove um certificado SSL de um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="c05b3-103">Removes an SSL certificate from an Azure application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c05b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c05b3-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewaySslCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c05b3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c05b3-105">DESCRIPTION</span></span>
<span data-ttu-id="c05b3-106">O cmdlet **Remove-AzureRmApplicationGatewaySslCertificate** remove um certificado Secure Sockets Layer (SSL) de um Application Gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="c05b3-106">The **Remove-AzureRmApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="c05b3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c05b3-107">EXAMPLES</span></span>

### <span data-ttu-id="c05b3-108">Exemplo 1: remover um certificado SSL de um aplicativo gateway</span><span class="sxs-lookup"><span data-stu-id="c05b3-108">Example 1: Remove an SSL certificate from an application gateway</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert02"
```

<span data-ttu-id="c05b3-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c05b3-109">The first command gets the application gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>

<span data-ttu-id="c05b3-110">O segundo comando Remove o certificado SSL chamado Cert02 do gateway do aplicativo armazenado na variável $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c05b3-110">The second command removes the SSL certificate named Cert02 from the application gateway stored in the $AppGW variable.</span></span>

## <span data-ttu-id="c05b3-111">OS</span><span class="sxs-lookup"><span data-stu-id="c05b3-111">PARAMETERS</span></span>

### <span data-ttu-id="c05b3-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c05b3-112">-ApplicationGateway</span></span>
<span data-ttu-id="c05b3-113">Especifica o Application Gateway do qual esse cmdlet Remove um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="c05b3-113">Specifies the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="c05b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05b3-114">-DefaultProfile</span></span>
<span data-ttu-id="c05b3-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c05b3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c05b3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c05b3-116">-Name</span></span>
<span data-ttu-id="c05b3-117">Especifica o nome de um certificado SSL que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c05b3-117">Specifies the name of an SSL certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c05b3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05b3-118">CommonParameters</span></span>
<span data-ttu-id="c05b3-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c05b3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05b3-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c05b3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05b3-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c05b3-121">INPUTS</span></span>

### <span data-ttu-id="c05b3-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c05b3-122">System.String</span></span>

## <span data-ttu-id="c05b3-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c05b3-123">OUTPUTS</span></span>

### <span data-ttu-id="c05b3-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c05b3-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c05b3-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c05b3-125">NOTES</span></span>

## <span data-ttu-id="c05b3-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c05b3-126">RELATED LINKS</span></span>

[<span data-ttu-id="c05b3-127">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c05b3-127">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c05b3-128">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c05b3-128">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c05b3-129">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c05b3-129">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="c05b3-130">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="c05b3-130">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


