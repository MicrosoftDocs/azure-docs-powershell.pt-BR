---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 551428a1c5d1737d32aeddf2dd5653586d1dbfbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887021"
---
# <span data-ttu-id="57666-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="57666-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="57666-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57666-102">SYNOPSIS</span></span>
<span data-ttu-id="57666-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="57666-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="57666-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="57666-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="57666-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="57666-105">DESCRIPTION</span></span>
<span data-ttu-id="57666-106">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="57666-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="57666-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="57666-107">EXAMPLES</span></span>

### <span data-ttu-id="57666-108">Exemplo 1: Publicar seu BotService no Azure</span><span class="sxs-lookup"><span data-stu-id="57666-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="57666-109">Publicar seu BotService no Azure por código</span><span class="sxs-lookup"><span data-stu-id="57666-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="57666-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="57666-110">PARAMETERS</span></span>

### <span data-ttu-id="57666-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="57666-111">-CodeDir</span></span>
<span data-ttu-id="57666-112">Este parâmetro define o Caminho do ZIP</span><span class="sxs-lookup"><span data-stu-id="57666-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="57666-113">-Name</span><span class="sxs-lookup"><span data-stu-id="57666-113">-Name</span></span>
<span data-ttu-id="57666-114">Esse parâmetro define o nome do bot.</span><span class="sxs-lookup"><span data-stu-id="57666-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="57666-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57666-115">-ResourceGroupName</span></span>
<span data-ttu-id="57666-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57666-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57666-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57666-117">-Confirm</span></span>
<span data-ttu-id="57666-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57666-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57666-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57666-119">-WhatIf</span></span>
<span data-ttu-id="57666-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="57666-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57666-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="57666-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57666-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57666-122">CommonParameters</span></span>
<span data-ttu-id="57666-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57666-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57666-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="57666-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57666-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57666-125">INPUTS</span></span>

## <span data-ttu-id="57666-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="57666-126">OUTPUTS</span></span>

## <span data-ttu-id="57666-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="57666-127">NOTES</span></span>

<span data-ttu-id="57666-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="57666-128">ALIASES</span></span>

## <span data-ttu-id="57666-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57666-129">RELATED LINKS</span></span>

