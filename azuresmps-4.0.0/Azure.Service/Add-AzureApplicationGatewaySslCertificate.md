---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: BA63476C-25CC-444D-AD2C-51BF76374FBC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76ac1f2d1ba5c64fb12bc10320efff8c34538ab8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945736"
---
# <span data-ttu-id="9adab-101">Add-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9adab-101">Add-AzureApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="9adab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9adab-102">SYNOPSIS</span></span>
<span data-ttu-id="9adab-103">Adiciona um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9adab-103">Adds an SSL certificate to an Application Gateway.</span></span>

## <span data-ttu-id="9adab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9adab-104">SYNTAX</span></span>

```
Add-AzureApplicationGatewaySslCertificate -Name <String> -CertificateName <String> -Password <String>
 -CertificateFile <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9adab-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9adab-105">DESCRIPTION</span></span>
<span data-ttu-id="9adab-106">O cmdlet **Add-AzureApplicationGatewaySslCertificate** adiciona um certificado SSL (Secure Sockets Layer) a um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9adab-106">The **Add-AzureApplicationGatewaySslCertificate** cmdlet adds a Secure Sockets Layer (SSL) certificate to an Azure Application Gateway.</span></span>

## <span data-ttu-id="9adab-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9adab-107">EXAMPLES</span></span>

### <span data-ttu-id="9adab-108">Exemplo 1: adicionar um certificado SSL</span><span class="sxs-lookup"><span data-stu-id="9adab-108">Example 1: Add an SSL certificate</span></span>
```
PS C:\> Add-AzureApplicationGatewaySslCertificate -Name "ApplicationGateway08" -CertificateName "SslCertificate13" -Password "password" -CertificateFile "c:\Certs\sslCertificate.pfx"
```

<span data-ttu-id="9adab-109">Esse comando adiciona um certificado SSL chamado SslCertificate13 ao gateway do aplicativo chamado ApplicationGateway08.</span><span class="sxs-lookup"><span data-stu-id="9adab-109">This command adds an SSL certificate named SslCertificate13 to the Application Gateway named ApplicationGateway08.</span></span>
<span data-ttu-id="9adab-110">O comando especifica o caminho do arquivo de certificado e a senha do certificado.</span><span class="sxs-lookup"><span data-stu-id="9adab-110">The command specifies the path of the certificate file and the password for the certificate.</span></span>

## <span data-ttu-id="9adab-111">OS</span><span class="sxs-lookup"><span data-stu-id="9adab-111">PARAMETERS</span></span>

### <span data-ttu-id="9adab-112">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="9adab-112">-CertificateFile</span></span>
<span data-ttu-id="9adab-113">Especifica o caminho de um arquivo de certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="9adab-113">Specifies the path of an SSL certificate file.</span></span>
<span data-ttu-id="9adab-114">Esse cmdlet adiciona o certificado no arquivo que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9adab-114">This cmdlet adds the certificate in the file that this parameter specifies.</span></span>

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

### <span data-ttu-id="9adab-115">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="9adab-115">-CertificateName</span></span>
<span data-ttu-id="9adab-116">Especifica o nome de um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="9adab-116">Specifies the name of an SSL certificate.</span></span>
<span data-ttu-id="9adab-117">Esse cmdlet adiciona o certificado que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="9adab-117">This cmdlet adds the certificate that this parameter specifies.</span></span>

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

### <span data-ttu-id="9adab-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9adab-118">-Name</span></span>
<span data-ttu-id="9adab-119">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="9adab-119">Specifies the name of the Application Gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="9adab-120">-Senha</span><span class="sxs-lookup"><span data-stu-id="9adab-120">-Password</span></span>
<span data-ttu-id="9adab-121">Especifica a senha do certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="9adab-121">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="9adab-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9adab-122">-Profile</span></span>
<span data-ttu-id="9adab-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9adab-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9adab-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9adab-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9adab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adab-125">CommonParameters</span></span>
<span data-ttu-id="9adab-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9adab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adab-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9adab-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adab-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9adab-128">INPUTS</span></span>

### <span data-ttu-id="9adab-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9adab-129">System.String</span></span>

## <span data-ttu-id="9adab-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9adab-130">OUTPUTS</span></span>

### <span data-ttu-id="9adab-131">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9adab-131">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="9adab-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9adab-132">NOTES</span></span>

## <span data-ttu-id="9adab-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9adab-133">RELATED LINKS</span></span>

[<span data-ttu-id="9adab-134">Get-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9adab-134">Get-AzureApplicationGatewaySslCertificate</span></span>](./Get-AzureApplicationGatewaySslCertificate.md)

[<span data-ttu-id="9adab-135">Remove-AzureApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="9adab-135">Remove-AzureApplicationGatewaySslCertificate</span></span>](./Remove-AzureApplicationGatewaySslCertificate.md)
