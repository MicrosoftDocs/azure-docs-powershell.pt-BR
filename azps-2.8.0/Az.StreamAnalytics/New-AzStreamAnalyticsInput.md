---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 60bc6754fb63d118e2b74e60ab503600a128ba3d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774239"
---
# <span data-ttu-id="4841d-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4841d-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="4841d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4841d-102">SYNOPSIS</span></span>
<span data-ttu-id="4841d-103">Cria ou atualiza uma entrada de trabalho.</span><span class="sxs-lookup"><span data-stu-id="4841d-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="4841d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4841d-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4841d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4841d-105">DESCRIPTION</span></span>
<span data-ttu-id="4841d-106">O cmdlet **New-AzStreamAnalyticsInput** cria uma entrada em um trabalho do Stream Analytics ou atualiza uma entrada existente.</span><span class="sxs-lookup"><span data-stu-id="4841d-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="4841d-107">O nome da entrada pode ser especificado no arquivo JSON ou na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4841d-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="4841d-108">Se ambos forem especificados, o nome na linha de comando deve coincidir com o nome no arquivo.</span><span class="sxs-lookup"><span data-stu-id="4841d-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="4841d-109">Se você especificar uma entrada que já existe e não especificar o parâmetro *Force* , o cmdlet perguntará se deseja ou não substituir a entrada existente.</span><span class="sxs-lookup"><span data-stu-id="4841d-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="4841d-110">Se você especificar o parâmetro *Force* e especificar um nome de entrada existente, a entrada será substituída sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="4841d-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="4841d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4841d-111">EXAMPLES</span></span>

### <span data-ttu-id="4841d-112">EXEMPLO 1: criar uma entrada de trabalho com uma definição de um arquivo</span><span class="sxs-lookup"><span data-stu-id="4841d-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="4841d-113">Esse comando cria uma entrada do arquivo Input.jsem.</span><span class="sxs-lookup"><span data-stu-id="4841d-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="4841d-114">Se uma entrada existente com o nome especificado no arquivo de definição de entrada já estiver definida, o cmdlet perguntará se deseja ou não substituí-la.</span><span class="sxs-lookup"><span data-stu-id="4841d-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="4841d-115">EXEMPLO 2: criar uma entrada de trabalho</span><span class="sxs-lookup"><span data-stu-id="4841d-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="4841d-116">Esse comando cria uma nova entrada no trabalho chamada EntryStream.</span><span class="sxs-lookup"><span data-stu-id="4841d-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="4841d-117">Se uma entrada existente com esse nome já estiver definida, o cmdlet perguntará se deseja ou não substituí-la.</span><span class="sxs-lookup"><span data-stu-id="4841d-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="4841d-118">EXEMPLO 3: substituir uma entrada de trabalho por uma definição de um arquivo</span><span class="sxs-lookup"><span data-stu-id="4841d-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="4841d-119">Esse comando substitui a definição da fonte de entrada existente chamada EntryStream com a definição do arquivo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="4841d-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="4841d-120">OS</span><span class="sxs-lookup"><span data-stu-id="4841d-120">PARAMETERS</span></span>

### <span data-ttu-id="4841d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4841d-121">-DefaultProfile</span></span>
<span data-ttu-id="4841d-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4841d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4841d-123">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="4841d-123">-File</span></span>
<span data-ttu-id="4841d-124">Especifica o caminho para um arquivo JSON que contém a representação JSON da entrada do Azure Stream Analytics a ser criada.</span><span class="sxs-lookup"><span data-stu-id="4841d-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4841d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4841d-125">-Force</span></span>
<span data-ttu-id="4841d-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="4841d-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4841d-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="4841d-127">-JobName</span></span>
<span data-ttu-id="4841d-128">Especifica o nome do trabalho do Azure Stream Analytics em que a entrada do Azure Stream Analytics deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="4841d-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="4841d-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="4841d-129">-Name</span></span>
<span data-ttu-id="4841d-130">Especifica o nome da entrada do Azure Stream Analytics a ser criada.</span><span class="sxs-lookup"><span data-stu-id="4841d-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4841d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4841d-131">-ResourceGroupName</span></span>
<span data-ttu-id="4841d-132">Especifica o nome do grupo de recursos sob o qual criar a entrada de fluxo do Azure.</span><span class="sxs-lookup"><span data-stu-id="4841d-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="4841d-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4841d-133">-Confirm</span></span>
<span data-ttu-id="4841d-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4841d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4841d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4841d-135">-WhatIf</span></span>
<span data-ttu-id="4841d-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4841d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4841d-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4841d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4841d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4841d-138">CommonParameters</span></span>
<span data-ttu-id="4841d-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4841d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4841d-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4841d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4841d-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4841d-141">INPUTS</span></span>

### <span data-ttu-id="4841d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4841d-142">System.String</span></span>

## <span data-ttu-id="4841d-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4841d-143">OUTPUTS</span></span>

### <span data-ttu-id="4841d-144">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="4841d-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="4841d-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4841d-145">NOTES</span></span>

## <span data-ttu-id="4841d-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4841d-146">RELATED LINKS</span></span>

[<span data-ttu-id="4841d-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4841d-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4841d-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4841d-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="4841d-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="4841d-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


