---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSourceControl.md
ms.openlocfilehash: 051eee1c191662e6ca4eb56e34088af651ea69f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901346"
---
# <span data-ttu-id="e3d42-101">Get-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="e3d42-101">Get-AzAutomationSourceControl</span></span>

## <span data-ttu-id="e3d42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d42-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d42-103">Obtém uma lista de controles de origem de automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d42-103">Gets a list of Azure Automation source controls.</span></span>

## <span data-ttu-id="e3d42-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3d42-104">SYNTAX</span></span>

### <span data-ttu-id="e3d42-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e3d42-105">ByAll (Default)</span></span>
```
Get-AzAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3d42-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e3d42-106">ByName</span></span>
```
Get-AzAutomationSourceControl -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3d42-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3d42-107">DESCRIPTION</span></span>
<span data-ttu-id="e3d42-108">O Get-AzAutomationSourceControl cmdlet obtém controles de origem de automação.</span><span class="sxs-lookup"><span data-stu-id="e3d42-108">The Get-AzAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="e3d42-109">Para obter um controle de origem específico, especifique seu nome.</span><span class="sxs-lookup"><span data-stu-id="e3d42-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="e3d42-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3d42-110">EXAMPLES</span></span>

### <span data-ttu-id="e3d42-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e3d42-111">Example 1</span></span>
<span data-ttu-id="e3d42-112">Este comando obtém um controle de origem de automação chamado VSTSNative na conta chamada devAccount.</span><span class="sxs-lookup"><span data-stu-id="e3d42-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="e3d42-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3d42-113">PARAMETERS</span></span>

### <span data-ttu-id="e3d42-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e3d42-114">-AutomationAccountName</span></span>
<span data-ttu-id="e3d42-115">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="e3d42-115">The automation account name.</span></span>

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

### <span data-ttu-id="e3d42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d42-116">-DefaultProfile</span></span>
<span data-ttu-id="e3d42-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d42-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d42-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e3d42-118">-Name</span></span>
<span data-ttu-id="e3d42-119">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="e3d42-119">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3d42-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d42-120">-ResourceGroupName</span></span>
<span data-ttu-id="e3d42-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e3d42-121">The resource group name.</span></span>

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

### <span data-ttu-id="e3d42-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="e3d42-122">-SourceType</span></span>
<span data-ttu-id="e3d42-123">O tipo de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="e3d42-123">The source control type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: GitHub, VsoGit, VsoTfvc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3d42-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d42-124">CommonParameters</span></span>
<span data-ttu-id="e3d42-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d42-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d42-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3d42-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d42-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3d42-127">INPUTS</span></span>

### <span data-ttu-id="e3d42-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e3d42-128">System.String</span></span>

## <span data-ttu-id="e3d42-129">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3d42-129">OUTPUTS</span></span>

### <span data-ttu-id="e3d42-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span><span class="sxs-lookup"><span data-stu-id="e3d42-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="e3d42-131">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3d42-131">NOTES</span></span>

## <span data-ttu-id="e3d42-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3d42-132">RELATED LINKS</span></span>
