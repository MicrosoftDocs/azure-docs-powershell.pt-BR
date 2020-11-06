---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: ab5697091cf36018601bb2417e42e74f763a5d8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600629"
---
# <span data-ttu-id="fb44c-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fb44c-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="fb44c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb44c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb44c-103">Obtém um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb44c-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="fb44c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb44c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb44c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb44c-105">DESCRIPTION</span></span>
<span data-ttu-id="fb44c-106">O cmdlet **Get-AzApplicationGatewaySslCertificate** Obtém um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb44c-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="fb44c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb44c-107">EXAMPLES</span></span>

### <span data-ttu-id="fb44c-108">Exemplo 1: obter um certificado SSL específico</span><span class="sxs-lookup"><span data-stu-id="fb44c-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="fb44c-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="fb44c-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="fb44c-110">O segundo comando obtém o certificado SSL chamado Cert01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="fb44c-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="fb44c-111">O comando armazena o certificado na variável chamada $Cert.</span><span class="sxs-lookup"><span data-stu-id="fb44c-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="fb44c-112">Exemplo 2: obter uma lista de certificados SSL</span><span class="sxs-lookup"><span data-stu-id="fb44c-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="fb44c-113">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="fb44c-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="fb44c-114">Este segundo comando obtém uma lista de certificados SSL do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="fb44c-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="fb44c-115">Em seguida, o comando armazena os resultados na variável chamada $Certs.</span><span class="sxs-lookup"><span data-stu-id="fb44c-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="fb44c-116">OS</span><span class="sxs-lookup"><span data-stu-id="fb44c-116">PARAMETERS</span></span>

### <span data-ttu-id="fb44c-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb44c-117">-ApplicationGateway</span></span>
<span data-ttu-id="fb44c-118">Especifica o objeto do gateway do aplicativo que contém o certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="fb44c-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="fb44c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb44c-119">-DefaultProfile</span></span>
<span data-ttu-id="fb44c-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb44c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb44c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb44c-121">-Name</span></span>
<span data-ttu-id="fb44c-122">Especifica o nome do pool de certificados SSL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fb44c-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fb44c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb44c-123">CommonParameters</span></span>
<span data-ttu-id="fb44c-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb44c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb44c-125">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb44c-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb44c-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb44c-126">INPUTS</span></span>

### <span data-ttu-id="fb44c-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb44c-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fb44c-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb44c-128">OUTPUTS</span></span>

### <span data-ttu-id="fb44c-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fb44c-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="fb44c-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb44c-130">NOTES</span></span>

## <span data-ttu-id="fb44c-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb44c-131">RELATED LINKS</span></span>

[<span data-ttu-id="fb44c-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fb44c-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="fb44c-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fb44c-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="fb44c-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fb44c-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="fb44c-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="fb44c-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


