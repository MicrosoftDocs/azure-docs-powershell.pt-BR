---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6B406310-287F-4BD3-BA38-A9C97E8EDC45
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9f68ca1667e7b028c7646bf5a569e4e467c1b03
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946273"
---
# <span data-ttu-id="9cec3-101">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="9cec3-101">Get-AzureWebsiteJob</span></span>

## <span data-ttu-id="9cec3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9cec3-102">SYNOPSIS</span></span>
<span data-ttu-id="9cec3-103">Obtém os trabalhos da Web associados a um site.</span><span class="sxs-lookup"><span data-stu-id="9cec3-103">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="9cec3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9cec3-104">SYNTAX</span></span>

```
Get-AzureWebsiteJob [-JobName <String>] [-JobType <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9cec3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9cec3-105">DESCRIPTION</span></span>
<span data-ttu-id="9cec3-106">Obtém os trabalhos da Web associados a um site.</span><span class="sxs-lookup"><span data-stu-id="9cec3-106">Gets the web jobs associated with a website.</span></span>

## <span data-ttu-id="9cec3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9cec3-107">EXAMPLES</span></span>

### <span data-ttu-id="9cec3-108">Exemplo 1: obter informações específicas do trabalho Web</span><span class="sxs-lookup"><span data-stu-id="9cec3-108">Example 1: Get specific web job info</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="9cec3-109">Obtém um trabalho da Web chamado MyWebJob do slot de produção mywebsite.</span><span class="sxs-lookup"><span data-stu-id="9cec3-109">Gets a web job called MyWebJob from MyWebsite production slot.</span></span>

### <span data-ttu-id="9cec3-110">Exemplo 2: obter todos os trabalhos da Web para um site</span><span class="sxs-lookup"><span data-stu-id="9cec3-110">Example 2: Get all web jobs for a website</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite
```

<span data-ttu-id="9cec3-111">Obtém todos os trabalhos da Web associados ao slot de produção mywebsite.</span><span class="sxs-lookup"><span data-stu-id="9cec3-111">Gets all web jobs associated with MyWebsite production slot.</span></span>

### <span data-ttu-id="9cec3-112">Exemplo 3: obter todos os trabalhos Web disparados</span><span class="sxs-lookup"><span data-stu-id="9cec3-112">Example 3: Get all triggered web jobs</span></span>
```
PS C:\> Get-AzureWebsiteJob -Name MyWebsite -Slot staging -Type Triggered
```

<span data-ttu-id="9cec3-113">Obtém todos os trabalhos da Web disparados no slot de preparo do mywebsite.</span><span class="sxs-lookup"><span data-stu-id="9cec3-113">Gets all triggered web jobs from staging slot of MyWebsite.</span></span>

## <span data-ttu-id="9cec3-114">OS</span><span class="sxs-lookup"><span data-stu-id="9cec3-114">PARAMETERS</span></span>

### <span data-ttu-id="9cec3-115">-JobName</span><span class="sxs-lookup"><span data-stu-id="9cec3-115">-JobName</span></span>
<span data-ttu-id="9cec3-116">O nome do trabalho da Web</span><span class="sxs-lookup"><span data-stu-id="9cec3-116">The web job name</span></span>

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

### <span data-ttu-id="9cec3-117">-JobType</span><span class="sxs-lookup"><span data-stu-id="9cec3-117">-JobType</span></span>
<span data-ttu-id="9cec3-118">O tipo de trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="9cec3-118">The web job type.</span></span>
<span data-ttu-id="9cec3-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9cec3-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9cec3-120">Ativou</span><span class="sxs-lookup"><span data-stu-id="9cec3-120">Triggered</span></span>
- <span data-ttu-id="9cec3-121">Continuou</span><span class="sxs-lookup"><span data-stu-id="9cec3-121">Continuous</span></span>

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

### <span data-ttu-id="9cec3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9cec3-122">-Name</span></span>
<span data-ttu-id="9cec3-123">O nome do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="9cec3-123">The name of the Azure website.</span></span>

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

### <span data-ttu-id="9cec3-124">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9cec3-124">-Profile</span></span>
<span data-ttu-id="9cec3-125">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9cec3-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9cec3-126">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9cec3-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9cec3-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="9cec3-127">-Slot</span></span>
<span data-ttu-id="9cec3-128">O nome do slot do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="9cec3-128">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="9cec3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cec3-129">CommonParameters</span></span>
<span data-ttu-id="9cec3-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cec3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cec3-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cec3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cec3-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9cec3-132">INPUTS</span></span>

## <span data-ttu-id="9cec3-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9cec3-133">OUTPUTS</span></span>

## <span data-ttu-id="9cec3-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9cec3-134">NOTES</span></span>

## <span data-ttu-id="9cec3-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9cec3-135">RELATED LINKS</span></span>

[<span data-ttu-id="9cec3-136">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="9cec3-136">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="9cec3-137">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="9cec3-137">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="9cec3-138">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="9cec3-138">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="9cec3-139">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="9cec3-139">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="9cec3-140">Parar-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="9cec3-140">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


