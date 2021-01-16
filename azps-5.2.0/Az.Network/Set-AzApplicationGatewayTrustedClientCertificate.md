---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 5f52b68e538072e6ff6aecde99f59337b532130c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258805"
---
# <span data-ttu-id="b9e6a-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9e6a-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="b9e6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e6a-103">Modifica a cadeia de certificados da autoridade de certificação do cliente confiável de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="b9e6a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9e6a-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9e6a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="b9e6a-106">O cmdlet **set-AzApplicationGatewayTrustedClientCertificate** modifica a cadeia de certificados da autoridade de certificação do cliente confiável de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="b9e6a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9e6a-107">EXAMPLES</span></span>

### <span data-ttu-id="b9e6a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9e6a-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="b9e6a-109">Os cenários de exemplo acima mostram como atualizar um objeto de cadeia de certificado de autoridade de certificação de cliente confiável existente.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="b9e6a-110">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $gw.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="b9e6a-111">O segundo comando modifica o objeto de cadeia de certificado de autoridade de certificação de cliente confiável existente com um novo arquivo de cadeia de certificados de autoridade de certificação.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="b9e6a-112">O terceiro comando atualiza o Application Gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="b9e6a-113">OS</span><span class="sxs-lookup"><span data-stu-id="b9e6a-113">PARAMETERS</span></span>

### <span data-ttu-id="b9e6a-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9e6a-114">-ApplicationGateway</span></span>
<span data-ttu-id="b9e6a-115">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9e6a-115">The applicationGateway</span></span>

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

### <span data-ttu-id="b9e6a-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="b9e6a-116">-CertificateFile</span></span>
<span data-ttu-id="b9e6a-117">Caminho do arquivo de cadeia de certificados da autoridade de certificação do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="b9e6a-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="b9e6a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e6a-118">-DefaultProfile</span></span>
<span data-ttu-id="b9e6a-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9e6a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9e6a-120">-Name</span></span>
<span data-ttu-id="b9e6a-121">O nome da cadeia de certificados da autoridade de certificação do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="b9e6a-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="b9e6a-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9e6a-122">-Confirm</span></span>
<span data-ttu-id="b9e6a-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9e6a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9e6a-124">-WhatIf</span></span>
<span data-ttu-id="b9e6a-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9e6a-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9e6a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e6a-127">CommonParameters</span></span>
<span data-ttu-id="b9e6a-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e6a-129">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9e6a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e6a-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9e6a-130">INPUTS</span></span>

### <span data-ttu-id="b9e6a-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9e6a-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9e6a-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9e6a-132">OUTPUTS</span></span>

### <span data-ttu-id="b9e6a-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9e6a-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9e6a-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9e6a-134">NOTES</span></span>

## <span data-ttu-id="b9e6a-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9e6a-135">RELATED LINKS</span></span>

[<span data-ttu-id="b9e6a-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9e6a-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b9e6a-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9e6a-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b9e6a-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9e6a-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="b9e6a-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="b9e6a-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)