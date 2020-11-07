---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1254A28B-F670-44B2-BB0E-BD41B9483E3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1910a0da546bdc4d5b167d82685608669b7565c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946183"
---
# <span data-ttu-id="d55d0-101">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d55d0-101">New-AzureWebsiteJob</span></span>

## <span data-ttu-id="d55d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d55d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d55d0-103">Cria um trabalho da Web para um site.</span><span class="sxs-lookup"><span data-stu-id="d55d0-103">Creates a web job for a website.</span></span>

## <span data-ttu-id="d55d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d55d0-104">SYNTAX</span></span>

```
New-AzureWebsiteJob -JobName <String> -JobType <WebJobType> -JobFile <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d55d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d55d0-105">DESCRIPTION</span></span>
<span data-ttu-id="d55d0-106">O cmdlet **New-AzureWebsiteJob** cria um trabalho da Web para um site.</span><span class="sxs-lookup"><span data-stu-id="d55d0-106">The **New-AzureWebsiteJob** cmdlet creates a web job for a website.</span></span>

## <span data-ttu-id="d55d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d55d0-107">EXAMPLES</span></span>

### <span data-ttu-id="d55d0-108">Exemplo 1: criar um novo trabalho Web para um site</span><span class="sxs-lookup"><span data-stu-id="d55d0-108">Example 1: Create new web job for a website</span></span>
```
PS C:\> New-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous -JobFile job.bat
```

<span data-ttu-id="d55d0-109">Cria um trabalho contínuo para chamar job.bat no site mywebsite.</span><span class="sxs-lookup"><span data-stu-id="d55d0-109">Creates a continuous job to call job.bat on website MyWebsite.</span></span>

## <span data-ttu-id="d55d0-110">OS</span><span class="sxs-lookup"><span data-stu-id="d55d0-110">PARAMETERS</span></span>

### <span data-ttu-id="d55d0-111">-JobFile</span><span class="sxs-lookup"><span data-stu-id="d55d0-111">-JobFile</span></span>
<span data-ttu-id="d55d0-112">O arquivo de trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="d55d0-112">The web job file.</span></span>

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

### <span data-ttu-id="d55d0-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="d55d0-113">-JobName</span></span>
<span data-ttu-id="d55d0-114">O nome do trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="d55d0-114">The web job name.</span></span>

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

### <span data-ttu-id="d55d0-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="d55d0-115">-JobType</span></span>
<span data-ttu-id="d55d0-116">O tipo de trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="d55d0-116">The web job type.</span></span>
<span data-ttu-id="d55d0-117">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d55d0-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d55d0-118">Ativou</span><span class="sxs-lookup"><span data-stu-id="d55d0-118">Triggered</span></span> 
- <span data-ttu-id="d55d0-119">Continuou</span><span class="sxs-lookup"><span data-stu-id="d55d0-119">Continuous</span></span>

```yaml
Type: WebJobType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d55d0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d55d0-120">-Name</span></span>
<span data-ttu-id="d55d0-121">O nome do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="d55d0-121">The name of the Azure website.</span></span>

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

### <span data-ttu-id="d55d0-122">-Perfil</span><span class="sxs-lookup"><span data-stu-id="d55d0-122">-Profile</span></span>
<span data-ttu-id="d55d0-123">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="d55d0-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d55d0-124">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="d55d0-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d55d0-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="d55d0-125">-Slot</span></span>
<span data-ttu-id="d55d0-126">O nome do slot do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="d55d0-126">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="d55d0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55d0-127">CommonParameters</span></span>
<span data-ttu-id="d55d0-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55d0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55d0-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d55d0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55d0-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d55d0-130">INPUTS</span></span>

## <span data-ttu-id="d55d0-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d55d0-131">OUTPUTS</span></span>

## <span data-ttu-id="d55d0-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d55d0-132">NOTES</span></span>

## <span data-ttu-id="d55d0-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d55d0-133">RELATED LINKS</span></span>

[<span data-ttu-id="d55d0-134">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="d55d0-134">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="d55d0-135">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d55d0-135">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="d55d0-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d55d0-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="d55d0-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d55d0-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="d55d0-138">Parar-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="d55d0-138">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


