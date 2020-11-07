---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 919B3755-81D4-43FB-AE8C-B071329A61D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaysslcertificate
schema: 2.0.0
ms.openlocfilehash: 6e2dceadf11323eb1798435df426c063f4d58858
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786473"
---
# <span data-ttu-id="5ba66-101">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ba66-101">Get-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5ba66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ba66-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba66-103">Obtém um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ba66-103">Gets an SSL certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ba66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ba66-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewaySslCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba66-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ba66-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba66-106">O cmdlet **Get-AzureRmApplicationGatewaySslCertificate** Obtém um certificado SSL para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5ba66-106">The **Get-AzureRmApplicationGatewaySslCertificate** cmdlet gets an SSL certificate for an application gateway.</span></span>

## <span data-ttu-id="5ba66-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ba66-107">EXAMPLES</span></span>

### <span data-ttu-id="5ba66-108">Exemplo 1: obter um certificado SSL específico</span><span class="sxs-lookup"><span data-stu-id="5ba66-108">Example 1: Get a specific SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Get-AzureRmApplicationGatewaySslCertificate -Name "Cert01" -ApplicationGateway $AppGW
```

<span data-ttu-id="5ba66-109">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5ba66-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5ba66-110">O segundo comando obtém o certificado SSL chamado Cert01 do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5ba66-110">The second command gets the SSL certificate named Cert01 from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="5ba66-111">O comando armazena o certificado na variável chamada $Cert.</span><span class="sxs-lookup"><span data-stu-id="5ba66-111">The command stores the certificate in the variable named $Cert.</span></span>

### <span data-ttu-id="5ba66-112">Exemplo 2: obter uma lista de certificados SSL</span><span class="sxs-lookup"><span data-stu-id="5ba66-112">Example 2: Get a list of SSL certificates</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Certs = Get-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW
```

<span data-ttu-id="5ba66-113">O primeiro comando obtém o gateway do aplicativo chamado ApplicationGateway01 e armazena o resultado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5ba66-113">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="5ba66-114">Este segundo comando obtém uma lista de certificados SSL do gateway do aplicativo armazenado na variável chamada $AppGW.</span><span class="sxs-lookup"><span data-stu-id="5ba66-114">This second command gets a list of SSL certificates from the application gateway stored in the variable named $AppGW.</span></span>
<span data-ttu-id="5ba66-115">Em seguida, o comando armazena os resultados na variável chamada $Certs.</span><span class="sxs-lookup"><span data-stu-id="5ba66-115">The command then stores the results in the variable named $Certs.</span></span>

## <span data-ttu-id="5ba66-116">OS</span><span class="sxs-lookup"><span data-stu-id="5ba66-116">PARAMETERS</span></span>

### <span data-ttu-id="5ba66-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ba66-117">-ApplicationGateway</span></span>
<span data-ttu-id="5ba66-118">Especifica o objeto do gateway do aplicativo que contém o certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="5ba66-118">Specifies the application gateway object that contains the SSL certificate.</span></span>

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

### <span data-ttu-id="5ba66-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba66-119">-DefaultProfile</span></span>
<span data-ttu-id="5ba66-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba66-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ba66-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ba66-121">-Name</span></span>
<span data-ttu-id="5ba66-122">Especifica o nome do pool de certificados SSL que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="5ba66-122">Specifies the name of SSL certificate pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5ba66-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba66-123">CommonParameters</span></span>
<span data-ttu-id="5ba66-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba66-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba66-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba66-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba66-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ba66-126">INPUTS</span></span>

### <span data-ttu-id="5ba66-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5ba66-127">System.String</span></span>

## <span data-ttu-id="5ba66-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ba66-128">OUTPUTS</span></span>

### <span data-ttu-id="5ba66-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ba66-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="5ba66-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ba66-130">NOTES</span></span>

## <span data-ttu-id="5ba66-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ba66-131">RELATED LINKS</span></span>

[<span data-ttu-id="5ba66-132">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ba66-132">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5ba66-133">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ba66-133">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5ba66-134">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ba66-134">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="5ba66-135">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="5ba66-135">Set-AzureRmApplicationGatewaySslCertificate</span></span>](./Set-AzureRmApplicationGatewaySslCertificate.md)


