---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 929F4593-2A71-49B9-87F8-F24FA9F6E314
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Test-AzureRmLogicApp.md
ms.openlocfilehash: fa848a8249fa01a61a7aa50855f24b2813b9fdf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441533"
---
# <span data-ttu-id="c7512-101">Test-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c7512-101">Test-AzureRmLogicApp</span></span>

## <span data-ttu-id="c7512-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7512-102">SYNOPSIS</span></span>
<span data-ttu-id="c7512-103">Valida uma definição de aplicativo lógica.</span><span class="sxs-lookup"><span data-stu-id="c7512-103">Validates a logic app definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7512-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7512-104">SYNTAX</span></span>

### <span data-ttu-id="c7512-105">LogicAppWithDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7512-105">LogicAppWithDefinitionParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-Definition <Object>] [-IntegrationAccountId <String>] [-Parameters <Object>] [-ParameterFilePath <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7512-106">LogicAppWithDefinitionFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7512-106">LogicAppWithDefinitionFileParameterSet</span></span>
```
Test-AzureRmLogicApp -ResourceGroupName <String> -Name <String> -Location <String> [-State <String>]
 [-DefinitionFilePath <String>] [-IntegrationAccountId <String>] [-Parameters <Object>]
 [-ParameterFilePath <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7512-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7512-107">DESCRIPTION</span></span>
<span data-ttu-id="c7512-108">O cmdlet **Test-AzureRmLogicApp** valida uma definição de aplicativo lógica em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7512-108">The **Test-AzureRmLogicApp** cmdlet validates a logic app definition in a resource group.</span></span>
<span data-ttu-id="c7512-109">Especifique o nome do aplicativo lógico, o nome do grupo de recursos, o local, o estado, a ID da conta de integração ou os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c7512-109">Specify the logic app name, resource group name, location, state, integration account ID, or parameters.</span></span>

<span data-ttu-id="c7512-110">Este módulo dá suporte a parâmetros dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="c7512-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c7512-111">Para usar um parâmetro dinâmico, digite-o no comando.</span><span class="sxs-lookup"><span data-stu-id="c7512-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c7512-112">Para descobrir os nomes dos parâmetros dinâmicos, digite um hífen (-) após o nome do cmdlet e, em seguida, pressione a tecla TAB repetidamente para percorrer os parâmetros disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c7512-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c7512-113">Se você omitir um parâmetro de modelo obrigatório, o cmdlet solicitará que você tenha o valor.</span><span class="sxs-lookup"><span data-stu-id="c7512-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c7512-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7512-114">EXAMPLES</span></span>

### <span data-ttu-id="c7512-115">Exemplo 1: validar um aplicativo lógico usando caminhos de arquivo</span><span class="sxs-lookup"><span data-stu-id="c7512-115">Example 1: Validate a logic app by using file paths</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -DefinitionFilePath "d:\workflows\Definition.json" -ParameterFilePath "d:\workflows\Parameters.json"
```

<span data-ttu-id="c7512-116">Esse comando valida um aplicativo lógico chamado LogicApp01 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c7512-116">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="c7512-117">O comando especifica caminhos de arquivo de definição e parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c7512-117">The command specifies definition and parameter file paths.</span></span>

### <span data-ttu-id="c7512-118">Exemplo 2: validar um aplicativo lógico usando objetos</span><span class="sxs-lookup"><span data-stu-id="c7512-118">Example 2: Validate a logic app by using objects</span></span>
```
PS C:\>Test-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp01" -Location "westus" -State "Enabled" -Definition [IO.File]::ReadAllText("d:\Workflows\Definition.json") -Parameters @{name1="value1", name2="value2"}
```

<span data-ttu-id="c7512-119">Esse comando valida um aplicativo lógico chamado LogicApp01 no grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="c7512-119">This command validates a logic app named LogicApp01 in the specified resource group.</span></span>
<span data-ttu-id="c7512-120">O comando especifica objetos de definição e parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c7512-120">The command specifies definition and parameter objects.</span></span>

## <span data-ttu-id="c7512-121">OS</span><span class="sxs-lookup"><span data-stu-id="c7512-121">PARAMETERS</span></span>

