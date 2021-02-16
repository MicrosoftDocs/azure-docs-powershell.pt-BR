---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaytrustedclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayTrustedClientCertificate.md
ms.openlocfilehash: 40f31fc2c8cc4d0cb3a9637b39d8c3fcbd18ee42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113463"
---
# <span data-ttu-id="e3eea-101">Remove-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3eea-101">Remove-AzApplicationGatewayTrustedClientCertificate</span></span>

## <span data-ttu-id="e3eea-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3eea-102">SYNOPSIS</span></span>
<span data-ttu-id="e3eea-103">Remove o objeto de cadeia de certificados da CA de cliente confiável de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e3eea-103">Removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="e3eea-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3eea-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayTrustedClientCertificate -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3eea-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3eea-105">DESCRIPTION</span></span>
<span data-ttu-id="e3eea-106">O cmdlet **Remove-AzApplicationGatewayTrustedClientCertificate** remove o objeto de cadeia de certificados da CA de cliente confiável de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e3eea-106">The **Remove-AzApplicationGatewayTrustedClientCertificate** cmdlet removes the trusted client CA certificate chain object from an application gateway.</span></span>

## <span data-ttu-id="e3eea-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3eea-107">EXAMPLES</span></span>

### <span data-ttu-id="e3eea-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3eea-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Remove-AzApplicationGatewayTrustedClientCertificate -ApplicationGateway $gw -Name "TrustedClientCertificate01"
```

<span data-ttu-id="e3eea-109">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $gw aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e3eea-109">The first command gets an application gateway and stores it in the $gw variable.</span></span> <span data-ttu-id="e3eea-110">O segundo comando remove a cadeia de certificados da CA de cliente confiável chamada "TrustedClientCertificate01" do gateway de aplicativo armazenado no $gw.</span><span class="sxs-lookup"><span data-stu-id="e3eea-110">The second command removes the trusted client CA certificate chain named "TrustedClientCertificate01" from the application gateway stored in $gw.</span></span>

## <span data-ttu-id="e3eea-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3eea-111">PARAMETERS</span></span>

### <span data-ttu-id="e3eea-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3eea-112">-ApplicationGateway</span></span>
<span data-ttu-id="e3eea-113">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3eea-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e3eea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3eea-114">-DefaultProfile</span></span>
<span data-ttu-id="e3eea-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3eea-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3eea-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3eea-116">-Name</span></span>
<span data-ttu-id="e3eea-117">O nome da cadeia de certificados de AC do cliente confiável</span><span class="sxs-lookup"><span data-stu-id="e3eea-117">The name of the trusted client CA certificate chain</span></span>

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

### <span data-ttu-id="e3eea-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e3eea-118">-Confirm</span></span>
<span data-ttu-id="e3eea-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3eea-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3eea-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3eea-120">-WhatIf</span></span>
<span data-ttu-id="e3eea-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e3eea-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3eea-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3eea-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3eea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3eea-123">CommonParameters</span></span>
<span data-ttu-id="e3eea-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3eea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3eea-125">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3eea-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3eea-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="e3eea-126">INPUTS</span></span>

### <span data-ttu-id="e3eea-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3eea-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3eea-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="e3eea-128">OUTPUTS</span></span>

### <span data-ttu-id="e3eea-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e3eea-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e3eea-130">Notas</span><span class="sxs-lookup"><span data-stu-id="e3eea-130">NOTES</span></span>

## <span data-ttu-id="e3eea-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3eea-131">RELATED LINKS</span></span>

[<span data-ttu-id="e3eea-132">New-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3eea-132">New-AzApplicationGatewayTrustedClientCertificate</span></span>](./New-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="e3eea-133">Add-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3eea-133">Add-AzApplicationGatewayTrustedClientCertificate</span></span>](./Add-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="e3eea-134">Get-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3eea-134">Get-AzApplicationGatewayTrustedClientCertificate</span></span>](./Get-AzApplicationGatewayTrustedClientCertificate.md)

[<span data-ttu-id="e3eea-135">Set-AzApplicationGatewayTrustedClientCertificate</span><span class="sxs-lookup"><span data-stu-id="e3eea-135">Set-AzApplicationGatewayTrustedClientCertificate</span></span>](./Set-AzApplicationGatewayTrustedClientCertificate.md)