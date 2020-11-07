---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946507"
---
# <span data-ttu-id="d9c40-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="d9c40-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="d9c40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d9c40-102">SYNOPSIS</span></span>
<span data-ttu-id="d9c40-103">Obtém um histórico de trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="d9c40-103">Gets a web job history.</span></span>

## <span data-ttu-id="d9c40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9c40-104">SYNTAX</span></span>

### <span data-ttu-id="d9c40-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d9c40-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="d9c40-106">RunIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d9c40-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d9c40-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="d9c40-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d9c40-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d9c40-108">DESCRIPTION</span></span>
<span data-ttu-id="d9c40-109">Obtém um histórico de trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="d9c40-109">Gets a web job history.</span></span>

## <span data-ttu-id="d9c40-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d9c40-110">EXAMPLES</span></span>

### <span data-ttu-id="d9c40-111">Exemplo 1: obter histórico completo para um trabalho da Web</span><span class="sxs-lookup"><span data-stu-id="d9c40-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="d9c40-112">Obtém histórico completo para MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="d9c40-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="d9c40-113">Exemplo 2: obter última execução para um trabalho da Web</span><span class="sxs-lookup"><span data-stu-id="d9c40-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="d9c40-114">Obtém as últimas informações de execução para MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="d9c40-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="d9c40-115">Exemplo 3: obter execução específica para um trabalho da Web</span><span class="sxs-lookup"><span data-stu-id="d9c40-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="d9c40-116">Obtém todas as informações sobre executar com a ID 10 para MyWebJob.</span><span class="sxs-lookup"><span data-stu-id="d9c40-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="d9c40-117">OS</span><span class="sxs-lookup"><span data-stu-id="d9c40-117">PARAMETERS</span></span>

### <span data-ttu-id="d9c40-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="d9c40-118">-JobName</span></span>
<span data-ttu-id="d9c40-119">O nome do trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="d9c40-119">The web job name.</span></span>

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

### <span data-ttu-id="d9c40-120">-Mais recente</span><span class="sxs-lookup"><span data-stu-id="d9c40-120">-Latest</span></span>
<span data-ttu-id="d9c40-121">Se especificado, retorne o histórico de execução mais recente.</span><span class="sxs-lookup"><span data-stu-id="d9c40-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9c40-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d9c40-122">-Name</span></span>
<span data-ttu-id="d9c40-123">O nome do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c40-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="d9c40-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d9c40-124">-Profile</span></span>
<span data-ttu-id="d9c40-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d9c40-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d9c40-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d9c40-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d9c40-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="d9c40-127">-RunId</span></span>
<span data-ttu-id="d9c40-128">Especifica a ID do histórico de execução que você deseja ver.</span><span class="sxs-lookup"><span data-stu-id="d9c40-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9c40-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="d9c40-129">-Slot</span></span>
<span data-ttu-id="d9c40-130">O nome do slot do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="d9c40-130">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="d9c40-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9c40-131">CommonParameters</span></span>
<span data-ttu-id="d9c40-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9c40-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9c40-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9c40-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9c40-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d9c40-134">INPUTS</span></span>

## <span data-ttu-id="d9c40-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d9c40-135">OUTPUTS</span></span>

## <span data-ttu-id="d9c40-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d9c40-136">NOTES</span></span>

## <span data-ttu-id="d9c40-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d9c40-137">RELATED LINKS</span></span>

[<span data-ttu-id="d9c40-138">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d9c40-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="d9c40-139">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d9c40-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="d9c40-140">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d9c40-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="d9c40-141">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d9c40-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="d9c40-142">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d9c40-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)


