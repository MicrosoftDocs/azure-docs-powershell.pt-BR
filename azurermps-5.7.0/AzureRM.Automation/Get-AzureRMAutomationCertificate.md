---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 012eb357b6d64964c2564dca51ac0b77a5f96880
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427717"
---
# <span data-ttu-id="3b09f-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3b09f-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="3b09f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b09f-102">SYNOPSIS</span></span>
<span data-ttu-id="3b09f-103">Obtém certificados de automação.</span><span class="sxs-lookup"><span data-stu-id="3b09f-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b09f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b09f-104">SYNTAX</span></span>

### <span data-ttu-id="3b09f-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="3b09f-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b09f-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="3b09f-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b09f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b09f-107">DESCRIPTION</span></span>
<span data-ttu-id="3b09f-108">O cmdlet **Get-AzureRmAutomationCertificate** Obtém um ou mais certificados de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="3b09f-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="3b09f-109">Por padrão, esse cmdlet obtém todos os certificados.</span><span class="sxs-lookup"><span data-stu-id="3b09f-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="3b09f-110">Especifique o nome de um certificado para obter um certificado específico.</span><span class="sxs-lookup"><span data-stu-id="3b09f-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="3b09f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b09f-111">EXAMPLES</span></span>

### <span data-ttu-id="3b09f-112">Exemplo 1: obter todos os certificados</span><span class="sxs-lookup"><span data-stu-id="3b09f-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3b09f-113">Esse comando obtém metadados para todos os certificados na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3b09f-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3b09f-114">Exemplo 2: obter um certificado</span><span class="sxs-lookup"><span data-stu-id="3b09f-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="3b09f-115">Esse comando obtém metadados para o certificado chamado ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="3b09f-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="3b09f-116">OS</span><span class="sxs-lookup"><span data-stu-id="3b09f-116">PARAMETERS</span></span>

### <span data-ttu-id="3b09f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3b09f-117">-AutomationAccountName</span></span>
<span data-ttu-id="3b09f-118">Especifica o nome da conta de automação para a qual esse cmdlet recupera um certificado.</span><span class="sxs-lookup"><span data-stu-id="3b09f-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b09f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b09f-119">-DefaultProfile</span></span>
<span data-ttu-id="3b09f-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3b09f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b09f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b09f-121">-Name</span></span>
<span data-ttu-id="3b09f-122">Especifica o nome de um certificado a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="3b09f-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b09f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b09f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b09f-124">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém um certificado de automação.</span><span class="sxs-lookup"><span data-stu-id="3b09f-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="3b09f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b09f-125">CommonParameters</span></span>
<span data-ttu-id="3b09f-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b09f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b09f-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b09f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b09f-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b09f-128">INPUTS</span></span>

### <span data-ttu-id="3b09f-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3b09f-129">None</span></span>
<span data-ttu-id="3b09f-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3b09f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b09f-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b09f-131">OUTPUTS</span></span>

### <span data-ttu-id="3b09f-132">Microsoft. Azure. Commands. Automation. Model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="3b09f-132">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="3b09f-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b09f-133">NOTES</span></span>

## <span data-ttu-id="3b09f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b09f-134">RELATED LINKS</span></span>

[<span data-ttu-id="3b09f-135">New-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3b09f-135">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3b09f-136">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3b09f-136">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3b09f-137">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3b09f-137">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


