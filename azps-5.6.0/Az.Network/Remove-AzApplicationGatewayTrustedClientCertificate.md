---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: c7fdf250ad7c322e47c26e023f04689a12a8eee5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888470"
---
# <span data-ttu-id="c1bf2-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c1bf2-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="c1bf2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="c1bf2-103">Remove o objeto de cadeia de certificados ca do cliente confiável de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1bf2-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="c1bf2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c1bf2-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1bf2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c1bf2-105">DESCRIPTION</span></span>
<span data-ttu-id="c1bf2-106">O cmdlet **Remove-AzApplicationGatewayTrustedClientCertificate** remove o objeto de cadeia de certificados de CA do cliente confiável de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c1bf2-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="c1bf2-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c1bf2-107">EXAMPLES</span></span>

### <span data-ttu-id="c1bf2-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c1bf2-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="c1bf2-109">O primeiro comando obtém um gateway de aplicativo e o armazena na $gw variável.</span><span class="sxs-lookup"><span data-stu-id="c1bf2-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="c1bf2-110">O segundo comando remove a cadeia de certificados de AC de cliente confiável chamada "TrustedClientCertificate01" do gateway de aplicativo armazenado em $gw.</span><span class="sxs-lookup"><span data-stu-id="c1bf2-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="c1bf2-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c1bf2-111">PARAMETERS</span></span>

### <span data-ttu-id="c1bf2-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1bf2-112">-ApplicationGateway</span></span>
<span data-ttu-id="c1bf2-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1bf2-113">The applicationGateway</span></span>

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

### <span data-ttu-id="c1bf2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1bf2-114">-DefaultProfile</span></span>
<span data-ttu-id="c1bf2-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c1bf2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1bf2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c1bf2-116">-Name</span></span>
<span data-ttu-id="c1bf2-117">O nome da cadeia de certificados ca de cliente confiável</span><span class="sxs-lookup"><span data-stu-id="c1bf2-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="c1bf2-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1bf2-118">-Confirm</span></span>
<span data-ttu-id="c1bf2-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1bf2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1bf2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1bf2-120">-WhatIf</span></span>
<span data-ttu-id="c1bf2-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c1bf2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1bf2-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c1bf2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1bf2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1bf2-123">CommonParameters</span></span>
<span data-ttu-id="c1bf2-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1bf2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1bf2-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1bf2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1bf2-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c1bf2-126">INPUTS</span></span>

### <span data-ttu-id="c1bf2-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1bf2-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1bf2-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c1bf2-128">OUTPUTS</span></span>

### <span data-ttu-id="c1bf2-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c1bf2-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c1bf2-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="c1bf2-130">NOTES</span></span>

## <span data-ttu-id="c1bf2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c1bf2-131">RELATED LINKS</span></span>

[<span data-ttu-id="c1bf2-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c1bf2-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="c1bf2-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c1bf2-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="c1bf2-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c1bf2-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="c1bf2-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="c1bf2-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)