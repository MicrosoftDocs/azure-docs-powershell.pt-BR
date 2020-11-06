---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 70b92cd7762b42fba7ae890cd22b529ba80318ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601640"
---
# <span data-ttu-id="b74b5-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b74b5-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="b74b5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b74b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b74b5-103">Obtém certificados de automação.</span><span class="sxs-lookup"><span data-stu-id="b74b5-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="b74b5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b74b5-104">SYNTAX</span></span>

### <span data-ttu-id="b74b5-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="b74b5-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b74b5-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="b74b5-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b74b5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b74b5-107">DESCRIPTION</span></span>
<span data-ttu-id="b74b5-108">O cmdlet **Get-AzAutomationCertificate** Obtém um ou mais certificados de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="b74b5-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="b74b5-109">Por padrão, esse cmdlet obtém todos os certificados.</span><span class="sxs-lookup"><span data-stu-id="b74b5-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="b74b5-110">Especifique o nome de um certificado para obter um certificado específico.</span><span class="sxs-lookup"><span data-stu-id="b74b5-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="b74b5-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b74b5-111">EXAMPLES</span></span>

### <span data-ttu-id="b74b5-112">Exemplo 1: obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="b74b5-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b74b5-113">Esse comando obtém metadados para todos os certificados na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b74b5-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b74b5-114">Exemplo 2: obter um certificado</span><span class="sxs-lookup"><span data-stu-id="b74b5-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="b74b5-115">Esse comando obtém metadados para o certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="b74b5-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="b74b5-116">OS</span><span class="sxs-lookup"><span data-stu-id="b74b5-116">PARAMETERS</span></span>

### <span data-ttu-id="b74b5-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b74b5-117">-AutomationAccountName</span></span>
<span data-ttu-id="b74b5-118">Especifica o nome da conta de automação para a qual esse cmdlet recupera um certificado.</span><span class="sxs-lookup"><span data-stu-id="b74b5-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="b74b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b74b5-119">-DefaultProfile</span></span>
<span data-ttu-id="b74b5-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b74b5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b74b5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b74b5-121">-Name</span></span>
<span data-ttu-id="b74b5-122">Especifica o nome de um certificado a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="b74b5-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="b74b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b74b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="b74b5-124">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="b74b5-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="b74b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b74b5-125">CommonParameters</span></span>
<span data-ttu-id="b74b5-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b74b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b74b5-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b74b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b74b5-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b74b5-128">INPUTS</span></span>

### <span data-ttu-id="b74b5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b74b5-129">System.String</span></span>

## <span data-ttu-id="b74b5-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b74b5-130">OUTPUTS</span></span>

### <span data-ttu-id="b74b5-131">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="b74b5-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="b74b5-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b74b5-132">NOTES</span></span>

## <span data-ttu-id="b74b5-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b74b5-133">RELATED LINKS</span></span>

[<span data-ttu-id="b74b5-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b74b5-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="b74b5-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b74b5-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="b74b5-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b74b5-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


