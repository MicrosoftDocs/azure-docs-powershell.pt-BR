---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945838"
---
# <span data-ttu-id="8598b-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="8598b-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="8598b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8598b-102">SYNOPSIS</span></span>
<span data-ttu-id="8598b-103">Interrompe um trabalho da Web para um site.</span><span class="sxs-lookup"><span data-stu-id="8598b-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="8598b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8598b-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8598b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8598b-105">DESCRIPTION</span></span>
<span data-ttu-id="8598b-106">O cmdlet **Stop-AzureWebsiteJob** interrompe um trabalho da Web para um site.</span><span class="sxs-lookup"><span data-stu-id="8598b-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="8598b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8598b-107">EXAMPLES</span></span>

### <span data-ttu-id="8598b-108">Exemplo 1: parar um trabalho da Web para um site</span><span class="sxs-lookup"><span data-stu-id="8598b-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="8598b-109">Interrompe um trabalho da Web chamado MyWebJob para mywebsite.</span><span class="sxs-lookup"><span data-stu-id="8598b-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="8598b-110">OS</span><span class="sxs-lookup"><span data-stu-id="8598b-110">PARAMETERS</span></span>

### <span data-ttu-id="8598b-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="8598b-111">-JobName</span></span>
<span data-ttu-id="8598b-112">O nome do trabalho da Web.</span><span class="sxs-lookup"><span data-stu-id="8598b-112">The web job name.</span></span>

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

### <span data-ttu-id="8598b-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="8598b-113">-Name</span></span>
<span data-ttu-id="8598b-114">O nome do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="8598b-114">The name of the Azure website.</span></span>

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

### <span data-ttu-id="8598b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8598b-115">-PassThru</span></span>
<span data-ttu-id="8598b-116">Retorna um valor booliano que indica que o trabalho parou com êxito.</span><span class="sxs-lookup"><span data-stu-id="8598b-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="8598b-117">Por padrão, esse cmdlet não retorna nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8598b-117">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="8598b-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8598b-118">-Profile</span></span>
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

### <span data-ttu-id="8598b-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="8598b-119">-Slot</span></span>
<span data-ttu-id="8598b-120">O nome do slot do site do Azure.</span><span class="sxs-lookup"><span data-stu-id="8598b-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="8598b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8598b-121">CommonParameters</span></span>
<span data-ttu-id="8598b-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8598b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8598b-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8598b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8598b-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8598b-124">INPUTS</span></span>

## <span data-ttu-id="8598b-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8598b-125">OUTPUTS</span></span>

## <span data-ttu-id="8598b-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8598b-126">NOTES</span></span>

## <span data-ttu-id="8598b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8598b-127">RELATED LINKS</span></span>

[<span data-ttu-id="8598b-128">Parar-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8598b-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="8598b-129">Get-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="8598b-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="8598b-130">New-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="8598b-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="8598b-131">Remove-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="8598b-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="8598b-132">Start-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="8598b-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


