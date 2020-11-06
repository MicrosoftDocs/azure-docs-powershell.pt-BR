---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 0820905ff8a4673c9abae56be2f7792912095e76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429596"
---
# <span data-ttu-id="936ce-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="936ce-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="936ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="936ce-102">SYNOPSIS</span></span>
<span data-ttu-id="936ce-103">Suspende um trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="936ce-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="936ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="936ce-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="936ce-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="936ce-105">DESCRIPTION</span></span>
<span data-ttu-id="936ce-106">O cmdlet **Suspend-AzureRmAutomationJob** suspende um trabalho de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="936ce-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="936ce-107">Especifique um trabalho de automação em execução.</span><span class="sxs-lookup"><span data-stu-id="936ce-107">Specify a running Automation job.</span></span>
<span data-ttu-id="936ce-108">Para retomar um trabalho suspenso, use o cmdlet Resume-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="936ce-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="936ce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="936ce-109">EXAMPLES</span></span>

### <span data-ttu-id="936ce-110">Exemplo 1: suspender um trabalho</span><span class="sxs-lookup"><span data-stu-id="936ce-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="936ce-111">Esse comando suspende o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="936ce-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="936ce-112">OS</span><span class="sxs-lookup"><span data-stu-id="936ce-112">PARAMETERS</span></span>

### <span data-ttu-id="936ce-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="936ce-113">-AutomationAccountName</span></span>
<span data-ttu-id="936ce-114">Especifica o nome de uma conta de automação na qual esse cmdlet suspende um trabalho.</span><span class="sxs-lookup"><span data-stu-id="936ce-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="936ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936ce-115">-DefaultProfile</span></span>
<span data-ttu-id="936ce-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="936ce-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="936ce-117">-ID</span><span class="sxs-lookup"><span data-stu-id="936ce-117">-Id</span></span>
<span data-ttu-id="936ce-118">Especifica a ID de um trabalho que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="936ce-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936ce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="936ce-119">-ResourceGroupName</span></span>
<span data-ttu-id="936ce-120">Especifica a ID de um trabalho que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="936ce-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="936ce-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936ce-121">CommonParameters</span></span>
<span data-ttu-id="936ce-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="936ce-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936ce-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="936ce-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936ce-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="936ce-124">INPUTS</span></span>

### <span data-ttu-id="936ce-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="936ce-125">System.Guid</span></span>

### <span data-ttu-id="936ce-126">System. String</span><span class="sxs-lookup"><span data-stu-id="936ce-126">System.String</span></span>

## <span data-ttu-id="936ce-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="936ce-127">OUTPUTS</span></span>

### <span data-ttu-id="936ce-128">System. void</span><span class="sxs-lookup"><span data-stu-id="936ce-128">System.Void</span></span>

## <span data-ttu-id="936ce-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="936ce-129">NOTES</span></span>

## <span data-ttu-id="936ce-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="936ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="936ce-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="936ce-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="936ce-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="936ce-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="936ce-133">Currículo-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="936ce-133">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="936ce-134">Parar-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="936ce-134">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


