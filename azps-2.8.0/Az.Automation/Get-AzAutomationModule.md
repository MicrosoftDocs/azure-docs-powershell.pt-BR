---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 54bbda0226cf2aa374e149bc4b5885b86b31ef12
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597840"
---
# <span data-ttu-id="d3ad4-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d3ad4-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="d3ad4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3ad4-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ad4-103">Obtém metadados para módulos da automação.</span><span class="sxs-lookup"><span data-stu-id="d3ad4-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="d3ad4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3ad4-104">SYNTAX</span></span>

### <span data-ttu-id="d3ad4-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3ad4-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3ad4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d3ad4-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3ad4-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3ad4-107">DESCRIPTION</span></span>
<span data-ttu-id="d3ad4-108">O cmdlet **Get-AzAutomationModule** obtém metadados para módulos da automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ad4-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="d3ad4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3ad4-109">EXAMPLES</span></span>

### <span data-ttu-id="d3ad4-110">Exemplo 1: obter todos os módulos</span><span class="sxs-lookup"><span data-stu-id="d3ad4-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d3ad4-111">Esse comando obtém todos os módulos na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d3ad4-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d3ad4-112">Exemplo 2: obter um módulo</span><span class="sxs-lookup"><span data-stu-id="d3ad4-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d3ad4-113">Esse comando obtém um módulo chamado ContosoModule na conta de automação chamado Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d3ad4-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d3ad4-114">OS</span><span class="sxs-lookup"><span data-stu-id="d3ad4-114">PARAMETERS</span></span>

### <span data-ttu-id="d3ad4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d3ad4-115">-AutomationAccountName</span></span>
<span data-ttu-id="d3ad4-116">Especifica o nome da conta de automação para a qual esse cmdlet obtém metadados de módulo.</span><span class="sxs-lookup"><span data-stu-id="d3ad4-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="d3ad4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ad4-117">-DefaultProfile</span></span>
<span data-ttu-id="d3ad4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d3ad4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3ad4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3ad4-119">-Name</span></span>
<span data-ttu-id="d3ad4-120">Especifica o nome do módulo para o qual esse cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="d3ad4-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="d3ad4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3ad4-121">-ResourceGroupName</span></span>
<span data-ttu-id="d3ad4-122">Especifica o nome de um grupo de recursos para o qual esse cmdlet obtém metadados de módulo.</span><span class="sxs-lookup"><span data-stu-id="d3ad4-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="d3ad4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ad4-123">CommonParameters</span></span>
<span data-ttu-id="d3ad4-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ad4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ad4-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ad4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ad4-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3ad4-126">INPUTS</span></span>

### <span data-ttu-id="d3ad4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d3ad4-127">System.String</span></span>

## <span data-ttu-id="d3ad4-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3ad4-128">OUTPUTS</span></span>

### <span data-ttu-id="d3ad4-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="d3ad4-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="d3ad4-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3ad4-130">NOTES</span></span>

## <span data-ttu-id="d3ad4-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3ad4-131">RELATED LINKS</span></span>

[<span data-ttu-id="d3ad4-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d3ad4-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="d3ad4-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d3ad4-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="d3ad4-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d3ad4-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


