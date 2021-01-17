---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9400E9EB-E927-44D5-8722-9706BDD92FD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/resume-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Resume-AzAutomationJob.md
ms.openlocfilehash: 731a2df87ce6ad575e9aa3e10eb124e52ec1b60b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430582"
---
# <span data-ttu-id="cf2b1-101">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="cf2b1-101">Resume-AzAutomationJob</span></span>

## <span data-ttu-id="cf2b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cf2b1-102">SYNOPSIS</span></span>
<span data-ttu-id="cf2b1-103">Retoma um trabalho de automação suspenso.</span><span class="sxs-lookup"><span data-stu-id="cf2b1-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="cf2b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cf2b1-104">SYNTAX</span></span>

```
Resume-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf2b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cf2b1-105">DESCRIPTION</span></span>
<span data-ttu-id="cf2b1-106">O cmdlet **resume-AzAutomationJob** retoma um trabalho suspenso de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="cf2b1-106">The **Resume-AzAutomationJob** cmdlet resumes a suspended Azure Automation job.</span></span>
<span data-ttu-id="cf2b1-107">Especifique o trabalho suspenso.</span><span class="sxs-lookup"><span data-stu-id="cf2b1-107">Specify the suspended job.</span></span>
<span data-ttu-id="cf2b1-108">Para suspender um trabalho, use o cmdlet Suspend-AzAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="cf2b1-108">To suspend a job, use the Suspend-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="cf2b1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cf2b1-109">EXAMPLES</span></span>

### <span data-ttu-id="cf2b1-110">Exemplo 1: retomar um trabalho suspenso</span><span class="sxs-lookup"><span data-stu-id="cf2b1-110">Example 1: Resume a suspended job</span></span>
```
PS C:\>Resume-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cf2b1-111">Esse comando retoma o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="cf2b1-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="cf2b1-112">OS</span><span class="sxs-lookup"><span data-stu-id="cf2b1-112">PARAMETERS</span></span>

### <span data-ttu-id="cf2b1-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cf2b1-113">-AutomationAccountName</span></span>
<span data-ttu-id="cf2b1-114">Especifica o nome de uma conta de automação na qual esse cmdlet retomará um trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf2b1-114">Specifies the name of an Automation account in which this cmdlet resume a job.</span></span>

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

### <span data-ttu-id="cf2b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf2b1-115">-DefaultProfile</span></span>
<span data-ttu-id="cf2b1-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cf2b1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf2b1-117">-ID</span><span class="sxs-lookup"><span data-stu-id="cf2b1-117">-Id</span></span>
<span data-ttu-id="cf2b1-118">Especifica a ID de um trabalho retomada por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf2b1-118">Specifies the ID of a job that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="cf2b1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf2b1-119">-ResourceGroupName</span></span>
<span data-ttu-id="cf2b1-120">Especifica o nome de um grupo de recursos para o qual esse cmdlet retomará um trabalho.</span><span class="sxs-lookup"><span data-stu-id="cf2b1-120">Specifies the name of a resource group for which this cmdlet resumes a job.</span></span>

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

### <span data-ttu-id="cf2b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf2b1-121">CommonParameters</span></span>
<span data-ttu-id="cf2b1-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf2b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf2b1-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf2b1-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf2b1-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cf2b1-124">INPUTS</span></span>

### <span data-ttu-id="cf2b1-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cf2b1-125">System.Guid</span></span>

### <span data-ttu-id="cf2b1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cf2b1-126">System.String</span></span>

## <span data-ttu-id="cf2b1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cf2b1-127">OUTPUTS</span></span>

### <span data-ttu-id="cf2b1-128">System. void</span><span class="sxs-lookup"><span data-stu-id="cf2b1-128">System.Void</span></span>

## <span data-ttu-id="cf2b1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cf2b1-129">NOTES</span></span>

## <span data-ttu-id="cf2b1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cf2b1-130">RELATED LINKS</span></span>

[<span data-ttu-id="cf2b1-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="cf2b1-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="cf2b1-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="cf2b1-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="cf2b1-133">Parar-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="cf2b1-133">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="cf2b1-134">Suspender-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="cf2b1-134">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


