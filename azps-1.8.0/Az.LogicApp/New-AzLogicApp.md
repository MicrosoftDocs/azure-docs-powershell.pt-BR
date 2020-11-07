---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzLogicApp.md
ms.openlocfilehash: 638bb3821cac8ea2f8e5b97656c1fff14b88621f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770496"
---
# <span data-ttu-id="1cfc2-101">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1cfc2-101">New-AzLogicApp</span></span>

## <span data-ttu-id="1cfc2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1cfc2-102">SYNOPSIS</span></span>
<span data-ttu-id="1cfc2-103">Cria um aplicativo lógico em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-103">Creates a logic app in a resource group.</span></span>

## <span data-ttu-id="1cfc2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cfc2-104">SYNTAX</span></span>

### <span data-ttu-id="1cfc2-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cfc2-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -Definition <Object> [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cfc2-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cfc2-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 -DefinitionFilePath <String> [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1cfc2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1cfc2-107">DESCRIPTION</span></span>
<span data-ttu-id="1cfc2-108">O cmdlet **New-AzLogicApp** cria um aplicativo lógico usando o recurso de aplicativos lógicos.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-108">The **New-AzLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="1cfc2-109">Um aplicativo lógico é uma coleção de ações ou disparadores definidos na definição de aplicativo lógica.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="1cfc2-110">Esse cmdlet retorna um objeto de **fluxo de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="1cfc2-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="1cfc2-111">Você pode criar um aplicativo lógico especificando um nome, local, definição de aplicativo lógico, grupo de recursos e plano.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="1cfc2-112">Uma definição de aplicativo lógica e parâmetros são formatados em JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="1cfc2-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="1cfc2-113">Você pode usar um aplicativo lógico como um modelo para definição e parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="1cfc2-114">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1cfc2-115">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1cfc2-116">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1cfc2-117">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="1cfc2-118">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="1cfc2-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1cfc2-119">EXAMPLES</span></span>

### <span data-ttu-id="1cfc2-120">Exemplo 1: criar um aplicativo lógico usando caminhos de arquivo de definição e parâmetro</span><span class="sxs-lookup"><span data-stu-id="1cfc2-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
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

<span data-ttu-id="1cfc2-121">Esse comando cria um aplicativo lógico no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="1cfc2-122">O aplicativo lógica inclui a definição e os parâmetros especificados pelos caminhos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="1cfc2-123">Exemplo 2: criar um aplicativo lógico usando objetos Definition e Parameter</span><span class="sxs-lookup"><span data-stu-id="1cfc2-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
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

<span data-ttu-id="1cfc2-124">Esse comando cria um aplicativo lógico no grupo de recursos do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="1cfc2-125">Exemplo 3: criar um aplicativo lógico usando o pipeline para especificar o grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1cfc2-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
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

<span data-ttu-id="1cfc2-126">Esse comando obtém o grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-126">This command gets the resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1cfc2-127">O comando passa o grupo de recursos para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1cfc2-128">O cmdlet atual cria um aplicativo lógico nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="1cfc2-129">O aplicativo lógica inclui a definição e os parâmetros especificados pelos caminhos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="1cfc2-130">Exemplo 4: criar um aplicativo lógico baseado em um aplicativo lógico existente</span><span class="sxs-lookup"><span data-stu-id="1cfc2-130">Example 4: Create a logic app based on an existing logic app</span></span>
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

<span data-ttu-id="1cfc2-131">O primeiro comando obtém o aplicativo lógico chamado LogicApp03 usando o cmdlet Get-AzLogicApp.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-131">The first command gets the logic app named LogicApp03 by using the Get-AzLogicApp cmdlet.</span></span>
<span data-ttu-id="1cfc2-132">O comando armazena o aplicativo lógico na variável $Workflow.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-132">The command stores the logic app in the $Workflow variable.</span></span>
<span data-ttu-id="1cfc2-133">O segundo comando cria um novo aplicativo lógico que usa a definição e os parâmetros do aplicativo lógico armazenado no $Workflow.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="1cfc2-134">OS</span><span class="sxs-lookup"><span data-stu-id="1cfc2-134">PARAMETERS</span></span>

