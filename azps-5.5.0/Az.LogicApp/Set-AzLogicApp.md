---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: AEDA89D3-EF80-4E56-9B97-677EC8F3959D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzLogicApp.md
ms.openlocfilehash: 53fa3d21089b150a7436311597a88e827f391562
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115264"
---
# <span data-ttu-id="97fab-101">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="97fab-101">Set-AzLogicApp</span></span>

## <span data-ttu-id="97fab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97fab-102">SYNOPSIS</span></span>
<span data-ttu-id="97fab-103">Modifica um aplicativo lógico em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97fab-103">Modifies a logic app in a resource group.</span></span>

## <span data-ttu-id="97fab-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97fab-104">SYNTAX</span></span>

### <span data-ttu-id="97fab-105">Consumo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="97fab-105">Consumption (Default)</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-UseConsumptionModel] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="97fab-106">HostingPlan</span><span class="sxs-lookup"><span data-stu-id="97fab-106">HostingPlan</span></span>
```
Set-AzLogicApp -ResourceGroupName <String> -Name <String> [-AppServicePlan <String>] [-State <String>]
 [-Definition <Object>] [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97fab-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="97fab-107">DESCRIPTION</span></span>
<span data-ttu-id="97fab-108">O **cmdlet Set-AzApp** modifica um aplicativo lógico usando o recurso Aplicativos Lógicos.</span><span class="sxs-lookup"><span data-stu-id="97fab-108">The **Set-AzLogicApp** cmdlet modifies a logic app by using the Logic Apps feature.</span></span>
<span data-ttu-id="97fab-109">Um aplicativo lógico é um conjunto de ações ou gatilhos definidos na definição do Aplicativo Lógico.</span><span class="sxs-lookup"><span data-stu-id="97fab-109">A logic app is a collection of actions or triggers defined in Logic App definition.</span></span>
<span data-ttu-id="97fab-110">Este cmdlet retorna um objeto **Fluxo de** Trabalho.</span><span class="sxs-lookup"><span data-stu-id="97fab-110">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="97fab-111">Você pode modificar um aplicativo lógico especificando um nome, um local, uma definição do Aplicativo Lógico, um grupo de recursos e um plano.</span><span class="sxs-lookup"><span data-stu-id="97fab-111">You can modify a logic app by specifying a name, location, Logic App definition, resource group, and plan.</span></span>
<span data-ttu-id="97fab-112">Uma definição e parâmetros do Aplicativo Lógico são formatados em Notação de Objeto JavaScript (JSON).</span><span class="sxs-lookup"><span data-stu-id="97fab-112">A Logic App definition and parameters are formatted in JavaScript Object Notation (JSON).</span></span>
<span data-ttu-id="97fab-113">Você pode usar um aplicativo lógico como um modelo para definição e parâmetros.</span><span class="sxs-lookup"><span data-stu-id="97fab-113">You can use a logic app as a template for definition and parameters.</span></span>
<span data-ttu-id="97fab-114">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="97fab-114">This module supports dynamic parameters.</span></span>
<span data-ttu-id="97fab-115">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="97fab-115">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="97fab-116">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="97fab-116">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="97fab-117">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="97fab-117">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="97fab-118">Os valores de arquivo de parâmetro de modelo especificados na linha de comando têm precedência sobre os valores dos parâmetros de modelo em um objeto de parâmetro de modelo.</span><span class="sxs-lookup"><span data-stu-id="97fab-118">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

## <span data-ttu-id="97fab-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97fab-119">EXAMPLES</span></span>

### <span data-ttu-id="97fab-120">Exemplo 1: Modificar um aplicativo lógico</span><span class="sxs-lookup"><span data-stu-id="97fab-120">Example 1: Modify a logic app</span></span>
```
PS C:\>Set-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp17" -State "Enabled" -AppServicePlan "ServicePlan01" -DefinitionFilePath "d:\workflows\Definition17.json" -ParameterFilePath "d:\workflows\Parameters17.json"
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

<span data-ttu-id="97fab-121">Esse comando modifica um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="97fab-121">This command modifies a logic app.</span></span>

## <span data-ttu-id="97fab-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97fab-122">PARAMETERS</span></span>

### <span data-ttu-id="97fab-123">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="97fab-123">-AppServicePlan</span></span>
<span data-ttu-id="97fab-124">Especifica o nome de um plano.</span><span class="sxs-lookup"><span data-stu-id="97fab-124">Specifies the name of a plan.</span></span>

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

