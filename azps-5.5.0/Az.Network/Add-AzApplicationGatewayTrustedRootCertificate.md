---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: f5e8624beeb8053cbf054526cddc24c7da6cdf3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114725"
---
# <span data-ttu-id="d45cf-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d45cf-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d45cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d45cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d45cf-103">Adiciona um certificado raiz confiável a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d45cf-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="d45cf-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d45cf-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d45cf-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="d45cf-105">DESCRIPTION</span></span>
<span data-ttu-id="d45cf-106">O cmdlet **Add-AzApplicationGatewayTrustedRootCertificate** adiciona um certificado raiz confiável a um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d45cf-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="d45cf-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d45cf-107">EXAMPLES</span></span>

### <span data-ttu-id="d45cf-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d45cf-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="d45cf-109">O primeiro comando obtém o gateway do aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="d45cf-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="d45cf-110">O segundo comando adiciona um novo certificado raiz confiável ao Gateway de Aplicativos, fazendo o caminho do certificado raiz como entrada.</span><span class="sxs-lookup"><span data-stu-id="d45cf-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="d45cf-111">O terceiro comando cria uma nova configuração de back-end http usando um certificado raiz confiável para validar o certificado do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="d45cf-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="d45cf-112">O quarto comando atualiza o Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d45cf-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="d45cf-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d45cf-113">PARAMETERS</span></span>

### <span data-ttu-id="d45cf-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45cf-114">-ApplicationGateway</span></span>
<span data-ttu-id="d45cf-115">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45cf-115">The applicationGateway</span></span>

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

### <span data-ttu-id="d45cf-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d45cf-116">-CertificateFile</span></span>
<span data-ttu-id="d45cf-117">Caminho do arquivo CER de certificado</span><span class="sxs-lookup"><span data-stu-id="d45cf-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="d45cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d45cf-118">-DefaultProfile</span></span>
<span data-ttu-id="d45cf-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d45cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d45cf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d45cf-120">-Name</span></span>
<span data-ttu-id="d45cf-121">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="d45cf-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="d45cf-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d45cf-122">-Confirm</span></span>
<span data-ttu-id="d45cf-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d45cf-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d45cf-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d45cf-124">-WhatIf</span></span>
<span data-ttu-id="d45cf-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d45cf-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d45cf-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d45cf-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d45cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d45cf-127">CommonParameters</span></span>
<span data-ttu-id="d45cf-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d45cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d45cf-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d45cf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d45cf-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="d45cf-130">INPUTS</span></span>

### <span data-ttu-id="d45cf-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45cf-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d45cf-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="d45cf-132">OUTPUTS</span></span>

### <span data-ttu-id="d45cf-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d45cf-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d45cf-134">Notas</span><span class="sxs-lookup"><span data-stu-id="d45cf-134">NOTES</span></span>

## <span data-ttu-id="d45cf-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d45cf-135">RELATED LINKS</span></span>

[<span data-ttu-id="d45cf-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d45cf-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d45cf-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d45cf-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d45cf-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d45cf-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d45cf-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d45cf-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
