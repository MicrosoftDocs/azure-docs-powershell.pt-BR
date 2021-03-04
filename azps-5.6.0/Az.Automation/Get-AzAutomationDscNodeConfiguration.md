---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: b139ed5b67bbc36bad45ab2528ed74299d40c1b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887600"
---
# <span data-ttu-id="357a6-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="357a6-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="357a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="357a6-102">SYNOPSIS</span></span>
<span data-ttu-id="357a6-103">Obtém metadados para configurações de nó DSC em Automação.</span><span class="sxs-lookup"><span data-stu-id="357a6-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="357a6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="357a6-104">SYNTAX</span></span>

### <span data-ttu-id="357a6-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="357a6-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="357a6-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="357a6-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="357a6-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="357a6-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="357a6-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="357a6-108">DESCRIPTION</span></span>
<span data-ttu-id="357a6-109">O cmdlet **Get-AzAutomationDscNodeConfiguration** obtém metadados para configurações de nó DSC (Configuração de Estado Desejado) do APS no Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="357a6-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="357a6-110">A automação armazena a configuração do nó DSC como um documento de configuração do Formato de Objeto Gerenciado (MOF).</span><span class="sxs-lookup"><span data-stu-id="357a6-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="357a6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="357a6-111">EXAMPLES</span></span>

### <span data-ttu-id="357a6-112">Exemplo 1: Obter todas as configurações de nó DSC</span><span class="sxs-lookup"><span data-stu-id="357a6-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="357a6-113">Este comando obtém metadados para todas as configurações de nó DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="357a6-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="357a6-114">Exemplo 2: Obter todas as configurações de nó DSC para uma configuração DSC</span><span class="sxs-lookup"><span data-stu-id="357a6-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="357a6-115">Este comando obtém metadados para todas as configurações de nó DSC na conta de automação chamada Contoso17 que a configuração DSC denominada ContosoConfiguration gerou.</span><span class="sxs-lookup"><span data-stu-id="357a6-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="357a6-116">Exemplo 3: Obter uma configuração de nó DSC pelo nome</span><span class="sxs-lookup"><span data-stu-id="357a6-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="357a6-117">Este comando obtém metadados para uma configuração de nó DSC com o nome ContosoConfiguration.webserver na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="357a6-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="357a6-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="357a6-118">PARAMETERS</span></span>

### <span data-ttu-id="357a6-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="357a6-119">-AutomationAccountName</span></span>
<span data-ttu-id="357a6-120">Especifica o nome de uma conta de automação que contém as configurações de nó DSC para as quais esse cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="357a6-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="357a6-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="357a6-121">-ConfigurationName</span></span>
<span data-ttu-id="357a6-122">Especifica o nome da configuração DSC para a qual este cmdlet obtém metadados de configuração do nó.</span><span class="sxs-lookup"><span data-stu-id="357a6-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357a6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357a6-123">-DefaultProfile</span></span>
<span data-ttu-id="357a6-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="357a6-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="357a6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="357a6-125">-Name</span></span>
<span data-ttu-id="357a6-126">Especifica o nome da configuração do nó DSC para a qual este cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="357a6-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="357a6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="357a6-127">-ResourceGroupName</span></span>
<span data-ttu-id="357a6-128">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="357a6-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="357a6-129">Este cmdlet obtém metadados para configurações de nó DSC no grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="357a6-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="357a6-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="357a6-130">-RollupStatus</span></span>
<span data-ttu-id="357a6-131">Especifica o status de acúmulo das configurações de nó DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="357a6-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="357a6-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="357a6-132">Valid values are:</span></span> 
- <span data-ttu-id="357a6-133">Bad</span><span class="sxs-lookup"><span data-stu-id="357a6-133">Bad</span></span> 
- <span data-ttu-id="357a6-134">Bom</span><span class="sxs-lookup"><span data-stu-id="357a6-134">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="357a6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357a6-135">CommonParameters</span></span>
<span data-ttu-id="357a6-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="357a6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357a6-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="357a6-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357a6-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="357a6-138">INPUTS</span></span>

### <span data-ttu-id="357a6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="357a6-139">System.String</span></span>

## <span data-ttu-id="357a6-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="357a6-140">OUTPUTS</span></span>

### <span data-ttu-id="357a6-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="357a6-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="357a6-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="357a6-142">NOTES</span></span>

## <span data-ttu-id="357a6-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="357a6-143">RELATED LINKS</span></span>

[<span data-ttu-id="357a6-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="357a6-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


