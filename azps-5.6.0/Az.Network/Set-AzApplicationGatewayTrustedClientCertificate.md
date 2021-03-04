---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 3c9b9b97e26738234acdf2c8f09c0e1da5eae2e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885404"
---
# <span data-ttu-id="d003f-101">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d003f-101">Set-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="d003f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d003f-102">SYNOPSIS</span></span>
<span data-ttu-id="d003f-103">Modifica a cadeia de certificados ca de cliente confiável de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d003f-103">Modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="d003f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d003f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d003f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d003f-105">DESCRIPTION</span></span>
<span data-ttu-id="d003f-106">O cmdlet **Set-AzApplicationGatewayTrustedClientCertificate** modifica a cadeia de certificados DE cliente confiável de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d003f-106">The **Set-AzApplicationGatewayTrustedClientCertificate** cmdlet modifies the trusted client CA certificate chain of an application gateway.</span></span>

## <span data-ttu-id="d003f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d003f-107">EXAMPLES</span></span>

### <span data-ttu-id="d003f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d003f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\clientCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="d003f-109">Cenários de exemplo acima mostram como atualizar um objeto de cadeia de certificados de CA de cliente confiável existente.</span><span class="sxs-lookup"><span data-stu-id="d003f-109">Above example scenarios shows how to update an existing trusted client CA certificate chain object.</span></span> <span data-ttu-id="d003f-110">O primeiro comando obtém um gateway de aplicativo e o armazena na $gw variável.</span><span class="sxs-lookup"><span data-stu-id="d003f-110">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="d003f-111">O segundo comando modifica o objeto de cadeia de certificados de CA de cliente confiável existente com um novo arquivo de cadeia de certificados da CA.</span><span class="sxs-lookup"><span data-stu-id="d003f-111">The second command modifies the existing trusted client CA certificate chain object with a new CA certificate chain file.</span></span> <span data-ttu-id="d003f-112">O terceiro comando atualiza o gateway de aplicativo no Azure.</span><span class="sxs-lookup"><span data-stu-id="d003f-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="d003f-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d003f-113">PARAMETERS</span></span>

### <span data-ttu-id="d003f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d003f-114">-ApplicationGateway</span></span>
<span data-ttu-id="d003f-115">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d003f-115">The applicationGateway</span></span>

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

### <span data-ttu-id="d003f-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d003f-116">-CertificateFile</span></span>
<span data-ttu-id="d003f-117">Caminho do arquivo de cadeia de certificados de CA do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="d003f-117">Path of the trusted client CA certificate chain file</span></span>

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

### <span data-ttu-id="d003f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d003f-118">-DefaultProfile</span></span>
<span data-ttu-id="d003f-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d003f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d003f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d003f-120">-Name</span></span>
<span data-ttu-id="d003f-121">O nome da cadeia de certificados ca de cliente confiável</span><span class="sxs-lookup"><span data-stu-id="d003f-121">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="d003f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d003f-122">-Confirm</span></span>
<span data-ttu-id="d003f-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d003f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d003f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d003f-124">-WhatIf</span></span>
<span data-ttu-id="d003f-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d003f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d003f-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d003f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d003f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d003f-127">CommonParameters</span></span>
<span data-ttu-id="d003f-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d003f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d003f-129">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d003f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d003f-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d003f-130">INPUTS</span></span>

### <span data-ttu-id="d003f-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d003f-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d003f-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d003f-132">OUTPUTS</span></span>

### <span data-ttu-id="d003f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d003f-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d003f-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="d003f-134">NOTES</span></span>

## <span data-ttu-id="d003f-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d003f-135">RELATED LINKS</span></span>

[<span data-ttu-id="d003f-136">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d003f-136">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="d003f-137">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d003f-137">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="d003f-138">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d003f-138">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="d003f-139">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="d003f-139">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>](./Remove-AzApplicationGatewayTrustedClientCertificate.md)