### <span data-ttu-id="97fab-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97fab-125">-DefaultProfile</span></span>
<span data-ttu-id="97fab-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="97fab-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97fab-127">-Definição</span><span class="sxs-lookup"><span data-stu-id="97fab-127">-Definition</span></span>
<span data-ttu-id="97fab-128">Especifica a definição de um aplicativo lógico como um objeto ou uma cadeia de caracteres no formato JSON (Notação de Objeto JavaScript).</span><span class="sxs-lookup"><span data-stu-id="97fab-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="97fab-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="97fab-129">-DefinitionFilePath</span></span>
<span data-ttu-id="97fab-130">Especifica a definição de um aplicativo lógico como o caminho de um arquivo de definição no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="97fab-130">Specifies the definition of a logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="97fab-131">-Forçar</span><span class="sxs-lookup"><span data-stu-id="97fab-131">-Force</span></span>
<span data-ttu-id="97fab-132">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="97fab-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97fab-133">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="97fab-133">-IntegrationAccountId</span></span>
<span data-ttu-id="97fab-134">Especifica uma ID de conta de integração para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="97fab-134">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="97fab-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="97fab-135">-Name</span></span>
<span data-ttu-id="97fab-136">Especifica o nome de um aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="97fab-136">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="97fab-137">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="97fab-137">-ParameterFilePath</span></span>
<span data-ttu-id="97fab-138">Especifica o caminho de um arquivo de parâmetro formatado JSON.</span><span class="sxs-lookup"><span data-stu-id="97fab-138">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="97fab-139">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97fab-139">-Parameters</span></span>
<span data-ttu-id="97fab-140">Especifica um objeto de conjunto de parâmetros para o aplicativo Logic.</span><span class="sxs-lookup"><span data-stu-id="97fab-140">Specifies a parameters collection object for the Logic App.</span></span>
<span data-ttu-id="97fab-141">Especifique uma tabela hash, dicionário \<string\> ou \<string, WorkflowParameter\> dicionário.</span><span class="sxs-lookup"><span data-stu-id="97fab-141">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="97fab-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97fab-142">-ResourceGroupName</span></span>
<span data-ttu-id="97fab-143">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="97fab-143">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="97fab-144">-Estado</span><span class="sxs-lookup"><span data-stu-id="97fab-144">-State</span></span>
<span data-ttu-id="97fab-145">Especifica o estado do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="97fab-145">Specifies the state of the logic app.</span></span>
<span data-ttu-id="97fab-146">Os valores aceitáveis para este parâmetro são: Habilitado e Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="97fab-146">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="97fab-147">-UseConsumptionModel</span><span class="sxs-lookup"><span data-stu-id="97fab-147">-UseConsumptionModel</span></span>
<span data-ttu-id="97fab-148">Indica que a cobrança do aplicativo lógico usa o modelo baseado em consumo.</span><span class="sxs-lookup"><span data-stu-id="97fab-148">Indicates that the logic app billing use the consumption based model.</span></span>

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

### <span data-ttu-id="97fab-149">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="97fab-149">-Confirm</span></span>
<span data-ttu-id="97fab-150">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97fab-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97fab-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97fab-151">-WhatIf</span></span>
<span data-ttu-id="97fab-152">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="97fab-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97fab-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97fab-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97fab-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97fab-154">CommonParameters</span></span>
<span data-ttu-id="97fab-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97fab-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97fab-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97fab-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97fab-157">Entradas</span><span class="sxs-lookup"><span data-stu-id="97fab-157">INPUTS</span></span>

### <span data-ttu-id="97fab-158">System.String</span><span class="sxs-lookup"><span data-stu-id="97fab-158">System.String</span></span>

## <span data-ttu-id="97fab-159">Saídas</span><span class="sxs-lookup"><span data-stu-id="97fab-159">OUTPUTS</span></span>

### <span data-ttu-id="97fab-160">System.Object</span><span class="sxs-lookup"><span data-stu-id="97fab-160">System.Object</span></span>

## <span data-ttu-id="97fab-161">Notas</span><span class="sxs-lookup"><span data-stu-id="97fab-161">NOTES</span></span>

## <span data-ttu-id="97fab-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97fab-162">RELATED LINKS</span></span>

[<span data-ttu-id="97fab-163">Get-AzApp</span><span class="sxs-lookup"><span data-stu-id="97fab-163">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="97fab-164">Novo-AzApp</span><span class="sxs-lookup"><span data-stu-id="97fab-164">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="97fab-165">Remove-AzApp</span><span class="sxs-lookup"><span data-stu-id="97fab-165">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="97fab-166">Start-AzApp</span><span class="sxs-lookup"><span data-stu-id="97fab-166">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


