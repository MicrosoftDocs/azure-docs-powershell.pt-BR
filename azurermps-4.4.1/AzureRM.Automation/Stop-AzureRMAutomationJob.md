---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BE1A9247-9F8E-45EA-9590-684A5A5662AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Stop-AzureRMAutomationJob.md
ms.openlocfilehash: db7e76a21f635429be598ca9f40899ece3fa0406
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440219"
---
# <span data-ttu-id="371aa-101">Stop-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="371aa-101">Stop-AzureRmAutomationJob</span></span>

## <span data-ttu-id="371aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="371aa-102">SYNOPSIS</span></span>
<span data-ttu-id="371aa-103">Interrompe um trabalho de automação.</span><span class="sxs-lookup"><span data-stu-id="371aa-103">Stops an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="371aa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="371aa-104">SYNTAX</span></span>

```
Stop-AzureRmAutomationJob [-Id] <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="371aa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="371aa-105">DESCRIPTION</span></span>
<span data-ttu-id="371aa-106">O cmdlet **Stop-AzureRmAutomationJob** interrompe um trabalho de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="371aa-106">The **Stop-AzureRmAutomationJob** cmdlet stops an Azure Automation job.</span></span>
<span data-ttu-id="371aa-107">Especifique um trabalho de automação em execução.</span><span class="sxs-lookup"><span data-stu-id="371aa-107">Specify a running Automation job.</span></span>

## <span data-ttu-id="371aa-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="371aa-108">EXAMPLES</span></span>

### <span data-ttu-id="371aa-109">Exemplo 1: parar um trabalho</span><span class="sxs-lookup"><span data-stu-id="371aa-109">Example 1: Stop a job</span></span>
```
PS C:\>Stop-AzureRmAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="371aa-110">Esse comando para o trabalho que tem a ID especificada.</span><span class="sxs-lookup"><span data-stu-id="371aa-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="371aa-111">OS</span><span class="sxs-lookup"><span data-stu-id="371aa-111">PARAMETERS</span></span>

### <span data-ttu-id="371aa-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="371aa-112">-AutomationAccountName</span></span>
<span data-ttu-id="371aa-113">Especifica o nome de uma conta de automação na qual esse cmdlet interrompe um trabalho.</span><span class="sxs-lookup"><span data-stu-id="371aa-113">Specifies the name of an Automation account in which this cmdlet stops a job.</span></span>

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

### <span data-ttu-id="371aa-114">-ID</span><span class="sxs-lookup"><span data-stu-id="371aa-114">-Id</span></span>
<span data-ttu-id="371aa-115">Especifica a ID de um trabalho que este cmdlet interrompe.</span><span class="sxs-lookup"><span data-stu-id="371aa-115">Specifies the ID of a job that this cmdlet stops.</span></span>

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

### <span data-ttu-id="371aa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="371aa-116">-ResourceGroupName</span></span>
<span data-ttu-id="371aa-117">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="371aa-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="371aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="371aa-118">-DefaultProfile</span></span>
<span data-ttu-id="371aa-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="371aa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="371aa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371aa-120">CommonParameters</span></span>
<span data-ttu-id="371aa-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="371aa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371aa-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="371aa-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371aa-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="371aa-123">INPUTS</span></span>

## <span data-ttu-id="371aa-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="371aa-124">OUTPUTS</span></span>

## <span data-ttu-id="371aa-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="371aa-125">NOTES</span></span>

## <span data-ttu-id="371aa-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="371aa-126">RELATED LINKS</span></span>

[<span data-ttu-id="371aa-127">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="371aa-127">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="371aa-128">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="371aa-128">Get-AzureRmAutomationJobOutput</span></span>](./Get-AzureRMAutomationJobOutput.md)

[<span data-ttu-id="371aa-129">Currículo-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="371aa-129">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="371aa-130">Suspender-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="371aa-130">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


