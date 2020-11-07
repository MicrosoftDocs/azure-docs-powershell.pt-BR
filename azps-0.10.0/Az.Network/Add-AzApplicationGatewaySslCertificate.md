---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 964e99912e4f21d48e89b725da1aa44ac32ea186
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775648"
---
# <span data-ttu-id="e668e-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e668e-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="e668e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e668e-102">SYNOPSIS</span></span>
<span data-ttu-id="e668e-103">Adiciona um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e668e-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="e668e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e668e-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 -CertificateFile <String> -Password <SecureString> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e668e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e668e-105">DESCRIPTION</span></span>
<span data-ttu-id="e668e-106">O cmdlet **Add-AzApplicationGatewaySslCertificate** adiciona um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e668e-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="e668e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e668e-107">EXAMPLES</span></span>

### <span data-ttu-id="e668e-108">Exemplo 1: adicionar um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e668e-108">Example 1: Add an SSL certificate to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="e668e-109">Esse comando obtém um gateway do aplicativo chamado ApplicationGateway01 e, em seguida, adiciona um certificado SSL chamado Cert01 a ele.</span><span class="sxs-lookup"><span data-stu-id="e668e-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

## <span data-ttu-id="e668e-110">OS</span><span class="sxs-lookup"><span data-stu-id="e668e-110">PARAMETERS</span></span>

### <span data-ttu-id="e668e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e668e-111">-ApplicationGateway</span></span>
<span data-ttu-id="e668e-112">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="e668e-112">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="e668e-113">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="e668e-113">-CertificateFile</span></span>
<span data-ttu-id="e668e-114">Especifica o arquivo. pfx de um certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="e668e-114">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e668e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e668e-115">-DefaultProfile</span></span>
<span data-ttu-id="e668e-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e668e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e668e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e668e-117">-Name</span></span>
<span data-ttu-id="e668e-118">Especifica o nome do certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="e668e-118">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="e668e-119">-Senha</span><span class="sxs-lookup"><span data-stu-id="e668e-119">-Password</span></span>
<span data-ttu-id="e668e-120">Especifica a senha do certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="e668e-120">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e668e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e668e-121">CommonParameters</span></span>
<span data-ttu-id="e668e-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e668e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e668e-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e668e-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e668e-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e668e-124">INPUTS</span></span>

### <span data-ttu-id="e668e-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e668e-125">System.String</span></span>

## <span data-ttu-id="e668e-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e668e-126">OUTPUTS</span></span>

### <span data-ttu-id="e668e-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e668e-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e668e-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e668e-128">NOTES</span></span>

## <span data-ttu-id="e668e-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e668e-129">RELATED LINKS</span></span>

[<span data-ttu-id="e668e-130">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e668e-130">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e668e-131">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e668e-131">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e668e-132">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e668e-132">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="e668e-133">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="e668e-133">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


