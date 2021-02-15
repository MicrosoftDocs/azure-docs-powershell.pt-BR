---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 99d56b837b67fe8b816c4f27c8658932a74452e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115196"
---
# <span data-ttu-id="daa77-101">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="daa77-101">Get-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="daa77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="daa77-102">SYNOPSIS</span></span>
<span data-ttu-id="daa77-103">Obtém a cadeia de certificados da CA de cliente confiável com um nome específico do Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="daa77-103">Gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="daa77-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="daa77-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayTrustedClientCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daa77-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="daa77-105">DESCRIPTION</span></span>
<span data-ttu-id="daa77-106">O Get-AzApplicationGatewayTrustedClientCertificate cmdlet obtém a cadeia de certificados de CA do cliente confiável com um nome específico do Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="daa77-106">The Get-AzApplicationGatewayTrustedClientCertificate cmdlet gets the trusted client CA certificate chain with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="daa77-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="daa77-107">EXAMPLES</span></span>

### <span data-ttu-id="daa77-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="daa77-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClientCert = Get-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName
```

<span data-ttu-id="daa77-109">O primeiro comando obtém o Gateway de Aplicativos e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="daa77-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span> <span data-ttu-id="daa77-110">O segundo comando obtém a cadeia de certificados de CA do cliente confiável com um nome especificado do Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="daa77-110">The second command gets the trusted client CA certificate chain with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="daa77-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="daa77-111">PARAMETERS</span></span>

### <span data-ttu-id="daa77-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daa77-112">-ApplicationGateway</span></span>
<span data-ttu-id="daa77-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="daa77-113">The applicationGateway</span></span>

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

### <span data-ttu-id="daa77-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa77-114">-DefaultProfile</span></span>
<span data-ttu-id="daa77-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="daa77-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="daa77-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="daa77-116">-Name</span></span>
<span data-ttu-id="daa77-117">O nome da cadeia de certificados de AC do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="daa77-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="daa77-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa77-118">CommonParameters</span></span>
<span data-ttu-id="daa77-119">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="daa77-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa77-120">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="daa77-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa77-121">Entradas</span><span class="sxs-lookup"><span data-stu-id="daa77-121">INPUTS</span></span>

### <span data-ttu-id="daa77-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daa77-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="daa77-123">Saídas</span><span class="sxs-lookup"><span data-stu-id="daa77-123">OUTPUTS</span></span>

### <span data-ttu-id="daa77-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="daa77-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="daa77-125">Notas</span><span class="sxs-lookup"><span data-stu-id="daa77-125">NOTES</span></span>

## <span data-ttu-id="daa77-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="daa77-126">RELATED LINKS</span></span>

[<span data-ttu-id="daa77-127">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="daa77-127">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="daa77-128">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="daa77-128">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="daa77-129">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="daa77-129">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="daa77-130">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="daa77-130">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)