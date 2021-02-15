---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 285e9c343ed18d4aa21c328344b7be82319f0d3b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115136"
---
# <span data-ttu-id="53c21-101">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="53c21-101">New-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="53c21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53c21-102">SYNOPSIS</span></span>
<span data-ttu-id="53c21-103">Cria uma cadeia de certificados de CA de cliente confiável para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53c21-103">Creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="53c21-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53c21-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedClientCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53c21-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="53c21-105">DESCRIPTION</span></span>
<span data-ttu-id="53c21-106">O cmdlet New-AzApplicationGatewayTrustedClientCertificate cria uma cadeia de certificados ca de cliente confiável para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="53c21-106">The New-AzApplicationGatewayTrustedClientCertificate cmdlet creates a trusted client CA certificate chain for an application gateway.</span></span>

## <span data-ttu-id="53c21-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="53c21-107">EXAMPLES</span></span>

### <span data-ttu-id="53c21-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="53c21-108">Example 1</span></span>
```powershell
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
```
<span data-ttu-id="53c21-109">O comando cria um novo objeto de cadeia de certificados da CA de cliente confiável que caminho para o certificado ca do cliente como entrada.</span><span class="sxs-lookup"><span data-stu-id="53c21-109">The command creates a new trusted client CA certificate chain object taking path of the client CA certificate as input.</span></span>

## <span data-ttu-id="53c21-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53c21-110">PARAMETERS</span></span>

### <span data-ttu-id="53c21-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="53c21-111">-CertificateFile</span></span>
<span data-ttu-id="53c21-112">Caminho do arquivo de cadeia de certificados da CA do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="53c21-112">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="53c21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53c21-113">-DefaultProfile</span></span>
<span data-ttu-id="53c21-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53c21-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53c21-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="53c21-115">-Name</span></span>
<span data-ttu-id="53c21-116">O nome da cadeia de certificados de AC do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="53c21-116">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="53c21-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="53c21-117">-Confirm</span></span>
<span data-ttu-id="53c21-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53c21-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53c21-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53c21-119">-WhatIf</span></span>
<span data-ttu-id="53c21-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="53c21-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53c21-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53c21-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53c21-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c21-122">CommonParameters</span></span>
<span data-ttu-id="53c21-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53c21-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c21-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53c21-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c21-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="53c21-125">INPUTS</span></span>

### <span data-ttu-id="53c21-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="53c21-126">None</span></span>

## <span data-ttu-id="53c21-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="53c21-127">OUTPUTS</span></span>

### <span data-ttu-id="53c21-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="53c21-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="53c21-129">Notas</span><span class="sxs-lookup"><span data-stu-id="53c21-129">NOTES</span></span>

## <span data-ttu-id="53c21-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53c21-130">RELATED LINKS</span></span>

[<span data-ttu-id="53c21-131">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="53c21-131">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="53c21-132">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="53c21-132">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="53c21-133">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="53c21-133">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="53c21-134">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="53c21-134">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)