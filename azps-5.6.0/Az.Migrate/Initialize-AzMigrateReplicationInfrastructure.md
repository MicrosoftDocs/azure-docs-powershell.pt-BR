---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/initialize-azmigratereplicationinfrastructure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Initialize-AzMigrateReplicationInfrastructure.md
ms.openlocfilehash: 27206ac1c4e256efcd4093c8cdc9647b6059b3ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889234"
---
# <span data-ttu-id="ae445-101">Initialize-AzMigrateReplicationInfrastructure</span><span class="sxs-lookup"><span data-stu-id="ae445-101">Initialize-AzMigrateReplicationInfrastructure</span></span>

## <span data-ttu-id="ae445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae445-102">SYNOPSIS</span></span>
<span data-ttu-id="ae445-103">Inicializa a infraestrutura do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="ae445-103">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="ae445-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae445-104">SYNTAX</span></span>

```
Initialize-AzMigrateReplicationInfrastructure -ProjectName <String> -ResourceGroupName <String>
 -Scenario <String> -TargetRegion <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae445-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae445-105">DESCRIPTION</span></span>
<span data-ttu-id="ae445-106">O Initialize-AzMigrateReplicationInfrastructure cmdlet inicializa a infraestrutura do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="ae445-106">The Initialize-AzMigrateReplicationInfrastructure cmdlet initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="ae445-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae445-107">EXAMPLES</span></span>

### <span data-ttu-id="ae445-108">Exemplo 1: inicializa a infraestrutura do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="ae445-108">Example 1: Initialises the infrastructure for the migrate project.</span></span>
```powershell
PS C:\> Initialize-AzMigrateReplicationInfrastructure.ps1 -ResourceGroupName TestRG  -ProjectName TestProject -Vmwareagentless -TargetRegion centralus

True
```

<span data-ttu-id="ae445-109">Inicializa a infraestrutura do projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="ae445-109">Initialises the infrastructure for the migrate project.</span></span>

## <span data-ttu-id="ae445-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae445-110">PARAMETERS</span></span>

### <span data-ttu-id="ae445-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae445-111">-DefaultProfile</span></span>
<span data-ttu-id="ae445-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae445-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae445-113">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="ae445-113">-ProjectName</span></span>
<span data-ttu-id="ae445-114">Especifica o nome do projeto Azure Migrate a ser usado para migração do servidor.</span><span class="sxs-lookup"><span data-stu-id="ae445-114">Specifies the name of the Azure Migrate project to be used for server migration.</span></span>

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

### <span data-ttu-id="ae445-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae445-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae445-116">Especifica o Grupo de Recursos do Projeto migrar do Azure na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ae445-116">Specifies the Resource Group of the Azure Migrate Project in the current subscription.</span></span>

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

### <span data-ttu-id="ae445-117">-Scenario</span><span class="sxs-lookup"><span data-stu-id="ae445-117">-Scenario</span></span>
<span data-ttu-id="ae445-118">Especifica o cenário de migração do servidor para o qual a infraestrutura de replicação precisa ser inicializada.</span><span class="sxs-lookup"><span data-stu-id="ae445-118">Specifies the server migration scenario for which the replication infrastructure needs to be initialized.</span></span>

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

### <span data-ttu-id="ae445-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae445-119">-SubscriptionId</span></span>
<span data-ttu-id="ae445-120">ID da Assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="ae445-120">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="ae445-121">-TargetRegion</span><span class="sxs-lookup"><span data-stu-id="ae445-121">-TargetRegion</span></span>
<span data-ttu-id="ae445-122">Especifica a região de destino do Azure para migrações de servidor.</span><span class="sxs-lookup"><span data-stu-id="ae445-122">Specifies the target Azure region for server migrations.</span></span>

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

### <span data-ttu-id="ae445-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae445-123">-Confirm</span></span>
<span data-ttu-id="ae445-124">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae445-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae445-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae445-125">-WhatIf</span></span>
<span data-ttu-id="ae445-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae445-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae445-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae445-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae445-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae445-128">CommonParameters</span></span>
<span data-ttu-id="ae445-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae445-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae445-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae445-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae445-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae445-131">INPUTS</span></span>

## <span data-ttu-id="ae445-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae445-132">OUTPUTS</span></span>

### <span data-ttu-id="ae445-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ae445-133">System.Boolean</span></span>

## <span data-ttu-id="ae445-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae445-134">NOTES</span></span>

<span data-ttu-id="ae445-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ae445-135">ALIASES</span></span>

## <span data-ttu-id="ae445-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae445-136">RELATED LINKS</span></span>

