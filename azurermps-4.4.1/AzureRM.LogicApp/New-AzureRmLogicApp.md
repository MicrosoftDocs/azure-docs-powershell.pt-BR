---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 8679240C-EA47-41C5-B8C1-A3C99547F42B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmLogicApp.md
ms.openlocfilehash: 990423db13f13f18f10fb768ac55d2e59b4f2baf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441541"
---
# <span data-ttu-id="996ec-101">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="996ec-101">New-AzureRmLogicApp</span></span>

## <span data-ttu-id="996ec-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="996ec-102">SYNOPSIS</span></span>
<span data-ttu-id="996ec-103">Cria um aplicativo lógico em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="996ec-103">Creates a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="996ec-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="996ec-104">SYNTAX</span></span>

### <span data-ttu-id="996ec-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="996ec-105">LogicAppWithDefinitionParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="996ec-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="996ec-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
New-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="996ec-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="996ec-107">DESCRIPTION</span></span>
<span data-ttu-id="996ec-108">O cmdlet **New-AzureRmLogicApp** cria um aplicativo lógico usando o recurso de aplicativos lógicos.</span><span class="sxs-lookup"><span data-stu-id="996ec-108">The **New-AzureRmLogicApp** cmdlet creates a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="996ec-109">Um aplicativo lógico é uma coleção de ações ou disparadores definidos na definição de aplicativo lógica.</span><span class="sxs-lookup"><span data-stu-id="996ec-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="996ec-110">Esse cmdlet retorna um objeto de **fluxo de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="996ec-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="996ec-111">Você pode criar um aplicativo lógico especificando um nome, local, definição de aplicativo lógico, grupo de recursos e plano.</span><span class="sxs-lookup"><span data-stu-id="996ec-111">You can create a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="996ec-112">Uma definição de aplicativo lógica e parâmetros são formatados em JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="996ec-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="996ec-113">Você pode usar um aplicativo lógico como um modelo para definição e parâmetros.</span><span class="sxs-lookup"><span data-stu-id="996ec-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="996ec-114">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="996ec-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="996ec-115">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="996ec-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="996ec-116">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="996ec-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="996ec-117">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="996ec-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="996ec-118">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="996ec-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="996ec-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="996ec-119">EXAMPLES</span></span>

### <span data-ttu-id="996ec-120">Exemplo 1: criar um aplicativo lógico usando caminhos de arquivo de definição e parâmetro</span><span class="sxs-lookup"><span data-stu-id="996ec-120">Example 1: Create a logic app by using definition and parameter file paths</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition03.json" -ParameterFilePath "d:\workflows\Parameters03.json"
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

<span data-ttu-id="996ec-121">Esse comando cria um aplicativo lógico no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="996ec-121">This command creates a logic app in the specified resource group.</span></span>
<span data-ttu-id="996ec-122">O aplicativo lógica inclui a definição e os parâmetros especificados pelos caminhos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="996ec-122">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="996ec-123">Exemplo 2: criar um aplicativo lógico usando objetos Definition e Parameter</span><span class="sxs-lookup"><span data-stu-id="996ec-123">Example 2: Create a logic app by using definition and parameter objects</span></span>
```
PS C:\>New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -Location "westus" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
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

<span data-ttu-id="996ec-124">Esse comando cria um aplicativo lógico no grupo de recursos do grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="996ec-124">This command creates a logic app in the specified resource group resource group.</span></span>

### <span data-ttu-id="996ec-125">Exemplo 3: criar um aplicativo lógico usando o pipeline para especificar o grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="996ec-125">Example 3: Create a logic app by using the pipeline to specify the resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroup -ResourceGroupName "ResourceGroup11" | New-AzureRmLogicApp -Name "LogicApp11" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\Workflow\Definition.json" -ParameterFilePath "d:\Workflow\Parameters.json"
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

<span data-ttu-id="996ec-126">Esse comando obtém o grupo de recursos chamado ResourceGroup11 usando o cmdlet Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="996ec-126">This command gets the resource group named ResourceGroup11 by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="996ec-127">O comando passa o grupo de recursos para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="996ec-127">The command passes that resource group to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="996ec-128">O cmdlet atual cria um aplicativo lógico nesse grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="996ec-128">The current cmdlet creates a logic app in that resource group.</span></span>
<span data-ttu-id="996ec-129">O aplicativo lógica inclui a definição e os parâmetros especificados pelos caminhos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="996ec-129">The logic app includes the definition and parameters specified by file paths.</span></span>

### <span data-ttu-id="996ec-130">Exemplo 4: criar um aplicativo lógico baseado em um aplicativo lógico existente</span><span class="sxs-lookup"><span data-stu-id="996ec-130">Example 4: Create a logic app based on an existing logic app</span></span>
```
PS C:\>$Workflow = Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
PS C:\> New-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp13" -State "Enabled" -AppServicePlan "ServicePlan01" -Definition $Workflow.Definition -Parameters $Workflow.Parameters
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

