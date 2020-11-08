---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 746bbc2ec606bff74a49130e356bd531a3f63f8c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115945"
---
# <span data-ttu-id="10d87-101">Set-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="10d87-101">Set-AzApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="10d87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="10d87-102">SYNOPSIS</span></span>
<span data-ttu-id="10d87-103">Atualiza um certificado raiz confiável de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="10d87-103">Updates a Trusted Root Certificate of an application gateway.</span></span>

## <span data-ttu-id="10d87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10d87-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10d87-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="10d87-105">DESCRIPTION</span></span>
<span data-ttu-id="10d87-106">O cmdlet **set-AzApplicationGatewayTrustedRootCertificate** modifica o certificado raiz confiável existente de um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="10d87-106">The **Set-AzApplicationGatewayTrustedRootCertificate** cmdlet modifies the existing trusted root certificate of an Application Gateway.</span></span>

## <span data-ttu-id="10d87-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="10d87-107">EXAMPLES</span></span>

### <span data-ttu-id="10d87-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="10d87-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $gw = Set-AzApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCAUpdated.cer"
PS C:\> $gw = Set-AzApplicationGateway -ApplicationGateway $gw
```

<span data-ttu-id="10d87-109">Os cenários de exemplo acima mostram como atualizar um certificado raiz confiável existente quando um certificado raiz é revertido.</span><span class="sxs-lookup"><span data-stu-id="10d87-109">Above example scenarios shows how to update an existing trusted root certificate when a root certificate is rolled.</span></span>
<span data-ttu-id="10d87-110">O primeiro comando obtém um gateway de aplicativo e o armazena na variável $gw.</span><span class="sxs-lookup"><span data-stu-id="10d87-110">The first command gets an application gateway and stores it in the $gw variable.</span></span>
<span data-ttu-id="10d87-111">O segundo comando modifica o certificado raiz confiável existente com um novo certificado raiz.</span><span class="sxs-lookup"><span data-stu-id="10d87-111">The second command modifies the existing trusted root certificate with a new root certificate.</span></span>
<span data-ttu-id="10d87-112">O terceiro comando atualiza o Application Gateway no Azure.</span><span class="sxs-lookup"><span data-stu-id="10d87-112">The third command updates the application gateway on Azure.</span></span>

## <span data-ttu-id="10d87-113">OS</span><span class="sxs-lookup"><span data-stu-id="10d87-113">PARAMETERS</span></span>

### <span data-ttu-id="10d87-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10d87-114">-ApplicationGateway</span></span>
<span data-ttu-id="10d87-115">O applicationGateway</span><span class="sxs-lookup"><span data-stu-id="10d87-115">The applicationGateway</span></span>

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

### <span data-ttu-id="10d87-116">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="10d87-116">-CertificateFile</span></span>
<span data-ttu-id="10d87-117">Caminho do arquivo CER do certificado</span><span class="sxs-lookup"><span data-stu-id="10d87-117">Path of certificate CER file</span></span>

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

### <span data-ttu-id="10d87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d87-118">-DefaultProfile</span></span>
<span data-ttu-id="10d87-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="10d87-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10d87-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="10d87-120">-Name</span></span>
<span data-ttu-id="10d87-121">O nome do certificado TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="10d87-121">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="10d87-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="10d87-122">-Confirm</span></span>
<span data-ttu-id="10d87-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10d87-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10d87-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10d87-124">-WhatIf</span></span>
<span data-ttu-id="10d87-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="10d87-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10d87-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="10d87-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10d87-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d87-127">CommonParameters</span></span>
<span data-ttu-id="10d87-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10d87-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d87-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d87-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d87-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="10d87-130">INPUTS</span></span>

### <span data-ttu-id="10d87-131">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10d87-131">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="10d87-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="10d87-132">OUTPUTS</span></span>

### <span data-ttu-id="10d87-133">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10d87-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="10d87-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="10d87-134">NOTES</span></span>

## <span data-ttu-id="10d87-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="10d87-135">RELATED LINKS</span></span>

[<span data-ttu-id="10d87-136">Add-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="10d87-136">Add-AzApplicationGatewayTrustedRootCertificate</span></span>](./Add-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="10d87-137">Get-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="10d87-137">Get-AzApplicationGatewayTrustedRootCertificate</span></span>](./Get-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="10d87-138">New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="10d87-138">New-AzApplicationGatewayTrustedRootCertificate</span></span>](./New-AzApplicationGatewayTrustedRootCertificate.md)

[<span data-ttu-id="10d87-139">Remove-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="10d87-139">Remove-AzApplicationGatewayTrustedRootCertificate</span></span>](./Remove-AzApplicationGatewayTrustedRootCertificate.md)
