---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8EED9813-5106-4D6C-B869-97BCBD7845AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 67e354616161ad7f2d2467a37b92c355c7c8c39e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946311"
---
# <span data-ttu-id="2914f-101">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="2914f-101">Get-AzureSchedulerJob</span></span>

## <span data-ttu-id="2914f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2914f-102">SYNOPSIS</span></span>
<span data-ttu-id="2914f-103">Obtém uma lista de trabalhos do Agendador ou um trabalho do Agendador específico.</span><span class="sxs-lookup"><span data-stu-id="2914f-103">Gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="2914f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2914f-104">SYNTAX</span></span>

```
Get-AzureSchedulerJob -Location <String> -JobCollectionName <String> [-JobName <String>] [-JobState <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2914f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2914f-105">DESCRIPTION</span></span>
<span data-ttu-id="2914f-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2914f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2914f-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2914f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2914f-108">O cmdlet **Get-AzureSchedulerJobCollection** Obtém uma lista de trabalhos do Agendador ou um trabalho específico do Agendador.</span><span class="sxs-lookup"><span data-stu-id="2914f-108">The **Get-AzureSchedulerJobCollection** cmdlet gets a list of scheduler jobs or a particular scheduler job.</span></span>

## <span data-ttu-id="2914f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2914f-109">EXAMPLES</span></span>

### <span data-ttu-id="2914f-110">Exemplo 1: obter todos os trabalhos em uma coleção</span><span class="sxs-lookup"><span data-stu-id="2914f-110">Example 1: Get all jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="2914f-111">Esse comando obtém os trabalhos do Agendador que fazem parte do conjunto de trabalhos chamado JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="2914f-111">This command gets scheduler jobs that are part of the job collection named JobCollection01.</span></span>

### <span data-ttu-id="2914f-112">Exemplo 2: obter um trabalho nomeado</span><span class="sxs-lookup"><span data-stu-id="2914f-112">Example 2: Get a named job</span></span>
```
PS C:\> Get-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job01"
```

<span data-ttu-id="2914f-113">Esse comando obtém o trabalho chamado Job01 da coleção chamada JobCollection01 no local especificado.</span><span class="sxs-lookup"><span data-stu-id="2914f-113">This command gets the job named Job01 from the collection named JobCollection01 in the specified location.</span></span>

### <span data-ttu-id="2914f-114">Exemplo 3: obter trabalhos desabilitados em uma coleção</span><span class="sxs-lookup"><span data-stu-id="2914f-114">Example 3: Get disabled jobs in a collection</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -JobState "Disabled"
```

<span data-ttu-id="2914f-115">Esse comando obtém todos os trabalhos do Agendador desabilitados que fazem parte do JobCollection01 no local especificado.</span><span class="sxs-lookup"><span data-stu-id="2914f-115">This command gets all disabled scheduler jobs that are part of JobCollection01 in the specified location.</span></span>

## <span data-ttu-id="2914f-116">OS</span><span class="sxs-lookup"><span data-stu-id="2914f-116">PARAMETERS</span></span>

### <span data-ttu-id="2914f-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2914f-117">-JobCollectionName</span></span>
<span data-ttu-id="2914f-118">Especifica o nome da coleção que contém o trabalho do Agendador a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="2914f-118">Specifies the name of the collection that contains the scheduler job to get.</span></span>

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

### <span data-ttu-id="2914f-119">-JobName</span><span class="sxs-lookup"><span data-stu-id="2914f-119">-JobName</span></span>
<span data-ttu-id="2914f-120">Especifica o nome do trabalho do Agendador a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="2914f-120">Specifies the name of a scheduler job to get.</span></span>

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

### <span data-ttu-id="2914f-121">-JobState</span><span class="sxs-lookup"><span data-stu-id="2914f-121">-JobState</span></span>
<span data-ttu-id="2914f-122">Especifica o estado dos trabalhos do Agendador a serem obtidos.</span><span class="sxs-lookup"><span data-stu-id="2914f-122">Specifies the state of scheduler jobs to get.</span></span>
<span data-ttu-id="2914f-123">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2914f-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2914f-124">Possibilita</span><span class="sxs-lookup"><span data-stu-id="2914f-124">Enabled</span></span>
- <span data-ttu-id="2914f-125">Ativo</span><span class="sxs-lookup"><span data-stu-id="2914f-125">Disabled</span></span>
- <span data-ttu-id="2914f-126">Com defeito</span><span class="sxs-lookup"><span data-stu-id="2914f-126">Faulted</span></span>
- <span data-ttu-id="2914f-127">Feito</span><span class="sxs-lookup"><span data-stu-id="2914f-127">Completed</span></span>

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

### <span data-ttu-id="2914f-128">-Local</span><span class="sxs-lookup"><span data-stu-id="2914f-128">-Location</span></span>
<span data-ttu-id="2914f-129">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="2914f-129">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="2914f-130">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2914f-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2914f-131">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="2914f-131">Anywhere Asia</span></span>
- <span data-ttu-id="2914f-132">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="2914f-132">Anywhere Europe</span></span>
- <span data-ttu-id="2914f-133">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="2914f-133">Anywhere US</span></span>
- <span data-ttu-id="2914f-134">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="2914f-134">East Asia</span></span>
- <span data-ttu-id="2914f-135">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="2914f-135">East US</span></span>
- <span data-ttu-id="2914f-136">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="2914f-136">North Central US</span></span>
- <span data-ttu-id="2914f-137">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="2914f-137">North Europe</span></span>
- <span data-ttu-id="2914f-138">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="2914f-138">South Central US</span></span>
- <span data-ttu-id="2914f-139">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="2914f-139">Southeast Asia</span></span>
- <span data-ttu-id="2914f-140">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="2914f-140">West Europe</span></span>
- <span data-ttu-id="2914f-141">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="2914f-141">West US</span></span>

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

### <span data-ttu-id="2914f-142">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2914f-142">-Profile</span></span>
<span data-ttu-id="2914f-143">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2914f-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2914f-144">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2914f-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2914f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2914f-145">CommonParameters</span></span>
<span data-ttu-id="2914f-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2914f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2914f-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2914f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2914f-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2914f-148">INPUTS</span></span>

## <span data-ttu-id="2914f-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2914f-149">OUTPUTS</span></span>

## <span data-ttu-id="2914f-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2914f-150">NOTES</span></span>

## <span data-ttu-id="2914f-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2914f-151">RELATED LINKS</span></span>

[<span data-ttu-id="2914f-152">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="2914f-152">Remove-AzureSchedulerJob</span></span>](./Remove-AzureSchedulerJob.md)


