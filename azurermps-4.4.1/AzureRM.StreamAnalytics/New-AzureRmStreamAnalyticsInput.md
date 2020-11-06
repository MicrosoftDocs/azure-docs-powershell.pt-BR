---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 84df5d0ed28b2d11b3e03e298242da4938a47eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440926"
---
# <span data-ttu-id="9a0ae-101">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="9a0ae-101">New-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="9a0ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a0ae-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0ae-103">Cria ou atualiza uma entrada de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-103">Creates or updates a job input.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a0ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a0ae-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a0ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a0ae-105">DESCRIPTION</span></span>
<span data-ttu-id="9a0ae-106">O cmdlet **New-AzureRmStreamAnalyticsInput** cria uma entrada em um trabalho do Stream Analytics ou atualiza uma entrada existente.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-106">The **New-AzureRmStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="9a0ae-107">O nome da entrada pode ser especificado no arquivo JSON ou na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="9a0ae-108">Se ambos forem especificados, o nome na linha de comando deve coincidir com o nome no arquivo.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="9a0ae-109">Se você especificar uma entrada que já existe e não especificar o parâmetro *Force* , o cmdlet perguntará se deseja ou não substituir a entrada existente.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>

<span data-ttu-id="9a0ae-110">Se você especificar o parâmetro *Force* e especificar um nome de entrada existente, a entrada será substituída sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="9a0ae-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a0ae-111">EXAMPLES</span></span>

### <span data-ttu-id="9a0ae-112">EXEMPLO 1: criar uma entrada de trabalho com uma definição de um arquivo</span><span class="sxs-lookup"><span data-stu-id="9a0ae-112">EXAMPLE 1: Create a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="9a0ae-113">Esse comando cria uma entrada do arquivo Input.jsem.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="9a0ae-114">Se uma entrada existente com o nome especificado no arquivo de definição de entrada já estiver definida, o cmdlet perguntará se deseja ou não substituí-la.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="9a0ae-115">EXEMPLO 2: criar uma entrada de trabalho</span><span class="sxs-lookup"><span data-stu-id="9a0ae-115">EXAMPLE 2: Create a job input</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="9a0ae-116">Esse comando cria uma nova entrada no trabalho chamada EntryStream.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="9a0ae-117">Se uma entrada existente com esse nome já estiver definida, o cmdlet perguntará se deseja ou não substituí-la.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="9a0ae-118">EXEMPLO 3: substituir uma entrada de trabalho por uma definição de um arquivo</span><span class="sxs-lookup"><span data-stu-id="9a0ae-118">EXAMPLE 3: Replace a job input with a definition from a file</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="9a0ae-119">Esse comando substitui a definição da fonte de entrada existente chamada EntryStream com a definição do arquivo sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="9a0ae-120">OS</span><span class="sxs-lookup"><span data-stu-id="9a0ae-120">PARAMETERS</span></span>

### <span data-ttu-id="9a0ae-121">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="9a0ae-121">-File</span></span>
<span data-ttu-id="9a0ae-122">Especifica o caminho para um arquivo JSON que contém a representação JSON da entrada do Azure Stream Analytics a ser criada.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-122">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="9a0ae-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9a0ae-123">-Force</span></span>
<span data-ttu-id="9a0ae-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9a0ae-125">-JobName</span><span class="sxs-lookup"><span data-stu-id="9a0ae-125">-JobName</span></span>
<span data-ttu-id="9a0ae-126">Especifica o nome do trabalho do Azure Stream Analytics em que a entrada do Azure Stream Analytics deve ser criada.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-126">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="9a0ae-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a0ae-127">-Name</span></span>
<span data-ttu-id="9a0ae-128">Especifica o nome da entrada do Azure Stream Analytics a ser criada.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-128">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="9a0ae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a0ae-129">-ResourceGroupName</span></span>
<span data-ttu-id="9a0ae-130">Especifica o nome do grupo de recursos sob o qual criar a entrada de fluxo do Azure.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-130">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="9a0ae-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9a0ae-131">-Confirm</span></span>
<span data-ttu-id="9a0ae-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a0ae-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a0ae-133">-WhatIf</span></span>
<span data-ttu-id="9a0ae-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a0ae-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a0ae-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0ae-136">-DefaultProfile</span></span>
<span data-ttu-id="9a0ae-137">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a0ae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0ae-138">CommonParameters</span></span>
<span data-ttu-id="9a0ae-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a0ae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0ae-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a0ae-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0ae-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a0ae-141">INPUTS</span></span>

## <span data-ttu-id="9a0ae-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a0ae-142">OUTPUTS</span></span>

### <span data-ttu-id="9a0ae-143">Microsoft. Azure. Commands. StreamAnalytics. Models. PSInput</span><span class="sxs-lookup"><span data-stu-id="9a0ae-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="9a0ae-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a0ae-144">NOTES</span></span>

## <span data-ttu-id="9a0ae-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a0ae-145">RELATED LINKS</span></span>

[<span data-ttu-id="9a0ae-146">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="9a0ae-146">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="9a0ae-147">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="9a0ae-147">Remove-AzureRmStreamAnalyticsInput</span></span>](./Remove-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="9a0ae-148">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="9a0ae-148">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


