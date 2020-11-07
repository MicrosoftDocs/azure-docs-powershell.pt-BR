---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 98AC0FAA-4786-4172-908E-FEB8588B0D74
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da9e9af2e96ee177a91dae7b7ccd12f7e588517
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946494"
---
# <span data-ttu-id="d8a2a-101">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d8a2a-101">Remove-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="d8a2a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d8a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="d8a2a-103">Remove um certificado SSL de um aplicativo gateway.</span><span class="sxs-lookup"><span data-stu-id="d8a2a-103">Removes an SSL certificate from an application gateway.</span></span>

## <span data-ttu-id="d8a2a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d8a2a-104">SYNTAX</span></span>

```
Remove-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d8a2a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d8a2a-105">DESCRIPTION</span></span>
<span data-ttu-id="d8a2a-106">O cmdlet **Remove-AzureApplicationGatewaySslCertificate** remove um certificado Secure Sockets Layer (SSL) de um Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d8a2a-106">The **Remove-AzureApplicationGatewaySslCertificate** cmdlet removes a Secure Sockets Layer (SSL) certificate from an application gateway.</span></span>

## <span data-ttu-id="d8a2a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8a2a-107">EXAMPLES</span></span>

### <span data-ttu-id="d8a2a-108">Exemplo 1: remover um certificado SSL</span><span class="sxs-lookup"><span data-stu-id="d8a2a-108">Example 1: Remove an SSL certificate</span></span>
```
PS C:\> Remove-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13"
```

<span data-ttu-id="d8a2a-109">Esse comando Remove um certificado SSL chamado SslCertificate13 do gateway do aplicativo chamado ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="d8a2a-109">This command removes an SSL certificate named SslCertificate13 from the application gateway named ApplicationGateway08.</span></span>

## <span data-ttu-id="d8a2a-110">OS</span><span class="sxs-lookup"><span data-stu-id="d8a2a-110">PARAMETERS</span></span>

### <span data-ttu-id="d8a2a-111">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d8a2a-111">-CertificateName</span></span>
<span data-ttu-id="d8a2a-112">Especifica o nome de um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="d8a2a-112">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="d8a2a-113">Esse cmdlet Remove o certificado que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="d8a2a-113">This cmdlet removes the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="d8a2a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8a2a-114">-Name</span></span>
<span data-ttu-id="d8a2a-115">Especifica o nome do aplicativo do gateway do qual esse cmdlet Remove um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="d8a2a-115">Specifies the name of the application gateway from which this cmdlet removes an SSL certificate.</span></span>

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

### <span data-ttu-id="d8a2a-116">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d8a2a-116">-Profile</span></span>
<span data-ttu-id="d8a2a-117">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d8a2a-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d8a2a-118">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d8a2a-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d8a2a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8a2a-119">CommonParameters</span></span>
<span data-ttu-id="d8a2a-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8a2a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8a2a-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8a2a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8a2a-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d8a2a-122">INPUTS</span></span>

### <span data-ttu-id="d8a2a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d8a2a-123">System.String</span></span>

## <span data-ttu-id="d8a2a-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d8a2a-124">OUTPUTS</span></span>

### <span data-ttu-id="d8a2a-125">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d8a2a-125">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="d8a2a-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d8a2a-126">NOTES</span></span>

## <span data-ttu-id="d8a2a-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8a2a-127">RELATED LINKS</span></span>

[<span data-ttu-id="d8a2a-128">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d8a2a-128">Add-AzureApplicationGatewaySslCertificate</span></span>](./Add-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d8a2a-129">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d8a2a-129">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)
