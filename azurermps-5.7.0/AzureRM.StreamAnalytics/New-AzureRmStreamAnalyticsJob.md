---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b17eb98ec8dc1aa64760a61ee731f67cf7b05139
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431534"
---
# <span data-ttu-id="89e16-101">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="89e16-101">New-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="89e16-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89e16-102">SYNOPSIS</span></span>
<span data-ttu-id="89e16-103">Cria ou atualiza um trabalho analítico do Stream.</span><span class="sxs-lookup"><span data-stu-id="89e16-103">Creates or updates a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89e16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89e16-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89e16-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89e16-105">DESCRIPTION</span></span>
<span data-ttu-id="89e16-106">O cmdlet **New-AzureRmStreamAnalyticsJob** cria um novo trabalho do Stream Analytics no Azure ou atualiza a definição de um trabalho especificado existente.</span><span class="sxs-lookup"><span data-stu-id="89e16-106">The **New-AzureRmStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="89e16-107">O nome do trabalho pode ser especificado no. Arquivo JSON ou na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="89e16-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="89e16-108">Se ambos forem especificados, o nome na linha de comando deve coincidir com o nome no arquivo.</span><span class="sxs-lookup"><span data-stu-id="89e16-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="89e16-109">Se você especificar um nome de trabalho que já existe e não especificar o parâmetro *Force* , o cmdlet perguntará se você deseja ou não substituir o trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="89e16-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>

<span data-ttu-id="89e16-110">Se você especificar o parâmetro *Force* e especificar um nome de trabalho existente, a definição do trabalho será substituída sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="89e16-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="89e16-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89e16-111">EXAMPLES</span></span>

### <span data-ttu-id="89e16-112">EXEMPLO 1: criar um trabalho</span><span class="sxs-lookup"><span data-stu-id="89e16-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="89e16-113">Esse comando cria um trabalho a partir da definição em JobDefinition.js.</span><span class="sxs-lookup"><span data-stu-id="89e16-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="89e16-114">Se um trabalho existente com o nome especificado no arquivo de definição de trabalho já estiver definido, o cmdlet perguntará se ele será substituído ou não.</span><span class="sxs-lookup"><span data-stu-id="89e16-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="89e16-115">EXEMPLO 2: substituir uma definição de trabalho</span><span class="sxs-lookup"><span data-stu-id="89e16-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="89e16-116">Esse comando substitui a definição do trabalho para StreamingJob sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="89e16-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="89e16-117">OS</span><span class="sxs-lookup"><span data-stu-id="89e16-117">PARAMETERS</span></span>

### <span data-ttu-id="89e16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e16-118">-DefaultProfile</span></span>
<span data-ttu-id="89e16-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89e16-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e16-120">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="89e16-120">-File</span></span>
<span data-ttu-id="89e16-121">Especifica o caminho para um arquivo JSON que contém a representação JSON do trabalho do Azure Stream Analytics a ser criado.</span><span class="sxs-lookup"><span data-stu-id="89e16-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e16-122">-Force</span><span class="sxs-lookup"><span data-stu-id="89e16-122">-Force</span></span>
<span data-ttu-id="89e16-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="89e16-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="89e16-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="89e16-124">-Name</span></span>
<span data-ttu-id="89e16-125">Especifica o nome do trabalho do Azure Stream Analytics a ser criado.</span><span class="sxs-lookup"><span data-stu-id="89e16-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89e16-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89e16-126">-ResourceGroupName</span></span>
<span data-ttu-id="89e16-127">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="89e16-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="89e16-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89e16-128">-Confirm</span></span>
<span data-ttu-id="89e16-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89e16-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e16-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e16-130">-WhatIf</span></span>
<span data-ttu-id="89e16-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89e16-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89e16-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89e16-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89e16-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e16-133">CommonParameters</span></span>
<span data-ttu-id="89e16-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e16-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e16-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e16-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e16-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89e16-136">INPUTS</span></span>

### <span data-ttu-id="89e16-137">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="89e16-137">None</span></span>
<span data-ttu-id="89e16-138">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="89e16-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89e16-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89e16-139">OUTPUTS</span></span>

### <span data-ttu-id="89e16-140">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="89e16-140">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="89e16-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89e16-141">NOTES</span></span>

## <span data-ttu-id="89e16-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89e16-142">RELATED LINKS</span></span>

[<span data-ttu-id="89e16-143">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="89e16-143">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="89e16-144">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="89e16-144">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="89e16-145">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="89e16-145">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="89e16-146">Parar-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="89e16-146">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="89e16-147">Parar-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="89e16-147">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

