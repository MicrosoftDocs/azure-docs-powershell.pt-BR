---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D2CE5D4B-8F1F-41FF-9E65-8956FEDD35AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4fad7ae6eab4b71febbd2ffe1f6c9002186ee8d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945664"
---
# <span data-ttu-id="ccfd3-101">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ccfd3-101">Get-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="ccfd3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ccfd3-102">SYNOPSIS</span></span>
<span data-ttu-id="ccfd3-103">Obtém certificados de gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-103">Gets Application Gateway certificates.</span></span>

## <span data-ttu-id="ccfd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ccfd3-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewaySslCertificate -Name <String> [-CertificateName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ccfd3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ccfd3-105">DESCRIPTION</span></span>
<span data-ttu-id="ccfd3-106">O cmdlet **Get-AzureApplicationGatewaySslCertificate** obtém certificados SSL (Secure Sockets Layer) para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-106">The **Get-AzureApplicationGatewaySslCertificate** cmdlet gets Secure Sockets Layer (SSL) certificates for an Azure Application Gateway.</span></span>

## <span data-ttu-id="ccfd3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ccfd3-107">EXAMPLES</span></span>

### <span data-ttu-id="ccfd3-108">Exemplo 1: obter um certificado SSL</span><span class="sxs-lookup"><span data-stu-id="ccfd3-108">Example 1: Get an SSL certificate</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="ccfd3-109">Esse comando obtém um certificado SSL chamado SslCertificate13 no gateway do aplicativo chamado ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-109">This command gets an SSL certificate named SslCertificate13 on the Application Gateway named ApplicationGateway08.</span></span>

### <span data-ttu-id="ccfd3-110">Exemplo 2: obter todos os certificados SSL</span><span class="sxs-lookup"><span data-stu-id="ccfd3-110">Example 2: Get all SSL certificates</span></span>
```
PS C:\> Get-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08"
```

<span data-ttu-id="ccfd3-111">Esse comando obtém todos os certificados SSL no gateway do aplicativo chamado ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-111">This command gets all the SSL certificates on the Application Gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="ccfd3-112">OS</span><span class="sxs-lookup"><span data-stu-id="ccfd3-112">PARAMETERS</span></span>

### <span data-ttu-id="ccfd3-113">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ccfd3-113">-CertificateName</span></span>
<span data-ttu-id="ccfd3-114">Especifica o nome de um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-114">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="ccfd3-115">Esse cmdlet obtém o certificado que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-115">This cmdlet gets the certificate that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccfd3-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccfd3-116">-Name</span></span>
<span data-ttu-id="ccfd3-117">Especifica o nome do aplicativo do gateway do qual esse cmdlet obtém um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-117">Specifies the name of the Application Gateway from which this cmdlet gets an SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccfd3-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ccfd3-118">-Profile</span></span>
<span data-ttu-id="ccfd3-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ccfd3-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccfd3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccfd3-121">CommonParameters</span></span>
<span data-ttu-id="ccfd3-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccfd3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccfd3-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccfd3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccfd3-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ccfd3-124">INPUTS</span></span>

### <span data-ttu-id="ccfd3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ccfd3-125">System.String</span></span>

## <span data-ttu-id="ccfd3-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ccfd3-126">OUTPUTS</span></span>

### <span data-ttu-id="ccfd3-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate, List<Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayCertificate></span><span class="sxs-lookup"><span data-stu-id="ccfd3-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate, List<Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayCertificate></span></span>

## <span data-ttu-id="ccfd3-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ccfd3-128">NOTES</span></span>

## <span data-ttu-id="ccfd3-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ccfd3-129">RELATED LINKS</span></span>

[<span data-ttu-id="ccfd3-130">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ccfd3-130">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="ccfd3-131">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ccfd3-131">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
