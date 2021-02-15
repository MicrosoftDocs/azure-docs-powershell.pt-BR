---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: e3a92085c15116527e1b6c14d5403f68748f4f90
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111705"
---
# <span data-ttu-id="41fac-101">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41fac-101">Add-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="41fac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41fac-102">SYNOPSIS</span></span>
<span data-ttu-id="41fac-103">Adiciona uma cadeia de certificados de AC de cliente confiável a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="41fac-103">Adds a trusted client CA certificate chain to an application gateway.</span></span>

## <span data-ttu-id="41fac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41fac-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41fac-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="41fac-105">DESCRIPTION</span></span>
<span data-ttu-id="41fac-106">O cmdlet **Add-AzApplicationGatewayTrustedClientCertificate** adiciona uma cadeia de certificados de CA de cliente confiável a um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="41fac-106">The **Add-AzApplicationGatewayTrustedClientCertificate** cmdlet adds a trusted client CA certificate chain to an Azure application gateway.</span></span>

## <span data-ttu-id="41fac-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="41fac-107">EXAMPLES</span></span>

### <span data-ttu-id="41fac-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41fac-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedClient = New-AzApplicationGatewayTrustedClientCertificate -Name "ClientCert" -CertificateFile "C:\clientCAChain.cer"
PS C:\> $AppGw = Add-AzApplicationGatewaySslProfile -Name $sslProfileName -ApplicationGateway $gw -TrustedClientCertificates $trustedClient
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="41fac-109">O primeiro comando obtém o gateway do aplicativo e o armazena $gw variável.</span><span class="sxs-lookup"><span data-stu-id="41fac-109">The first command gets the application gateway and stores it in $gw variable.</span></span> <span data-ttu-id="41fac-110">O segundo comando cria um novo caminho de certificação de CA de cliente confiável no caminho do certificado ca do cliente como entrada.</span><span class="sxs-lookup"><span data-stu-id="41fac-110">The second command creates a new trusted client CA certificate chain taking path of the client CA certificate as input.</span></span> <span data-ttu-id="41fac-111">O terceiro comando cria um perfil SSL usando certificado de cliente confiável.</span><span class="sxs-lookup"><span data-stu-id="41fac-111">The third command creates a SSL profile using trusted client certificate.</span></span> <span data-ttu-id="41fac-112">O quarto comando atualiza o Gateway de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="41fac-112">The fourth command updates the Application Gateway.</span></span>

## <span data-ttu-id="41fac-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41fac-113">PARAMETERS</span></span>

### <span data-ttu-id="41fac-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41fac-114">-ApplicationGateway</span></span>
<span data-ttu-id="41fac-115">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="41fac-115">The applicationGateway</span></span>

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

### <span data-ttu-id="41fac-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="41fac-116">-CertificateFile</span></span>
<span data-ttu-id="41fac-117">Caminho do arquivo de cadeia de certificados da CA do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="41fac-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="41fac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fac-118">-DefaultProfile</span></span>
<span data-ttu-id="41fac-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41fac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41fac-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="41fac-120">-Name</span></span>
<span data-ttu-id="41fac-121">O nome da cadeia de certificados de AC do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="41fac-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="41fac-122">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="41fac-122">-Confirm</span></span>
<span data-ttu-id="41fac-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41fac-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41fac-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41fac-124">-WhatIf</span></span>
<span data-ttu-id="41fac-125">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="41fac-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41fac-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41fac-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41fac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fac-127">CommonParameters</span></span>
<span data-ttu-id="41fac-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41fac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fac-129">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41fac-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fac-130">Entradas</span><span class="sxs-lookup"><span data-stu-id="41fac-130">INPUTS</span></span>

### <span data-ttu-id="41fac-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41fac-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="41fac-132">Saídas</span><span class="sxs-lookup"><span data-stu-id="41fac-132">OUTPUTS</span></span>

### <span data-ttu-id="41fac-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="41fac-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="41fac-134">Notas</span><span class="sxs-lookup"><span data-stu-id="41fac-134">NOTES</span></span>

## <span data-ttu-id="41fac-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41fac-135">RELATED LINKS</span></span>

[<span data-ttu-id="41fac-136">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41fac-136">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="41fac-137">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41fac-137">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="41fac-138">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41fac-138">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="41fac-139">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="41fac-139">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)