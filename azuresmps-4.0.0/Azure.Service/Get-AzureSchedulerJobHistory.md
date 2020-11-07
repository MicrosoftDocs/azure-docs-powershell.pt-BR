---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2BF5BDF8-3743-46FC-8E04-1A4EA920A2AF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 77b4d184ffbdb1d054f3d14aa3c51c8d2afc928b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946310"
---
# <span data-ttu-id="77b74-101">Get-AzureSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="77b74-101">Get-AzureSchedulerJobHistory</span></span>

## <span data-ttu-id="77b74-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="77b74-102">SYNOPSIS</span></span>
<span data-ttu-id="77b74-103">Obtém o histórico de um trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="77b74-103">Gets history for a scheduler job.</span></span>

## <span data-ttu-id="77b74-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="77b74-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobHistory -Location <String> -JobCollectionName <String> -JobName <String>
 [-JobStatus <String>] [-Profile <AzureSMProfile>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="77b74-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="77b74-105">DESCRIPTION</span></span>
<span data-ttu-id="77b74-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="77b74-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="77b74-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="77b74-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="77b74-108">O cmdlet **Get-AzureSchedulerJobHistory** Obtém o histórico de um trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="77b74-108">The **Get-AzureSchedulerJobHistory** cmdlet gets the history for a scheduler job.</span></span>

## <span data-ttu-id="77b74-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77b74-109">EXAMPLES</span></span>

### <span data-ttu-id="77b74-110">Exemplo 1: obter histórico de um trabalho usando seu nome</span><span class="sxs-lookup"><span data-stu-id="77b74-110">Example 1: Get history for a job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="77b74-111">Esse comando obtém o histórico do trabalho chamado Job01.</span><span class="sxs-lookup"><span data-stu-id="77b74-111">This command gets the history of the job named Job01.</span></span>
<span data-ttu-id="77b74-112">Esse trabalho pertence à coleção de trabalhos chamada JobCollection01 no local especificado.</span><span class="sxs-lookup"><span data-stu-id="77b74-112">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="77b74-113">Exemplo 2: obter histórico de um trabalho com falha usando seu nome</span><span class="sxs-lookup"><span data-stu-id="77b74-113">Example 2: Get history for a failed job by using its name</span></span>
```
PS C:\> Get-AzureSchedulerJobHistory -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job12" -JobStatus "Failed"
```

<span data-ttu-id="77b74-114">Esse comando obtém o histórico do trabalho chamado Job12 que tem um status de falha.</span><span class="sxs-lookup"><span data-stu-id="77b74-114">This command gets the history of the job named Job12 that has a status of Failed.</span></span>
<span data-ttu-id="77b74-115">Esse trabalho pertence à coleção de trabalhos chamada JobCollection01 no local especificado.</span><span class="sxs-lookup"><span data-stu-id="77b74-115">That job belongs to the job collection named JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="77b74-116">OS</span><span class="sxs-lookup"><span data-stu-id="77b74-116">PARAMETERS</span></span>

### <span data-ttu-id="77b74-117">-Primeiro</span><span class="sxs-lookup"><span data-stu-id="77b74-117">-First</span></span>
<span data-ttu-id="77b74-118">Obtém apenas o número especificado de objetos.</span><span class="sxs-lookup"><span data-stu-id="77b74-118">Gets only the specified number of objects.</span></span>
<span data-ttu-id="77b74-119">Digite o número de objetos a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="77b74-119">Enter the number of objects to get.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b74-120">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="77b74-120">-IncludeTotalCount</span></span>
<span data-ttu-id="77b74-121">Relata o número total de objetos no conjunto de dados (um número inteiro) seguido pelos objetos selecionados.</span><span class="sxs-lookup"><span data-stu-id="77b74-121">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="77b74-122">Se o cmdlet não puder determinar a contagem total, ele exibirá "contagem total desconhecida".</span><span class="sxs-lookup"><span data-stu-id="77b74-122">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="77b74-123">O inteiro tem uma propriedade exactidão que indica a confiabilidade do valor total de contagem.</span><span class="sxs-lookup"><span data-stu-id="77b74-123">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="77b74-124">O valor de precisão varia de 0,0 a 1,0, onde 0,0 significa que o cmdlet não pôde contar os objetos, 1,0 significa que a contagem é exata e um valor entre 0,0 e 1,0 indica uma estimativa mais confiável.</span><span class="sxs-lookup"><span data-stu-id="77b74-124">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b74-125">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="77b74-125">-JobCollectionName</span></span>
<span data-ttu-id="77b74-126">Especifica o nome de um conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="77b74-126">Specifies the name of a scheduler job collection.</span></span>
<span data-ttu-id="77b74-127">Esse cmdlet obtém o histórico de um trabalho que pertence à coleção que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="77b74-127">This cmdlet gets the history for a job that belongs to the collection that this parameter specifies.</span></span>

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

### <span data-ttu-id="77b74-128">-JobName</span><span class="sxs-lookup"><span data-stu-id="77b74-128">-JobName</span></span>
<span data-ttu-id="77b74-129">Especifica o nome de um trabalho do Agendador para o qual obter o histórico.</span><span class="sxs-lookup"><span data-stu-id="77b74-129">Specifies the name of a scheduler job for which to get the history.</span></span>

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

### <span data-ttu-id="77b74-130">-JobStatus</span><span class="sxs-lookup"><span data-stu-id="77b74-130">-JobStatus</span></span>
<span data-ttu-id="77b74-131">Especifica o status do trabalho do Agendador para o qual obter o histórico.</span><span class="sxs-lookup"><span data-stu-id="77b74-131">Specifies the status of scheduler job for which to get the history.</span></span>
<span data-ttu-id="77b74-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="77b74-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="77b74-133">Feito</span><span class="sxs-lookup"><span data-stu-id="77b74-133">Completed</span></span>
- <span data-ttu-id="77b74-134">Conseguiu</span><span class="sxs-lookup"><span data-stu-id="77b74-134">Failed</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77b74-135">-Local</span><span class="sxs-lookup"><span data-stu-id="77b74-135">-Location</span></span>
<span data-ttu-id="77b74-136">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="77b74-136">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="77b74-137">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="77b74-137">Valid values are:</span></span> 

- <span data-ttu-id="77b74-138">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="77b74-138">Anywhere Asia</span></span>
- <span data-ttu-id="77b74-139">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="77b74-139">Anywhere Europe</span></span>
- <span data-ttu-id="77b74-140">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="77b74-140">Anywhere US</span></span>
- <span data-ttu-id="77b74-141">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="77b74-141">East Asia</span></span>
- <span data-ttu-id="77b74-142">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="77b74-142">East US</span></span>
- <span data-ttu-id="77b74-143">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="77b74-143">North Central US</span></span>
- <span data-ttu-id="77b74-144">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="77b74-144">North Europe</span></span>
- <span data-ttu-id="77b74-145">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="77b74-145">South Central US</span></span>
- <span data-ttu-id="77b74-146">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="77b74-146">Southeast Asia</span></span>
- <span data-ttu-id="77b74-147">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="77b74-147">West Europe</span></span>
- <span data-ttu-id="77b74-148">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="77b74-148">West US</span></span>

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

### <span data-ttu-id="77b74-149">-Perfil</span><span class="sxs-lookup"><span data-stu-id="77b74-149">-Profile</span></span>
<span data-ttu-id="77b74-150">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="77b74-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="77b74-151">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="77b74-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b74-152">-Skip</span><span class="sxs-lookup"><span data-stu-id="77b74-152">-Skip</span></span>
<span data-ttu-id="77b74-153">Ignora o número especificado de objetos e obtém os objetos restantes.</span><span class="sxs-lookup"><span data-stu-id="77b74-153">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="77b74-154">Digite o número de objetos a serem ignorados.</span><span class="sxs-lookup"><span data-stu-id="77b74-154">Enter the number of objects to skip.</span></span>

```yaml
Type: UInt64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77b74-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77b74-155">CommonParameters</span></span>
<span data-ttu-id="77b74-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77b74-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77b74-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77b74-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77b74-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="77b74-158">INPUTS</span></span>

## <span data-ttu-id="77b74-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="77b74-159">OUTPUTS</span></span>

## <span data-ttu-id="77b74-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="77b74-160">NOTES</span></span>

## <span data-ttu-id="77b74-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77b74-161">RELATED LINKS</span></span>

[<span data-ttu-id="77b74-162">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="77b74-162">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)

[<span data-ttu-id="77b74-163">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="77b74-163">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)


