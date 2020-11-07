---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: b50141c37c55d55f8fd8e823f09fefad49a55543
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774237"
---
# <span data-ttu-id="81a44-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81a44-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="81a44-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="81a44-102">SYNOPSIS</span></span>
<span data-ttu-id="81a44-103">Cria ou atualiza um trabalho analítico do Stream.</span><span class="sxs-lookup"><span data-stu-id="81a44-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="81a44-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="81a44-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81a44-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="81a44-105">DESCRIPTION</span></span>
<span data-ttu-id="81a44-106">O cmdlet **New-AzStreamAnalyticsJob** cria um novo trabalho do Stream Analytics no Azure ou atualiza a definição de um trabalho especificado existente.</span><span class="sxs-lookup"><span data-stu-id="81a44-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="81a44-107">O nome do trabalho pode ser especificado no. Arquivo JSON ou na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="81a44-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="81a44-108">Se ambos forem especificados, o nome na linha de comando deve coincidir com o nome no arquivo.</span><span class="sxs-lookup"><span data-stu-id="81a44-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="81a44-109">Se você especificar um nome de trabalho que já existe e não especificar o parâmetro *Force* , o cmdlet perguntará se você deseja ou não substituir o trabalho existente.</span><span class="sxs-lookup"><span data-stu-id="81a44-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="81a44-110">Se você especificar o parâmetro *Force* e especificar um nome de trabalho existente, a definição do trabalho será substituída sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="81a44-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="81a44-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81a44-111">EXAMPLES</span></span>

### <span data-ttu-id="81a44-112">EXEMPLO 1: criar um trabalho</span><span class="sxs-lookup"><span data-stu-id="81a44-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="81a44-113">Esse comando cria um trabalho a partir da definição em JobDefinition.js.</span><span class="sxs-lookup"><span data-stu-id="81a44-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="81a44-114">Se um trabalho existente com o nome especificado no arquivo de definição de trabalho já estiver definido, o cmdlet perguntará se ele será substituído ou não.</span><span class="sxs-lookup"><span data-stu-id="81a44-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="81a44-115">EXEMPLO 2: substituir uma definição de trabalho</span><span class="sxs-lookup"><span data-stu-id="81a44-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="81a44-116">Esse comando substitui a definição do trabalho para StreamingJob sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="81a44-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="81a44-117">OS</span><span class="sxs-lookup"><span data-stu-id="81a44-117">PARAMETERS</span></span>

### <span data-ttu-id="81a44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81a44-118">-DefaultProfile</span></span>
<span data-ttu-id="81a44-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81a44-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81a44-120">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="81a44-120">-File</span></span>
<span data-ttu-id="81a44-121">Especifica o caminho para um arquivo JSON que contém a representação JSON do trabalho do Azure Stream Analytics a ser criado.</span><span class="sxs-lookup"><span data-stu-id="81a44-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81a44-122">-Force</span><span class="sxs-lookup"><span data-stu-id="81a44-122">-Force</span></span>
<span data-ttu-id="81a44-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="81a44-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81a44-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="81a44-124">-Name</span></span>
<span data-ttu-id="81a44-125">Especifica o nome do trabalho do Azure Stream Analytics a ser criado.</span><span class="sxs-lookup"><span data-stu-id="81a44-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81a44-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81a44-126">-ResourceGroupName</span></span>
<span data-ttu-id="81a44-127">Especifica o nome do grupo de recursos ao qual o trabalho do Azure Stream Analytics deve pertencer.</span><span class="sxs-lookup"><span data-stu-id="81a44-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="81a44-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="81a44-128">-Confirm</span></span>
<span data-ttu-id="81a44-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81a44-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81a44-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81a44-130">-WhatIf</span></span>
<span data-ttu-id="81a44-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="81a44-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81a44-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="81a44-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81a44-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a44-133">CommonParameters</span></span>
<span data-ttu-id="81a44-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a44-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a44-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a44-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a44-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="81a44-136">INPUTS</span></span>

### <span data-ttu-id="81a44-137">System. String</span><span class="sxs-lookup"><span data-stu-id="81a44-137">System.String</span></span>

## <span data-ttu-id="81a44-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="81a44-138">OUTPUTS</span></span>

### <span data-ttu-id="81a44-139">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="81a44-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="81a44-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="81a44-140">NOTES</span></span>

## <span data-ttu-id="81a44-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81a44-141">RELATED LINKS</span></span>

[<span data-ttu-id="81a44-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81a44-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="81a44-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81a44-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="81a44-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81a44-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="81a44-145">Parar-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81a44-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="81a44-146">Parar-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="81a44-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


