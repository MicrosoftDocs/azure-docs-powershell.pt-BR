---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433448"
---
# <span data-ttu-id="76628-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="76628-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="76628-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76628-102">SYNOPSIS</span></span>
<span data-ttu-id="76628-103">Remove o objeto de cadeia de certificados da autoridade de certificação do cliente confiável de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="76628-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="76628-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="76628-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76628-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="76628-105">DESCRIPTION</span></span>
<span data-ttu-id="76628-106">O cmdlet **Remove-AzApplicationGatewayTrustedClientCertificate** remove o objeto de cadeia de certificado de autoridade de certificação de cliente confiável de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="76628-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="76628-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="76628-107">EXAMPLES</span></span>

### <span data-ttu-id="76628-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="76628-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="76628-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $gw.</span><span class="sxs-lookup"><span data-stu-id="76628-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="76628-110">O segundo comando Remove a cadeia de certificados da CA do cliente confiável chamada "TrustedClientCertificate01" do gateway do aplicativo armazenado em $gw.</span><span class="sxs-lookup"><span data-stu-id="76628-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="76628-111">OS</span><span class="sxs-lookup"><span data-stu-id="76628-111">PARAMETERS</span></span>

### <span data-ttu-id="76628-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76628-112">-ApplicationGateway</span></span>
<span data-ttu-id="76628-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="76628-113">The applicationGateway</span></span>

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

### <span data-ttu-id="76628-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76628-114">-DefaultProfile</span></span>
<span data-ttu-id="76628-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76628-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76628-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="76628-116">-Name</span></span>
<span data-ttu-id="76628-117">O nome da cadeia de certificados da autoridade de certificação do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="76628-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="76628-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="76628-118">-Confirm</span></span>
<span data-ttu-id="76628-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76628-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76628-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76628-120">-WhatIf</span></span>
<span data-ttu-id="76628-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="76628-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76628-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76628-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76628-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76628-123">CommonParameters</span></span>
<span data-ttu-id="76628-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76628-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76628-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76628-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76628-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="76628-126">INPUTS</span></span>

### <span data-ttu-id="76628-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76628-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="76628-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="76628-128">OUTPUTS</span></span>

### <span data-ttu-id="76628-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="76628-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="76628-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="76628-130">NOTES</span></span>

## <span data-ttu-id="76628-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76628-131">RELATED LINKS</span></span>

[<span data-ttu-id="76628-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="76628-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="76628-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="76628-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="76628-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="76628-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="76628-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="76628-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)