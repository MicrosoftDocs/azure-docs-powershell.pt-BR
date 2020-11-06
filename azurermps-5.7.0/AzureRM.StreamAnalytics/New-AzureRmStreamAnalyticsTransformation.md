---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: a235619452966aa4dbce8381fdb22ea6c5f5fedc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431530"
---
# <span data-ttu-id="ffdb6-101">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="ffdb6-101">New-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="ffdb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffdb6-102">SYNOPSIS</span></span>
<span data-ttu-id="ffdb6-103">Cria ou atualiza uma transformação dentro de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-103">Creates or updates a transformation within a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffdb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffdb6-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffdb6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffdb6-105">DESCRIPTION</span></span>
<span data-ttu-id="ffdb6-106">O cmdlet **New-AzureRmStreamAnalyticsTransformation** cria uma transformação dentro de um trabalho do Stream Analytics ou atualiza a transformação existente.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-106">The **New-AzureRmStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="ffdb6-107">O nome da transformação pode ser especificado no. Arquivo JSON ou na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="ffdb6-108">Se ambos forem especificados, o nome na linha de comando deve coincidir com o nome no arquivo.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="ffdb6-109">Se você especificar uma transformação que já existe e não especificar o parâmetro Force, o cmdlet perguntará se deseja ou não substituir a transformação existente.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>

<span data-ttu-id="ffdb6-110">Se você especificar o parâmetro *Force* e especificar um nome de transformação existente, a transformação será substituída sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="ffdb6-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffdb6-111">EXAMPLES</span></span>

### <span data-ttu-id="ffdb6-112">EXEMPLO 1: criar ou substituir uma transformação em um trabalho</span><span class="sxs-lookup"><span data-stu-id="ffdb6-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="ffdb6-113">Esse comando cria uma transformação chamada StreamingJobTransform no trabalho chamado StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="ffdb6-114">Se uma transformação existente já estiver definida com esse nome, o cmdlet perguntará se ela será substituída ou não.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="ffdb6-115">EXEMPLO 2: substituir uma transformação em um trabalho</span><span class="sxs-lookup"><span data-stu-id="ffdb6-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="ffdb6-116">Esse comando substitui a definição de StreamingJobTransform no trabalho StreamingJob sem confirmação.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="ffdb6-117">OS</span><span class="sxs-lookup"><span data-stu-id="ffdb6-117">PARAMETERS</span></span>

### <span data-ttu-id="ffdb6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffdb6-118">-DefaultProfile</span></span>
<span data-ttu-id="ffdb6-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ffdb6-120">-Arquivo</span><span class="sxs-lookup"><span data-stu-id="ffdb6-120">-File</span></span>
<span data-ttu-id="ffdb6-121">Especifica o caminho para um arquivo JSON que contém a representação JSON da transformação do Azure Stream Analytics a ser criada.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="ffdb6-122">-Force</span><span class="sxs-lookup"><span data-stu-id="ffdb6-122">-Force</span></span>
<span data-ttu-id="ffdb6-123">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ffdb6-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="ffdb6-124">-JobName</span></span>
<span data-ttu-id="ffdb6-125">Especifica o nome do trabalho do Azure Stream Analytics em que a transformação do Azure Stream Analytics será criada.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="ffdb6-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffdb6-126">-Name</span></span>
<span data-ttu-id="ffdb6-127">Especifica o nome da transformação do Azure Stream Analytics a ser criada.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="ffdb6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffdb6-128">-ResourceGroupName</span></span>
<span data-ttu-id="ffdb6-129">Especifica o nome do grupo de recursos sob o qual criar a transformação do Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="ffdb6-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffdb6-130">-Confirm</span></span>
<span data-ttu-id="ffdb6-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffdb6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffdb6-132">-WhatIf</span></span>
<span data-ttu-id="ffdb6-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffdb6-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffdb6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffdb6-135">CommonParameters</span></span>
<span data-ttu-id="ffdb6-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffdb6-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffdb6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffdb6-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffdb6-138">INPUTS</span></span>

### <span data-ttu-id="ffdb6-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ffdb6-139">None</span></span>
<span data-ttu-id="ffdb6-140">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ffdb6-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ffdb6-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffdb6-141">OUTPUTS</span></span>

### <span data-ttu-id="ffdb6-142">Microsoft. Azure. Commands. StreamAnalytics. Models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="ffdb6-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="ffdb6-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffdb6-143">NOTES</span></span>

## <span data-ttu-id="ffdb6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffdb6-144">RELATED LINKS</span></span>

[<span data-ttu-id="ffdb6-145">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="ffdb6-145">Get-AzureRmStreamAnalyticsTransformation</span></span>](./Get-AzureRmStreamAnalyticsTransformation.md)


