---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 3e8c4f6bc25ea5ff9b8efcee989937fb688fea57
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114795"
---
# <span data-ttu-id="d374d-101">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d374d-101">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="d374d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d374d-102">SYNOPSIS</span></span>
<span data-ttu-id="d374d-103">Remove um certificado raiz confiável de um Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d374d-103">Removes a Trusted Root Certificate from an application gateway.</span></span>

## <span data-ttu-id="d374d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d374d-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedRootCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d374d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d374d-105">DESCRIPTION</span></span>
<span data-ttu-id="d374d-106">O cmdlet **Remove-AzApplicationGatewayTrustedRootCertificate** remove um certificado raiz confiável de um Application Gateway existente.</span><span class="sxs-lookup"><span data-stu-id="d374d-106">The **Remove-AzApplicationGatewayTrustedRootCertificate** cmdlet removes a Trusted Root Certificate from an existing Application Gateway.</span></span>

## <span data-ttu-id="d374d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d374d-107">EXAMPLES</span></span>

### <span data-ttu-id="d374d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d374d-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name "myRootCA"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="d374d-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $gw.</span><span class="sxs-lookup"><span data-stu-id="d374d-109">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="d374d-110">O segundo comando Remove o certificado raiz confiável chamado myRootCA do gateway do aplicativo armazenado em $gw.</span><span class="sxs-lookup"><span data-stu-id="d374d-110">The second command removes the trusted root certificate named myRootCA from the application gateway stored in $gw.</span></span>
<span data-ttu-id="d374d-111">O terceiro comando atualiza o Application Gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="d374d-111">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="d374d-112">OS</span><span class="sxs-lookup"><span data-stu-id="d374d-112">PARAMETERS</span></span>

### <span data-ttu-id="d374d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d374d-113">-ApplicationGateway</span></span>
<span data-ttu-id="d374d-114">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="d374d-114">The applicationGateway</span></span>

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

### <span data-ttu-id="d374d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d374d-115">-DefaultProfile</span></span>
<span data-ttu-id="d374d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d374d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d374d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d374d-117">-Name</span></span>
<span data-ttu-id="d374d-118">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="d374d-118">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="d374d-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d374d-119">-Confirm</span></span>
<span data-ttu-id="d374d-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d374d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d374d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d374d-121">-WhatIf</span></span>
<span data-ttu-id="d374d-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d374d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d374d-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d374d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d374d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d374d-124">CommonParameters</span></span>
<span data-ttu-id="d374d-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d374d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d374d-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d374d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d374d-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d374d-127">INPUTS</span></span>

### <span data-ttu-id="d374d-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d374d-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d374d-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d374d-129">OUTPUTS</span></span>

### <span data-ttu-id="d374d-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d374d-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d374d-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d374d-131">NOTES</span></span>

## <span data-ttu-id="d374d-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d374d-132">RELATED LINKS</span></span>

[<span data-ttu-id="d374d-133">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d374d-133">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d374d-134">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d374d-134">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d374d-135">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d374d-135">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="d374d-136">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d374d-136">Set-AzApplicationGatewayTrustedRootCertificate</span></span>](./Set-AzApplicationGatewayTrustedRootCertificate.md)
