---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 29BB24C4-1EC9-47DE-A5B8-5EEA4525AE3A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 00ad021e86617d08f0ca30f660cac28110348885
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785488"
---
# <span data-ttu-id="b1fe5-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1fe5-101">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="b1fe5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1fe5-102">SYNOPSIS</span></span>
<span data-ttu-id="b1fe5-103">Remove um certificado de autenticação de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1fe5-103">Removes an authentication certificate from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1fe5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1fe5-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayAuthenticationCertificate -Name <String>
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1fe5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1fe5-105">DESCRIPTION</span></span>
<span data-ttu-id="b1fe5-106">O cmdlet **Remove-AzureRmApplicationGatewayAuthenticationCertificate** remove um certificado de autenticação de um Application Gateway do Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fe5-106">The **Remove-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet removes an authentication certificate from an Azure application gateway.</span></span>

## <span data-ttu-id="b1fe5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1fe5-107">EXAMPLES</span></span>

### <span data-ttu-id="b1fe5-108">1:</span><span class="sxs-lookup"><span data-stu-id="b1fe5-108">1:</span></span>
```

```

## <span data-ttu-id="b1fe5-109">OS</span><span class="sxs-lookup"><span data-stu-id="b1fe5-109">PARAMETERS</span></span>

### <span data-ttu-id="b1fe5-110">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1fe5-110">-ApplicationGateway</span></span>
<span data-ttu-id="b1fe5-111">Especifica o nome do aplicativo de gateway do qual esse cmdlet Remove um certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b1fe5-111">Specifies the name of application gateway from which this cmdlet removes an authentication certificate.</span></span>

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

### <span data-ttu-id="b1fe5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1fe5-112">-DefaultProfile</span></span>
<span data-ttu-id="b1fe5-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1fe5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fe5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1fe5-114">-Name</span></span>
<span data-ttu-id="b1fe5-115">Especifica o nome do certificado de autenticação que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="b1fe5-115">Specifies the name of the authentication certificate that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b1fe5-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b1fe5-116">-Confirm</span></span>
<span data-ttu-id="b1fe5-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1fe5-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fe5-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1fe5-118">-WhatIf</span></span>
<span data-ttu-id="b1fe5-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b1fe5-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1fe5-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b1fe5-120">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1fe5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1fe5-121">CommonParameters</span></span>
<span data-ttu-id="b1fe5-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1fe5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1fe5-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1fe5-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1fe5-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1fe5-124">INPUTS</span></span>

### <span data-ttu-id="b1fe5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="b1fe5-125">System.String</span></span>

## <span data-ttu-id="b1fe5-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1fe5-126">OUTPUTS</span></span>

### <span data-ttu-id="b1fe5-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b1fe5-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b1fe5-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1fe5-128">NOTES</span></span>
* <span data-ttu-id="b1fe5-129">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="b1fe5-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b1fe5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1fe5-130">RELATED LINKS</span></span>

[<span data-ttu-id="b1fe5-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1fe5-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b1fe5-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1fe5-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b1fe5-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1fe5-133">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="b1fe5-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="b1fe5-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


