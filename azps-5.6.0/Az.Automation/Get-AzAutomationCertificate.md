---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 1680f4080f0e3def2e18d90273ce9e6f2f6d0bcb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890676"
---
# <span data-ttu-id="5eb7d-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5eb7d-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="5eb7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5eb7d-102">SYNOPSIS</span></span>
<span data-ttu-id="5eb7d-103">Obtém certificados de automação.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="5eb7d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5eb7d-104">SYNTAX</span></span>

### <span data-ttu-id="5eb7d-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5eb7d-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5eb7d-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="5eb7d-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5eb7d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5eb7d-107">DESCRIPTION</span></span>
<span data-ttu-id="5eb7d-108">O cmdlet **Get-AzAutomationCertificate** obtém um ou mais certificados de Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="5eb7d-109">Por padrão, esse cmdlet obtém todos os certificados.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="5eb7d-110">Especifique o nome de um certificado para obter um certificado específico.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="5eb7d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5eb7d-111">EXAMPLES</span></span>

### <span data-ttu-id="5eb7d-112">Exemplo 1: Obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="5eb7d-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5eb7d-113">Este comando obtém metadados para todos os certificados na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5eb7d-114">Exemplo 2: Obter um certificado</span><span class="sxs-lookup"><span data-stu-id="5eb7d-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="5eb7d-115">Este comando obtém metadados para o certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="5eb7d-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5eb7d-116">PARAMETERS</span></span>

### <span data-ttu-id="5eb7d-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5eb7d-117">-AutomationAccountName</span></span>
<span data-ttu-id="5eb7d-118">Especifica o nome da conta de automação para a qual este cmdlet recupera um certificado.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="5eb7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5eb7d-119">-DefaultProfile</span></span>
<span data-ttu-id="5eb7d-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5eb7d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5eb7d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5eb7d-121">-Name</span></span>
<span data-ttu-id="5eb7d-122">Especifica o nome de um certificado a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="5eb7d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5eb7d-123">-ResourceGroupName</span></span>
<span data-ttu-id="5eb7d-124">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="5eb7d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5eb7d-125">CommonParameters</span></span>
<span data-ttu-id="5eb7d-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5eb7d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5eb7d-127">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5eb7d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5eb7d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5eb7d-128">INPUTS</span></span>

### <span data-ttu-id="5eb7d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5eb7d-129">System.String</span></span>

## <span data-ttu-id="5eb7d-130">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5eb7d-130">OUTPUTS</span></span>

### <span data-ttu-id="5eb7d-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="5eb7d-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="5eb7d-132">NOTES</span><span class="sxs-lookup"><span data-stu-id="5eb7d-132">NOTES</span></span>

## <span data-ttu-id="5eb7d-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5eb7d-133">RELATED LINKS</span></span>

[<span data-ttu-id="5eb7d-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5eb7d-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="5eb7d-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5eb7d-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="5eb7d-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5eb7d-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


