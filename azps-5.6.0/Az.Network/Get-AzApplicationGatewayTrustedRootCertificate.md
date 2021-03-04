---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f040110ea3e00e99b989c07e8757d3c3a0c4b976
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890800"
---
# <span data-ttu-id="f7199-101">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f7199-101">Get-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f7199-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7199-102">SYNOPSIS</span></span>
<span data-ttu-id="f7199-103">Obtém o Certificado Raiz Confiável com um nome específico do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7199-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="f7199-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f7199-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7199-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f7199-105">DESCRIPTION</span></span>
<span data-ttu-id="f7199-106">O cmdlet **Get-AzApplicationGatewayTrustedRootCertificate** obtém Certificado Raiz Confiável com um nome específico do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7199-106">The **Get-AzApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="f7199-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7199-107">EXAMPLES</span></span>

### <span data-ttu-id="f7199-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f7199-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="f7199-109">O primeiro comando obtém o Gateway de Aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="f7199-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="f7199-110">O segundo comando obtém o Certificado Raiz Confiável com um nome especificado do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f7199-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="f7199-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f7199-111">PARAMETERS</span></span>

### <span data-ttu-id="f7199-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7199-112">-ApplicationGateway</span></span>
<span data-ttu-id="f7199-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7199-113">The applicationGateway</span></span>

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

### <span data-ttu-id="f7199-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7199-114">-DefaultProfile</span></span>
<span data-ttu-id="f7199-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7199-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7199-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f7199-116">-Name</span></span>
<span data-ttu-id="f7199-117">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="f7199-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="f7199-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7199-118">CommonParameters</span></span>
<span data-ttu-id="f7199-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7199-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7199-120">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7199-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7199-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7199-121">INPUTS</span></span>

### <span data-ttu-id="f7199-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f7199-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f7199-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f7199-123">OUTPUTS</span></span>

### <span data-ttu-id="f7199-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f7199-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="f7199-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="f7199-125">NOTES</span></span>

## <span data-ttu-id="f7199-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7199-126">RELATED LINKS</span></span>

[<span data-ttu-id="f7199-127">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f7199-127">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f7199-128">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f7199-128">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f7199-129">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f7199-129">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="f7199-130">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f7199-130">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
