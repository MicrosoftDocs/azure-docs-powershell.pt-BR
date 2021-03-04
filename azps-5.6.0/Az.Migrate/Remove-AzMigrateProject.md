---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: d9edb00bf7944400fa681f857dd7005d9eaf69b5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892121"
---
# <span data-ttu-id="98bee-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="98bee-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="98bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98bee-102">SYNOPSIS</span></span>
<span data-ttu-id="98bee-103">Exclua o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="98bee-103">Delete the migrate project.</span></span>
<span data-ttu-id="98bee-104">Excluir projeto não existente é uma não operação.</span><span class="sxs-lookup"><span data-stu-id="98bee-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="98bee-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="98bee-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98bee-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="98bee-106">DESCRIPTION</span></span>
<span data-ttu-id="98bee-107">Exclua o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="98bee-107">Delete the migrate project.</span></span>
<span data-ttu-id="98bee-108">Excluir projeto não existente é uma não operação.</span><span class="sxs-lookup"><span data-stu-id="98bee-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="98bee-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98bee-109">EXAMPLES</span></span>

### <span data-ttu-id="98bee-110">Exemplo 1: Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="98bee-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="98bee-111">Exclua o projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="98bee-111">Delete the migrate project.</span></span>
<span data-ttu-id="98bee-112">Excluir projeto não existente é uma não operação.</span><span class="sxs-lookup"><span data-stu-id="98bee-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="98bee-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="98bee-113">PARAMETERS</span></span>

### <span data-ttu-id="98bee-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="98bee-114">-AcceptLanguage</span></span>
<span data-ttu-id="98bee-115">Header de solicitação padrão.</span><span class="sxs-lookup"><span data-stu-id="98bee-115">Standard request header.</span></span>
<span data-ttu-id="98bee-116">Usado pelo serviço para responder ao cliente no idioma apropriado.</span><span class="sxs-lookup"><span data-stu-id="98bee-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="98bee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98bee-117">-DefaultProfile</span></span>
<span data-ttu-id="98bee-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98bee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98bee-119">-Name</span><span class="sxs-lookup"><span data-stu-id="98bee-119">-Name</span></span>
<span data-ttu-id="98bee-120">Nome do projeto migrar do Azure.</span><span class="sxs-lookup"><span data-stu-id="98bee-120">Name of the Azure Migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrateProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bee-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98bee-121">-PassThru</span></span>
<span data-ttu-id="98bee-122">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="98bee-122">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98bee-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98bee-123">-ResourceGroupName</span></span>
<span data-ttu-id="98bee-124">O nome do Grupo de Recursos do Azure que migra o projeto faz parte.</span><span class="sxs-lookup"><span data-stu-id="98bee-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="98bee-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98bee-125">-SubscriptionId</span></span>
<span data-ttu-id="98bee-126">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="98bee-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="98bee-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98bee-127">-Confirm</span></span>
<span data-ttu-id="98bee-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98bee-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98bee-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98bee-129">-WhatIf</span></span>
<span data-ttu-id="98bee-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="98bee-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98bee-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="98bee-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98bee-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98bee-132">CommonParameters</span></span>
<span data-ttu-id="98bee-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98bee-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98bee-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98bee-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98bee-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="98bee-135">INPUTS</span></span>

## <span data-ttu-id="98bee-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="98bee-136">OUTPUTS</span></span>

### <span data-ttu-id="98bee-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98bee-137">System.Boolean</span></span>

## <span data-ttu-id="98bee-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="98bee-138">NOTES</span></span>

<span data-ttu-id="98bee-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="98bee-139">ALIASES</span></span>

## <span data-ttu-id="98bee-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98bee-140">RELATED LINKS</span></span>

