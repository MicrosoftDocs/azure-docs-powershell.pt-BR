---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Publish-AzureRMAutomationRunbook.md
ms.openlocfilehash: 71d66c6440091e50da2809f4b8c0669410d09d50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432676"
---
# <span data-ttu-id="9ac2f-101">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-101">Publish-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="9ac2f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ac2f-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac2f-103">Publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="9ac2f-103">Publishes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ac2f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ac2f-104">SYNTAX</span></span>

```
Publish-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ac2f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ac2f-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac2f-106">O cmdlet **Publish-AzureRmAutomationRunbook** publica um runbook para uso no ambiente de produção da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac2f-106">The **Publish-AzureRmAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="9ac2f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ac2f-107">EXAMPLES</span></span>

### <span data-ttu-id="9ac2f-108">Exemplo 1: publicar um runbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9ac2f-109">Esse comando publica o runbook chamado Runbk01 na conta de automação do Azure chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ac2f-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="9ac2f-110">OS</span><span class="sxs-lookup"><span data-stu-id="9ac2f-110">PARAMETERS</span></span>

### <span data-ttu-id="9ac2f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9ac2f-111">-AutomationAccountName</span></span>
<span data-ttu-id="9ac2f-112">Especifica o nome da conta de automação na qual esse cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="9ac2f-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="9ac2f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9ac2f-113">-Name</span></span>
<span data-ttu-id="9ac2f-114">Especifica o nome do runbook que esse cmdlet publica.</span><span class="sxs-lookup"><span data-stu-id="9ac2f-114">Specifies the name of the runbook that this cmdlet publishes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac2f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ac2f-115">-ResourceGroupName</span></span>
<span data-ttu-id="9ac2f-116">Especifica o nome do grupo de recursos para o qual esse cmdlet publica um runbook.</span><span class="sxs-lookup"><span data-stu-id="9ac2f-116">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="9ac2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac2f-117">-DefaultProfile</span></span>
<span data-ttu-id="9ac2f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ac2f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ac2f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac2f-119">CommonParameters</span></span>
<span data-ttu-id="9ac2f-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ac2f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac2f-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac2f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac2f-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ac2f-122">INPUTS</span></span>

## <span data-ttu-id="9ac2f-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ac2f-123">OUTPUTS</span></span>

### <span data-ttu-id="9ac2f-124">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-124">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="9ac2f-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ac2f-125">NOTES</span></span>

## <span data-ttu-id="9ac2f-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ac2f-126">RELATED LINKS</span></span>

[<span data-ttu-id="9ac2f-127">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-127">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9ac2f-128">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-128">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9ac2f-129">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-129">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9ac2f-130">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-130">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9ac2f-131">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-131">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9ac2f-132">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-132">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9ac2f-133">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-133">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="9ac2f-134">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9ac2f-134">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


