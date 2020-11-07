---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945663"
---
# <span data-ttu-id="632a3-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="632a3-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="632a3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="632a3-102">SYNOPSIS</span></span>

<span data-ttu-id="632a3-103">Obtém um certificado de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="632a3-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="632a3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="632a3-104">SYNTAX</span></span>

### <span data-ttu-id="632a3-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="632a3-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="632a3-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="632a3-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="632a3-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="632a3-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="632a3-108">O cmdlet **Get-AzureAutomationCertificate** Obtém um ou mais certificados de automação do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="632a3-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="632a3-109">Por padrão, todos os certificados são retornados.</span><span class="sxs-lookup"><span data-stu-id="632a3-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="632a3-110">Para obter um certificado específico, especifique seu nome.</span><span class="sxs-lookup"><span data-stu-id="632a3-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="632a3-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="632a3-111">EXAMPLES</span></span>

### <span data-ttu-id="632a3-112">Exemplo 1: obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="632a3-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="632a3-113">Esse comando obtém todos os certificados na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="632a3-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="632a3-114">Exemplo 2: obter um certificado</span><span class="sxs-lookup"><span data-stu-id="632a3-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="632a3-115">Esse comando obtém o certificado chamado MyUserCertificate.</span><span class="sxs-lookup"><span data-stu-id="632a3-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="632a3-116">OS</span><span class="sxs-lookup"><span data-stu-id="632a3-116">PARAMETERS</span></span>

### <span data-ttu-id="632a3-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="632a3-117">-AutomationAccountName</span></span>
<span data-ttu-id="632a3-118">Especifica o nome da conta de automação com o certificado.</span><span class="sxs-lookup"><span data-stu-id="632a3-118">Specifies the name of the automation account with the certificate.</span></span>

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

### <span data-ttu-id="632a3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="632a3-119">-Name</span></span>
<span data-ttu-id="632a3-120">Especifica o nome de um certificado a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="632a3-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="632a3-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="632a3-121">-Profile</span></span>
<span data-ttu-id="632a3-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="632a3-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="632a3-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="632a3-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="632a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="632a3-124">CommonParameters</span></span>
<span data-ttu-id="632a3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="632a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="632a3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="632a3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="632a3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="632a3-127">INPUTS</span></span>

## <span data-ttu-id="632a3-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="632a3-128">OUTPUTS</span></span>

### <span data-ttu-id="632a3-129">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="632a3-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="632a3-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="632a3-130">NOTES</span></span>

## <span data-ttu-id="632a3-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="632a3-131">RELATED LINKS</span></span>

[<span data-ttu-id="632a3-132">New-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="632a3-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="632a3-133">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="632a3-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="632a3-134">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="632a3-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


