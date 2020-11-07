---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DBB3DD-B02D-4288-89CB-550EBECC2E79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4373e4eed8524db1dd5311778b3e297e766c74dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945443"
---
# <span data-ttu-id="46f7a-101">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="46f7a-101">Set-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="46f7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="46f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="46f7a-103">Atualiza um conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="46f7a-103">Updates a scheduler job collection.</span></span>

## <span data-ttu-id="46f7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="46f7a-104">SYNTAX</span></span>

```
Set-AzureSchedulerJobCollection -Location <String> -JobCollectionName <String> [-Plan <String>]
 [-MaxJobCount <Int32>] [-Frequency <String>] [-Interval <Int32>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="46f7a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="46f7a-105">DESCRIPTION</span></span>
<span data-ttu-id="46f7a-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="46f7a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="46f7a-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="46f7a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="46f7a-108">O cmdlet **set-AzureSchedulerJobCollection** atualiza um conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="46f7a-108">The **Set-AzureSchedulerJobCollection** cmdlet updates a scheduler job collection.</span></span>

## <span data-ttu-id="46f7a-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="46f7a-109">EXAMPLES</span></span>

### <span data-ttu-id="46f7a-110">Exemplo 1: alterar a contagem máxima de trabalhos para uma coleção</span><span class="sxs-lookup"><span data-stu-id="46f7a-110">Example 1: Change the maximum job count for a collection</span></span>
```
PS C:\> Set-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01" -MaxJobCount 30
```

<span data-ttu-id="46f7a-111">Esse comando altera a contagem máxima de trabalhos para 30 no conjunto de trabalhos do Agendador existente chamado JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="46f7a-111">This command changes the maximum job count to 30 on the existing scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="46f7a-112">OS</span><span class="sxs-lookup"><span data-stu-id="46f7a-112">PARAMETERS</span></span>

### <span data-ttu-id="46f7a-113">-Frequency</span><span class="sxs-lookup"><span data-stu-id="46f7a-113">-Frequency</span></span>
<span data-ttu-id="46f7a-114">Especifica a frequência máxima que pode ser especificada em qualquer trabalho deste conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="46f7a-114">Specifies the maximum frequency that can be specified on any job in this scheduler job collection.</span></span>
<span data-ttu-id="46f7a-115">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="46f7a-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46f7a-116">Minuto</span><span class="sxs-lookup"><span data-stu-id="46f7a-116">Minute</span></span>
- <span data-ttu-id="46f7a-117">Ampulheta</span><span class="sxs-lookup"><span data-stu-id="46f7a-117">Hour</span></span>
- <span data-ttu-id="46f7a-118">Contas</span><span class="sxs-lookup"><span data-stu-id="46f7a-118">Day</span></span>
- <span data-ttu-id="46f7a-119">Emana</span><span class="sxs-lookup"><span data-stu-id="46f7a-119">Week</span></span>
- <span data-ttu-id="46f7a-120">Mensais</span><span class="sxs-lookup"><span data-stu-id="46f7a-120">Month</span></span>
- <span data-ttu-id="46f7a-121">Year</span><span class="sxs-lookup"><span data-stu-id="46f7a-121">Year</span></span>

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

### <span data-ttu-id="46f7a-122">-Intervalo</span><span class="sxs-lookup"><span data-stu-id="46f7a-122">-Interval</span></span>
<span data-ttu-id="46f7a-123">Especifica o intervalo de recorrência na frequência especificada usando-se o parâmetro *Frequency* .</span><span class="sxs-lookup"><span data-stu-id="46f7a-123">Specifies the interval of recurrence at the frequency specified by using the *Frequency* parameter.</span></span>

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

### <span data-ttu-id="46f7a-124">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="46f7a-124">-JobCollectionName</span></span>
<span data-ttu-id="46f7a-125">Especifica o nome do conjunto de trabalhos do Agendador a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="46f7a-125">Specifies the name of scheduler job collection to update.</span></span>

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

### <span data-ttu-id="46f7a-126">-Local</span><span class="sxs-lookup"><span data-stu-id="46f7a-126">-Location</span></span>
<span data-ttu-id="46f7a-127">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="46f7a-127">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="46f7a-128">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="46f7a-128">Valid values are:</span></span> 

- <span data-ttu-id="46f7a-129">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="46f7a-129">Anywhere Asia</span></span>
- <span data-ttu-id="46f7a-130">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="46f7a-130">Anywhere Europe</span></span>
- <span data-ttu-id="46f7a-131">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="46f7a-131">Anywhere US</span></span>
- <span data-ttu-id="46f7a-132">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="46f7a-132">East Asia</span></span>
- <span data-ttu-id="46f7a-133">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="46f7a-133">East US</span></span>
- <span data-ttu-id="46f7a-134">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="46f7a-134">North Central US</span></span>
- <span data-ttu-id="46f7a-135">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="46f7a-135">North Europe</span></span>
- <span data-ttu-id="46f7a-136">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="46f7a-136">South Central US</span></span>
- <span data-ttu-id="46f7a-137">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="46f7a-137">Southeast Asia</span></span>
- <span data-ttu-id="46f7a-138">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="46f7a-138">West Europe</span></span>
- <span data-ttu-id="46f7a-139">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="46f7a-139">West US</span></span>

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

### <span data-ttu-id="46f7a-140">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="46f7a-140">-MaxJobCount</span></span>
<span data-ttu-id="46f7a-141">Especifica o número máximo de trabalhos que podem ser criados no conjunto de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="46f7a-141">Specifies the maximum number of jobs that can be created in the scheduler job collection.</span></span>

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

### <span data-ttu-id="46f7a-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46f7a-142">-PassThru</span></span>
<span data-ttu-id="46f7a-143">Indica que esse cmdlet retorna um objeto que representa o item no qual ele funciona.</span><span class="sxs-lookup"><span data-stu-id="46f7a-143">Indicates that this cmdlet returns an object representing the item on which it operates.</span></span>
<span data-ttu-id="46f7a-144">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="46f7a-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="46f7a-145">-Plano</span><span class="sxs-lookup"><span data-stu-id="46f7a-145">-Plan</span></span>
<span data-ttu-id="46f7a-146">Especifica o plano de coleta de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="46f7a-146">Specifies the scheduler job collection plan.</span></span>

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

### <span data-ttu-id="46f7a-147">-Perfil</span><span class="sxs-lookup"><span data-stu-id="46f7a-147">-Profile</span></span>
<span data-ttu-id="46f7a-148">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="46f7a-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46f7a-149">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="46f7a-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46f7a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f7a-150">CommonParameters</span></span>
<span data-ttu-id="46f7a-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46f7a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f7a-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46f7a-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f7a-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="46f7a-153">INPUTS</span></span>

## <span data-ttu-id="46f7a-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="46f7a-154">OUTPUTS</span></span>

## <span data-ttu-id="46f7a-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="46f7a-155">NOTES</span></span>

## <span data-ttu-id="46f7a-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="46f7a-156">RELATED LINKS</span></span>

[<span data-ttu-id="46f7a-157">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="46f7a-157">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="46f7a-158">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="46f7a-158">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="46f7a-159">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="46f7a-159">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)


