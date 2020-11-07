---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationJob.md
ms.openlocfilehash: 451457cf4483d9af6d8a7aca8731b95dc5c95859
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93954444"
---
# <span data-ttu-id="a0d8a-101">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a0d8a-101">Stop-AzAutomationJob</span></span>

## <span data-ttu-id="a0d8a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a0d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d8a-103">Interrompe um trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="a0d8a-103">Stops an Automation job.</span></span>

## <span data-ttu-id="a0d8a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0d8a-104">SYNTAX</span></span>

```
Stop-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0d8a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a0d8a-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d8a-106">O cmdlet **Stop-AzAutomationJob** interrompe um trabalho de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d8a-106">The **Stop-AzAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="a0d8a-107">Especifique um trabalho de automação em execução.</span><span class="sxs-lookup"><span data-stu-id="a0d8a-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="a0d8a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a0d8a-108">EXAMPLES</span></span>

### <span data-ttu-id="a0d8a-109">Exemplo 1: parar um trabalho</span><span class="sxs-lookup"><span data-stu-id="a0d8a-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a0d8a-110">Esse comando para o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="a0d8a-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="a0d8a-111">OS</span><span class="sxs-lookup"><span data-stu-id="a0d8a-111">PARAMETERS</span></span>

### <span data-ttu-id="a0d8a-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a0d8a-112">-AutomationAccountName</span></span>
<span data-ttu-id="a0d8a-113">Especifica o nome de uma conta de automação na qual esse cmdlet interrompe um trabalho.</span><span class="sxs-lookup"><span data-stu-id="a0d8a-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="a0d8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d8a-114">-DefaultProfile</span></span>
<span data-ttu-id="a0d8a-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a0d8a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0d8a-116">-ID</span><span class="sxs-lookup"><span data-stu-id="a0d8a-116">-Id</span></span>
<span data-ttu-id="a0d8a-117">Especifica a ID de um trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="a0d8a-117">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="a0d8a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d8a-118">-ResourceGroupName</span></span>
<span data-ttu-id="a0d8a-119">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a0d8a-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a0d8a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d8a-120">CommonParameters</span></span>
<span data-ttu-id="a0d8a-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d8a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d8a-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d8a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d8a-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a0d8a-123">INPUTS</span></span>

### <span data-ttu-id="a0d8a-124">System. GUID</span><span class="sxs-lookup"><span data-stu-id="a0d8a-124">System.Guid</span></span>

### <span data-ttu-id="a0d8a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a0d8a-125">System.String</span></span>

## <span data-ttu-id="a0d8a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a0d8a-126">OUTPUTS</span></span>

### <span data-ttu-id="a0d8a-127">System. void</span><span class="sxs-lookup"><span data-stu-id="a0d8a-127">System.Void</span></span>

## <span data-ttu-id="a0d8a-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a0d8a-128">NOTES</span></span>

## <span data-ttu-id="a0d8a-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a0d8a-129">RELATED LINKS</span></span>

[<span data-ttu-id="a0d8a-130">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a0d8a-130">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="a0d8a-131">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="a0d8a-131">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="a0d8a-132">Currículo-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a0d8a-132">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="a0d8a-133">Suspender-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="a0d8a-133">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


