---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427593"
---
# <span data-ttu-id="78f3e-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="78f3e-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="78f3e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="78f3e-102">SYNOPSIS</span></span>
<span data-ttu-id="78f3e-103">Cria uma cadeia de certificados de autoridade de certificação de cliente confiável para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78f3e-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="78f3e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78f3e-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78f3e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="78f3e-105">DESCRIPTION</span></span>
<span data-ttu-id="78f3e-106">O cmdlet New-AzApplicationGatewayTrustedClientCertificate cria uma cadeia de certificados de autoridade de certificação de cliente confiável para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="78f3e-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="78f3e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="78f3e-107">EXAMPLES</span></span>

### <span data-ttu-id="78f3e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="78f3e-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="78f3e-109">O comando cria um novo objeto de cadeia de certificados de autoridade de certificação de cliente confiável fazendo o caminho do certificado da autoridade de certificação do cliente como entrada.</span><span class="sxs-lookup"><span data-stu-id="78f3e-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="78f3e-110">OS</span><span class="sxs-lookup"><span data-stu-id="78f3e-110">PARAMETERS</span></span>

### <span data-ttu-id="78f3e-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="78f3e-111">-CertificateFile</span></span>
<span data-ttu-id="78f3e-112">Caminho do arquivo de cadeia de certificados da autoridade de certificação do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="78f3e-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="78f3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f3e-113">-DefaultProfile</span></span>
<span data-ttu-id="78f3e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="78f3e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f3e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="78f3e-115">-Name</span></span>
<span data-ttu-id="78f3e-116">O nome da cadeia de certificados da autoridade de certificação do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="78f3e-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="78f3e-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="78f3e-117">-Confirm</span></span>
<span data-ttu-id="78f3e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78f3e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78f3e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78f3e-119">-WhatIf</span></span>
<span data-ttu-id="78f3e-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="78f3e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78f3e-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="78f3e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78f3e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f3e-122">CommonParameters</span></span>
<span data-ttu-id="78f3e-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f3e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f3e-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78f3e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f3e-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="78f3e-125">INPUTS</span></span>

### <span data-ttu-id="78f3e-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="78f3e-126">None</span></span>

## <span data-ttu-id="78f3e-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="78f3e-127">OUTPUTS</span></span>

### <span data-ttu-id="78f3e-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="78f3e-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="78f3e-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="78f3e-129">NOTES</span></span>

## <span data-ttu-id="78f3e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="78f3e-130">RELATED LINKS</span></span>

[<span data-ttu-id="78f3e-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="78f3e-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="78f3e-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="78f3e-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="78f3e-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="78f3e-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="78f3e-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="78f3e-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)