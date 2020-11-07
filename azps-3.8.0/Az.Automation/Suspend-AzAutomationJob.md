---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/suspend-azautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Suspend-AzAutomationJob.md
ms.openlocfilehash: 3aecdb18579f46722a73e3de538f5f3c929b606f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944654"
---
# <span data-ttu-id="da7c0-101">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="da7c0-101">Suspend-AzAutomationJob</span></span>

## <span data-ttu-id="da7c0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da7c0-102">SYNOPSIS</span></span>
<span data-ttu-id="da7c0-103">Suspende um trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="da7c0-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="da7c0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da7c0-104">SYNTAX</span></span>

```
Suspend-AzAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da7c0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da7c0-105">DESCRIPTION</span></span>
<span data-ttu-id="da7c0-106">O cmdlet **Suspend-AzAutomationJob** suspende um trabalho de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="da7c0-106">The **Suspend-AzAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="da7c0-107">Especifique um trabalho de automação em execução.</span><span class="sxs-lookup"><span data-stu-id="da7c0-107">Specify a running Automation job.</span></span>
<span data-ttu-id="da7c0-108">Para retomar um trabalho suspenso, use o cmdlet Resume-AzAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="da7c0-108">To resume a suspended job, use the Resume-AzAutomationJob cmdlet.</span></span>

## <span data-ttu-id="da7c0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da7c0-109">EXAMPLES</span></span>

### <span data-ttu-id="da7c0-110">Exemplo 1: suspender um trabalho</span><span class="sxs-lookup"><span data-stu-id="da7c0-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="da7c0-111">Esse comando suspende o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="da7c0-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="da7c0-112">OS</span><span class="sxs-lookup"><span data-stu-id="da7c0-112">PARAMETERS</span></span>

### <span data-ttu-id="da7c0-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da7c0-113">-AutomationAccountName</span></span>
<span data-ttu-id="da7c0-114">Especifica o nome de uma conta de automação na qual esse cmdlet suspende um trabalho.</span><span class="sxs-lookup"><span data-stu-id="da7c0-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="da7c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7c0-115">-DefaultProfile</span></span>
<span data-ttu-id="da7c0-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="da7c0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da7c0-117">-ID</span><span class="sxs-lookup"><span data-stu-id="da7c0-117">-Id</span></span>
<span data-ttu-id="da7c0-118">Especifica a ID de um trabalho que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="da7c0-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="da7c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da7c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="da7c0-120">Especifica a ID de um trabalho que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="da7c0-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="da7c0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7c0-121">CommonParameters</span></span>
<span data-ttu-id="da7c0-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7c0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7c0-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da7c0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7c0-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da7c0-124">INPUTS</span></span>

### <span data-ttu-id="da7c0-125">System. GUID</span><span class="sxs-lookup"><span data-stu-id="da7c0-125">System.Guid</span></span>

### <span data-ttu-id="da7c0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="da7c0-126">System.String</span></span>

## <span data-ttu-id="da7c0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da7c0-127">OUTPUTS</span></span>

### <span data-ttu-id="da7c0-128">System. void</span><span class="sxs-lookup"><span data-stu-id="da7c0-128">System.Void</span></span>

## <span data-ttu-id="da7c0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da7c0-129">NOTES</span></span>

## <span data-ttu-id="da7c0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da7c0-130">RELATED LINKS</span></span>

[<span data-ttu-id="da7c0-131">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="da7c0-131">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="da7c0-132">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="da7c0-132">Get-AzAutomationJobOutput</span></span>](./Get-AzAutomationJobOutput.md)

[<span data-ttu-id="da7c0-133">Currículo-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="da7c0-133">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="da7c0-134">Parar-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="da7c0-134">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)


