---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 839f2a647c4a06ddd1bdebe9b95fac0fdbdd91dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890995"
---
# <span data-ttu-id="d6b9c-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d6b9c-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d6b9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b9c-103">Atualiza um Certificado Raiz Confiável de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="d6b9c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d6b9c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6b9c-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d6b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="d6b9c-106">O cmdlet **Set-AzApplicationGatewayTrustedRootCertificate** modifica o certificado raiz confiável existente de um Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="d6b9c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6b9c-107">EXAMPLES</span></span>

### <span data-ttu-id="d6b9c-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d6b9c-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="d6b9c-109">Cenários de exemplo acima mostram como atualizar um certificado raiz confiável existente quando um certificado raiz é rolado.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="d6b9c-110">O primeiro comando obtém um gateway de aplicativo e o armazena na $gw variável.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="d6b9c-111">O segundo comando modifica o certificado raiz confiável existente com um novo certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="d6b9c-112">O terceiro comando atualiza o gateway de aplicativo no Azure.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="d6b9c-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d6b9c-113">PARAMETERS</span></span>

### <span data-ttu-id="d6b9c-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6b9c-114">-ApplicationGateway</span></span>
<span data-ttu-id="d6b9c-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6b9c-115">The applicationGateway</span></span>

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

### <span data-ttu-id="d6b9c-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d6b9c-116">-CertificateFile</span></span>
<span data-ttu-id="d6b9c-117">Caminho do arquivo CER de certificado</span><span class="sxs-lookup"><span data-stu-id="d6b9c-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="d6b9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b9c-118">-DefaultProfile</span></span>
<span data-ttu-id="d6b9c-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6b9c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d6b9c-120">-Name</span></span>
<span data-ttu-id="d6b9c-121">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="d6b9c-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="d6b9c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6b9c-122">-Confirm</span></span>
<span data-ttu-id="d6b9c-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6b9c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b9c-124">-WhatIf</span></span>
<span data-ttu-id="d6b9c-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6b9c-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6b9c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b9c-127">CommonParameters</span></span>
<span data-ttu-id="d6b9c-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6b9c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b9c-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b9c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b9c-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6b9c-130">INPUTS</span></span>

### <span data-ttu-id="d6b9c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6b9c-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6b9c-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d6b9c-132">OUTPUTS</span></span>

### <span data-ttu-id="d6b9c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d6b9c-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d6b9c-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="d6b9c-134">NOTES</span></span>

## <span data-ttu-id="d6b9c-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6b9c-135">RELATED LINKS</span></span>

[<span data-ttu-id="d6b9c-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d6b9c-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d6b9c-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d6b9c-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d6b9c-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d6b9c-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d6b9c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d6b9c-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