### <span data-ttu-id="c7512-122">-Definição</span><span class="sxs-lookup"><span data-stu-id="c7512-122">-Definition</span></span>
<span data-ttu-id="c7512-123">Especifica a definição de um aplicativo lógico como um objeto ou uma cadeia de caracteres em formato JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="c7512-123">Specifies the definition of a logic app as an object or a string in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="c7512-124">-DefinitionFilePath</span><span class="sxs-lookup"><span data-stu-id="c7512-124">-DefinitionFilePath</span></span>
<span data-ttu-id="c7512-125">Especifica a definição do aplicativo lógico como o caminho de um arquivo de definição no formato JSON.</span><span class="sxs-lookup"><span data-stu-id="c7512-125">Specifies the definition of your logic app as the path of a definition file in JSON format.</span></span>

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

### <span data-ttu-id="c7512-126">-IntegrationAccountId</span><span class="sxs-lookup"><span data-stu-id="c7512-126">-IntegrationAccountId</span></span>
<span data-ttu-id="c7512-127">Especifica uma ID de conta de integração para o aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c7512-127">Specifies an integration account ID for the logic app.</span></span>

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

### <span data-ttu-id="c7512-128">-Local</span><span class="sxs-lookup"><span data-stu-id="c7512-128">-Location</span></span>
<span data-ttu-id="c7512-129">Especifica o local do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c7512-129">Specifies the location of the logic app.</span></span>
<span data-ttu-id="c7512-130">Insira um local do Azure Data Center, como Oeste EUA ou sudeste asiático.</span><span class="sxs-lookup"><span data-stu-id="c7512-130">Enter an Azure data center location, such as West US or Southeast Asia.</span></span>
<span data-ttu-id="c7512-131">Você pode colocar um aplicativo lógico em qualquer local.</span><span class="sxs-lookup"><span data-stu-id="c7512-131">You can place a logic app in any location.</span></span>

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

### <span data-ttu-id="c7512-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7512-132">-Name</span></span>
<span data-ttu-id="c7512-133">Especifica o nome do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c7512-133">Specifies the name of the logic app.</span></span>

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

### <span data-ttu-id="c7512-134">-ParameterFilePath</span><span class="sxs-lookup"><span data-stu-id="c7512-134">-ParameterFilePath</span></span>
<span data-ttu-id="c7512-135">Especifica o caminho de um arquivo de parâmetro JSON formatado.</span><span class="sxs-lookup"><span data-stu-id="c7512-135">Specifies the path of a JSON formatted parameter file.</span></span>

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

### <span data-ttu-id="c7512-136">-Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7512-136">-Parameters</span></span>
<span data-ttu-id="c7512-137">Especifica um objeto da coleção Parameters do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c7512-137">Specifies a parameters collection object of the logic app.</span></span>
<span data-ttu-id="c7512-138">Especifique uma tabela de hash, dicionário \<string\> ou dicionário \<string, WorkflowParameter\> .</span><span class="sxs-lookup"><span data-stu-id="c7512-138">Specify a hash table, Dictionary\<string\>, or Dictionary\<string, WorkflowParameter\>.</span></span>

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

### <span data-ttu-id="c7512-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7512-139">-ResourceGroupName</span></span>
<span data-ttu-id="c7512-140">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c7512-140">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c7512-141">-Estado</span><span class="sxs-lookup"><span data-stu-id="c7512-141">-State</span></span>
<span data-ttu-id="c7512-142">Especifica um estado do aplicativo lógico.</span><span class="sxs-lookup"><span data-stu-id="c7512-142">Specifies a state of the logic app.</span></span>
<span data-ttu-id="c7512-143">Os valores aceitáveis para esse parâmetro são: Enabled e Disabled.</span><span class="sxs-lookup"><span data-stu-id="c7512-143">The acceptable values for this parameter are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="c7512-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7512-144">-DefaultProfile</span></span>
<span data-ttu-id="c7512-145">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7512-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7512-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7512-146">CommonParameters</span></span>
<span data-ttu-id="c7512-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7512-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7512-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7512-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7512-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7512-149">INPUTS</span></span>

## <span data-ttu-id="c7512-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7512-150">OUTPUTS</span></span>

### <span data-ttu-id="c7512-151">System. Object</span><span class="sxs-lookup"><span data-stu-id="c7512-151">System.Object</span></span>

## <span data-ttu-id="c7512-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7512-152">NOTES</span></span>

## <span data-ttu-id="c7512-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7512-153">RELATED LINKS</span></span>

[<span data-ttu-id="c7512-154">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c7512-154">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="c7512-155">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c7512-155">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="c7512-156">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c7512-156">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="c7512-157">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c7512-157">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="c7512-158">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c7512-158">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


