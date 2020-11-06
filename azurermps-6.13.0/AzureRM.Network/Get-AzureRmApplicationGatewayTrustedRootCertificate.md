---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93609393"
---
# <span data-ttu-id="d5f19-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d5f19-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d5f19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d5f19-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f19-103">Obtém o certificado raiz confiável com um nome específico do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5f19-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5f19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d5f19-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5f19-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d5f19-105">DESCRIPTION</span></span>
<span data-ttu-id="d5f19-106">O cmdlet **Get-AzureRmApplicationGatewayTrustedRootCertificate** Obtém um certificado raiz confiável com um nome específico do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5f19-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="d5f19-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d5f19-107">EXAMPLES</span></span>

### <span data-ttu-id="d5f19-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d5f19-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="d5f19-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="d5f19-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="d5f19-110">O segundo comando obtém o certificado raiz confiável com um nome especificado do gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5f19-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="d5f19-111">OS</span><span class="sxs-lookup"><span data-stu-id="d5f19-111">PARAMETERS</span></span>

### <span data-ttu-id="d5f19-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5f19-112">-ApplicationGateway</span></span>
<span data-ttu-id="d5f19-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5f19-113">The applicationGateway</span></span>

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

### <span data-ttu-id="d5f19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f19-114">-DefaultProfile</span></span>
<span data-ttu-id="d5f19-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d5f19-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5f19-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5f19-116">-Name</span></span>
<span data-ttu-id="d5f19-117">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="d5f19-117">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="d5f19-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f19-118">CommonParameters</span></span>
<span data-ttu-id="d5f19-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5f19-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f19-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5f19-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f19-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d5f19-121">INPUTS</span></span>

### <span data-ttu-id="d5f19-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d5f19-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d5f19-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d5f19-123">OUTPUTS</span></span>

### <span data-ttu-id="d5f19-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d5f19-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d5f19-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d5f19-125">NOTES</span></span>

## <span data-ttu-id="d5f19-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d5f19-126">RELATED LINKS</span></span>
