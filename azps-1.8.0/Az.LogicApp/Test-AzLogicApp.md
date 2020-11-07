---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: aa1a4148da7958c587363bcfdc11d53ae7a25b7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770453"
---
# <span data-ttu-id="6d636-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d636-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="6d636-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6d636-102">SYNOPSIS</span></span>
<span data-ttu-id="6d636-103">Valida uma definição de aplicativo lógica.</span><span class="sxs-lookup"><span data-stu-id="6d636-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="6d636-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6d636-104">SYNTAX</span></span>

### <span data-ttu-id="6d636-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d636-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d636-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d636-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d636-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6d636-107">DESCRIPTION</span></span>
<span data-ttu-id="6d636-108">O cmdlet **Test-AzLogicApp** valida uma definição de aplicativo lógica em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d636-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="6d636-109">Especifique o nome do aplicativo lógico, o nome do grupo de recursos, o local, o estado, a ID da conta de integração ou os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6d636-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="6d636-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="6d636-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6d636-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="6d636-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6d636-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="6d636-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6d636-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="6d636-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6d636-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6d636-114">EXAMPLES</span></span>

### <span data-ttu-id="6d636-115">Exemplo 1: validar um aplicativo lógico usando caminhos de arquivo</span><span class="sxs-lookup"><span data-stu-id="6d636-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="6d636-116">Esse comando valida um aplicativo lógico chamado LogicApp01 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="6d636-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="6d636-117">O comando especifica caminhos de arquivo de definição e parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6d636-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="6d636-118">Exemplo 2: validar um aplicativo lógico usando objetos</span><span class="sxs-lookup"><span data-stu-id="6d636-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="6d636-119">Esse comando valida um aplicativo lógico chamado LogicApp01 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="6d636-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="6d636-120">O comando especifica objetos de definição e parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6d636-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="6d636-121">OS</span><span class="sxs-lookup"><span data-stu-id="6d636-121">PARAMETERS</span></span>

### <span data-ttu-id="6d636-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d636-122">-DefaultProfile</span></span>
<span data-ttu-id="6d636-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6d636-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d636-124">-Definição</span><span class="sxs-lookup"><span data-stu-id="6d636-124">-Definition</span></span>
<span data-ttu-id="6d636-125">Especifica a definição de um aplicativo lógico como um objeto ou uma cadeia de caracteres em formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="6d636-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="6d636-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="6d636-126">-DefinitionFilePath</span></span>
<span data-ttu-id="6d636-127">Especifica a definição do aplicativo lógico como o caminho de um arquivo de definição no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="6d636-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="6d636-128">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="6d636-128">-IntegrationAccountId</span></span>
<span data-ttu-id="6d636-129">Especifica uma ID de conta de integração para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="6d636-129">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="6d636-130">-Local</span><span class="sxs-lookup"><span data-stu-id="6d636-130">-Location</span></span>
<span data-ttu-id="6d636-131">Especifica o local do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="6d636-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="6d636-132">Insira um local do Azure Data Center, como Oeste EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="6d636-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="6d636-133">Você pode colocar um aplicativo lógico em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="6d636-133">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="6d636-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d636-134">-Name</span></span>
<span data-ttu-id="6d636-135">Especifica o nome do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="6d636-135">Specifies the name of the logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d636-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="6d636-136">-ParameterFilePath</span></span>
<span data-ttu-id="6d636-137">Especifica o caminho de um arquivo de parâmetro JSON formatado.</span><span class="sxs-lookup"><span data-stu-id="6d636-137">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="6d636-138">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d636-138">-Parameters</span></span>
<span data-ttu-id="6d636-139">Especifica um objeto da coleção Parameters do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="6d636-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="6d636-140">Especifique uma tabela de hash, uma \< cadeia \> de caracteres de dicionário ou uma \< cadeia de caracteres de dicionário, WorkflowParameter \> .</span><span class="sxs-lookup"><span data-stu-id="6d636-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="6d636-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d636-141">-ResourceGroupName</span></span>
<span data-ttu-id="6d636-142">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6d636-142">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6d636-143">-Estado</span><span class="sxs-lookup"><span data-stu-id="6d636-143">-State</span></span>
<span data-ttu-id="6d636-144">Especifica um estado do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="6d636-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="6d636-145">Os valores aceitáveis para esse parâmetro são: Enabled e Disabled.</span><span class="sxs-lookup"><span data-stu-id="6d636-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="6d636-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d636-146">CommonParameters</span></span>
<span data-ttu-id="6d636-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d636-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d636-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d636-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d636-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6d636-149">INPUTS</span></span>

### <span data-ttu-id="6d636-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6d636-150">System.String</span></span>

## <span data-ttu-id="6d636-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6d636-151">OUTPUTS</span></span>

### <span data-ttu-id="6d636-152">System. void</span><span class="sxs-lookup"><span data-stu-id="6d636-152">System.Void</span></span>

## <span data-ttu-id="6d636-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6d636-153">NOTES</span></span>

## <span data-ttu-id="6d636-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6d636-154">RELATED LINKS</span></span>

[<span data-ttu-id="6d636-155">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d636-155">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="6d636-156">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d636-156">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="6d636-157">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d636-157">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="6d636-158">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d636-158">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="6d636-159">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d636-159">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


