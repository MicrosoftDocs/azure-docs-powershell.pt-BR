---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117011"
---
# <span data-ttu-id="a19aa-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a19aa-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="a19aa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a19aa-102">SYNOPSIS</span></span>
<span data-ttu-id="a19aa-103">Obtém metadados para configurações de nó DSC em Automação.</span><span class="sxs-lookup"><span data-stu-id="a19aa-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="a19aa-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a19aa-104">SYNTAX</span></span>

### <span data-ttu-id="a19aa-105">ByAll (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a19aa-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a19aa-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a19aa-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a19aa-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a19aa-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a19aa-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a19aa-108">DESCRIPTION</span></span>
<span data-ttu-id="a19aa-109">O cmdlet **Get-AzAutomationDscNodeConfiguration** obtém metadados para configurações de nó DSC (Configuração de Estado Desejado) APS na Automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="a19aa-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="a19aa-110">A automação armazena a configuração do nó DSC como um documento de configuração MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="a19aa-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="a19aa-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a19aa-111">EXAMPLES</span></span>

### <span data-ttu-id="a19aa-112">Exemplo 1: Obter todas as configurações de nó DSC</span><span class="sxs-lookup"><span data-stu-id="a19aa-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="a19aa-113">Esse comando obtém metadados para todas as configurações de nó DSC na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a19aa-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="a19aa-114">Exemplo 2: Obter todas as configurações de nó DSC para uma configuração de DSC</span><span class="sxs-lookup"><span data-stu-id="a19aa-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="a19aa-115">Esse comando obtém metadados para todas as configurações de nó DSC na conta automação chamada Contoso17 gerada pela configuração DSC chamada ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a19aa-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="a19aa-116">Exemplo 3: Obter uma configuração de nó DSC por nome</span><span class="sxs-lookup"><span data-stu-id="a19aa-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="a19aa-117">Esse comando obtém metadados para uma configuração de nó DSC com o nome ContosoConfiguration.webserver na conta automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a19aa-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a19aa-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a19aa-118">PARAMETERS</span></span>

### <span data-ttu-id="a19aa-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a19aa-119">-AutomationAccountName</span></span>
<span data-ttu-id="a19aa-120">Especifica o nome de uma conta de Automação que contém as configurações de nó DSC para as quais esse cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="a19aa-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="a19aa-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a19aa-121">-ConfigurationName</span></span>
<span data-ttu-id="a19aa-122">Especifica o nome da configuração DSC para a qual este cmdlet obtém metadados de configuração do nó.</span><span class="sxs-lookup"><span data-stu-id="a19aa-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="a19aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19aa-123">-DefaultProfile</span></span>
<span data-ttu-id="a19aa-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="a19aa-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a19aa-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a19aa-125">-Name</span></span>
<span data-ttu-id="a19aa-126">Especifica o nome da configuração do nó DSC para a qual este cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="a19aa-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="a19aa-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a19aa-127">-ResourceGroupName</span></span>
<span data-ttu-id="a19aa-128">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a19aa-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a19aa-129">Esse cmdlet obtém metadados para configurações de nó DSC no grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a19aa-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a19aa-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="a19aa-130">-RollupStatus</span></span>
<span data-ttu-id="a19aa-131">Especifica o status de pacote de configurações de nó DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="a19aa-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="a19aa-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="a19aa-132">Valid values are:</span></span> 
- <span data-ttu-id="a19aa-133">Ruim</span><span class="sxs-lookup"><span data-stu-id="a19aa-133">Bad</span></span> 
- <span data-ttu-id="a19aa-134">Bom</span><span class="sxs-lookup"><span data-stu-id="a19aa-134">Good</span></span>

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

### <span data-ttu-id="a19aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19aa-135">CommonParameters</span></span>
<span data-ttu-id="a19aa-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19aa-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a19aa-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19aa-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="a19aa-138">INPUTS</span></span>

### <span data-ttu-id="a19aa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a19aa-139">System.String</span></span>

## <span data-ttu-id="a19aa-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="a19aa-140">OUTPUTS</span></span>

### <span data-ttu-id="a19aa-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="a19aa-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="a19aa-142">Notas</span><span class="sxs-lookup"><span data-stu-id="a19aa-142">NOTES</span></span>

## <span data-ttu-id="a19aa-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a19aa-143">RELATED LINKS</span></span>

[<span data-ttu-id="a19aa-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a19aa-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


