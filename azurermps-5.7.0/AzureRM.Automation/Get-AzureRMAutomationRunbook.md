---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: d9ffd6ae2f7695a02f8c29fbe745202642039af6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440885"
---
# <span data-ttu-id="6af05-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6af05-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="6af05-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6af05-102">SYNOPSIS</span></span>
<span data-ttu-id="6af05-103">Obtém um runbook.</span><span class="sxs-lookup"><span data-stu-id="6af05-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6af05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6af05-104">SYNTAX</span></span>

### <span data-ttu-id="6af05-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="6af05-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6af05-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="6af05-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6af05-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6af05-107">DESCRIPTION</span></span>
<span data-ttu-id="6af05-108">O cmdlet **Get-AzureRmAutomationRunbook** Obtém os Runbooks de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="6af05-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="6af05-109">Para obter um runbook específico, especifique seu nome.</span><span class="sxs-lookup"><span data-stu-id="6af05-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="6af05-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6af05-110">EXAMPLES</span></span>

### <span data-ttu-id="6af05-111">Exemplo 1: obter todos os runbooks</span><span class="sxs-lookup"><span data-stu-id="6af05-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6af05-112">Esse comando obtém todos os runbooks na conta de automação do Azure chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6af05-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="6af05-113">OS</span><span class="sxs-lookup"><span data-stu-id="6af05-113">PARAMETERS</span></span>

### <span data-ttu-id="6af05-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6af05-114">-AutomationAccountName</span></span>
<span data-ttu-id="6af05-115">Especifica o nome de uma conta de automação na qual esse cmdlet recebe runbooks.</span><span class="sxs-lookup"><span data-stu-id="6af05-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="6af05-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af05-116">-DefaultProfile</span></span>
<span data-ttu-id="6af05-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6af05-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6af05-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6af05-118">-Name</span></span>
<span data-ttu-id="6af05-119">Especifica o nome de um runbook que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="6af05-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6af05-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6af05-120">-ResourceGroupName</span></span>
<span data-ttu-id="6af05-121">Especifica o nome do grupo de recursos para o qual esse cmdlet recebe runbooks.</span><span class="sxs-lookup"><span data-stu-id="6af05-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="6af05-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af05-122">CommonParameters</span></span>
<span data-ttu-id="6af05-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af05-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af05-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6af05-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af05-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6af05-125">INPUTS</span></span>

### <span data-ttu-id="6af05-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="6af05-126">None</span></span>
<span data-ttu-id="6af05-127">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="6af05-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6af05-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6af05-128">OUTPUTS</span></span>

### <span data-ttu-id="6af05-129">Microsoft. Azure. Commands. Automation. Model. runbook</span><span class="sxs-lookup"><span data-stu-id="6af05-129">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="6af05-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6af05-130">NOTES</span></span>

## <span data-ttu-id="6af05-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6af05-131">RELATED LINKS</span></span>

[<span data-ttu-id="6af05-132">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6af05-132">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6af05-133">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6af05-133">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6af05-134">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6af05-134">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6af05-135">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6af05-135">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6af05-136">Publicar-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6af05-136">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6af05-137">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6af05-137">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6af05-138">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6af05-138">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="6af05-139">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="6af05-139">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


