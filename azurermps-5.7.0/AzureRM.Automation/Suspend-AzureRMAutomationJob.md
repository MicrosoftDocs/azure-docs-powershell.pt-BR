---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FF44BCD2-AD8E-4F5C-AB10-BD6BD69E7F45
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/suspend-azurermautomationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Suspend-AzureRMAutomationJob.md
ms.openlocfilehash: 05747721219610524e0a245df5b5a67e8e69b483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432969"
---
# <span data-ttu-id="21c69-101">Suspend-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="21c69-101">Suspend-AzureRmAutomationJob</span></span>

## <span data-ttu-id="21c69-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="21c69-102">SYNOPSIS</span></span>
<span data-ttu-id="21c69-103">Suspende um trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="21c69-103">Suspends an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21c69-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21c69-104">SYNTAX</span></span>

```
Suspend-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21c69-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="21c69-105">DESCRIPTION</span></span>
<span data-ttu-id="21c69-106">O cmdlet **Suspend-AzureRmAutomationJob** suspende um trabalho de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="21c69-106">The **Suspend-AzureRmAutomationJob** cmdlet suspends an Azure Automation job.</span></span>
<span data-ttu-id="21c69-107">Especifique um trabalho de automação em execução.</span><span class="sxs-lookup"><span data-stu-id="21c69-107">Specify a running Automation job.</span></span>

<span data-ttu-id="21c69-108">Para retomar um trabalho suspenso, use o cmdlet Resume-AzureRmAutomationJob.</span><span class="sxs-lookup"><span data-stu-id="21c69-108">To resume a suspended job, use the Resume-AzureRmAutomationJob cmdlet.</span></span>

## <span data-ttu-id="21c69-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="21c69-109">EXAMPLES</span></span>

### <span data-ttu-id="21c69-110">Exemplo 1: suspender um trabalho</span><span class="sxs-lookup"><span data-stu-id="21c69-110">Example 1: Suspend a job</span></span>
```
PS C:\>Suspend-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="21c69-111">Esse comando suspende o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="21c69-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="21c69-112">OS</span><span class="sxs-lookup"><span data-stu-id="21c69-112">PARAMETERS</span></span>

### <span data-ttu-id="21c69-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="21c69-113">-AutomationAccountName</span></span>
<span data-ttu-id="21c69-114">Especifica o nome de uma conta de automação na qual esse cmdlet suspende um trabalho.</span><span class="sxs-lookup"><span data-stu-id="21c69-114">Specifies the name of an Automation account in which this cmdlet suspends a job.</span></span>

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

### <span data-ttu-id="21c69-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c69-115">-DefaultProfile</span></span>
<span data-ttu-id="21c69-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="21c69-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21c69-117">-ID</span><span class="sxs-lookup"><span data-stu-id="21c69-117">-Id</span></span>
<span data-ttu-id="21c69-118">Especifica a ID de um trabalho que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="21c69-118">Specifies the ID of a job that this cmdlet suspends.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21c69-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c69-119">-ResourceGroupName</span></span>
<span data-ttu-id="21c69-120">Especifica a ID de um trabalho que este cmdlet suspende.</span><span class="sxs-lookup"><span data-stu-id="21c69-120">Specifies the ID of a job that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="21c69-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c69-121">CommonParameters</span></span>
<span data-ttu-id="21c69-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c69-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c69-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c69-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c69-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="21c69-124">INPUTS</span></span>

### <span data-ttu-id="21c69-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="21c69-125">None</span></span>
<span data-ttu-id="21c69-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="21c69-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21c69-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="21c69-127">OUTPUTS</span></span>

## <span data-ttu-id="21c69-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="21c69-128">NOTES</span></span>

## <span data-ttu-id="21c69-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="21c69-129">RELATED LINKS</span></span>

[<span data-ttu-id="21c69-130">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="21c69-130">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="21c69-131">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="21c69-131">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="21c69-132">Currículo-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="21c69-132">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="21c69-133">Parar-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="21c69-133">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)


