---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c8db96e9758e04a96f3f7b28c9fda9d8ac73a47e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772110"
---
# <span data-ttu-id="11c7d-101">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="11c7d-101">Add-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="11c7d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="11c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="11c7d-103">Adiciona um certificado raiz confiável a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11c7d-103">Adds a trusted root certificate to an application gateway.</span></span>

## <span data-ttu-id="11c7d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11c7d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c7d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="11c7d-105">DESCRIPTION</span></span>
<span data-ttu-id="11c7d-106">O cmdlet **Add-AzApplicationGatewayTrustedRootCertificate** adiciona um certificado raiz confiável a um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="11c7d-106">The **Add-AzApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="11c7d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="11c7d-107">EXAMPLES</span></span>

### <span data-ttu-id="11c7d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="11c7d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName -CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzApplicationGatewayBackendHttpSettings -ApplicationGateway $gw -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="11c7d-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="11c7d-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="11c7d-110">O segundo comando adiciona um novo certificado raiz confiável ao gateway do aplicativo fazendo o caminho do certificado raiz como entrada.</span><span class="sxs-lookup"><span data-stu-id="11c7d-110">The second command adds a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="11c7d-111">O terceiro comando cria uma nova configuração de http back-end usando o certificado raiz confiável para a validação do certificado do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="11c7d-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="11c7d-112">O quarto comando atualiza o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="11c7d-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="11c7d-113">OS</span><span class="sxs-lookup"><span data-stu-id="11c7d-113">PARAMETERS</span></span>

### <span data-ttu-id="11c7d-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11c7d-114">-ApplicationGateway</span></span>
<span data-ttu-id="11c7d-115">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="11c7d-115">The applicationGateway</span></span>

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

### <span data-ttu-id="11c7d-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="11c7d-116">-CertificateFile</span></span>
<span data-ttu-id="11c7d-117">Caminho do arquivo CER do certificado</span><span class="sxs-lookup"><span data-stu-id="11c7d-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="11c7d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c7d-118">-DefaultProfile</span></span>
<span data-ttu-id="11c7d-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="11c7d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11c7d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="11c7d-120">-Name</span></span>
<span data-ttu-id="11c7d-121">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="11c7d-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="11c7d-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="11c7d-122">-Confirm</span></span>
<span data-ttu-id="11c7d-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11c7d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c7d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c7d-124">-WhatIf</span></span>
<span data-ttu-id="11c7d-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="11c7d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11c7d-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="11c7d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c7d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c7d-127">CommonParameters</span></span>
<span data-ttu-id="11c7d-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11c7d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c7d-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11c7d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c7d-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="11c7d-130">INPUTS</span></span>

### <span data-ttu-id="11c7d-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11c7d-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11c7d-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="11c7d-132">OUTPUTS</span></span>

### <span data-ttu-id="11c7d-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11c7d-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11c7d-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="11c7d-134">NOTES</span></span>

## <span data-ttu-id="11c7d-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="11c7d-135">RELATED LINKS</span></span>

[<span data-ttu-id="11c7d-136">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="11c7d-136">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="11c7d-137">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="11c7d-137">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="11c7d-138">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="11c7d-138">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="11c7d-139">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="11c7d-139">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)