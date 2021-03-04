---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: bacdca3f26e18f3dc41ac19990e48f9e6bb63c1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887697"
---
# <span data-ttu-id="04dcb-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="04dcb-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="04dcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="04dcb-103">Cria um Certificado Raiz Confiável para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="04dcb-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="04dcb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="04dcb-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04dcb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="04dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="04dcb-106">O cmdlet **New-AzApplicationGatewayTrustedRootCertificate** cria um Certificado Raiz Confiável para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="04dcb-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="04dcb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04dcb-107">EXAMPLES</span></span>

### <span data-ttu-id="04dcb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="04dcb-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="04dcb-109">Este comando cria um Certificado Raiz Confiável denominado Lista "trc1" e armazena o resultado na variável chamada $trc.</span><span class="sxs-lookup"><span data-stu-id="04dcb-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="04dcb-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="04dcb-110">PARAMETERS</span></span>

### <span data-ttu-id="04dcb-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="04dcb-111">-CertificateFile</span></span>
<span data-ttu-id="04dcb-112">Caminho do arquivo CER de certificado</span><span class="sxs-lookup"><span data-stu-id="04dcb-112">Path of certificate CER file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04dcb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04dcb-113">-DefaultProfile</span></span>
<span data-ttu-id="04dcb-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="04dcb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04dcb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="04dcb-115">-Name</span></span>
<span data-ttu-id="04dcb-116">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="04dcb-116">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04dcb-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04dcb-117">-Confirm</span></span>
<span data-ttu-id="04dcb-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04dcb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04dcb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04dcb-119">-WhatIf</span></span>
<span data-ttu-id="04dcb-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="04dcb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04dcb-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="04dcb-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04dcb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04dcb-122">CommonParameters</span></span>
<span data-ttu-id="04dcb-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04dcb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04dcb-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04dcb-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04dcb-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04dcb-125">INPUTS</span></span>

### <span data-ttu-id="04dcb-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="04dcb-126">None</span></span>

## <span data-ttu-id="04dcb-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="04dcb-127">OUTPUTS</span></span>

### <span data-ttu-id="04dcb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="04dcb-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="04dcb-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="04dcb-129">NOTES</span></span>

## <span data-ttu-id="04dcb-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04dcb-130">RELATED LINKS</span></span>

[<span data-ttu-id="04dcb-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="04dcb-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="04dcb-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="04dcb-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="04dcb-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="04dcb-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="04dcb-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="04dcb-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
