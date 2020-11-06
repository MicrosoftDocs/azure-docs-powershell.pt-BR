---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/test-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: c93cf0fdceebb3507a19c06ea5b6dda96fbc0656
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610389"
---
# <span data-ttu-id="be803-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="be803-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="be803-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be803-102">SYNOPSIS</span></span>
<span data-ttu-id="be803-103">Valida uma definição de aplicativo lógica.</span><span class="sxs-lookup"><span data-stu-id="be803-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be803-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be803-104">SYNTAX</span></span>

### <span data-ttu-id="be803-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="be803-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be803-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="be803-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be803-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be803-107">DESCRIPTION</span></span>
<span data-ttu-id="be803-108">O cmdlet **Test-AzureRmLogicApp** valida uma definição de aplicativo lógica em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="be803-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="be803-109">Especifique o nome do aplicativo lógico, o nome do grupo de recursos, o local, o estado, a ID da conta de integração ou os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="be803-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>

<span data-ttu-id="be803-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="be803-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="be803-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="be803-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="be803-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="be803-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="be803-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="be803-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="be803-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be803-114">EXAMPLES</span></span>

### <span data-ttu-id="be803-115">Exemplo 1: validar um aplicativo lógico usando caminhos de arquivo</span><span class="sxs-lookup"><span data-stu-id="be803-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="be803-116">Esse comando valida um aplicativo lógico chamado LogicApp01 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="be803-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="be803-117">O comando especifica caminhos de arquivo de definição e parâmetro.</span><span class="sxs-lookup"><span data-stu-id="be803-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="be803-118">Exemplo 2: validar um aplicativo lógico usando objetos</span><span class="sxs-lookup"><span data-stu-id="be803-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="be803-119">Esse comando valida um aplicativo lógico chamado LogicApp01 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="be803-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="be803-120">O comando especifica objetos de definição e parâmetro.</span><span class="sxs-lookup"><span data-stu-id="be803-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="be803-121">OS</span><span class="sxs-lookup"><span data-stu-id="be803-121">PARAMETERS</span></span>

### <span data-ttu-id="be803-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be803-122">-DefaultProfile</span></span>
<span data-ttu-id="be803-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="be803-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be803-124">-Definição</span><span class="sxs-lookup"><span data-stu-id="be803-124">-Definition</span></span>
<span data-ttu-id="be803-125">Especifica a definição de um aplicativo lógico como um objeto ou uma cadeia de caracteres em formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="be803-125">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

```yaml
Type: Object
Parameter Sets: LogicAppWithDefinitionParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be803-126">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="be803-126">-DefinitionFilePath</span></span>
<span data-ttu-id="be803-127">Especifica a definição do aplicativo lógico como o caminho de um arquivo de definição no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="be803-127">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: LogicAppWithDefinitionFileParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be803-128">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="be803-128">-IntegrationAccountId</span></span>
<span data-ttu-id="be803-129">Especifica uma ID de conta de integração para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="be803-129">Specifies an integration account ID for the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be803-130">-Local</span><span class="sxs-lookup"><span data-stu-id="be803-130">-Location</span></span>
<span data-ttu-id="be803-131">Especifica o local do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="be803-131">Specifies the location of the logic app.</span></span>
<span data-ttu-id="be803-132">Insira um local do Azure Data Center, como Oeste EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="be803-132">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="be803-133">Você pode colocar um aplicativo lógico em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="be803-133">You can place a logic app in any location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be803-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="be803-134">-Name</span></span>
<span data-ttu-id="be803-135">Especifica o nome do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="be803-135">Specifies the name of the logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be803-136">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="be803-136">-ParameterFilePath</span></span>
<span data-ttu-id="be803-137">Especifica o caminho de um arquivo de parâmetro JSON formatado.</span><span class="sxs-lookup"><span data-stu-id="be803-137">Specifies the path of a JSON formatted parameter file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be803-138">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be803-138">-Parameters</span></span>
<span data-ttu-id="be803-139">Especifica um objeto da coleção Parameters do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="be803-139">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="be803-140">Especifique uma tabela de hash, dicionário \<string\> ou dicionário \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="be803-140">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be803-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be803-141">-ResourceGroupName</span></span>
<span data-ttu-id="be803-142">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="be803-142">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be803-143">-Estado</span><span class="sxs-lookup"><span data-stu-id="be803-143">-State</span></span>
<span data-ttu-id="be803-144">Especifica um estado do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="be803-144">Specifies a state of the logic app.</span></span>
<span data-ttu-id="be803-145">Os valores aceitáveis para esse parâmetro são: Enabled e Disabled.</span><span class="sxs-lookup"><span data-stu-id="be803-145">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be803-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be803-146">CommonParameters</span></span>
<span data-ttu-id="be803-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be803-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be803-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be803-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be803-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be803-149">INPUTS</span></span>

### <span data-ttu-id="be803-150">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="be803-150">None</span></span>
<span data-ttu-id="be803-151">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="be803-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="be803-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be803-152">OUTPUTS</span></span>

### <span data-ttu-id="be803-153">System. Object</span><span class="sxs-lookup"><span data-stu-id="be803-153">System.Object</span></span>

## <span data-ttu-id="be803-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be803-154">NOTES</span></span>

## <span data-ttu-id="be803-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be803-155">RELATED LINKS</span></span>

[<span data-ttu-id="be803-156">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="be803-156">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="be803-157">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="be803-157">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="be803-158">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="be803-158">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="be803-159">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="be803-159">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="be803-160">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="be803-160">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


