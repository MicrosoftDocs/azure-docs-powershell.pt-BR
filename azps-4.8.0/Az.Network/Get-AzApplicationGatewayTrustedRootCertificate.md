---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5c3976ddeeaa856f956ecb785a9d35e62ba322fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110599"
---
# <span data-ttu-id="231c7-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="231c7-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="231c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="231c7-102">SYNOPSIS</span></span>
<span data-ttu-id="231c7-103">Obtém o certificado raiz confiável com um nome específico do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="231c7-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="231c7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="231c7-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="231c7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="231c7-105">DESCRIPTION</span></span>
<span data-ttu-id="231c7-106">O cmdlet **Get-AzApplicationGatewayTrustedRootCertificate** Obtém um certificado raiz confiável com um nome específico do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="231c7-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="231c7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="231c7-107">EXAMPLES</span></span>

### <span data-ttu-id="231c7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="231c7-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="231c7-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="231c7-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="231c7-110">O segundo comando obtém o certificado raiz confiável com um nome especificado do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="231c7-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="231c7-111">OS</span><span class="sxs-lookup"><span data-stu-id="231c7-111">PARAMETERS</span></span>

### <span data-ttu-id="231c7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="231c7-112">-ApplicationGateway</span></span>
<span data-ttu-id="231c7-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="231c7-113">The applicationGateway</span></span>

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

### <span data-ttu-id="231c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="231c7-114">-DefaultProfile</span></span>
<span data-ttu-id="231c7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="231c7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="231c7-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="231c7-116">-Name</span></span>
<span data-ttu-id="231c7-117">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="231c7-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="231c7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="231c7-118">CommonParameters</span></span>
<span data-ttu-id="231c7-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="231c7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="231c7-120">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="231c7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="231c7-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="231c7-121">INPUTS</span></span>

### <span data-ttu-id="231c7-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="231c7-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="231c7-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="231c7-123">OUTPUTS</span></span>

### <span data-ttu-id="231c7-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="231c7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="231c7-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="231c7-125">NOTES</span></span>

## <span data-ttu-id="231c7-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="231c7-126">RELATED LINKS</span></span>

[<span data-ttu-id="231c7-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="231c7-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="231c7-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="231c7-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="231c7-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="231c7-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="231c7-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="231c7-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
