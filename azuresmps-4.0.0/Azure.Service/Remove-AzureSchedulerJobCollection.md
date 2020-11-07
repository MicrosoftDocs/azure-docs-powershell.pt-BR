---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D4349562-1392-44B6-9353-6231F0CB5C51
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66618c0a684a8e54d41bbe4014ee1e6c893acdbf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946128"
---
# <span data-ttu-id="f7137-101">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f7137-101">Remove-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="f7137-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7137-102">SYNOPSIS</span></span>
<span data-ttu-id="f7137-103">Exclui uma coleção de trabalhos do Agendador.</span><span class="sxs-lookup"><span data-stu-id="f7137-103">Deletes a scheduler job collection.</span></span>

## <span data-ttu-id="f7137-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7137-104">SYNTAX</span></span>

```
Remove-AzureSchedulerJobCollection [-Force] [-Location <String>] -JobCollectionName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f7137-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7137-105">DESCRIPTION</span></span>
<span data-ttu-id="f7137-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7137-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f7137-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f7137-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f7137-108">O cmdlet **Remove-AzureSchedulerJobCollection** exclui um conjunto de trabalhos do Agendador e qualquer trabalho dessa coleção.</span><span class="sxs-lookup"><span data-stu-id="f7137-108">The **Remove-AzureSchedulerJobCollection** cmdlet deletes a scheduler job collection and any jobs under that collection.</span></span>

## <span data-ttu-id="f7137-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7137-109">EXAMPLES</span></span>

### <span data-ttu-id="f7137-110">Exemplo 1: excluir uma coleção de trabalhos para um local</span><span class="sxs-lookup"><span data-stu-id="f7137-110">Example 1: Delete a job collection for a location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="f7137-111">Esse comando exclui o conjunto de trabalhos do Agendador chamado JobCollection01 na localização EUA Central do Norte.</span><span class="sxs-lookup"><span data-stu-id="f7137-111">This command deletes the scheduler job collection named JobCollection01 in the North Central US location.</span></span>
<span data-ttu-id="f7137-112">O comando também exclui os trabalhos em JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="f7137-112">The command also deletes the jobs under JobCollection01.</span></span>

### <span data-ttu-id="f7137-113">Exemplo 2: excluir um local de trabalho</span><span class="sxs-lookup"><span data-stu-id="f7137-113">Example 2: Delete a job location</span></span>
```
PS C:\> Remove-AzureSchedulerJobCollection -JobCollectionName "JobCollection02"
```

<span data-ttu-id="f7137-114">Esse comando exclui o conjunto de trabalhos do Agendador chamado JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="f7137-114">This command deletes the scheduler job collection named JobCollection02.</span></span>
<span data-ttu-id="f7137-115">O comando também exclui os trabalhos em JobCollection02.</span><span class="sxs-lookup"><span data-stu-id="f7137-115">The command also deletes the jobs under JobCollection02.</span></span>

## <span data-ttu-id="f7137-116">OS</span><span class="sxs-lookup"><span data-stu-id="f7137-116">PARAMETERS</span></span>

### <span data-ttu-id="f7137-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f7137-117">-Force</span></span>
<span data-ttu-id="f7137-118">Indica que esse cmdlet Remove a coleta de trabalho do Agendador sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="f7137-118">Indicates that this cmdlet removes the scheduler job collection without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f7137-119">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="f7137-119">-JobCollectionName</span></span>
<span data-ttu-id="f7137-120">Especifica o nome do conjunto de trabalhos do Agendador a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="f7137-120">Specifies the name of the scheduler job collection to delete.</span></span>

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

### <span data-ttu-id="f7137-121">-Local</span><span class="sxs-lookup"><span data-stu-id="f7137-121">-Location</span></span>
<span data-ttu-id="f7137-122">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="f7137-122">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="f7137-123">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="f7137-123">Valid values are:</span></span> 

- <span data-ttu-id="f7137-124">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="f7137-124">Anywhere Asia</span></span>
- <span data-ttu-id="f7137-125">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="f7137-125">Anywhere Europe</span></span>
- <span data-ttu-id="f7137-126">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="f7137-126">Anywhere US</span></span>
- <span data-ttu-id="f7137-127">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="f7137-127">East Asia</span></span>
- <span data-ttu-id="f7137-128">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="f7137-128">East US</span></span>
- <span data-ttu-id="f7137-129">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="f7137-129">North Central US</span></span>
- <span data-ttu-id="f7137-130">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="f7137-130">North Europe</span></span>
- <span data-ttu-id="f7137-131">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="f7137-131">South Central US</span></span>
- <span data-ttu-id="f7137-132">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="f7137-132">Southeast Asia</span></span>
- <span data-ttu-id="f7137-133">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="f7137-133">West Europe</span></span>
- <span data-ttu-id="f7137-134">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="f7137-134">West US</span></span>

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

### <span data-ttu-id="f7137-135">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f7137-135">-Profile</span></span>
<span data-ttu-id="f7137-136">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f7137-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f7137-137">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f7137-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f7137-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7137-138">CommonParameters</span></span>
<span data-ttu-id="f7137-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7137-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7137-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7137-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7137-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7137-141">INPUTS</span></span>

## <span data-ttu-id="f7137-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7137-142">OUTPUTS</span></span>

## <span data-ttu-id="f7137-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7137-143">NOTES</span></span>

## <span data-ttu-id="f7137-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7137-144">RELATED LINKS</span></span>

[<span data-ttu-id="f7137-145">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f7137-145">Get-AzureSchedulerJobCollection</span></span>](./Get-AzureSchedulerJobCollection.md)

[<span data-ttu-id="f7137-146">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f7137-146">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="f7137-147">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="f7137-147">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


