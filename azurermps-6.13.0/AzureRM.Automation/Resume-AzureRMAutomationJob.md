---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/resume-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Resume-AzureRMAutomationJob.md
ms.openlocfilehash: 8e84f2f66703410b626769be8c2c2d5a57e531e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428612"
---
# <span data-ttu-id="e9066-101">Resume-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e9066-101">Resume-AzureRmAutomationJob</span></span>

## <span data-ttu-id="e9066-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e9066-102">SYNOPSIS</span></span>
<span data-ttu-id="e9066-103">Retoma um trabalho de automação suspenso.</span><span class="sxs-lookup"><span data-stu-id="e9066-103">Resumes a suspended Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9066-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9066-104">SYNTAX</span></span>

```
Resume-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9066-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e9066-105">DESCRIPTION</span></span>
<span data-ttu-id="e9066-106">O cmdlet **resume-AzureRmAutomationJob** retoma um trabalho suspenso de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e9066-106">The **Resume-AzureRmAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="e9066-107">Especifique o trabalho suspenso.</span><span class="sxs-lookup"><span data-stu-id="e9066-107">Specify the suspended job.</span></span>
<span data-ttu-id="e9066-108">Para suspender um trabalho, use o cmdlet Suspend-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="e9066-108">To suspend a job, use the Suspend-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="e9066-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e9066-109">EXAMPLES</span></span>

### <span data-ttu-id="e9066-110">Exemplo 1: retomar um trabalho suspenso</span><span class="sxs-lookup"><span data-stu-id="e9066-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e9066-111">Esse comando retoma o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="e9066-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="e9066-112">OS</span><span class="sxs-lookup"><span data-stu-id="e9066-112">PARAMETERS</span></span>

### <span data-ttu-id="e9066-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9066-113">-AutomationAccountName</span></span>
<span data-ttu-id="e9066-114">Especifica o nome de uma conta de automação na qual esse cmdlet retomará um trabalho.</span><span class="sxs-lookup"><span data-stu-id="e9066-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="e9066-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9066-115">-DefaultProfile</span></span>
<span data-ttu-id="e9066-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e9066-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9066-117">-ID</span><span class="sxs-lookup"><span data-stu-id="e9066-117">-Id</span></span>
<span data-ttu-id="e9066-118">Especifica a ID de um trabalho retomada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9066-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="e9066-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9066-119">-ResourceGroupName</span></span>
<span data-ttu-id="e9066-120">Especifica o nome de um grupo de recursos para o qual esse cmdlet retomará um trabalho.</span><span class="sxs-lookup"><span data-stu-id="e9066-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="e9066-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9066-121">CommonParameters</span></span>
<span data-ttu-id="e9066-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9066-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9066-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9066-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9066-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e9066-124">INPUTS</span></span>

### <span data-ttu-id="e9066-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e9066-125">System.Guid</span></span>

### <span data-ttu-id="e9066-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e9066-126">System.String</span></span>

## <span data-ttu-id="e9066-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e9066-127">OUTPUTS</span></span>

### <span data-ttu-id="e9066-128">System. void</span><span class="sxs-lookup"><span data-stu-id="e9066-128">System.Void</span></span>

## <span data-ttu-id="e9066-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e9066-129">NOTES</span></span>

## <span data-ttu-id="e9066-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e9066-130">RELATED LINKS</span></span>

[<span data-ttu-id="e9066-131">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e9066-131">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="e9066-132">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e9066-132">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="e9066-133">Parar-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e9066-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="e9066-134">Suspender-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="e9066-134">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)