<span data-ttu-id="996ec-131">O primeiro comando obtém o aplicativo lógico chamado LogicApp03 usando o cmdlet Get-AzureRmLogicApp.</span><span class="sxs-lookup"><span data-stu-id="996ec-131">The first command gets the logic app named LogicApp03 by using the Get-AzureRmLogicApp cmdlet.</span></span>
<span data-ttu-id="996ec-132">O comando armazena o aplicativo lógico na variável $Workflow.</span><span class="sxs-lookup"><span data-stu-id="996ec-132">The command stores the logic app in the $Workflow variable.</span></span>

<span data-ttu-id="996ec-133">O segundo comando cria um novo aplicativo lógico que usa a definição e os parâmetros do aplicativo lógico armazenado no $Workflow.</span><span class="sxs-lookup"><span data-stu-id="996ec-133">The second command creates a new logic app that uses the definition and parameters of the logic app stored in $Workflow.</span></span>

## <span data-ttu-id="996ec-134">OS</span><span class="sxs-lookup"><span data-stu-id="996ec-134">PARAMETERS</span></span>

### <span data-ttu-id="996ec-135">-Definição</span><span class="sxs-lookup"><span data-stu-id="996ec-135">-Definition</span></span>
<span data-ttu-id="996ec-136">Especifica a definição do seu aplicativo lógico como um objeto ou uma cadeia de caracteres no formato JSON (JavaScript Object Notataion).</span><span class="sxs-lookup"><span data-stu-id="996ec-136">Specifies the definition for your logic app as an object or a string in JavaScript Object Notataion (JSON) format.</span></span>

```yaml
Type: System.Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="996ec-137">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="996ec-137">-DefinitionFilePath</span></span>
<span data-ttu-id="996ec-138">Especifica a definição de um aplicativo lógico como o caminho de um arquivo de definição no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="996ec-138">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: System.String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="996ec-139">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="996ec-139">-IntegrationAccountId</span></span>
<span data-ttu-id="996ec-140">Especifica uma ID de conta de integração para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="996ec-140">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="996ec-141">-Local</span><span class="sxs-lookup"><span data-stu-id="996ec-141">-Location</span></span>
<span data-ttu-id="996ec-142">Especifica o local do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="996ec-142">Specifies the location of the logic app.</span></span>
<span data-ttu-id="996ec-143">Insira um local do Azure Data Center, como Oeste EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="996ec-143">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="996ec-144">Você pode colocar um aplicativo lógico em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="996ec-144">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="996ec-145">-Nome</span><span class="sxs-lookup"><span data-stu-id="996ec-145">-Name</span></span>
<span data-ttu-id="996ec-146">Especifica o nome do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="996ec-146">Specifies the name for the logic app.</span></span>

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

### <span data-ttu-id="996ec-147">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="996ec-147">-ParameterFilePath</span></span>
<span data-ttu-id="996ec-148">Especifica o caminho de um arquivo de parâmetro JSON formatado.</span><span class="sxs-lookup"><span data-stu-id="996ec-148">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="996ec-149">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="996ec-149">-Parameters</span></span>
<span data-ttu-id="996ec-150">Especifica um objeto de coleção Parameters para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="996ec-150">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="996ec-151">Especifique uma tabela de hash, dicionário \<string\> ou dicionário \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="996ec-151">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="996ec-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="996ec-152">-ResourceGroupName</span></span>
<span data-ttu-id="996ec-153">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="996ec-153">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="996ec-154">-Estado</span><span class="sxs-lookup"><span data-stu-id="996ec-154">-State</span></span>
<span data-ttu-id="996ec-155">Especifica o estado do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="996ec-155">Specifies the state of the logic app.</span></span>
<span data-ttu-id="996ec-156">Os valores aceitáveis para esse parâmetro são: Enabled e Disabled.</span><span class="sxs-lookup"><span data-stu-id="996ec-156">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="996ec-157">-Confirme</span><span class="sxs-lookup"><span data-stu-id="996ec-157">-Confirm</span></span>
<span data-ttu-id="996ec-158">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="996ec-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="996ec-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="996ec-159">-WhatIf</span></span>
<span data-ttu-id="996ec-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="996ec-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="996ec-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="996ec-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="996ec-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996ec-162">-DefaultProfile</span></span>
<span data-ttu-id="996ec-163">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="996ec-163">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="996ec-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996ec-164">CommonParameters</span></span>
<span data-ttu-id="996ec-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="996ec-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996ec-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="996ec-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996ec-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="996ec-167">INPUTS</span></span>

### <span data-ttu-id="996ec-168">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="996ec-168">None</span></span>

## <span data-ttu-id="996ec-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="996ec-169">OUTPUTS</span></span>

### <span data-ttu-id="996ec-170">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="996ec-170">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="996ec-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="996ec-171">NOTES</span></span>

## <span data-ttu-id="996ec-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="996ec-172">RELATED LINKS</span></span>

[<span data-ttu-id="996ec-173">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="996ec-173">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="996ec-174">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="996ec-174">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="996ec-175">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="996ec-175">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="996ec-176">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="996ec-176">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


