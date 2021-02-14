---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116928"
---
# <span data-ttu-id="fb835-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="fb835-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="fb835-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb835-102">SYNOPSIS</span></span>
<span data-ttu-id="fb835-103">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fb835-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="fb835-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb835-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fb835-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb835-105">DESCRIPTION</span></span>
<span data-ttu-id="fb835-106">Retorna um BotService especificado pelos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fb835-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="fb835-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fb835-107">EXAMPLES</span></span>

### <span data-ttu-id="fb835-108">Exemplo 1: Publicar seu BotService no Azure</span><span class="sxs-lookup"><span data-stu-id="fb835-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="fb835-109">Publicar seu BotService no Azure por código</span><span class="sxs-lookup"><span data-stu-id="fb835-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="fb835-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fb835-110">PARAMETERS</span></span>

### <span data-ttu-id="fb835-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="fb835-111">-CodeDir</span></span>
<span data-ttu-id="fb835-112">Este parâmetro define o Caminho do ZIP</span><span class="sxs-lookup"><span data-stu-id="fb835-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="fb835-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb835-113">-Name</span></span>
<span data-ttu-id="fb835-114">Esse parâmetro define o nome do bot.</span><span class="sxs-lookup"><span data-stu-id="fb835-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="fb835-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb835-115">-ResourceGroupName</span></span>
<span data-ttu-id="fb835-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb835-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb835-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fb835-117">-Confirm</span></span>
<span data-ttu-id="fb835-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb835-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb835-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb835-119">-WhatIf</span></span>
<span data-ttu-id="fb835-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fb835-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb835-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb835-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb835-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb835-122">CommonParameters</span></span>
<span data-ttu-id="fb835-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb835-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb835-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fb835-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb835-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="fb835-125">INPUTS</span></span>

## <span data-ttu-id="fb835-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="fb835-126">OUTPUTS</span></span>

## <span data-ttu-id="fb835-127">Notas</span><span class="sxs-lookup"><span data-stu-id="fb835-127">NOTES</span></span>

<span data-ttu-id="fb835-128">Aliases</span><span class="sxs-lookup"><span data-stu-id="fb835-128">ALIASES</span></span>

## <span data-ttu-id="fb835-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb835-129">RELATED LINKS</span></span>

