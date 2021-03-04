---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/powershell/module/az.logicapp/test-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Test-AzLogicApp.md
ms.openlocfilehash: 6639a397c97be35565d374279b2981fa2b1eabd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885432"
---
# <span data-ttu-id="2fe6d-101">Test-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fe6d-101">Test-AzLogicApp</span></span>

## <span data-ttu-id="2fe6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fe6d-102">SYNOPSIS</span></span>
<span data-ttu-id="2fe6d-103">Valida uma definição de aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-103">Validates a logic app definition.</span></span>

## <span data-ttu-id="2fe6d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2fe6d-104">SYNTAX</span></span>

### <span data-ttu-id="2fe6d-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fe6d-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fe6d-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fe6d-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fe6d-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2fe6d-107">DESCRIPTION</span></span>
<span data-ttu-id="2fe6d-108">O cmdlet **Test-AzLogicApp** valida uma definição de aplicativo lógico em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-108">The **Test-AzLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="2fe6d-109">Especifique o nome do aplicativo lógico, o nome do grupo de recursos, o local, o estado, a ID da conta de integração ou os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>
<span data-ttu-id="2fe6d-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2fe6d-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2fe6d-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e pressione a tecla Tab repetidamente para passar pelos parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2fe6d-113">Se você omitir um parâmetro de modelo necessário, o cmdlet solicitará o valor.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2fe6d-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fe6d-114">EXAMPLES</span></span>

### <span data-ttu-id="2fe6d-115">Exemplo 1: Validar um aplicativo lógico usando caminhos de arquivo</span><span class="sxs-lookup"><span data-stu-id="2fe6d-115">Example 1: Validate a logic app by using file paths</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="2fe6d-116">Este comando valida um aplicativo lógico chamado LogicApp01 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="2fe6d-117">O comando especifica caminhos de arquivo de definição e parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="2fe6d-118">Exemplo 2: Validar um aplicativo lógico usando objetos</span><span class="sxs-lookup"><span data-stu-id="2fe6d-118">Example 2: Validate a logic app by using objects</span></span>
```powershell
PS C:\>Test-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="2fe6d-119">Este comando valida um aplicativo lógico chamado LogicApp01 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="2fe6d-120">O comando especifica objetos de definição e parâmetro.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-120">The command specifies definition and parameter objects.</span></span>

### <span data-ttu-id="2fe6d-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="2fe6d-121">Example 3</span></span>

<span data-ttu-id="2fe6d-122">Valida uma definição de aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-122">Validates a logic app definition.</span></span> <span data-ttu-id="2fe6d-123">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="2fe6d-123">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Test-AzLogicApp -DefinitionFilePath 'd:\workflows\Definition.json' -IntegrationAccountId <String> -Location 'westus' -Name 'LogicApp01' -ParameterFilePath 'd:\workflows\Parameters.json' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="2fe6d-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2fe6d-124">PARAMETERS</span></span>

### <span data-ttu-id="2fe6d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fe6d-125">-DefaultProfile</span></span>
<span data-ttu-id="2fe6d-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2fe6d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fe6d-127">-Definition</span><span class="sxs-lookup"><span data-stu-id="2fe6d-127">-Definition</span></span>
<span data-ttu-id="2fe6d-128">Especifica a definição de um aplicativo lógico como um objeto ou uma cadeia de caracteres no formato JSON (Notação de Objeto JavaScript).</span><span class="sxs-lookup"><span data-stu-id="2fe6d-128">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="2fe6d-129">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="2fe6d-129">-DefinitionFilePath</span></span>
<span data-ttu-id="2fe6d-130">Especifica a definição de seu aplicativo lógico como o caminho de um arquivo de definição no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-130">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="2fe6d-131">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="2fe6d-131">-IntegrationAccountId</span></span>
<span data-ttu-id="2fe6d-132">Especifica uma ID de conta de integração para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-132">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="2fe6d-133">-Location</span><span class="sxs-lookup"><span data-stu-id="2fe6d-133">-Location</span></span>
<span data-ttu-id="2fe6d-134">Especifica o local do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-134">Specifies the location of the logic app.</span></span>
<span data-ttu-id="2fe6d-135">Insira um local do data center do Azure, como o Oeste dos EUA ou o Sudeste Asiático.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-135">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="2fe6d-136">Você pode colocar um aplicativo lógico em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-136">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="2fe6d-137">-Name</span><span class="sxs-lookup"><span data-stu-id="2fe6d-137">-Name</span></span>
<span data-ttu-id="2fe6d-138">Especifica o nome do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-138">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="2fe6d-139">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="2fe6d-139">-ParameterFilePath</span></span>
<span data-ttu-id="2fe6d-140">Especifica o caminho de um arquivo de parâmetro formatado JSON.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-140">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="2fe6d-141">-Parameters</span><span class="sxs-lookup"><span data-stu-id="2fe6d-141">-Parameters</span></span>
<span data-ttu-id="2fe6d-142">Especifica um objeto de coleção de parâmetros do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-142">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="2fe6d-143">Especifique uma tabela de hash, Dicionário \<string\> ou \<string, WorkflowParameter\> Dicionário.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-143">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="2fe6d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fe6d-144">-ResourceGroupName</span></span>
<span data-ttu-id="2fe6d-145">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-145">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2fe6d-146">-State</span><span class="sxs-lookup"><span data-stu-id="2fe6d-146">-State</span></span>
<span data-ttu-id="2fe6d-147">Especifica um estado do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-147">Specifies a state of the logic app.</span></span>
<span data-ttu-id="2fe6d-148">Os valores aceitáveis para este parâmetro são: Habilitado e Desabilitado.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-148">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="2fe6d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fe6d-149">CommonParameters</span></span>
<span data-ttu-id="2fe6d-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fe6d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fe6d-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fe6d-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fe6d-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fe6d-152">INPUTS</span></span>

### <span data-ttu-id="2fe6d-153">System.String</span><span class="sxs-lookup"><span data-stu-id="2fe6d-153">System.String</span></span>

## <span data-ttu-id="2fe6d-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2fe6d-154">OUTPUTS</span></span>

### <span data-ttu-id="2fe6d-155">System.Void</span><span class="sxs-lookup"><span data-stu-id="2fe6d-155">System.Void</span></span>

## <span data-ttu-id="2fe6d-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="2fe6d-156">NOTES</span></span>

## <span data-ttu-id="2fe6d-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fe6d-157">RELATED LINKS</span></span>

[<span data-ttu-id="2fe6d-158">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fe6d-158">Get-AzLogicApp</span></span>](./Get-AzLogicApp.md)

[<span data-ttu-id="2fe6d-159">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fe6d-159">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="2fe6d-160">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fe6d-160">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="2fe6d-161">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fe6d-161">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="2fe6d-162">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="2fe6d-162">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


