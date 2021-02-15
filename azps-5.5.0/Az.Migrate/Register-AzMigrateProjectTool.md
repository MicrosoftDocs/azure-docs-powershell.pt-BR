---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112986"
---
# <span data-ttu-id="c8a4b-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="c8a4b-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="c8a4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8a4b-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a4b-103">Registra uma ferramenta com o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="c8a4b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8a4b-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c8a4b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8a4b-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a4b-106">Registra uma ferramenta com o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="c8a4b-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8a4b-107">EXAMPLES</span></span>

### <span data-ttu-id="c8a4b-108">Exemplo 1: ferramenta REgister.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="c8a4b-109">Registra uma ferramenta com o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="c8a4b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8a4b-110">PARAMETERS</span></span>

### <span data-ttu-id="c8a4b-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="c8a4b-111">-AcceptLanguage</span></span>
<span data-ttu-id="c8a4b-112">Header de solicitação padrão.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-112">Standard request header.</span></span>
<span data-ttu-id="c8a4b-113">Usado pelo serviço para responder ao cliente no idioma apropriado.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="c8a4b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a4b-114">-DefaultProfile</span></span>
<span data-ttu-id="c8a4b-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a4b-116">-MigrarProjectName</span><span class="sxs-lookup"><span data-stu-id="c8a4b-116">-MigrateProjectName</span></span>
<span data-ttu-id="c8a4b-117">Nome do projeto migrar do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="c8a4b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a4b-118">-ResourceGroupName</span></span>
<span data-ttu-id="c8a4b-119">O nome do Grupo de Recursos do Azure que migra o projeto faz parte.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="c8a4b-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c8a4b-120">-SubscriptionId</span></span>
<span data-ttu-id="c8a4b-121">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="c8a4b-122">-Ferramenta</span><span class="sxs-lookup"><span data-stu-id="c8a4b-122">-Tool</span></span>
<span data-ttu-id="c8a4b-123">Obtém ou define a ferramenta a ser registrada.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="c8a4b-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c8a4b-124">-Confirm</span></span>
<span data-ttu-id="c8a4b-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a4b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a4b-126">-WhatIf</span></span>
<span data-ttu-id="c8a4b-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a4b-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a4b-129">CommonParameters</span></span>
<span data-ttu-id="c8a4b-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a4b-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8a4b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a4b-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="c8a4b-132">INPUTS</span></span>

## <span data-ttu-id="c8a4b-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="c8a4b-133">OUTPUTS</span></span>

### <span data-ttu-id="c8a4b-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c8a4b-134">System.Boolean</span></span>

## <span data-ttu-id="c8a4b-135">Notas</span><span class="sxs-lookup"><span data-stu-id="c8a4b-135">NOTES</span></span>

<span data-ttu-id="c8a4b-136">Aliases</span><span class="sxs-lookup"><span data-stu-id="c8a4b-136">ALIASES</span></span>

## <span data-ttu-id="c8a4b-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8a4b-137">RELATED LINKS</span></span>