### <span data-ttu-id="1cfc2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cfc2-135">-DefaultProfile</span></span>
<span data-ttu-id="1cfc2-136">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1cfc2-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cfc2-137">-Definição</span><span class="sxs-lookup"><span data-stu-id="1cfc2-137">-Definition</span></span>
<span data-ttu-id="1cfc2-138">Especifica a definição do seu aplicativo lógico como um objeto ou uma cadeia de caracteres no formato JSON (JavaScript Object Notataion).</span><span class="sxs-lookup"><span data-stu-id="1cfc2-138">Specifies the definition for your logic app as an object or a string in JavaScript Object Notataion (JSON) format.</span></span>

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

### <span data-ttu-id="1cfc2-139">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="1cfc2-139">-DefinitionFilePath</span></span>
<span data-ttu-id="1cfc2-140">Especifica a definição de um aplicativo lógico como o caminho de um arquivo de definição no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-140">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="1cfc2-141">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="1cfc2-141">-IntegrationAccountId</span></span>
<span data-ttu-id="1cfc2-142">Especifica uma ID de conta de integração para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-142">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="1cfc2-143">-Local</span><span class="sxs-lookup"><span data-stu-id="1cfc2-143">-Location</span></span>
<span data-ttu-id="1cfc2-144">Especifica o local do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-144">Specifies the location of the logic app.</span></span>
<span data-ttu-id="1cfc2-145">Insira um local do Azure Data Center, como Oeste EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-145">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="1cfc2-146">Você pode colocar um aplicativo lógico em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-146">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="1cfc2-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="1cfc2-147">-Name</span></span>
<span data-ttu-id="1cfc2-148">Especifica o nome do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-148">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="1cfc2-149">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="1cfc2-149">-ParameterFilePath</span></span>
<span data-ttu-id="1cfc2-150">Especifica o caminho de um arquivo de parâmetro JSON formatado.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-150">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="1cfc2-151">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cfc2-151">-Parameters</span></span>
<span data-ttu-id="1cfc2-152">Especifica um objeto de coleção Parameters para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-152">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="1cfc2-153">Especifique uma tabela de hash, uma \< cadeia \> de caracteres de dicionário ou uma \< cadeia de caracteres de dicionário, WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="1cfc2-153">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="1cfc2-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cfc2-154">-ResourceGroupName</span></span>
<span data-ttu-id="1cfc2-155">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-155">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1cfc2-156">-Estado</span><span class="sxs-lookup"><span data-stu-id="1cfc2-156">-State</span></span>
<span data-ttu-id="1cfc2-157">Especifica o estado do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-157">Specifies the state of the logic app.</span></span>
<span data-ttu-id="1cfc2-158">Os valores aceitáveis para esse parâmetro são: Enabled e Disabled.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-158">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="1cfc2-159">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1cfc2-159">-Confirm</span></span>
<span data-ttu-id="1cfc2-160">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cfc2-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cfc2-161">-WhatIf</span></span>
<span data-ttu-id="1cfc2-162">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cfc2-163">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cfc2-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cfc2-164">CommonParameters</span></span>
<span data-ttu-id="1cfc2-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cfc2-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cfc2-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cfc2-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cfc2-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1cfc2-167">INPUTS</span></span>

### <span data-ttu-id="1cfc2-168">System. String</span><span class="sxs-lookup"><span data-stu-id="1cfc2-168">System.String</span></span>

## <span data-ttu-id="1cfc2-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1cfc2-169">OUTPUTS</span></span>

### <span data-ttu-id="1cfc2-170">System. Object</span><span class="sxs-lookup"><span data-stu-id="1cfc2-170">System.Object</span></span>

## <span data-ttu-id="1cfc2-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1cfc2-171">NOTES</span></span>

## <span data-ttu-id="1cfc2-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1cfc2-172">RELATED LINKS</span></span>

[<span data-ttu-id="1cfc2-173">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1cfc2-173">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="1cfc2-174">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1cfc2-174">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="1cfc2-175">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1cfc2-175">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="1cfc2-176">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1cfc2-176">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


