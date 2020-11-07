---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4736FA0D-222D-4D69-BCBD-72036303A20E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayauthenticationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 8f3685fddf4796cd0ad500c261f157e8ac5b95f5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775446"
---
# <span data-ttu-id="34564-101">New-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34564-101">New-AzApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="34564-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34564-102">SYNOPSIS</span></span>
<span data-ttu-id="34564-103">Cria um certificado de autenticação para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="34564-103">Creates an authentication certificate for an application gateway.</span></span>

## <span data-ttu-id="34564-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34564-104">SYNTAX</span></span>

```
New-AzApplicationGatewayAuthenticationCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34564-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34564-105">DESCRIPTION</span></span>
<span data-ttu-id="34564-106">O cmdlet **New-AzApplicationGatewayAuthenticationCertificate** cria um certificado de autenticação para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="34564-106">The **New-AzApplicationGatewayAuthenticationCertificate** cmdlet creates an authentication certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="34564-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34564-107">EXAMPLES</span></span>

### <span data-ttu-id="34564-108">1:</span><span class="sxs-lookup"><span data-stu-id="34564-108">1:</span></span>
```

```

## <span data-ttu-id="34564-109">OS</span><span class="sxs-lookup"><span data-stu-id="34564-109">PARAMETERS</span></span>

### <span data-ttu-id="34564-110">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="34564-110">-CertificateFile</span></span>
<span data-ttu-id="34564-111">Especifica o caminho do certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="34564-111">Specifies the path of the authentication certificate.</span></span>

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

### <span data-ttu-id="34564-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34564-112">-DefaultProfile</span></span>
<span data-ttu-id="34564-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="34564-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34564-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="34564-114">-Name</span></span>
<span data-ttu-id="34564-115">Especifica um nome para o certificado de autenticação.</span><span class="sxs-lookup"><span data-stu-id="34564-115">Specifies a name for the authentication certificate.</span></span>

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

### <span data-ttu-id="34564-116">-Confirme</span><span class="sxs-lookup"><span data-stu-id="34564-116">-Confirm</span></span>
<span data-ttu-id="34564-117">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34564-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34564-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34564-118">-WhatIf</span></span>
<span data-ttu-id="34564-119">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="34564-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34564-120">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="34564-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34564-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34564-121">CommonParameters</span></span>
<span data-ttu-id="34564-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34564-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34564-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34564-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34564-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34564-124">INPUTS</span></span>

### <span data-ttu-id="34564-125">System. String</span><span class="sxs-lookup"><span data-stu-id="34564-125">System.String</span></span>

## <span data-ttu-id="34564-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34564-126">OUTPUTS</span></span>

### <span data-ttu-id="34564-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34564-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate</span></span>

## <span data-ttu-id="34564-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34564-128">NOTES</span></span>
* <span data-ttu-id="34564-129">Palavras-chave: Azure, azurerm, ARM, recurso, gerenciamento, gerente, rede, rede</span><span class="sxs-lookup"><span data-stu-id="34564-129">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="34564-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34564-130">RELATED LINKS</span></span>

[<span data-ttu-id="34564-131">Add-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34564-131">Add-AzApplicationGatewayAuthenticationCertificate</span></span>](./Add-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="34564-132">Get-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34564-132">Get-AzApplicationGatewayAuthenticationCertificate</span></span>](./Get-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="34564-133">Remove-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34564-133">Remove-AzApplicationGatewayAuthenticationCertificate</span></span>](./Remove-AzApplicationGatewayAuthenticationCertificate.md)

[<span data-ttu-id="34564-134">Set-AzApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="34564-134">Set-AzApplicationGatewayAuthenticationCertificate</span></span>](./Set-AzApplicationGatewayAuthenticationCertificate.md)


