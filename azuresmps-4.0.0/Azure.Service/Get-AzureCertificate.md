---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7BEFA810-685C-4553-BED8-4CD6BCF8A5FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: d88784e5d4fdd153700bd3879262198e5dd3807a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946356"
---
# <span data-ttu-id="fa1bd-101">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="fa1bd-101">Get-AzureCertificate</span></span>

## <span data-ttu-id="fa1bd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="fa1bd-103">Obtém um objeto de certificado de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-103">Gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="fa1bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa1bd-104">SYNTAX</span></span>

```
Get-AzureCertificate [-ServiceName] <String> [-ThumbprintAlgorithm <String>] [-Thumbprint <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa1bd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa1bd-105">DESCRIPTION</span></span>
<span data-ttu-id="fa1bd-106">O cmdlet **Get-AzureCertificate** Obtém um objeto de certificado de um serviço do Azure.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-106">The **Get-AzureCertificate** cmdlet gets a certificate object from an Azure service.</span></span>

## <span data-ttu-id="fa1bd-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa1bd-107">EXAMPLES</span></span>

### <span data-ttu-id="fa1bd-108">Exemplo 1: obter certificados de um serviço</span><span class="sxs-lookup"><span data-stu-id="fa1bd-108">Example 1: Get certificates from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService"
```

<span data-ttu-id="fa1bd-109">Esse comando obtém objetos de certificado do serviço denominado ContosoService e, em seguida, os armazena na variável $AzureCert.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-109">This command gets certificate objects from the service named ContosoService, and then stores them in the $AzureCert variable.</span></span>

### <span data-ttu-id="fa1bd-110">Exemplo 2: obter um certificado de um serviço</span><span class="sxs-lookup"><span data-stu-id="fa1bd-110">Example 2: Get a certificate from a service</span></span>
```
PS C:\> $AzureCert = Get-AzureCertificate -ServiceName "ContosoService" -Thumbprint '5383CE0343CB6563281CA97C1D4D712209CFFA97'
```

<span data-ttu-id="fa1bd-111">Esse comando obtém o objeto de certificado identificado pela impressão digital especificada do serviço denominado ContosoService e, em seguida, armazena-o na variável $AzureCert.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-111">This command gets the certificate object identified by the specified thumbprint from the service named ContosoService, and then stores it in the $AzureCert variable.</span></span>

## <span data-ttu-id="fa1bd-112">OS</span><span class="sxs-lookup"><span data-stu-id="fa1bd-112">PARAMETERS</span></span>

### <span data-ttu-id="fa1bd-113">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fa1bd-113">-InformationAction</span></span>
<span data-ttu-id="fa1bd-114">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fa1bd-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="fa1bd-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fa1bd-116">Contínuo</span><span class="sxs-lookup"><span data-stu-id="fa1bd-116">Continue</span></span>
- <span data-ttu-id="fa1bd-117">Ignorar</span><span class="sxs-lookup"><span data-stu-id="fa1bd-117">Ignore</span></span>
- <span data-ttu-id="fa1bd-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="fa1bd-118">Inquire</span></span>
- <span data-ttu-id="fa1bd-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fa1bd-119">SilentlyContinue</span></span>
- <span data-ttu-id="fa1bd-120">Finaliza</span><span class="sxs-lookup"><span data-stu-id="fa1bd-120">Stop</span></span>
- <span data-ttu-id="fa1bd-121">Suspensão</span><span class="sxs-lookup"><span data-stu-id="fa1bd-121">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa1bd-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fa1bd-122">-InformationVariable</span></span>
<span data-ttu-id="fa1bd-123">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-123">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa1bd-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="fa1bd-124">-Profile</span></span>
<span data-ttu-id="fa1bd-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fa1bd-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fa1bd-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fa1bd-127">-ServiceName</span></span>
<span data-ttu-id="fa1bd-128">Especifica o nome do serviço do Azure do qual esse cmdlet recebe um certificado.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-128">Specifies the name of the Azure service from which this cmdlet gets a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa1bd-129">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="fa1bd-129">-Thumbprint</span></span>
<span data-ttu-id="fa1bd-130">Especifica a impressão digital do certificado que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-130">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fa1bd-131">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="fa1bd-131">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="fa1bd-132">Especifica o algoritmo que é usado para criar a impressão digital do certificado.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-132">Specifies the algorithm that is used to create the certificate thumbprint.</span></span>

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

### <span data-ttu-id="fa1bd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa1bd-133">CommonParameters</span></span>
<span data-ttu-id="fa1bd-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa1bd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa1bd-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa1bd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa1bd-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa1bd-136">INPUTS</span></span>

## <span data-ttu-id="fa1bd-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa1bd-137">OUTPUTS</span></span>

### <span data-ttu-id="fa1bd-138">CertificateContext</span><span class="sxs-lookup"><span data-stu-id="fa1bd-138">CertificateContext</span></span>

## <span data-ttu-id="fa1bd-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa1bd-139">NOTES</span></span>

## <span data-ttu-id="fa1bd-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa1bd-140">RELATED LINKS</span></span>

[<span data-ttu-id="fa1bd-141">Add-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="fa1bd-141">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="fa1bd-142">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="fa1bd-142">New-AzureCertificateSetting</span></span>](./New-AzureCertificateSetting.md)

[<span data-ttu-id="fa1bd-143">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="fa1bd-143">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


