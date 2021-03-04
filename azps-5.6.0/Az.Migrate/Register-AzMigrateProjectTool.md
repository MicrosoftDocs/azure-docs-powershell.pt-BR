---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: 60cc9b5b537c1d8e46f5bae56d93b33fa04f6c89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888483"
---
# <span data-ttu-id="14026-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="14026-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="14026-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14026-102">SYNOPSIS</span></span>
<span data-ttu-id="14026-103">Registra uma ferramenta com o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="14026-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="14026-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="14026-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14026-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="14026-105">DESCRIPTION</span></span>
<span data-ttu-id="14026-106">Registra uma ferramenta com o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="14026-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="14026-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14026-107">EXAMPLES</span></span>

### <span data-ttu-id="14026-108">Exemplo 1: ferramenta REgister.</span><span class="sxs-lookup"><span data-stu-id="14026-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="14026-109">Registra uma ferramenta com o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="14026-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="14026-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="14026-110">PARAMETERS</span></span>

### <span data-ttu-id="14026-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="14026-111">-AcceptLanguage</span></span>
<span data-ttu-id="14026-112">Header de solicitação padrão.</span><span class="sxs-lookup"><span data-stu-id="14026-112">Standard request header.</span></span>
<span data-ttu-id="14026-113">Usado pelo serviço para responder ao cliente no idioma apropriado.</span><span class="sxs-lookup"><span data-stu-id="14026-113">Used by service to respond to client in appropriate language.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14026-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14026-114">-DefaultProfile</span></span>
<span data-ttu-id="14026-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14026-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14026-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="14026-116">-MigrateProjectName</span></span>
<span data-ttu-id="14026-117">Nome do projeto migrar do Azure.</span><span class="sxs-lookup"><span data-stu-id="14026-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="14026-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14026-118">-ResourceGroupName</span></span>
<span data-ttu-id="14026-119">O nome do Grupo de Recursos do Azure que migra o projeto faz parte.</span><span class="sxs-lookup"><span data-stu-id="14026-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="14026-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14026-120">-SubscriptionId</span></span>
<span data-ttu-id="14026-121">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="14026-121">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14026-122">-Tool</span><span class="sxs-lookup"><span data-stu-id="14026-122">-Tool</span></span>
<span data-ttu-id="14026-123">Obtém ou define a ferramenta a ser registrada.</span><span class="sxs-lookup"><span data-stu-id="14026-123">Gets or sets the tool to be registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14026-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14026-124">-Confirm</span></span>
<span data-ttu-id="14026-125">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14026-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14026-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14026-126">-WhatIf</span></span>
<span data-ttu-id="14026-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14026-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14026-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14026-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14026-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14026-129">CommonParameters</span></span>
<span data-ttu-id="14026-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14026-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14026-131">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14026-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14026-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14026-132">INPUTS</span></span>

## <span data-ttu-id="14026-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="14026-133">OUTPUTS</span></span>

### <span data-ttu-id="14026-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14026-134">System.Boolean</span></span>

## <span data-ttu-id="14026-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="14026-135">NOTES</span></span>

<span data-ttu-id="14026-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="14026-136">ALIASES</span></span>

## <span data-ttu-id="14026-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14026-137">RELATED LINKS</span></span>

