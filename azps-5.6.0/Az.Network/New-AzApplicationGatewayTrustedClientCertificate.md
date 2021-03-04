---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e34d170167aac09cd64ca11d0838f36fc0515423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890241"
---
# <span data-ttu-id="1168d-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1168d-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="1168d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1168d-102">SYNOPSIS</span></span>
<span data-ttu-id="1168d-103">Cria uma cadeia de certificados de AC de cliente confiável para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1168d-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="1168d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1168d-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1168d-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1168d-105">DESCRIPTION</span></span>
<span data-ttu-id="1168d-106">O New-AzApplicationGatewayTrustedClientCertificate cmdlet cria uma cadeia de certificados ca de cliente confiável para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1168d-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="1168d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1168d-107">EXAMPLES</span></span>

### <span data-ttu-id="1168d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1168d-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="1168d-109">O comando cria um novo objeto de cadeia de certificados de CA de cliente confiável que está tomando o caminho do certificado ca do cliente como entrada.</span><span class="sxs-lookup"><span data-stu-id="1168d-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="1168d-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1168d-110">PARAMETERS</span></span>

### <span data-ttu-id="1168d-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="1168d-111">-CertificateFile</span></span>
<span data-ttu-id="1168d-112">Caminho do arquivo de cadeia de certificados de CA do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="1168d-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="1168d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1168d-113">-DefaultProfile</span></span>
<span data-ttu-id="1168d-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1168d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1168d-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1168d-115">-Name</span></span>
<span data-ttu-id="1168d-116">O nome da cadeia de certificados ca de cliente confiável</span><span class="sxs-lookup"><span data-stu-id="1168d-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="1168d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1168d-117">-Confirm</span></span>
<span data-ttu-id="1168d-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1168d-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1168d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1168d-119">-WhatIf</span></span>
<span data-ttu-id="1168d-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1168d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1168d-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1168d-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1168d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1168d-122">CommonParameters</span></span>
<span data-ttu-id="1168d-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1168d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1168d-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1168d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1168d-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1168d-125">INPUTS</span></span>

### <span data-ttu-id="1168d-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="1168d-126">None</span></span>

## <span data-ttu-id="1168d-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1168d-127">OUTPUTS</span></span>

### <span data-ttu-id="1168d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1168d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="1168d-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="1168d-129">NOTES</span></span>

## <span data-ttu-id="1168d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1168d-130">RELATED LINKS</span></span>

[<span data-ttu-id="1168d-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1168d-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1168d-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1168d-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1168d-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1168d-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="1168d-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="1168d-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)