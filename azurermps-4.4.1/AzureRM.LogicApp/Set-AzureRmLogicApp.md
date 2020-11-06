---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmLogicApp.md
ms.openlocfilehash: d60897564843c403f5502da22e2f7a7122b1f841
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441539"
---
# <span data-ttu-id="e214c-101">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e214c-101">Set-AzureRmLogicApp</span></span>

## <span data-ttu-id="e214c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e214c-102">SYNOPSIS</span></span>
<span data-ttu-id="e214c-103">Modifica um aplicativo lógico em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e214c-103">Modifies a logic app in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e214c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e214c-104">SYNTAX</span></span>

### <span data-ttu-id="e214c-105">Consumo (padrão)</span><span class="sxs-lookup"><span data-stu-id="e214c-105">Consumption (Default)</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e214c-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="e214c-106">HostingPlan</span></span>
```
Set-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e214c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e214c-107">DESCRIPTION</span></span>
<span data-ttu-id="e214c-108">O cmdlet **set-AzureRmLogicApp** modifica um aplicativo lógico usando o recurso de aplicativos lógicos.</span><span class="sxs-lookup"><span data-stu-id="e214c-108">The **Set-AzureRmLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="e214c-109">Um aplicativo lógico é uma coleção de ações ou disparadores definidos na definição de aplicativo lógica.</span><span class="sxs-lookup"><span data-stu-id="e214c-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="e214c-110">Esse cmdlet retorna um objeto de **fluxo de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="e214c-110">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="e214c-111">Você pode modificar um aplicativo lógico especificando um nome, local, definição de aplicativo lógico, grupo de recursos e plano.</span><span class="sxs-lookup"><span data-stu-id="e214c-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="e214c-112">Uma definição de aplicativo lógica e parâmetros são formatados em JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="e214c-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="e214c-113">Você pode usar um aplicativo lógico como um modelo para definição e parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e214c-113">You can use a logic app as a template for definition and parameters.</span></span>

<span data-ttu-id="e214c-114">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="e214c-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e214c-115">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="e214c-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e214c-116">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e214c-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e214c-117">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="e214c-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="e214c-118">Os valores de arquivo de parâmetro de modelo que você especifica na linha de comando têm precedência sobre os valores de parâmetro de template em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="e214c-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="e214c-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e214c-119">EXAMPLES</span></span>

### <span data-ttu-id="e214c-120">Exemplo 1: modificar um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="e214c-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp1
Name                         : LogicApp17
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp17
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
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/ServicePlan17
Version                      : 08587489107859952120
```

<span data-ttu-id="e214c-121">Esse comando modifica um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e214c-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="e214c-122">OS</span><span class="sxs-lookup"><span data-stu-id="e214c-122">PARAMETERS</span></span>

### <span data-ttu-id="e214c-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e214c-123">-AppServicePlan</span></span>
<span data-ttu-id="e214c-124">Especifica o nome de um plano.</span><span class="sxs-lookup"><span data-stu-id="e214c-124">Specifies the name of a plan.</span></span>

```yaml
Type: System.String
Parameter Sets: HostingPlan
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e214c-125">-Definição</span><span class="sxs-lookup"><span data-stu-id="e214c-125">-Definition</span></span>
<span data-ttu-id="e214c-126">Especifica a definição de um aplicativo lógico como um objeto ou uma cadeia de caracteres em formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="e214c-126">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="e214c-127">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="e214c-127">-DefinitionFilePath</span></span>
<span data-ttu-id="e214c-128">Especifica a definição de um aplicativo lógico como o caminho de um arquivo de definição no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="e214c-128">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="e214c-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e214c-129">-Force</span></span>
<span data-ttu-id="e214c-130">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e214c-130">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e214c-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="e214c-131">-IntegrationAccountId</span></span>
<span data-ttu-id="e214c-132">Especifica uma ID de conta de integração para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e214c-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="e214c-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="e214c-133">-Name</span></span>
<span data-ttu-id="e214c-134">Especifica o nome de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e214c-134">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="e214c-135">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="e214c-135">-ParameterFilePath</span></span>
<span data-ttu-id="e214c-136">Especifica o caminho de um arquivo de parâmetro JSON formatado.</span><span class="sxs-lookup"><span data-stu-id="e214c-136">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="e214c-137">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e214c-137">-Parameters</span></span>
<span data-ttu-id="e214c-138">Especifica um objeto de coleção Parameters para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e214c-138">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="e214c-139">Especifique uma tabela de hash, dicionário \<string\> ou dicionário \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="e214c-139">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="e214c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e214c-140">-ResourceGroupName</span></span>
<span data-ttu-id="e214c-141">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e214c-141">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e214c-142">-Estado</span><span class="sxs-lookup"><span data-stu-id="e214c-142">-State</span></span>
<span data-ttu-id="e214c-143">Especifica o estado do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="e214c-143">Specifies the state of the logic app.</span></span>
<span data-ttu-id="e214c-144">Os valores aceitáveis para esse parâmetro são: Enabled e Disabled.</span><span class="sxs-lookup"><span data-stu-id="e214c-144">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="e214c-145">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="e214c-145">-UseConsumptionModel</span></span>
<span data-ttu-id="e214c-146">Indica que a cobrança do aplicativo lógico usa o modelo baseado em consumo.</span><span class="sxs-lookup"><span data-stu-id="e214c-146">Indicates that the logic app billing use the consumption based model.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Consumption
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e214c-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e214c-147">-Confirm</span></span>
<span data-ttu-id="e214c-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e214c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e214c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e214c-149">-WhatIf</span></span>
<span data-ttu-id="e214c-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e214c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e214c-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e214c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e214c-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e214c-152">-DefaultProfile</span></span>
<span data-ttu-id="e214c-153">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e214c-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e214c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e214c-154">CommonParameters</span></span>
<span data-ttu-id="e214c-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e214c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e214c-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e214c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e214c-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e214c-157">INPUTS</span></span>

## <span data-ttu-id="e214c-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e214c-158">OUTPUTS</span></span>

### <span data-ttu-id="e214c-159">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="e214c-159">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="e214c-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e214c-160">NOTES</span></span>

## <span data-ttu-id="e214c-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e214c-161">RELATED LINKS</span></span>

[<span data-ttu-id="e214c-162">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e214c-162">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="e214c-163">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e214c-163">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="e214c-164">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e214c-164">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="e214c-165">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="e214c-165">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


