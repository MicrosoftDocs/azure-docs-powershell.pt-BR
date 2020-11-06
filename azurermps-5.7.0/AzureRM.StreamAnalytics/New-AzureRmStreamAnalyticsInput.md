---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: d16b59ed089c4756cc83363f645bdd7c47bb7f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431536"
---
# <span data-ttu-id="77f11-101">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="77f11-101">New-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="77f11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77f11-102">SYNOPSIS</span></span>
<span data-ttu-id="77f11-103">Cria ou atualiza uma entrada de trabalho.</span><span class="sxs-lookup"><span data-stu-id="77f11-103">Creates or updates a job input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77f11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77f11-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77f11-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77f11-105">DESCRIPTION</span></span>
<span data-ttu-id="77f11-106">O cmdlet **New-AzureRmStreamAnalyticsInput** cria uma entrada em um trabalho do Stream Analytics ou atualiza uma entrada existente.</span><span class="sxs-lookup"><span data-stu-id="77f11-106">The **New-AzureRmStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="77f11-107">O nome da entrada pode ser especificado no arquivo JSON ou na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="77f11-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="77f11-108">Se ambos forem especificados, o nome na linha de comando deve coincidir com o nome no arquivo.</span><span class="sxs-lookup"><span data-stu-id="77f11-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="77f11-109">Se você especificar uma entrada que já existe e não especificar o parâmetro *Force* , o cmdlet perguntará se deseja ou não substituir a entrada existente.</span><span class="sxs-lookup"><span data-stu-id="77f11-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>

<span data-ttu-id="77f11-110">Se você especificar o parâmetro *Force* e especificar um nome de entrada existente, a entrada será substituída sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="77f11-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="77f11-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77f11-111">EXAMPLES</span></span>

### <span data-ttu-id="77f11-112">EXEMPLO 1: criar uma entrada de trabalho com uma definição de um arquivo</span><span class="sxs-lookup"><span data-stu-id="77f11-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="77f11-113">Esse comando cria uma entrada do arquivo Input.jsem.</span><span class="sxs-lookup"><span data-stu-id="77f11-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="77f11-114">Se uma entrada existente com o nome especificado no arquivo de definição de entrada já estiver definida, o cmdlet perguntará se deseja ou não substituí-la.</span><span class="sxs-lookup"><span data-stu-id="77f11-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="77f11-115">EXEMPLO 2: criar uma entrada de trabalho</span><span class="sxs-lookup"><span data-stu-id="77f11-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="77f11-116">Esse comando cria uma nova entrada no trabalho chamada EntryStream.</span><span class="sxs-lookup"><span data-stu-id="77f11-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="77f11-117">Se uma entrada existente com esse nome já estiver definida, o cmdlet perguntará se deseja ou não substituí-la.</span><span class="sxs-lookup"><span data-stu-id="77f11-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="77f11-118">EXEMPLO 3: substituir uma entrada de trabalho por uma definição de um arquivo</span><span class="sxs-lookup"><span data-stu-id="77f11-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="77f11-119">Esse comando substitui a definição da fonte de entrada existente chamada EntryStream com a definição do arquivo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="77f11-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="77f11-120">OS</span><span class="sxs-lookup"><span data-stu-id="77f11-120">PARAMETERS</span></span>

### <span data-ttu-id="77f11-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77f11-121">-DefaultProfile</span></span>
<span data-ttu-id="77f11-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77f11-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77f11-123">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="77f11-123">-File</span></span>
<span data-ttu-id="77f11-124">Especifica o caminho para um arquivo JSON que contém a representação JSON da entrada do Azure Stream Analytics a ser criada.</span><span class="sxs-lookup"><span data-stu-id="77f11-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f11-125">-Force</span><span class="sxs-lookup"><span data-stu-id="77f11-125">-Force</span></span>
<span data-ttu-id="77f11-126">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="77f11-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f11-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="77f11-127">-JobName</span></span>
<span data-ttu-id="77f11-128">Especifica o nome do trabalho do Azure Stream Analytics em que a entrada do Azure Stream Analytics deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="77f11-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f11-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="77f11-129">-Name</span></span>
<span data-ttu-id="77f11-130">Especifica o nome da entrada do Azure Stream Analytics a ser criada.</span><span class="sxs-lookup"><span data-stu-id="77f11-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f11-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77f11-131">-ResourceGroupName</span></span>
<span data-ttu-id="77f11-132">Especifica o nome do grupo de recursos sob o qual criar a entrada de fluxo do Azure.</span><span class="sxs-lookup"><span data-stu-id="77f11-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77f11-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="77f11-133">-Confirm</span></span>
<span data-ttu-id="77f11-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77f11-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f11-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77f11-135">-WhatIf</span></span>
<span data-ttu-id="77f11-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="77f11-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77f11-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="77f11-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77f11-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77f11-138">CommonParameters</span></span>
<span data-ttu-id="77f11-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77f11-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77f11-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77f11-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77f11-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77f11-141">INPUTS</span></span>

### <span data-ttu-id="77f11-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="77f11-142">None</span></span>
<span data-ttu-id="77f11-143">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="77f11-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="77f11-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77f11-144">OUTPUTS</span></span>

### <span data-ttu-id="77f11-145">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="77f11-145">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="77f11-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77f11-146">NOTES</span></span>

## <span data-ttu-id="77f11-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77f11-147">RELATED LINKS</span></span>

[<span data-ttu-id="77f11-148">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="77f11-148">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="77f11-149">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="77f11-149">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="77f11-150">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="77f11-150">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


