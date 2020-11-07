---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 473e759e43c59c48b9e47706ac55b388379b6d6d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771912"
---
# <span data-ttu-id="41144-101">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="41144-101">New-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="41144-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41144-102">SYNOPSIS</span></span>
<span data-ttu-id="41144-103">Cria um certificado raiz confiável para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="41144-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

## <span data-ttu-id="41144-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41144-104">SYNTAX</span></span>

```
New-AzApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41144-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41144-105">DESCRIPTION</span></span>
<span data-ttu-id="41144-106">O cmdlet **New-AzApplicationGatewayTrustedRootCertificate** cria um certificado raiz confiável para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="41144-106">The **New-AzApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="41144-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41144-107">EXAMPLES</span></span>

### <span data-ttu-id="41144-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41144-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzApplicationGatewayTrustedRootCertificate -Name "trc1" -CertificateFile $certFilePath
```

<span data-ttu-id="41144-109">Esse comando cria um certificado raiz confiável denominado List "TRC1" e armazena o resultado na variável chamada $trc.</span><span class="sxs-lookup"><span data-stu-id="41144-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="41144-110">OS</span><span class="sxs-lookup"><span data-stu-id="41144-110">PARAMETERS</span></span>

### <span data-ttu-id="41144-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="41144-111">-CertificateFile</span></span>
<span data-ttu-id="41144-112">Caminho do arquivo CER do certificado</span><span class="sxs-lookup"><span data-stu-id="41144-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="41144-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41144-113">-DefaultProfile</span></span>
<span data-ttu-id="41144-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41144-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41144-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="41144-115">-Name</span></span>
<span data-ttu-id="41144-116">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="41144-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="41144-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41144-117">-Confirm</span></span>
<span data-ttu-id="41144-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41144-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41144-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41144-119">-WhatIf</span></span>
<span data-ttu-id="41144-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41144-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41144-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41144-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41144-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41144-122">CommonParameters</span></span>
<span data-ttu-id="41144-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41144-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41144-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41144-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41144-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41144-125">INPUTS</span></span>

### <span data-ttu-id="41144-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="41144-126">None</span></span>

## <span data-ttu-id="41144-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41144-127">OUTPUTS</span></span>

### <span data-ttu-id="41144-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="41144-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="41144-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41144-129">NOTES</span></span>

## <span data-ttu-id="41144-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41144-130">RELATED LINKS</span></span>

[<span data-ttu-id="41144-131">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="41144-131">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="41144-132">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="41144-132">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="41144-133">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="41144-133">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="41144-134">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="41144-134">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
