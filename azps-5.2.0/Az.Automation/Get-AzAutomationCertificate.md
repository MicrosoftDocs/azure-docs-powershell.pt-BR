---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264122"
---
# <span data-ttu-id="cf02b-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cf02b-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="cf02b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf02b-102">SYNOPSIS</span></span>
<span data-ttu-id="cf02b-103">Obtém certificados de automação.</span><span class="sxs-lookup"><span data-stu-id="cf02b-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="cf02b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf02b-104">SYNTAX</span></span>

### <span data-ttu-id="cf02b-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf02b-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf02b-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="cf02b-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf02b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf02b-107">DESCRIPTION</span></span>
<span data-ttu-id="cf02b-108">O cmdlet **Get-AzAutomationCertificate** Obtém um ou mais certificados de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf02b-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="cf02b-109">Por padrão, esse cmdlet obtém todos os certificados.</span><span class="sxs-lookup"><span data-stu-id="cf02b-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="cf02b-110">Especifique o nome de um certificado para obter um certificado específico.</span><span class="sxs-lookup"><span data-stu-id="cf02b-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="cf02b-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf02b-111">EXAMPLES</span></span>

### <span data-ttu-id="cf02b-112">Exemplo 1: obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="cf02b-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="cf02b-113">Esse comando obtém metadados para todos os certificados na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="cf02b-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="cf02b-114">Exemplo 2: obter um certificado</span><span class="sxs-lookup"><span data-stu-id="cf02b-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="cf02b-115">Esse comando obtém metadados para o certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="cf02b-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="cf02b-116">OS</span><span class="sxs-lookup"><span data-stu-id="cf02b-116">PARAMETERS</span></span>

### <span data-ttu-id="cf02b-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cf02b-117">-AutomationAccountName</span></span>
<span data-ttu-id="cf02b-118">Especifica o nome da conta de automação para a qual esse cmdlet recupera um certificado.</span><span class="sxs-lookup"><span data-stu-id="cf02b-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf02b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf02b-119">-DefaultProfile</span></span>
<span data-ttu-id="cf02b-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cf02b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf02b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf02b-121">-Name</span></span>
<span data-ttu-id="cf02b-122">Especifica o nome de um certificado a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="cf02b-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf02b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf02b-123">-ResourceGroupName</span></span>
<span data-ttu-id="cf02b-124">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="cf02b-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cf02b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf02b-125">CommonParameters</span></span>
<span data-ttu-id="cf02b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf02b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf02b-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf02b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf02b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf02b-128">INPUTS</span></span>

### <span data-ttu-id="cf02b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cf02b-129">System.String</span></span>

## <span data-ttu-id="cf02b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf02b-130">OUTPUTS</span></span>

### <span data-ttu-id="cf02b-131">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="cf02b-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="cf02b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf02b-132">NOTES</span></span>

## <span data-ttu-id="cf02b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf02b-133">RELATED LINKS</span></span>

[<span data-ttu-id="cf02b-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cf02b-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="cf02b-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cf02b-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="cf02b-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="cf02b-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


