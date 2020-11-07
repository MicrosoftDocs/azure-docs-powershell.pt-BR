---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 89B28B7C-CA61-4CAB-A4DD-69363AB48A65
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a33739cfad37269fc2f91654e82d6ea36eb2336
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945612"
---
# <span data-ttu-id="9d200-101">Get-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9d200-101">Get-AzureSchedulerJobCollection</span></span>

## <span data-ttu-id="9d200-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d200-102">SYNOPSIS</span></span>
<span data-ttu-id="9d200-103">Obtém coletas de trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="9d200-103">Gets scheduler job collections.</span></span>

## <span data-ttu-id="9d200-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d200-104">SYNTAX</span></span>

```
Get-AzureSchedulerJobCollection [-Location <String>] [-JobCollectionName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d200-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d200-105">DESCRIPTION</span></span>
<span data-ttu-id="9d200-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9d200-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9d200-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9d200-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9d200-108">O cmdlet **Get-AzureSchedulerJobCollection** Obtém uma ou mais coleções de trabalho do Agendador.</span><span class="sxs-lookup"><span data-stu-id="9d200-108">The **Get-AzureSchedulerJobCollection** cmdlet gets one or more scheduler job collections.</span></span>

## <span data-ttu-id="9d200-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d200-109">EXAMPLES</span></span>

### <span data-ttu-id="9d200-110">Exemplo 1: obter todas as coleções</span><span class="sxs-lookup"><span data-stu-id="9d200-110">Example 1: Get all collections</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection
```

<span data-ttu-id="9d200-111">Este comando obtém todas as coleções de trabalhos do Agendador em todos os locais da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9d200-111">This command gets all scheduler job collections across all locations in the current subscription.</span></span>

### <span data-ttu-id="9d200-112">Exemplo 2: obter todas as coleções para um local</span><span class="sxs-lookup"><span data-stu-id="9d200-112">Example 2: Get all collections for a location</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US"
```

<span data-ttu-id="9d200-113">Esse comando obtém todas as coleções de trabalhos do Agendador no local chamado norte central dos EUA.</span><span class="sxs-lookup"><span data-stu-id="9d200-113">This command gets all scheduler job collections in the location named North Central US.</span></span>

### <span data-ttu-id="9d200-114">Exemplo 3: obter uma coleção usando um nome</span><span class="sxs-lookup"><span data-stu-id="9d200-114">Example 3: Get a collection by using a name</span></span>
```
PS C:\> Get-AzureSchedulerJobCollection -Location "North Central US" -JobCollectionName "JobCollection01"
```

<span data-ttu-id="9d200-115">Esse comando obtém o conjunto de trabalhos do Agendador chamado JobCollection01.</span><span class="sxs-lookup"><span data-stu-id="9d200-115">This command gets the scheduler job collection named JobCollection01.</span></span>

## <span data-ttu-id="9d200-116">OS</span><span class="sxs-lookup"><span data-stu-id="9d200-116">PARAMETERS</span></span>

### <span data-ttu-id="9d200-117">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="9d200-117">-JobCollectionName</span></span>
<span data-ttu-id="9d200-118">Especifica o nome da coleção de trabalhos do Agendador a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="9d200-118">Specifies the name of the scheduler job collection to get.</span></span>

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

### <span data-ttu-id="9d200-119">-Local</span><span class="sxs-lookup"><span data-stu-id="9d200-119">-Location</span></span>
<span data-ttu-id="9d200-120">Especifica o nome do local que hospeda o serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="9d200-120">Specifies the name of the location that hosts the cloud service.</span></span>
<span data-ttu-id="9d200-121">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="9d200-121">Valid values are:</span></span> 

- <span data-ttu-id="9d200-122">Qualquer lugar da Ásia</span><span class="sxs-lookup"><span data-stu-id="9d200-122">Anywhere Asia</span></span>
- <span data-ttu-id="9d200-123">Em qualquer lugar da Europa</span><span class="sxs-lookup"><span data-stu-id="9d200-123">Anywhere Europe</span></span>
- <span data-ttu-id="9d200-124">Em qualquer lugar nos EUA</span><span class="sxs-lookup"><span data-stu-id="9d200-124">Anywhere US</span></span>
- <span data-ttu-id="9d200-125">Leste da Ásia</span><span class="sxs-lookup"><span data-stu-id="9d200-125">East Asia</span></span>
- <span data-ttu-id="9d200-126">Leste dos EUA</span><span class="sxs-lookup"><span data-stu-id="9d200-126">East US</span></span>
- <span data-ttu-id="9d200-127">Centro Norte dos EUA</span><span class="sxs-lookup"><span data-stu-id="9d200-127">North Central US</span></span>
- <span data-ttu-id="9d200-128">Norte da Europa</span><span class="sxs-lookup"><span data-stu-id="9d200-128">North Europe</span></span>
- <span data-ttu-id="9d200-129">Centro-Sul dos EUA</span><span class="sxs-lookup"><span data-stu-id="9d200-129">South Central US</span></span>
- <span data-ttu-id="9d200-130">Sudeste Asiático</span><span class="sxs-lookup"><span data-stu-id="9d200-130">Southeast Asia</span></span>
- <span data-ttu-id="9d200-131">Oeste da Europa</span><span class="sxs-lookup"><span data-stu-id="9d200-131">West Europe</span></span>
- <span data-ttu-id="9d200-132">Oeste dos EUA</span><span class="sxs-lookup"><span data-stu-id="9d200-132">West US</span></span>

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

### <span data-ttu-id="9d200-133">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9d200-133">-Profile</span></span>
<span data-ttu-id="9d200-134">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9d200-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d200-135">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9d200-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d200-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d200-136">CommonParameters</span></span>
<span data-ttu-id="9d200-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d200-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d200-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d200-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d200-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d200-139">INPUTS</span></span>

## <span data-ttu-id="9d200-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d200-140">OUTPUTS</span></span>

## <span data-ttu-id="9d200-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d200-141">NOTES</span></span>

## <span data-ttu-id="9d200-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d200-142">RELATED LINKS</span></span>

[<span data-ttu-id="9d200-143">New-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9d200-143">New-AzureSchedulerJobCollection</span></span>](./New-AzureSchedulerJobCollection.md)

[<span data-ttu-id="9d200-144">Remove-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9d200-144">Remove-AzureSchedulerJobCollection</span></span>](./Remove-AzureSchedulerJobCollection.md)

[<span data-ttu-id="9d200-145">Set-AzureSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="9d200-145">Set-AzureSchedulerJobCollection</span></span>](./Set-AzureSchedulerJobCollection.md)


