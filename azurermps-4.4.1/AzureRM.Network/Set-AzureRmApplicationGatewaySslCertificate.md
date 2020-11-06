---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D7C275E5-BC43-454B-BF1E-48D639C4B4F0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySslCertificate.md
ms.openlocfilehash: cec5a6aa0b61889e7923ebce67d1247f99d215e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610208"
---
# <span data-ttu-id="4b107-101">Set-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b107-101">Set-AzureRmApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="4b107-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b107-102">SYNOPSIS</span></span>
<span data-ttu-id="4b107-103">Define o estado da meta de um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="4b107-103">Sets the goal state of an SSL certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b107-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b107-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b107-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b107-105">DESCRIPTION</span></span>
<span data-ttu-id="4b107-106">O cmdlet **set-AzureRmApplicationGatewaySslCertificate** define o estado da meta de um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="4b107-106">The **Set-AzureRmApplicationGatewaySslCertificate** cmdlet sets the goal state of an SSL certificate.</span></span>

## <span data-ttu-id="4b107-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b107-107">EXAMPLES</span></span>

### <span data-ttu-id="4b107-108">Exemplo 1: definir o estado da meta de um certificado SSL</span><span class="sxs-lookup"><span data-stu-id="4b107-108">Example 1: Set the goal state of an SSL certificate</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Cert = Set-AzureRmApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password "Password01"
```

<span data-ttu-id="4b107-109">Esse comando define o estado da meta para um certificado SSL do gateway do aplicativo chamado ApplicationGateway01.</span><span class="sxs-lookup"><span data-stu-id="4b107-109">This command sets the goal state for an SSL certificate from the application gateway named ApplicationGateway01.</span></span>

## <span data-ttu-id="4b107-110">OS</span><span class="sxs-lookup"><span data-stu-id="4b107-110">PARAMETERS</span></span>

### <span data-ttu-id="4b107-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b107-111">-ApplicationGateway</span></span>
<span data-ttu-id="4b107-112">Especifica o gateway do aplicativo com o qual o certificado SSL (Secure Socket Layer) está associado.</span><span class="sxs-lookup"><span data-stu-id="4b107-112">Specifies the application gateway with which the Secure Socket Layer (SSL) certificate is associated.</span></span>

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

### <span data-ttu-id="4b107-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="4b107-113">-CertificateFile</span></span>
<span data-ttu-id="4b107-114">Especifica o caminho do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="4b107-114">Specifies the path of the SSL certificate.</span></span>

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

### <span data-ttu-id="4b107-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b107-115">-Name</span></span>
<span data-ttu-id="4b107-116">Especifica o nome do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="4b107-116">Specifies the name of the SSL certificate.</span></span>

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

### <span data-ttu-id="4b107-117">-Senha</span><span class="sxs-lookup"><span data-stu-id="4b107-117">-Password</span></span>
<span data-ttu-id="4b107-118">Especifica a senha do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="4b107-118">Specifies the password of the SSL certificate.</span></span>

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

### <span data-ttu-id="4b107-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b107-119">-DefaultProfile</span></span>
<span data-ttu-id="4b107-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b107-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b107-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b107-121">CommonParameters</span></span>
<span data-ttu-id="4b107-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b107-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b107-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b107-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b107-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b107-124">INPUTS</span></span>

### <span data-ttu-id="4b107-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4b107-125">System.String</span></span>

## <span data-ttu-id="4b107-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b107-126">OUTPUTS</span></span>

### <span data-ttu-id="4b107-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4b107-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4b107-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b107-128">NOTES</span></span>

## <span data-ttu-id="4b107-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b107-129">RELATED LINKS</span></span>

[<span data-ttu-id="4b107-130">Add-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b107-130">Add-AzureRmApplicationGatewaySslCertificate</span></span>](./Add-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4b107-131">Get-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b107-131">Get-AzureRmApplicationGatewaySslCertificate</span></span>](./Get-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4b107-132">New-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b107-132">New-AzureRmApplicationGatewaySslCertificate</span></span>](./New-AzureRmApplicationGatewaySslCertificate.md)

[<span data-ttu-id="4b107-133">Remove-AzureRmApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="4b107-133">Remove-AzureRmApplicationGatewaySslCertificate</span></span>](./Remove-AzureRmApplicationGatewaySslCertificate.md)


