---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/remove-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Remove-AzMigrateProject.md
ms.openlocfilehash: e0918573b7fc1190d32aaaaa4bfe73ed9fe05fe6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124570"
---
# <span data-ttu-id="7e0f0-101">Remove-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7e0f0-101">Remove-AzMigrateProject</span></span>

## <span data-ttu-id="7e0f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7e0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0f0-103">Exclua o projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-103">Delete the migrate project.</span></span>
<span data-ttu-id="7e0f0-104">A exclusão de um projeto não existente não é uma operação.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-104">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="7e0f0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7e0f0-105">SYNTAX</span></span>

```
Remove-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7e0f0-106">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7e0f0-106">DESCRIPTION</span></span>
<span data-ttu-id="7e0f0-107">Exclua o projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-107">Delete the migrate project.</span></span>
<span data-ttu-id="7e0f0-108">A exclusão de um projeto não existente não é uma operação.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-108">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="7e0f0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e0f0-109">EXAMPLES</span></span>

### <span data-ttu-id="7e0f0-110">Exemplo 1: excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="7e0f0-110">Example 1: Delete (Default)</span></span>
```powershell
PS C:\> Remove-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

--No output--
```

<span data-ttu-id="7e0f0-111">Exclua o projeto migrar.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-111">Delete the migrate project.</span></span>
<span data-ttu-id="7e0f0-112">A exclusão de um projeto não existente não é uma operação.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-112">Deleting non-existent project is a no-operation.</span></span>

## <span data-ttu-id="7e0f0-113">OS</span><span class="sxs-lookup"><span data-stu-id="7e0f0-113">PARAMETERS</span></span>

### <span data-ttu-id="7e0f0-114">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="7e0f0-114">-AcceptLanguage</span></span>
<span data-ttu-id="7e0f0-115">Cabeçalho de solicitação padrão.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-115">Standard request header.</span></span>
<span data-ttu-id="7e0f0-116">Usado pelo serviço para responder ao cliente no idioma apropriado.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-116">Used by service to respond to client in appropriate language.</span></span>

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

### <span data-ttu-id="7e0f0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0f0-117">-DefaultProfile</span></span>
<span data-ttu-id="7e0f0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e0f0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e0f0-119">-Name</span></span>
<span data-ttu-id="7e0f0-120">Nome do projeto de migração do Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-120">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="7e0f0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e0f0-121">-PassThru</span></span>
<span data-ttu-id="7e0f0-122">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="7e0f0-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7e0f0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e0f0-123">-ResourceGroupName</span></span>
<span data-ttu-id="7e0f0-124">Nome do grupo de recursos do Azure do qual a migração do Project faz parte.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-124">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="7e0f0-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e0f0-125">-SubscriptionId</span></span>
<span data-ttu-id="7e0f0-126">ID da assinatura do Azure na qual migrar projeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-126">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="7e0f0-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7e0f0-127">-Confirm</span></span>
<span data-ttu-id="7e0f0-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e0f0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e0f0-129">-WhatIf</span></span>
<span data-ttu-id="7e0f0-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e0f0-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e0f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0f0-132">CommonParameters</span></span>
<span data-ttu-id="7e0f0-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0f0-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e0f0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0f0-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7e0f0-135">INPUTS</span></span>

## <span data-ttu-id="7e0f0-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7e0f0-136">OUTPUTS</span></span>

### <span data-ttu-id="7e0f0-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e0f0-137">System.Boolean</span></span>

## <span data-ttu-id="7e0f0-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7e0f0-138">NOTES</span></span>

<span data-ttu-id="7e0f0-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7e0f0-139">ALIASES</span></span>

## <span data-ttu-id="7e0f0-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e0f0-140">RELATED LINKS</span></span>

