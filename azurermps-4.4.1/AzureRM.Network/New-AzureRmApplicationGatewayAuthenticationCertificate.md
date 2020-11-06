---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 51bb8ff46613080d3fa62a2b4953419348cb99bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432179"
---
# <span data-ttu-id="14565-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14565-101">New-AzureRmApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="14565-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14565-102">SYNOPSIS</span></span>
<span data-ttu-id="14565-103">Cria um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="14565-103">Creates an authentication certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14565-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14565-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14565-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14565-105">DESCRIPTION</span></span>
<span data-ttu-id="14565-106">O cmdlet **New-AzureRmApplicationGatewayAuthenticationCertificate** cria um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="14565-106">The **New-AzureRmApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="14565-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14565-107">EXAMPLES</span></span>

## <span data-ttu-id="14565-108">OS</span><span class="sxs-lookup"><span data-stu-id="14565-108">PARAMETERS</span></span>

### <span data-ttu-id="14565-109">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="14565-109">-CertificateFile</span></span>
<span data-ttu-id="14565-110">Especifica o caminho do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="14565-110">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="14565-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="14565-111">-Name</span></span>
<span data-ttu-id="14565-112">Especifica um nome para o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="14565-112">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="14565-113">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14565-113">-Confirm</span></span>
<span data-ttu-id="14565-114">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14565-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14565-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14565-115">-WhatIf</span></span>
<span data-ttu-id="14565-116">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14565-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14565-117">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14565-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14565-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14565-118">-DefaultProfile</span></span>
<span data-ttu-id="14565-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14565-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14565-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14565-120">CommonParameters</span></span>
<span data-ttu-id="14565-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14565-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14565-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14565-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14565-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14565-123">INPUTS</span></span>

### <span data-ttu-id="14565-124">System. String</span><span class="sxs-lookup"><span data-stu-id="14565-124">System.String</span></span>

## <span data-ttu-id="14565-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14565-125">OUTPUTS</span></span>

### <span data-ttu-id="14565-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14565-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="14565-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14565-127">NOTES</span></span>
* <span data-ttu-id="14565-128">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="14565-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="14565-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14565-129">RELATED LINKS</span></span>

[<span data-ttu-id="14565-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14565-130">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="14565-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14565-131">Get-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="14565-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14565-132">Remove-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="14565-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="14565-133">Set-AzureRmApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


