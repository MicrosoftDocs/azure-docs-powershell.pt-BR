---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22DEC693-32BA-4048-8912-D1626DD511E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c95fb7f79cdb160bf2dd2014cad49d1bc96eb3b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946129"
---
# <span data-ttu-id="2b21f-101">Remove-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="2b21f-101">Remove-AzureSchedulerJob</span></span>

## <span data-ttu-id="2b21f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b21f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b21f-103">Exclui um trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="2b21f-103">Deletes a scheduler job.</span></span>

## <span data-ttu-id="2b21f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b21f-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJob [-Force] [-Location <String>] -JobCollectionName <String> -JobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2b21f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b21f-105">DESCRIPTION</span></span>
<span data-ttu-id="2b21f-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2b21f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2b21f-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="2b21f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="2b21f-108">O cmdlet **Remove-AzureSchedulerJob** exclui um trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="2b21f-108">The **Remove-AzureSchedulerJob** cmdlet deletes a scheduler job.</span></span>

## <span data-ttu-id="2b21f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b21f-109">EXAMPLES</span></span>

### <span data-ttu-id="2b21f-110">Exemplo 1: excluir um trabalho do Agendador</span><span class="sxs-lookup"><span data-stu-id="2b21f-110">Example 1: Delete a scheduler job</span></span>
```
PS C:\> Remove-AzureSchedulerJob -Location "North Central US" -JobCollectionName "JobCollection01" -JobName "Job17"
```

<span data-ttu-id="2b21f-111">Esse comando exclui o trabalho chamado Job17.</span><span class="sxs-lookup"><span data-stu-id="2b21f-111">This command deletes the job named Job17.</span></span>
<span data-ttu-id="2b21f-112">Esse trabalho faz parte do conjunto de trabalhos chamado JobCollection01 e é do local especificado.</span><span class="sxs-lookup"><span data-stu-id="2b21f-112">That job is part of the job collection named JobCollection01 and is in of the specified location.</span></span>

## <span data-ttu-id="2b21f-113">OS</span><span class="sxs-lookup"><span data-stu-id="2b21f-113">PARAMETERS</span></span>

### <span data-ttu-id="2b21f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="2b21f-114">-Force</span></span>
<span data-ttu-id="2b21f-115">Indica que esse cmdlet Remove o trabalho do Agendador sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="2b21f-115">Indicates that this cmdlet removes the scheduler job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2b21f-116">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2b21f-116">-JobCollectionName</span></span>
<span data-ttu-id="2b21f-117">Especifica o nome da coleção que contém o trabalho do Agendador a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2b21f-117">Specifies the name of the collection that contains the scheduler job to delete.</span></span>

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

### <span data-ttu-id="2b21f-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="2b21f-118">-JobName</span></span>
<span data-ttu-id="2b21f-119">Especifica o nome de um trabalho do Agendador a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="2b21f-119">Specifies the name of a scheduler job to delete.</span></span>

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

### <span data-ttu-id="2b21f-120">-Local</span><span class="sxs-lookup"><span data-stu-id="2b21f-120">-Location</span></span>
<span data-ttu-id="2b21f-121">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="2b21f-121">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="2b21f-122">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="2b21f-122">Valid values are:</span></span> 

- <span data-ttu-id="2b21f-123">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="2b21f-123">Anywhere Asia</span></span>
- <span data-ttu-id="2b21f-124">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="2b21f-124">Anywhere Europe</span></span>
- <span data-ttu-id="2b21f-125">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="2b21f-125">Anywhere US</span></span>
- <span data-ttu-id="2b21f-126">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="2b21f-126">East Asia</span></span>
- <span data-ttu-id="2b21f-127">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="2b21f-127">East US</span></span>
- <span data-ttu-id="2b21f-128">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="2b21f-128">North Central US</span></span>
- <span data-ttu-id="2b21f-129">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="2b21f-129">North Europe</span></span>
- <span data-ttu-id="2b21f-130">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="2b21f-130">South Central US</span></span>
- <span data-ttu-id="2b21f-131">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="2b21f-131">Southeast Asia</span></span>
- <span data-ttu-id="2b21f-132">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="2b21f-132">West Europe</span></span>
- <span data-ttu-id="2b21f-133">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="2b21f-133">West US</span></span>

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

### <span data-ttu-id="2b21f-134">-Perfil</span><span class="sxs-lookup"><span data-stu-id="2b21f-134">-Profile</span></span>
<span data-ttu-id="2b21f-135">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="2b21f-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b21f-136">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="2b21f-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b21f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b21f-137">CommonParameters</span></span>
<span data-ttu-id="2b21f-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b21f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b21f-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b21f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b21f-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b21f-140">INPUTS</span></span>

## <span data-ttu-id="2b21f-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b21f-141">OUTPUTS</span></span>

## <span data-ttu-id="2b21f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b21f-142">NOTES</span></span>

## <span data-ttu-id="2b21f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b21f-143">RELATED LINKS</span></span>

[<span data-ttu-id="2b21f-144">Get-AzureSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="2b21f-144">Get-AzureSchedulerJob</span></span>](./Get-AzureSchedulerJob.md)


