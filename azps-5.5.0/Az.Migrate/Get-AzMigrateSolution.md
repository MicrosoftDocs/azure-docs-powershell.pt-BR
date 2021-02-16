---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118423"
---
# <span data-ttu-id="c9298-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="c9298-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="c9298-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9298-102">SYNOPSIS</span></span>
<span data-ttu-id="c9298-103">Obtém uma solução no projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="c9298-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="c9298-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9298-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9298-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9298-105">DESCRIPTION</span></span>
<span data-ttu-id="c9298-106">Obtém uma solução no projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="c9298-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="c9298-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c9298-107">EXAMPLES</span></span>

### <span data-ttu-id="c9298-108">Exemplo 1: Obter</span><span class="sxs-lookup"><span data-stu-id="c9298-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="c9298-109">Obter a solução migrar projeto por nome.</span><span class="sxs-lookup"><span data-stu-id="c9298-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="c9298-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9298-110">PARAMETERS</span></span>

### <span data-ttu-id="c9298-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9298-111">-DefaultProfile</span></span>
<span data-ttu-id="c9298-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9298-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9298-113">-MigrarProjectName</span><span class="sxs-lookup"><span data-stu-id="c9298-113">-MigrateProjectName</span></span>
<span data-ttu-id="c9298-114">Nome do projeto migrar do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9298-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="c9298-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9298-115">-Name</span></span>
<span data-ttu-id="c9298-116">Nome exclusivo de uma solução de migração dentro de um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="c9298-116">Unique name of a migration solution within a migrate project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SolutionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9298-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9298-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9298-118">O nome do Grupo de Recursos do Azure que migra o projeto faz parte.</span><span class="sxs-lookup"><span data-stu-id="c9298-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="c9298-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9298-119">-SubscriptionId</span></span>
<span data-ttu-id="c9298-120">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="c9298-120">Azure Subscription Id in which migrate project was created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9298-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9298-121">CommonParameters</span></span>
<span data-ttu-id="c9298-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9298-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9298-123">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9298-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9298-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="c9298-124">INPUTS</span></span>

## <span data-ttu-id="c9298-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="c9298-125">OUTPUTS</span></span>

### <span data-ttu-id="c9298-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="c9298-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="c9298-127">Notas</span><span class="sxs-lookup"><span data-stu-id="c9298-127">NOTES</span></span>

<span data-ttu-id="c9298-128">Aliases</span><span class="sxs-lookup"><span data-stu-id="c9298-128">ALIASES</span></span>

## <span data-ttu-id="c9298-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9298-129">RELATED LINKS</span></span>

