---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 545CAB1C-F08C-4472-A41A-1FE900D2EDA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc8ae51b2f239fd9ec7f09fe27e08ccdaa41c4bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945482"
---
# <span data-ttu-id="0e235-101">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0e235-101">Remove-AzureWebsiteJob</span></span>

## <span data-ttu-id="0e235-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e235-102">SYNOPSIS</span></span>
<span data-ttu-id="0e235-103">Remove um trabalho da Web existente para um site.</span><span class="sxs-lookup"><span data-stu-id="0e235-103">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="0e235-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0e235-104">SYNTAX</span></span>

```
Remove-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-Force] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0e235-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0e235-105">DESCRIPTION</span></span>
<span data-ttu-id="0e235-106">Remove um trabalho da Web existente para um site.</span><span class="sxs-lookup"><span data-stu-id="0e235-106">Removes an existing web job for a website.</span></span>

## <span data-ttu-id="0e235-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0e235-107">EXAMPLES</span></span>

### <span data-ttu-id="0e235-108">Exemplo 1: remover um trabalho da Web existente para um site</span><span class="sxs-lookup"><span data-stu-id="0e235-108">Example 1: Remove an existing web job for a website</span></span>
```
PS C:\> Remove-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="0e235-109">Remove um trabalho da Web chamado MyWebJob para mywebsite.</span><span class="sxs-lookup"><span data-stu-id="0e235-109">Removes a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="0e235-110">OS</span><span class="sxs-lookup"><span data-stu-id="0e235-110">PARAMETERS</span></span>

### <span data-ttu-id="0e235-111">-Force</span><span class="sxs-lookup"><span data-stu-id="0e235-111">-Force</span></span>
<span data-ttu-id="0e235-112">Indica que esse cmdlet Remove o trabalho da Web sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="0e235-112">Indicates that this cmdlet removes the web job without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="0e235-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="0e235-113">-JobName</span></span>
<span data-ttu-id="0e235-114">O nome do trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="0e235-114">The web job name.</span></span>

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

### <span data-ttu-id="0e235-115">-JobType</span><span class="sxs-lookup"><span data-stu-id="0e235-115">-JobType</span></span>
<span data-ttu-id="0e235-116">O tipo de trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="0e235-116">The web job type.</span></span>
<span data-ttu-id="0e235-117">Pode ser disparada ou contínua.</span><span class="sxs-lookup"><span data-stu-id="0e235-117">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="0e235-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e235-118">-Name</span></span>
<span data-ttu-id="0e235-119">O nome do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e235-119">The name of the Azure website.</span></span>

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

### <span data-ttu-id="0e235-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="0e235-120">-Profile</span></span>
<span data-ttu-id="0e235-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="0e235-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0e235-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="0e235-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0e235-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="0e235-123">-Slot</span></span>
<span data-ttu-id="0e235-124">O nome do slot do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="0e235-124">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="0e235-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e235-125">CommonParameters</span></span>
<span data-ttu-id="0e235-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e235-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e235-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e235-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e235-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0e235-128">INPUTS</span></span>

## <span data-ttu-id="0e235-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0e235-129">OUTPUTS</span></span>

## <span data-ttu-id="0e235-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0e235-130">NOTES</span></span>

## <span data-ttu-id="0e235-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e235-131">RELATED LINKS</span></span>

[<span data-ttu-id="0e235-132">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="0e235-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="0e235-133">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0e235-133">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="0e235-134">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0e235-134">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="0e235-135">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0e235-135">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)

[<span data-ttu-id="0e235-136">Parar-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="0e235-136">Stop-AzureWebsiteJob</span></span>](./Stop-AzureWebsiteJob.md)


