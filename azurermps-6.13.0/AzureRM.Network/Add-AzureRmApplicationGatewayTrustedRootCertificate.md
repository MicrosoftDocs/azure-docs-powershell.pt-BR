---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: e44136d5fa9b0a6b0b979005c13faf6041d98f61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433219"
---
# <span data-ttu-id="2fceb-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2fceb-101">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="2fceb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2fceb-102">SYNOPSIS</span></span>
<span data-ttu-id="2fceb-103">Adiciona um certificado raiz confiável a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2fceb-103">Adds a trusted root certificate to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fceb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fceb-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fceb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2fceb-105">DESCRIPTION</span></span>
<span data-ttu-id="2fceb-106">O cmdlet **Add-AzureRmApplicationGatewayTrustedRootCertificate** adiciona um certificado raiz confiável a um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="2fceb-106">The **Add-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet adds a trusted root certificate to an Azure application gateway.</span></span>

## <span data-ttu-id="2fceb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fceb-107">EXAMPLES</span></span>

### <span data-ttu-id="2fceb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2fceb-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Add-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
PS C:\> $gw = Add-AzureRmApplicationGatewayBackendHttpSetting -Name $poolSetting01Name -Port 443 -Protocol Https -CookieBasedAffinity Enabled -PickHostNameFromBackendAddress -TrustedRootCertificate $gw.TrustedRootCertificates[0]
PS C:\> $gw = Set-AzureRmApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="2fceb-109">O primeiro comando obtém o gateway do aplicativo e o armazena em $gw variável.</span><span class="sxs-lookup"><span data-stu-id="2fceb-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="2fceb-110">O segundo comando Addes um novo certificado raiz confiável ao gateway do aplicativo que está fazendo o caminho do certificado raiz como entrada.</span><span class="sxs-lookup"><span data-stu-id="2fceb-110">The second command addes a new trusted root certificate to Application Gateway taking path of the root certificate as input.</span></span>
<span data-ttu-id="2fceb-111">O terceiro comando cria uma nova configuração de http back-end usando o certificado raiz confiável para a validação do certificado do servidor back-end.</span><span class="sxs-lookup"><span data-stu-id="2fceb-111">The third command creates new backend http setting using trusted root certificate for validating the backend server certificate against.</span></span>
<span data-ttu-id="2fceb-112">O comando Fouth atualiza o Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="2fceb-112">The fouth command updates the Application Gateway.</span></span>

## <span data-ttu-id="2fceb-113">OS</span><span class="sxs-lookup"><span data-stu-id="2fceb-113">PARAMETERS</span></span>

### <span data-ttu-id="2fceb-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fceb-114">-ApplicationGateway</span></span>
<span data-ttu-id="2fceb-115">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fceb-115">The applicationGateway</span></span>

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

### <span data-ttu-id="2fceb-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="2fceb-116">-CertificateFile</span></span>
<span data-ttu-id="2fceb-117">Caminho do arquivo CER do certificado</span><span class="sxs-lookup"><span data-stu-id="2fceb-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="2fceb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fceb-118">-DefaultProfile</span></span>
<span data-ttu-id="2fceb-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2fceb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fceb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fceb-120">-Name</span></span>
<span data-ttu-id="2fceb-121">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="2fceb-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="2fceb-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2fceb-122">-Confirm</span></span>
<span data-ttu-id="2fceb-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fceb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fceb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fceb-124">-WhatIf</span></span>
<span data-ttu-id="2fceb-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2fceb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fceb-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2fceb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fceb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fceb-127">CommonParameters</span></span>
<span data-ttu-id="2fceb-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fceb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fceb-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fceb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fceb-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2fceb-130">INPUTS</span></span>

### <span data-ttu-id="2fceb-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fceb-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fceb-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2fceb-132">OUTPUTS</span></span>

### <span data-ttu-id="2fceb-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2fceb-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2fceb-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2fceb-134">NOTES</span></span>

## <span data-ttu-id="2fceb-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fceb-135">RELATED LINKS</span></span>
