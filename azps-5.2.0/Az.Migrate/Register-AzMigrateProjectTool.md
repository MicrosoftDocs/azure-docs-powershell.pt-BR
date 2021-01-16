---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/register-azmigrateprojecttool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Register-AzMigrateProjectTool.md
ms.openlocfilehash: dff4b1b5ae83363a5a67cccbe70ee5c000af4419
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98262162"
---
# <span data-ttu-id="e7b30-101">Register-AzMigrateProjectTool</span><span class="sxs-lookup"><span data-stu-id="e7b30-101">Register-AzMigrateProjectTool</span></span>

## <span data-ttu-id="e7b30-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7b30-102">SYNOPSIS</span></span>
<span data-ttu-id="e7b30-103">Registra uma ferramenta com o projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="e7b30-103">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="e7b30-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7b30-104">SYNTAX</span></span>

```
Register-AzMigrateProjectTool -MigrateProjectName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AcceptLanguage <String>] [-Tool <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e7b30-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7b30-105">DESCRIPTION</span></span>
<span data-ttu-id="e7b30-106">Registra uma ferramenta com o projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="e7b30-106">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="e7b30-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7b30-107">EXAMPLES</span></span>

### <span data-ttu-id="e7b30-108">Exemplo 1: ferramenta de registro.</span><span class="sxs-lookup"><span data-stu-id="e7b30-108">Example 1: REgister tool.</span></span>
```powershell
PS C:\> Register-AzMigrateProjectTool -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Tool Zerto

True
```

<span data-ttu-id="e7b30-109">Registra uma ferramenta com o projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="e7b30-109">Registers a tool with the migrate project.</span></span>

## <span data-ttu-id="e7b30-110">OS</span><span class="sxs-lookup"><span data-stu-id="e7b30-110">PARAMETERS</span></span>

### <span data-ttu-id="e7b30-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="e7b30-111">-AcceptLanguage</span></span>
<span data-ttu-id="e7b30-112">Cabeçalho de solicitação padrão.</span><span class="sxs-lookup"><span data-stu-id="e7b30-112">Standard request header.</span></span>
<span data-ttu-id="e7b30-113">Usado pelo serviço para responder ao cliente no idioma apropriado.</span><span class="sxs-lookup"><span data-stu-id="e7b30-113">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="e7b30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7b30-114">-DefaultProfile</span></span>
<span data-ttu-id="e7b30-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e7b30-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7b30-116">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="e7b30-116">-MigrateProjectName</span></span>
<span data-ttu-id="e7b30-117">Nome do projeto de migração do Azure.</span><span class="sxs-lookup"><span data-stu-id="e7b30-117">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="e7b30-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7b30-118">-ResourceGroupName</span></span>
<span data-ttu-id="e7b30-119">Nome do grupo de recursos do Azure do qual a migração do Project faz parte.</span><span class="sxs-lookup"><span data-stu-id="e7b30-119">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="e7b30-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7b30-120">-SubscriptionId</span></span>
<span data-ttu-id="e7b30-121">ID da assinatura do Azure na qual migrar projeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="e7b30-121">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="e7b30-122">-Ferramenta</span><span class="sxs-lookup"><span data-stu-id="e7b30-122">-Tool</span></span>
<span data-ttu-id="e7b30-123">Obtém ou define a ferramenta a ser registrada.</span><span class="sxs-lookup"><span data-stu-id="e7b30-123">Gets or sets the tool to be registered.</span></span>

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

### <span data-ttu-id="e7b30-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7b30-124">-Confirm</span></span>
<span data-ttu-id="e7b30-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7b30-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7b30-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7b30-126">-WhatIf</span></span>
<span data-ttu-id="e7b30-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7b30-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7b30-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7b30-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7b30-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7b30-129">CommonParameters</span></span>
<span data-ttu-id="e7b30-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7b30-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7b30-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7b30-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7b30-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7b30-132">INPUTS</span></span>

## <span data-ttu-id="e7b30-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7b30-133">OUTPUTS</span></span>

### <span data-ttu-id="e7b30-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7b30-134">System.Boolean</span></span>

## <span data-ttu-id="e7b30-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7b30-135">NOTES</span></span>

<span data-ttu-id="e7b30-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e7b30-136">ALIASES</span></span>

## <span data-ttu-id="e7b30-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7b30-137">RELATED LINKS</span></span>

