---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: a3b0b53146703a13f0ae8ea1627d2d9722c85eeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93597859"
---
# <span data-ttu-id="c6368-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6368-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="c6368-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6368-102">SYNOPSIS</span></span>
<span data-ttu-id="c6368-103">Obtém metadados para configurações de nó DSC na automação.</span><span class="sxs-lookup"><span data-stu-id="c6368-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="c6368-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6368-104">SYNTAX</span></span>

### <span data-ttu-id="c6368-105">ByAll (padrão)</span><span class="sxs-lookup"><span data-stu-id="c6368-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6368-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c6368-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6368-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c6368-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6368-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6368-108">DESCRIPTION</span></span>
<span data-ttu-id="c6368-109">O cmdlet **Get-AzAutomationDscNodeConfiguration** obtém metadados das configurações do nó DSC (configuração de estado desejado) do APS na automação do Azure.</span><span class="sxs-lookup"><span data-stu-id="c6368-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="c6368-110">A automação armazena a configuração do nó DSC como um documento de configuração do MOF (formato de objeto gerenciado).</span><span class="sxs-lookup"><span data-stu-id="c6368-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="c6368-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6368-111">EXAMPLES</span></span>

### <span data-ttu-id="c6368-112">Exemplo 1: obter todas as configurações do nó DSC</span><span class="sxs-lookup"><span data-stu-id="c6368-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c6368-113">Esse comando obtém metadados para todas as configurações de nó DSC na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c6368-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c6368-114">Exemplo 2: obter todas as configurações do nó DSC para uma configuração DSC</span><span class="sxs-lookup"><span data-stu-id="c6368-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="c6368-115">Esse comando obtém metadados para todas as configurações de nó DSC na conta de automação chamada Contoso17 que a configuração DSC nomeada ContosoConfiguration gerou.</span><span class="sxs-lookup"><span data-stu-id="c6368-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="c6368-116">Exemplo 3: obter uma configuração de nó DSC por nome</span><span class="sxs-lookup"><span data-stu-id="c6368-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="c6368-117">Esse comando obtém metadados para uma configuração de nó DSC com o nome ContosoConfiguration. WebServer na conta de automação chamada Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c6368-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c6368-118">OS</span><span class="sxs-lookup"><span data-stu-id="c6368-118">PARAMETERS</span></span>

### <span data-ttu-id="c6368-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c6368-119">-AutomationAccountName</span></span>
<span data-ttu-id="c6368-120">Especifica o nome de uma conta de automação que contém as configurações de nó DSC para as quais esse cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="c6368-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="c6368-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c6368-121">-ConfigurationName</span></span>
<span data-ttu-id="c6368-122">Especifica o nome da configuração DSC para a qual esse cmdlet obtém metadados de configuração de nó.</span><span class="sxs-lookup"><span data-stu-id="c6368-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="c6368-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6368-123">-DefaultProfile</span></span>
<span data-ttu-id="c6368-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c6368-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6368-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6368-125">-Name</span></span>
<span data-ttu-id="c6368-126">Especifica o nome da configuração do nó DSC para a qual esse cmdlet obtém metadados.</span><span class="sxs-lookup"><span data-stu-id="c6368-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="c6368-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6368-127">-ResourceGroupName</span></span>
<span data-ttu-id="c6368-128">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c6368-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="c6368-129">Esse cmdlet obtém metadados para configurações de nó DSC no grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="c6368-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6368-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="c6368-130">-RollupStatus</span></span>
<span data-ttu-id="c6368-131">Especifica o status de acúmulo das configurações de nó DSC que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="c6368-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="c6368-132">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="c6368-132">Valid values are:</span></span> 
- <span data-ttu-id="c6368-133">Mal</span><span class="sxs-lookup"><span data-stu-id="c6368-133">Bad</span></span> 
- <span data-ttu-id="c6368-134">Corretamente</span><span class="sxs-lookup"><span data-stu-id="c6368-134">Good</span></span>

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

### <span data-ttu-id="c6368-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6368-135">CommonParameters</span></span>
<span data-ttu-id="c6368-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6368-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6368-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6368-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6368-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6368-138">INPUTS</span></span>

### <span data-ttu-id="c6368-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6368-139">System.String</span></span>

## <span data-ttu-id="c6368-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6368-140">OUTPUTS</span></span>

### <span data-ttu-id="c6368-141">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="c6368-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="c6368-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6368-142">NOTES</span></span>

## <span data-ttu-id="c6368-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6368-143">RELATED LINKS</span></span>

[<span data-ttu-id="c6368-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6368-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


