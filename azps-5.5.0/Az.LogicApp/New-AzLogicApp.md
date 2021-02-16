---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 4222b50ed941df6f84421cff867845b31744d9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113621"
---
# <span data-ttu-id="762a6-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="762a6-101">New-AzLogicApp</span></span>

## <span data-ttu-id="762a6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="762a6-102">SYNOPSIS</span></span>
<span data-ttu-id="762a6-103">Cria um aplicativo lógico em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="762a6-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="762a6-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="762a6-104">SYNTAX</span></span>

### <span data-ttu-id="762a6-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="762a6-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="762a6-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="762a6-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="762a6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="762a6-107">DESCRIPTION</span></span>
<span data-ttu-id="762a6-108">O **cmdlet New-Az LogicApp** cria um aplicativo lógico usando o recurso Aplicativos Lógicos.</span><span class="sxs-lookup"><span data-stu-id="762a6-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="762a6-109">Um aplicativo lógico é um conjunto de ações ou gatilhos definidos na definição do Aplicativo Lógico.</span><span class="sxs-lookup"><span data-stu-id="762a6-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="762a6-110">Este cmdlet retorna um objeto **Fluxo de** Trabalho.</span><span class="sxs-lookup"><span data-stu-id="762a6-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="762a6-111">Você pode criar um aplicativo lógico especificando um nome, um local, uma definição do Aplicativo Lógico, um grupo de recursos e um plano.</span><span class="sxs-lookup"><span data-stu-id="762a6-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="762a6-112">Uma definição e parâmetros do Aplicativo Lógico são formatados em Notação de Objeto JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="762a6-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="762a6-113">Você pode usar um aplicativo lógico como um modelo para definição e parâmetros.</span><span class="sxs-lookup"><span data-stu-id="762a6-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="762a6-114">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="762a6-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="762a6-115">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="762a6-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="762a6-116">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="762a6-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="762a6-117">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="762a6-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="762a6-118">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores de parâmetros de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="762a6-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="762a6-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="762a6-119">EXAMPLES</span></span>

### <span data-ttu-id="762a6-120">Exemplo 1: Criar um aplicativo lógico usando caminhos de arquivo de definição e parâmetros</span><span class="sxs-lookup"><span data-stu-id="762a6-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup1/providers/Microsoft.Logic/workflows/LogicApp1
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="762a6-121">Esse comando cria um aplicativo lógico no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="762a6-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="762a6-122">O aplicativo lógica inclui a definição e os parâmetros especificados por caminhos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="762a6-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="762a6-123">Exemplo 2: Criar um aplicativo lógico usando objetos de definição e parâmetros</span><span class="sxs-lookup"><span data-stu-id="762a6-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp05
Name                         : LogicApp05
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp05
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan1
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan1
Version                      : 08587489107859952120
```

<span data-ttu-id="762a6-124">Esse comando cria um aplicativo lógico no grupo de recursos de grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="762a6-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="762a6-125">Exemplo 3: Criar um aplicativo lógico usando o pipeline para especificar o grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="762a6-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp11
Name                         : LogicApp11
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp11
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="762a6-126">Esse comando obtém o grupo de recursos chamado ResourceGroup11 usando Get-AzResourceGroup cmdlet.</span><span class="sxs-lookup"><span data-stu-id="762a6-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="762a6-127">O comando passa esse grupo de recursos para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="762a6-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="762a6-128">O cmdlet atual cria um aplicativo lógico nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="762a6-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="762a6-129">O aplicativo lógica inclui a definição e os parâmetros especificados por caminhos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="762a6-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="762a6-130">Exemplo 4: Criar um aplicativo lógico com base em um aplicativo lógico existente</span><span class="sxs-lookup"><span data-stu-id="762a6-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp13
Name                         : LogicApp13
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp13
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : ServicePlan01
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan01
Version                      : 08587489107859952120
```

<span data-ttu-id="762a6-131">O primeiro comando obtém o aplicativo lógico chamado LogicApp03 usando Get-AzLogicApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="762a6-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="762a6-132">O comando armazena o aplicativo lógico na variável $Workflow dados.</span><span class="sxs-lookup"><span data-stu-id="762a6-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="762a6-133">O segundo comando cria um novo aplicativo lógico que usa a definição e os parâmetros do aplicativo lógico armazenados $Workflow.</span><span class="sxs-lookup"><span data-stu-id="762a6-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="762a6-134">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="762a6-134">PARAMETERS</span></span>

