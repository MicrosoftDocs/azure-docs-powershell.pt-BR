---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayauthenticationcertificate
schema: 2.0.0
ms.openlocfilehash: 3847c1026f8cea6f3c33db45215a7a3253e4c680
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785689"
---
# <span data-ttu-id="145ca-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="145ca-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="145ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="145ca-102">SYNOPSIS</span></span>
<span data-ttu-id="145ca-103">Cria um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="145ca-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="145ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="145ca-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="145ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="145ca-105">DESCRIPTION</span></span>
<span data-ttu-id="145ca-106">O cmdlet **New-AzureRmApplicationGatewayAuthenticationCertificate** cria um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="145ca-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="145ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="145ca-107">EXAMPLES</span></span>

### <span data-ttu-id="145ca-108">1:</span><span class="sxs-lookup"><span data-stu-id="145ca-108">1:</span></span>
```

```

## <span data-ttu-id="145ca-109">OS</span><span class="sxs-lookup"><span data-stu-id="145ca-109">PARAMETERS</span></span>

### <span data-ttu-id="145ca-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="145ca-110">-CertificateFile</span></span>
<span data-ttu-id="145ca-111">Especifica o caminho do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="145ca-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="145ca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145ca-112">-DefaultProfile</span></span>
<span data-ttu-id="145ca-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="145ca-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="145ca-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="145ca-114">-Name</span></span>
<span data-ttu-id="145ca-115">Especifica um nome para o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="145ca-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="145ca-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="145ca-116">-Confirm</span></span>
<span data-ttu-id="145ca-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="145ca-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="145ca-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145ca-118">-WhatIf</span></span>
<span data-ttu-id="145ca-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="145ca-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="145ca-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="145ca-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="145ca-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145ca-121">CommonParameters</span></span>
<span data-ttu-id="145ca-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="145ca-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145ca-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="145ca-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145ca-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="145ca-124">INPUTS</span></span>

### <span data-ttu-id="145ca-125">System. String</span><span class="sxs-lookup"><span data-stu-id="145ca-125">System.String</span></span>

## <span data-ttu-id="145ca-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="145ca-126">OUTPUTS</span></span>

### <span data-ttu-id="145ca-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="145ca-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="145ca-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="145ca-128">NOTES</span></span>
* <span data-ttu-id="145ca-129">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="145ca-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="145ca-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="145ca-130">RELATED LINKS</span></span>

[<span data-ttu-id="145ca-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="145ca-131">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="145ca-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="145ca-132">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="145ca-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="145ca-133">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="145ca-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="145ca-134">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


