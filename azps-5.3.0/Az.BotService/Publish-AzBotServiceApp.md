---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434455"
---
# <span data-ttu-id="09da4-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="09da4-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="09da4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09da4-102">SYNOPSIS</span></span>
<span data-ttu-id="09da4-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="09da4-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="09da4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="09da4-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="09da4-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="09da4-105">DESCRIPTION</span></span>
<span data-ttu-id="09da4-106">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="09da4-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="09da4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="09da4-107">EXAMPLES</span></span>

### <span data-ttu-id="09da4-108">Exemplo 1: publicar seu BotService para o Azure</span><span class="sxs-lookup"><span data-stu-id="09da4-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="09da4-109">Publicar seu BotService no Azure por código</span><span class="sxs-lookup"><span data-stu-id="09da4-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="09da4-110">OS</span><span class="sxs-lookup"><span data-stu-id="09da4-110">PARAMETERS</span></span>

### <span data-ttu-id="09da4-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="09da4-111">-CodeDir</span></span>
<span data-ttu-id="09da4-112">Esse parâmetro define o caminho do ZIP</span><span class="sxs-lookup"><span data-stu-id="09da4-112">This parameter defines the Path of the ZIP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09da4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="09da4-113">-Name</span></span>
<span data-ttu-id="09da4-114">Esse parâmetro define o nome do bot.</span><span class="sxs-lookup"><span data-stu-id="09da4-114">This parameter defines the name of the bot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09da4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09da4-115">-ResourceGroupName</span></span>
<span data-ttu-id="09da4-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="09da4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09da4-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="09da4-117">-Confirm</span></span>
<span data-ttu-id="09da4-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09da4-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09da4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09da4-119">-WhatIf</span></span>
<span data-ttu-id="09da4-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="09da4-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09da4-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="09da4-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09da4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09da4-122">CommonParameters</span></span>
<span data-ttu-id="09da4-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09da4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09da4-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09da4-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09da4-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="09da4-125">INPUTS</span></span>

## <span data-ttu-id="09da4-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="09da4-126">OUTPUTS</span></span>

## <span data-ttu-id="09da4-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="09da4-127">NOTES</span></span>

<span data-ttu-id="09da4-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="09da4-128">ALIASES</span></span>

## <span data-ttu-id="09da4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09da4-129">RELATED LINKS</span></span>