### <span data-ttu-id="762a6-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="762a6-135">-DefaultProfile</span></span>
<span data-ttu-id="762a6-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="762a6-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="762a6-137">-Definição</span><span class="sxs-lookup"><span data-stu-id="762a6-137">-Definition</span></span>
<span data-ttu-id="762a6-138">Especifica a definição do seu aplicativo lógico como um objeto ou uma cadeia de caracteres no formato de Notação de Objeto JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="762a6-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="762a6-139">-DefinitionFilePath</span></span>
<span data-ttu-id="762a6-140">Especifica a definição de um aplicativo lógico como o caminho de um arquivo de definição no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="762a6-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="762a6-141">-IntegrationAccountId</span></span>
<span data-ttu-id="762a6-142">Especifica uma ID de conta de integração para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="762a6-142">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-143">-Local</span><span class="sxs-lookup"><span data-stu-id="762a6-143">-Location</span></span>
<span data-ttu-id="762a6-144">Especifica o local do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="762a6-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="762a6-145">Insira um local de data center do Azure, como Oeste dos EUA ou Sudeste Asiático.</span><span class="sxs-lookup"><span data-stu-id="762a6-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="762a6-146">Você pode colocar um aplicativo lógico em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="762a6-146">You can place a logic app in any location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="762a6-147">-Name</span></span>
<span data-ttu-id="762a6-148">Especifica o nome do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="762a6-148">Specifies the name for the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="762a6-149">-ParameterFilePath</span></span>
<span data-ttu-id="762a6-150">Especifica o caminho de um arquivo de parâmetro formatado JSON.</span><span class="sxs-lookup"><span data-stu-id="762a6-150">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-151">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="762a6-151">-Parameters</span></span>
<span data-ttu-id="762a6-152">Especifica um objeto de conjunto de parâmetros para o aplicativo Logic.</span><span class="sxs-lookup"><span data-stu-id="762a6-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="762a6-153">Especifique uma tabela hash, dicionário \<string\> ou \<string, WorkflowParameter\> dicionário.</span><span class="sxs-lookup"><span data-stu-id="762a6-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="762a6-154">-ResourceGroupName</span></span>
<span data-ttu-id="762a6-155">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="762a6-155">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-156">-Estado</span><span class="sxs-lookup"><span data-stu-id="762a6-156">-State</span></span>
<span data-ttu-id="762a6-157">Especifica o estado do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="762a6-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="762a6-158">Os valores aceitáveis para este parâmetro são: Habilitado e Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="762a6-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-159">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="762a6-159">-Confirm</span></span>
<span data-ttu-id="762a6-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="762a6-160">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="762a6-161">-WhatIf</span></span>
<span data-ttu-id="762a6-162">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="762a6-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="762a6-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="762a6-163">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="762a6-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="762a6-164">CommonParameters</span></span>
<span data-ttu-id="762a6-165">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="762a6-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="762a6-166">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="762a6-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="762a6-167">Entradas</span><span class="sxs-lookup"><span data-stu-id="762a6-167">INPUTS</span></span>

### <span data-ttu-id="762a6-168">System.String</span><span class="sxs-lookup"><span data-stu-id="762a6-168">System.String</span></span>

## <span data-ttu-id="762a6-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="762a6-169">OUTPUTS</span></span>

### <span data-ttu-id="762a6-170">System.Object</span><span class="sxs-lookup"><span data-stu-id="762a6-170">System.Object</span></span>

## <span data-ttu-id="762a6-171">Notas</span><span class="sxs-lookup"><span data-stu-id="762a6-171">NOTES</span></span>

## <span data-ttu-id="762a6-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="762a6-172">RELATED LINKS</span></span>

[<span data-ttu-id="762a6-173">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="762a6-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="762a6-174">Remove-AzApp</span><span class="sxs-lookup"><span data-stu-id="762a6-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="762a6-175">Set-AzApp</span><span class="sxs-lookup"><span data-stu-id="762a6-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="762a6-176">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="762a6-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


