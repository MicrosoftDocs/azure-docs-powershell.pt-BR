---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 62c73fe60e147ca34083851db50c3830198dd60e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775581"
---
# <span data-ttu-id="e72b9-101">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e72b9-101">Get-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e72b9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e72b9-102">SYNOPSIS</span></span>
<span data-ttu-id="e72b9-103">Obtém um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e72b9-103">Gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="e72b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e72b9-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e72b9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e72b9-105">DESCRIPTION</span></span>
<span data-ttu-id="e72b9-106">O cmdlet **Get-AzApplicationGatewaySslCertificate** Obtém um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e72b9-106">The **Get-AzApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="e72b9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e72b9-107">EXAMPLES</span></span>

### <span data-ttu-id="e72b9-108">Exemplo 1: obter um certificado SSL específico</span><span class="sxs-lookup"><span data-stu-id="e72b9-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="e72b9-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e72b9-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e72b9-110">O segundo comando obtém o certificado SSL chamado Cert01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e72b9-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="e72b9-111">O comando armazena o certificado na variável chamada $Cert.</span><span class="sxs-lookup"><span data-stu-id="e72b9-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="e72b9-112">Exemplo 2: obter uma lista de certificados SSL</span><span class="sxs-lookup"><span data-stu-id="e72b9-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="e72b9-113">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e72b9-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="e72b9-114">Este segundo comando obtém uma lista de certificados SSL do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e72b9-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="e72b9-115">Em seguida, o comando armazena os resultados na variável chamada $Certs.</span><span class="sxs-lookup"><span data-stu-id="e72b9-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="e72b9-116">OS</span><span class="sxs-lookup"><span data-stu-id="e72b9-116">PARAMETERS</span></span>

### <span data-ttu-id="e72b9-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e72b9-117">-ApplicationGateway</span></span>
<span data-ttu-id="e72b9-118">Especifica o objeto do gateway do aplicativo que contém o certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="e72b9-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="e72b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e72b9-119">-DefaultProfile</span></span>
<span data-ttu-id="e72b9-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e72b9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e72b9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e72b9-121">-Name</span></span>
<span data-ttu-id="e72b9-122">Especifica o nome do pool de certificados SSL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="e72b9-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e72b9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e72b9-123">CommonParameters</span></span>
<span data-ttu-id="e72b9-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e72b9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e72b9-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e72b9-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e72b9-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e72b9-126">INPUTS</span></span>

### <span data-ttu-id="e72b9-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e72b9-127">System.String</span></span>

## <span data-ttu-id="e72b9-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e72b9-128">OUTPUTS</span></span>

### <span data-ttu-id="e72b9-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e72b9-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e72b9-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e72b9-130">NOTES</span></span>

## <span data-ttu-id="e72b9-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e72b9-131">RELATED LINKS</span></span>

[<span data-ttu-id="e72b9-132">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e72b9-132">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e72b9-133">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e72b9-133">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e72b9-134">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e72b9-134">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e72b9-135">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e72b9-135">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


