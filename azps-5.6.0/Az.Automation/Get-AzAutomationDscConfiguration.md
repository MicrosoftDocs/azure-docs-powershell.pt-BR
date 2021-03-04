---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 82c853f6f18f12c1e7005a859a5df924d3555b79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890665"
---
# <span data-ttu-id="b473e-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b473e-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="b473e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b473e-102">SYNOPSIS</span></span>
<span data-ttu-id="b473e-103">Obtém configurações de DSC da Automação.</span><span class="sxs-lookup"><span data-stu-id="b473e-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="b473e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b473e-104">SYNTAX</span></span>

### <span data-ttu-id="b473e-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b473e-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b473e-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b473e-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b473e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b473e-107">DESCRIPTION</span></span>
<span data-ttu-id="b473e-108">O cmdlet **Get-AzAutomationDscConfiguration** obtém as configurações de DSC (Configuração de Estado Desejado) do Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b473e-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="b473e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b473e-109">EXAMPLES</span></span>

### <span data-ttu-id="b473e-110">Exemplo 1: Obter todas as configurações do DSC</span><span class="sxs-lookup"><span data-stu-id="b473e-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b473e-111">Este comando obtém metadados para todas as configurações de DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b473e-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b473e-112">Exemplo 2: Obter uma configuração DSC pelo nome</span><span class="sxs-lookup"><span data-stu-id="b473e-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="b473e-113">Este comando obtém metadados para uma configuração DSC chamada MyConfiguration na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b473e-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b473e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b473e-114">PARAMETERS</span></span>

### <span data-ttu-id="b473e-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b473e-115">-AutomationAccountName</span></span>
<span data-ttu-id="b473e-116">Especifica o nome da conta de automação que contém configurações de DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b473e-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b473e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b473e-117">-DefaultProfile</span></span>
<span data-ttu-id="b473e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b473e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b473e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b473e-119">-Name</span></span>
<span data-ttu-id="b473e-120">Especifica o nome da configuração DSC que este cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="b473e-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b473e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b473e-121">-ResourceGroupName</span></span>
<span data-ttu-id="b473e-122">Especifica o nome de um grupo de recursos para o qual este cmdlet obtém configurações de DSC.</span><span class="sxs-lookup"><span data-stu-id="b473e-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="b473e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b473e-123">CommonParameters</span></span>
<span data-ttu-id="b473e-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b473e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b473e-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b473e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b473e-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b473e-126">INPUTS</span></span>

### <span data-ttu-id="b473e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b473e-127">System.String</span></span>

## <span data-ttu-id="b473e-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b473e-128">OUTPUTS</span></span>

### <span data-ttu-id="b473e-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b473e-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="b473e-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="b473e-130">NOTES</span></span>

## <span data-ttu-id="b473e-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b473e-131">RELATED LINKS</span></span>

[<span data-ttu-id="b473e-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b473e-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="b473e-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="b473e-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


