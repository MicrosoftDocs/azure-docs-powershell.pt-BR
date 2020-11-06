---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 3e7affd09e8c24c1d3c1759e78ea09a0c849ff32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432808"
---
# <span data-ttu-id="ef4c4-101">Get-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="ef4c4-101">Get-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="ef4c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ef4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4c4-103">Obtém uma lista de controles de origem da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-103">Gets a list of Azure Automation source controls.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef4c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef4c4-104">SYNTAX</span></span>

### <span data-ttu-id="ef4c4-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="ef4c4-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSourceControl [-SourceType <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef4c4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ef4c4-106">ByName</span></span>
```
Get-AzureRmAutomationSourceControl -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef4c4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ef4c4-107">DESCRIPTION</span></span>
<span data-ttu-id="ef4c4-108">O cmdlet Get-AzureRmAutomationSourceControl Obtém controles de fonte de automação.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-108">The Get-AzureRmAutomationSourceControl cmdlet gets Automation source controls.</span></span>
<span data-ttu-id="ef4c4-109">Para obter um controle de origem específico, especifique o nome.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-109">To get a specific source control, specify its name.</span></span>

## <span data-ttu-id="ef4c4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef4c4-110">EXAMPLES</span></span>

### <span data-ttu-id="ef4c4-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ef4c4-111">Example 1</span></span>
<span data-ttu-id="ef4c4-112">Esse comando obtém um controle de origem de automação chamado VSTSNative na conta chamada devAccount.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-112">This command gets an Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
PS C:\> Get-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                           -AutomationAccountName "devAccount" `
                                           -Name "VSTSNative" 


Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    True           https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="ef4c4-113">OS</span><span class="sxs-lookup"><span data-stu-id="ef4c4-113">PARAMETERS</span></span>

### <span data-ttu-id="ef4c4-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ef4c4-114">-AutomationAccountName</span></span>
<span data-ttu-id="ef4c4-115">O nome da conta de automação.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-115">The automation account name.</span></span>

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

### <span data-ttu-id="ef4c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4c4-116">-DefaultProfile</span></span>
<span data-ttu-id="ef4c4-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4c4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef4c4-118">-Name</span></span>
<span data-ttu-id="ef4c4-119">O nome do controle de origem.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-119">The source control name.</span></span>

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

### <span data-ttu-id="ef4c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="ef4c4-121">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-121">The resource group name.</span></span>

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

### <span data-ttu-id="ef4c4-122">-SourceType</span><span class="sxs-lookup"><span data-stu-id="ef4c4-122">-SourceType</span></span>
<span data-ttu-id="ef4c4-123">O tipo de controle de origem.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-123">The source control type.</span></span>

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

### <span data-ttu-id="ef4c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4c4-124">CommonParameters</span></span>
<span data-ttu-id="ef4c4-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4c4-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4c4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4c4-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ef4c4-127">INPUTS</span></span>

### <span data-ttu-id="ef4c4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ef4c4-128">System.String</span></span>

## <span data-ttu-id="ef4c4-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ef4c4-129">OUTPUTS</span></span>

### <span data-ttu-id="ef4c4-130">Microsoft. Azure. Commands. Automation. Model. SourceControl</span><span class="sxs-lookup"><span data-stu-id="ef4c4-130">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="ef4c4-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ef4c4-131">NOTES</span></span>

## <span data-ttu-id="ef4c4-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef4c4-132">RELATED LINKS</span></span>
