---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98263526"
---
# <span data-ttu-id="bcd21-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bcd21-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="bcd21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcd21-102">SYNOPSIS</span></span>
<span data-ttu-id="bcd21-103">Cria ou atualiza saídas para um trabalho do Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bcd21-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="bcd21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcd21-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bcd21-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcd21-105">DESCRIPTION</span></span>
<span data-ttu-id="bcd21-106">O cmdlet **New-AzStreamAnalyticsOutput** cria uma saída dentro de um trabalho do Stream Analytics ou atualiza uma saída existente.</span><span class="sxs-lookup"><span data-stu-id="bcd21-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="bcd21-107">O nome da saída pode ser especificado na guia. Arquivo JSON ou na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="bcd21-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="bcd21-108">Se ambos forem especificados, o nome na linha de comando deve coincidir com o nome no arquivo.</span><span class="sxs-lookup"><span data-stu-id="bcd21-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="bcd21-109">Se você especificar uma saída que já existe e não especificar o parâmetro *Force* , o cmdlet perguntará se deseja ou não substituir a saída existente.</span><span class="sxs-lookup"><span data-stu-id="bcd21-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="bcd21-110">Se você especificar o parâmetro *Force* e especificar um nome de saída existente, a saída será substituída sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="bcd21-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="bcd21-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcd21-111">EXAMPLES</span></span>

### <span data-ttu-id="bcd21-112">Exemplo 1: adicionar uma saída a um trabalho</span><span class="sxs-lookup"><span data-stu-id="bcd21-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="bcd21-113">Esse comando cria uma nova saída chamada output no trabalho chamado StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="bcd21-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="bcd21-114">Se uma saída existente com esse nome já estiver definida, o cmdlet perguntará se deseja ou não substituí-la.</span><span class="sxs-lookup"><span data-stu-id="bcd21-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="bcd21-115">Exemplo 2: substituir uma definição de saída de trabalho</span><span class="sxs-lookup"><span data-stu-id="bcd21-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="bcd21-116">Esse comando substitui a definição de output no trabalho chamado StreamingJob sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="bcd21-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="bcd21-117">OS</span><span class="sxs-lookup"><span data-stu-id="bcd21-117">PARAMETERS</span></span>

### <span data-ttu-id="bcd21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcd21-118">-DefaultProfile</span></span>
<span data-ttu-id="bcd21-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcd21-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcd21-120">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="bcd21-120">-File</span></span>
<span data-ttu-id="bcd21-121">Especifica o caminho para um arquivo JSON que contém a representação JSON da saída do Azure Stream Analytics para criar.</span><span class="sxs-lookup"><span data-stu-id="bcd21-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="bcd21-122">-Force</span><span class="sxs-lookup"><span data-stu-id="bcd21-122">-Force</span></span>
<span data-ttu-id="bcd21-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="bcd21-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bcd21-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="bcd21-124">-JobName</span></span>
<span data-ttu-id="bcd21-125">Especifica o nome do trabalho do Azure Stream Analytics em que será criada a saída do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bcd21-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="bcd21-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcd21-126">-Name</span></span>
<span data-ttu-id="bcd21-127">Especifica o nome da saída do Azure Stream Analytics a ser criada.</span><span class="sxs-lookup"><span data-stu-id="bcd21-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="bcd21-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcd21-128">-ResourceGroupName</span></span>
<span data-ttu-id="bcd21-129">Especifica o nome do grupo de recursos sob o qual criar a saída do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="bcd21-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="bcd21-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bcd21-130">-Confirm</span></span>
<span data-ttu-id="bcd21-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcd21-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcd21-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcd21-132">-WhatIf</span></span>
<span data-ttu-id="bcd21-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bcd21-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcd21-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bcd21-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcd21-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcd21-135">CommonParameters</span></span>
<span data-ttu-id="bcd21-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcd21-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcd21-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcd21-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcd21-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcd21-138">INPUTS</span></span>

### <span data-ttu-id="bcd21-139">System. String</span><span class="sxs-lookup"><span data-stu-id="bcd21-139">System.String</span></span>

## <span data-ttu-id="bcd21-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcd21-140">OUTPUTS</span></span>

### <span data-ttu-id="bcd21-141">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="bcd21-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="bcd21-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcd21-142">NOTES</span></span>

## <span data-ttu-id="bcd21-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcd21-143">RELATED LINKS</span></span>

[<span data-ttu-id="bcd21-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bcd21-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="bcd21-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bcd21-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="bcd21-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="bcd21-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


