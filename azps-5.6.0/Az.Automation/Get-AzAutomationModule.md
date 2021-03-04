---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 978e1bf2e826e576745748c43249bf8257f129cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901364"
---
# <span data-ttu-id="644cb-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="644cb-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="644cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="644cb-102">SYNOPSIS</span></span>
<span data-ttu-id="644cb-103">Obtém metadados para módulos de Automação.</span><span class="sxs-lookup"><span data-stu-id="644cb-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="644cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="644cb-104">SYNTAX</span></span>

### <span data-ttu-id="644cb-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="644cb-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="644cb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="644cb-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="644cb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="644cb-107">DESCRIPTION</span></span>
<span data-ttu-id="644cb-108">O cmdlet **Get-AzAutomationModule** obtém metadados para módulos do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="644cb-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="644cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="644cb-109">EXAMPLES</span></span>

### <span data-ttu-id="644cb-110">Exemplo 1: Obter todos os módulos</span><span class="sxs-lookup"><span data-stu-id="644cb-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="644cb-111">Este comando obtém todos os módulos na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="644cb-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="644cb-112">Exemplo 2: Obter um módulo</span><span class="sxs-lookup"><span data-stu-id="644cb-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="644cb-113">Este comando obtém um módulo chamado ContosoModule na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="644cb-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="644cb-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="644cb-114">PARAMETERS</span></span>

### <span data-ttu-id="644cb-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="644cb-115">-AutomationAccountName</span></span>
<span data-ttu-id="644cb-116">Especifica o nome da conta de automação para a qual este cmdlet obtém metadados do módulo.</span><span class="sxs-lookup"><span data-stu-id="644cb-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="644cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="644cb-117">-DefaultProfile</span></span>
<span data-ttu-id="644cb-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="644cb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="644cb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="644cb-119">-Name</span></span>
<span data-ttu-id="644cb-120">Especifica o nome do módulo para o qual este cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="644cb-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="644cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="644cb-122">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém metadados do módulo.</span><span class="sxs-lookup"><span data-stu-id="644cb-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="644cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644cb-123">CommonParameters</span></span>
<span data-ttu-id="644cb-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="644cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644cb-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="644cb-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644cb-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="644cb-126">INPUTS</span></span>

### <span data-ttu-id="644cb-127">System.String</span><span class="sxs-lookup"><span data-stu-id="644cb-127">System.String</span></span>

## <span data-ttu-id="644cb-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="644cb-128">OUTPUTS</span></span>

### <span data-ttu-id="644cb-129">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="644cb-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="644cb-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="644cb-130">NOTES</span></span>

## <span data-ttu-id="644cb-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="644cb-131">RELATED LINKS</span></span>

[<span data-ttu-id="644cb-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="644cb-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="644cb-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="644cb-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="644cb-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="644cb-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


