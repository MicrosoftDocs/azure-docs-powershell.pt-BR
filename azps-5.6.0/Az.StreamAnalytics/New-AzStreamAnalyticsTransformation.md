---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: d9529d31ab53c16b3d8be10c2d92761a2c8a5fee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892592"
---
# <span data-ttu-id="7ff50-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="7ff50-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="7ff50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ff50-102">SYNOPSIS</span></span>
<span data-ttu-id="7ff50-103">Cria ou atualiza uma transformação dentro de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="7ff50-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="7ff50-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7ff50-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ff50-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7ff50-105">DESCRIPTION</span></span>
<span data-ttu-id="7ff50-106">O cmdlet **New-AzStreamAnalyticsTransformation** cria uma transformação dentro de um trabalho do Stream Analytics ou atualiza a transformação existente.</span><span class="sxs-lookup"><span data-stu-id="7ff50-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="7ff50-107">O nome da transformação pode ser especificado no . Arquivo JSON ou na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="7ff50-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="7ff50-108">Se ambos são especificados, o nome na linha de comando deve corresponder ao nome no arquivo.</span><span class="sxs-lookup"><span data-stu-id="7ff50-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="7ff50-109">Se você especificar uma transformação que já existe e não especificar o parâmetro Force, o cmdlet perguntará se deve ou não substituir a transformação existente.</span><span class="sxs-lookup"><span data-stu-id="7ff50-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="7ff50-110">Se você especificar o *parâmetro Force* e especificar um nome de transformação existente, a transformação será substituída sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="7ff50-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="7ff50-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ff50-111">EXAMPLES</span></span>

### <span data-ttu-id="7ff50-112">Exemplo 1: Criar ou substituir uma transformação em um trabalho</span><span class="sxs-lookup"><span data-stu-id="7ff50-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="7ff50-113">Este comando cria uma transformação chamada StreamingJobTransform no trabalho chamado StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="7ff50-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="7ff50-114">Se uma transformação existente já estiver definida com esse nome, o cmdlet perguntará se a substituirá ou não.</span><span class="sxs-lookup"><span data-stu-id="7ff50-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="7ff50-115">Exemplo 2: Substituir uma transformação em um trabalho</span><span class="sxs-lookup"><span data-stu-id="7ff50-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="7ff50-116">Este comando substitui a definição de StreamingJobTransform no trabalho StreamingJob sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="7ff50-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="7ff50-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7ff50-117">PARAMETERS</span></span>

### <span data-ttu-id="7ff50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ff50-118">-DefaultProfile</span></span>
<span data-ttu-id="7ff50-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7ff50-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ff50-120">-File</span><span class="sxs-lookup"><span data-stu-id="7ff50-120">-File</span></span>
<span data-ttu-id="7ff50-121">Especifica o caminho para um arquivo JSON que contém a representação JSON da transformação do Azure Stream Analytics a ser criado.</span><span class="sxs-lookup"><span data-stu-id="7ff50-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="7ff50-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7ff50-122">-Force</span></span>
<span data-ttu-id="7ff50-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="7ff50-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ff50-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="7ff50-124">-JobName</span></span>
<span data-ttu-id="7ff50-125">Especifica o nome do trabalho do Azure Stream Analytics no qual criar a transformação do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ff50-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="7ff50-126">-Name</span><span class="sxs-lookup"><span data-stu-id="7ff50-126">-Name</span></span>
<span data-ttu-id="7ff50-127">Especifica o nome da transformação do Azure Stream Analytics a ser criado.</span><span class="sxs-lookup"><span data-stu-id="7ff50-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="7ff50-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ff50-128">-ResourceGroupName</span></span>
<span data-ttu-id="7ff50-129">Especifica o nome do grupo de recursos no qual criar a transformação do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ff50-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="7ff50-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ff50-130">-Confirm</span></span>
<span data-ttu-id="7ff50-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ff50-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ff50-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ff50-132">-WhatIf</span></span>
<span data-ttu-id="7ff50-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ff50-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ff50-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ff50-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ff50-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ff50-135">CommonParameters</span></span>
<span data-ttu-id="7ff50-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ff50-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ff50-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ff50-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ff50-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7ff50-138">INPUTS</span></span>

### <span data-ttu-id="7ff50-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7ff50-139">System.String</span></span>

## <span data-ttu-id="7ff50-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7ff50-140">OUTPUTS</span></span>

### <span data-ttu-id="7ff50-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="7ff50-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="7ff50-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="7ff50-142">NOTES</span></span>

## <span data-ttu-id="7ff50-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ff50-143">RELATED LINKS</span></span>

[<span data-ttu-id="7ff50-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="7ff50-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


