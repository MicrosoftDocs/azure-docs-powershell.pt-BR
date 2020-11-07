---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: DF12406D-894C-4732-95EE-D75524023B82
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2e6596c0de702175927f51bfd70fc5271b13bfd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945980"
---
# <span data-ttu-id="8ba27-101">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8ba27-101">New-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="8ba27-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ba27-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba27-103">Cria um conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="8ba27-103">Creates a scheduler job collection.</span></span>

## <span data-ttu-id="8ba27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ba27-104">SYNTAX</span></span>

```
New-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ba27-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ba27-105">DESCRIPTION</span></span>
<span data-ttu-id="8ba27-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ba27-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8ba27-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8ba27-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8ba27-108">O cmdlet **New-AzureSchedulerJobCollection** cria um conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="8ba27-108">The **New-AzureSchedulerJobCollection** cmdlet creates a scheduler job collection.</span></span>
<span data-ttu-id="8ba27-109">Se você não especificar um valor para o parâmetro do *plano* , o cmdlet criará uma coleta de trabalho padrão.</span><span class="sxs-lookup"><span data-stu-id="8ba27-109">If you do not specify a value for the *Plan* parameter, the cmdlet creates a standard job collection.</span></span>

## <span data-ttu-id="8ba27-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ba27-110">EXAMPLES</span></span>

### <span data-ttu-id="8ba27-111">Exemplo 1: criar um conjunto de trabalhos do Agendador que inclua valores padrão</span><span class="sxs-lookup"><span data-stu-id="8ba27-111">Example 1: Create a scheduler job collection that includes default values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection01" -Location "North Central US" -Plan "Standard"
```

<span data-ttu-id="8ba27-112">Esse comando cria um conjunto de trabalhos padrão do Agendador chamado JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="8ba27-112">This command creates a standard scheduler job collection named JobCollection01.</span></span>
<span data-ttu-id="8ba27-113">A nova coleção tem uma contagem de trabalho padrão e valores de recorrência máximos para um conjunto de trabalhos do agendador padrão.</span><span class="sxs-lookup"><span data-stu-id="8ba27-113">The new collection has a default job count and maximum recurrence values for a standard scheduler job collection.</span></span>

### <span data-ttu-id="8ba27-114">Exemplo 2: criar um conjunto de trabalhos do Agendador com valores especificados</span><span class="sxs-lookup"><span data-stu-id="8ba27-114">Example 2: Create a scheduler job collection with specified values</span></span>
```
PS C:\> New-AzureSchedulerJobCollection -JobCollectionName "JobCollection02" -Location "North Central US" -Frequency "Hour" -Interval 12 -MaxJobCount 30 -Plan "Standard"
```

<span data-ttu-id="8ba27-115">Esse comando cria um conjunto de trabalhos padrão do Agendador chamado JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="8ba27-115">This command creates a standard scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="8ba27-116">A nova coleção tem uma contagem de trabalho máxima de 30 e uma recorrência máxima de 12 por hora.</span><span class="sxs-lookup"><span data-stu-id="8ba27-116">The new collection has a maximum job count of 30 and a maximum recurrence of 12 per hour.</span></span>

## <span data-ttu-id="8ba27-117">OS</span><span class="sxs-lookup"><span data-stu-id="8ba27-117">PARAMETERS</span></span>

### <span data-ttu-id="8ba27-118">-Frequency</span><span class="sxs-lookup"><span data-stu-id="8ba27-118">-Frequency</span></span>
<span data-ttu-id="8ba27-119">Especifica a frequência máxima que pode ser especificada em qualquer trabalho deste conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="8ba27-119">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba27-120">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="8ba27-120">-Interval</span></span>
<span data-ttu-id="8ba27-121">Especifica o intervalo de recorrência na frequência especificada usando-se o parâmetro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="8ba27-121">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba27-122">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="8ba27-122">-JobCollectionName</span></span>
<span data-ttu-id="8ba27-123">Especifica o nome do novo conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="8ba27-123">Specifies the name for the new scheduler job collection.</span></span>

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

### <span data-ttu-id="8ba27-124">-Local</span><span class="sxs-lookup"><span data-stu-id="8ba27-124">-Location</span></span>
<span data-ttu-id="8ba27-125">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="8ba27-125">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="8ba27-126">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="8ba27-126">Valid values are:</span></span> 

- <span data-ttu-id="8ba27-127">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="8ba27-127">Anywhere Asia</span></span>
- <span data-ttu-id="8ba27-128">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="8ba27-128">Anywhere Europe</span></span>
- <span data-ttu-id="8ba27-129">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="8ba27-129">Anywhere US</span></span>
- <span data-ttu-id="8ba27-130">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="8ba27-130">East Asia</span></span>
- <span data-ttu-id="8ba27-131">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="8ba27-131">East US</span></span>
- <span data-ttu-id="8ba27-132">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="8ba27-132">North Central US</span></span>
- <span data-ttu-id="8ba27-133">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="8ba27-133">North Europe</span></span>
- <span data-ttu-id="8ba27-134">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="8ba27-134">South Central US</span></span>
- <span data-ttu-id="8ba27-135">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="8ba27-135">Southeast Asia</span></span>
- <span data-ttu-id="8ba27-136">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="8ba27-136">West Europe</span></span>
- <span data-ttu-id="8ba27-137">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="8ba27-137">West US</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba27-138">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="8ba27-138">-MaxJobCount</span></span>
<span data-ttu-id="8ba27-139">Especifica o número máximo de trabalhos que podem ser criados no conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="8ba27-139">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba27-140">-Plano</span><span class="sxs-lookup"><span data-stu-id="8ba27-140">-Plan</span></span>
<span data-ttu-id="8ba27-141">Especifica o plano de coleta de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="8ba27-141">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="8ba27-142">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8ba27-142">-Profile</span></span>
<span data-ttu-id="8ba27-143">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8ba27-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ba27-144">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8ba27-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ba27-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba27-145">CommonParameters</span></span>
<span data-ttu-id="8ba27-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba27-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba27-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba27-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba27-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ba27-148">INPUTS</span></span>

## <span data-ttu-id="8ba27-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ba27-149">OUTPUTS</span></span>

## <span data-ttu-id="8ba27-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ba27-150">NOTES</span></span>

## <span data-ttu-id="8ba27-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ba27-151">RELATED LINKS</span></span>

[<span data-ttu-id="8ba27-152">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8ba27-152">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="8ba27-153">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8ba27-153">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="8ba27-154">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="8ba27-154">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


