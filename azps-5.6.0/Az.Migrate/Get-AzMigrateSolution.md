---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: c3829997703feb0ca3098dfd7bc314b71d5b5d5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889235"
---
# <span data-ttu-id="8b9d4-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="8b9d4-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="8b9d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b9d4-102">SYNOPSIS</span></span>
<span data-ttu-id="8b9d4-103">Obtém uma solução no projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="8b9d4-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="8b9d4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8b9d4-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8b9d4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8b9d4-105">DESCRIPTION</span></span>
<span data-ttu-id="8b9d4-106">Obtém uma solução no projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="8b9d4-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="8b9d4-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b9d4-107">EXAMPLES</span></span>

### <span data-ttu-id="8b9d4-108">Exemplo 1: Obter</span><span class="sxs-lookup"><span data-stu-id="8b9d4-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="8b9d4-109">Obter Migrar solução de projeto pelo nome.</span><span class="sxs-lookup"><span data-stu-id="8b9d4-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="8b9d4-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8b9d4-110">PARAMETERS</span></span>

### <span data-ttu-id="8b9d4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b9d4-111">-DefaultProfile</span></span>
<span data-ttu-id="8b9d4-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b9d4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b9d4-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="8b9d4-113">-MigrateProjectName</span></span>
<span data-ttu-id="8b9d4-114">Nome do projeto migrar do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b9d4-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="8b9d4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b9d4-115">-Name</span></span>
<span data-ttu-id="8b9d4-116">Nome exclusivo de uma solução de migração dentro de um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="8b9d4-116">Unique name of a migration solution within a migrate project.</span></span>

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

### <span data-ttu-id="8b9d4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b9d4-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b9d4-118">O nome do Grupo de Recursos do Azure que migra o projeto faz parte.</span><span class="sxs-lookup"><span data-stu-id="8b9d4-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="8b9d4-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b9d4-119">-SubscriptionId</span></span>
<span data-ttu-id="8b9d4-120">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="8b9d4-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="8b9d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b9d4-121">CommonParameters</span></span>
<span data-ttu-id="8b9d4-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b9d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b9d4-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b9d4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b9d4-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b9d4-124">INPUTS</span></span>

## <span data-ttu-id="8b9d4-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8b9d4-125">OUTPUTS</span></span>

### <span data-ttu-id="8b9d4-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span><span class="sxs-lookup"><span data-stu-id="8b9d4-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="8b9d4-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="8b9d4-127">NOTES</span></span>

<span data-ttu-id="8b9d4-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8b9d4-128">ALIASES</span></span>

## <span data-ttu-id="8b9d4-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b9d4-129">RELATED LINKS</span></span>

