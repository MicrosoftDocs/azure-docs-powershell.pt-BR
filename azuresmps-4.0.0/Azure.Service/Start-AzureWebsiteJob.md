---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A66ADA39-56D9-421B-BC69-996253352236
online version: ''
schema: 2.0.0
ms.openlocfilehash: b5b2cfaea544b5a8575715ec89735b5b9a1ad28f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945767"
---
# <span data-ttu-id="e4d37-101">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e4d37-101">Start-AzureWebsiteJob</span></span>

## <span data-ttu-id="e4d37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4d37-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d37-103">Inicia um trabalho da Web para um site.</span><span class="sxs-lookup"><span data-stu-id="e4d37-103">Starts a web job for a website.</span></span>

## <span data-ttu-id="e4d37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4d37-104">SYNTAX</span></span>

```
Start-AzureWebsiteJob -JobName <String> -JobType <WebJobType> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e4d37-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4d37-105">DESCRIPTION</span></span>
<span data-ttu-id="e4d37-106">O cmdlet **Start-AzureWebsiteJob** inicia um trabalho da Web para um site.</span><span class="sxs-lookup"><span data-stu-id="e4d37-106">The **Start-AzureWebsiteJob** cmdlet starts a web job for a website.</span></span>

## <span data-ttu-id="e4d37-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4d37-107">EXAMPLES</span></span>

### <span data-ttu-id="e4d37-108">Exemplo 1: iniciar um trabalho da Web para um site</span><span class="sxs-lookup"><span data-stu-id="e4d37-108">Example 1: Start a web job for a website</span></span>
```
PS C:\> Start-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob -JobType Continuous
```

<span data-ttu-id="e4d37-109">Inicia um trabalho da Web chamado MyWebJob para mywebsite.</span><span class="sxs-lookup"><span data-stu-id="e4d37-109">Starts a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="e4d37-110">OS</span><span class="sxs-lookup"><span data-stu-id="e4d37-110">PARAMETERS</span></span>

### <span data-ttu-id="e4d37-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="e4d37-111">-JobName</span></span>
<span data-ttu-id="e4d37-112">O nome do trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="e4d37-112">The web job name.</span></span>

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

### <span data-ttu-id="e4d37-113">-JobType</span><span class="sxs-lookup"><span data-stu-id="e4d37-113">-JobType</span></span>
<span data-ttu-id="e4d37-114">O tipo de trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="e4d37-114">The web job type.</span></span>
<span data-ttu-id="e4d37-115">Pode ser disparada ou contínua.</span><span class="sxs-lookup"><span data-stu-id="e4d37-115">Can be triggered or continuous.</span></span>

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

### <span data-ttu-id="e4d37-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4d37-116">-Name</span></span>
<span data-ttu-id="e4d37-117">O nome do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d37-117">The name of the Azure website.</span></span>

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

### <span data-ttu-id="e4d37-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4d37-118">-PassThru</span></span>
<span data-ttu-id="e4d37-119">Retorna um valor booliano que indica que o trabalho foi iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="e4d37-119">Returns a boolean value indicating that the job started successfully.</span></span>
<span data-ttu-id="e4d37-120">Por padrão, esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e4d37-120">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="e4d37-121">-Perfil</span><span class="sxs-lookup"><span data-stu-id="e4d37-121">-Profile</span></span>
<span data-ttu-id="e4d37-122">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="e4d37-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e4d37-123">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="e4d37-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e4d37-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="e4d37-124">-Slot</span></span>
<span data-ttu-id="e4d37-125">O nome do slot do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d37-125">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="e4d37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d37-126">CommonParameters</span></span>
<span data-ttu-id="e4d37-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d37-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4d37-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d37-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4d37-129">INPUTS</span></span>

## <span data-ttu-id="e4d37-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4d37-130">OUTPUTS</span></span>

## <span data-ttu-id="e4d37-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4d37-131">NOTES</span></span>

## <span data-ttu-id="e4d37-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4d37-132">RELATED LINKS</span></span>

[<span data-ttu-id="e4d37-133">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="e4d37-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="e4d37-134">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e4d37-134">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="e4d37-135">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e4d37-135">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="e4d37-136">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e4d37-136">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="e4d37-137">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="e4d37-137">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


