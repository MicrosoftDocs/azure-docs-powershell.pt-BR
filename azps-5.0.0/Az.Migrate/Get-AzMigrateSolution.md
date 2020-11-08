---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratesolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateSolution.md
ms.openlocfilehash: 62b43668e8d886a11a26204edcd3c8b13635eff4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124813"
---
# <span data-ttu-id="f7ee1-101">Get-AzMigrateSolution</span><span class="sxs-lookup"><span data-stu-id="f7ee1-101">Get-AzMigrateSolution</span></span>

## <span data-ttu-id="f7ee1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f7ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="f7ee1-103">Obtém uma solução no projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-103">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="f7ee1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7ee1-104">SYNTAX</span></span>

```
Get-AzMigrateSolution -MigrateProjectName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f7ee1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f7ee1-105">DESCRIPTION</span></span>
<span data-ttu-id="f7ee1-106">Obtém uma solução no projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-106">Gets a solution in the migrate project.</span></span>

## <span data-ttu-id="f7ee1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f7ee1-107">EXAMPLES</span></span>

### <span data-ttu-id="f7ee1-108">Exemplo 1: obter</span><span class="sxs-lookup"><span data-stu-id="f7ee1-108">Example 1: Get</span></span>
```powershell
PS C:\>Get-AzMigrateSolution -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -MigrateProjectName BugBashAVSVMware -Name Servers-Migration-ServerMigration

Etag                                   Name                              Type
----                                   ----                              ----
"010097f1-0000-1800-0000-5ee9ae2b0000" Servers-Migration-ServerMigration Microsoft.Migrate/MigrateProjec…
```

<span data-ttu-id="f7ee1-109">Obter solução de migração de projeto por nome.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-109">Get Migrate project solution by name.</span></span>

## <span data-ttu-id="f7ee1-110">OS</span><span class="sxs-lookup"><span data-stu-id="f7ee1-110">PARAMETERS</span></span>

### <span data-ttu-id="f7ee1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7ee1-111">-DefaultProfile</span></span>
<span data-ttu-id="f7ee1-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7ee1-113">-MigrateProjectName</span><span class="sxs-lookup"><span data-stu-id="f7ee1-113">-MigrateProjectName</span></span>
<span data-ttu-id="f7ee1-114">Nome do projeto de migração do Azure.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="f7ee1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7ee1-115">-Name</span></span>
<span data-ttu-id="f7ee1-116">Nome exclusivo de uma solução de migração em um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-116">Unique name of a migration solution within a migrate project.</span></span>

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

### <span data-ttu-id="f7ee1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7ee1-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7ee1-118">Nome do grupo de recursos do Azure do qual a migração do Project faz parte.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-118">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="f7ee1-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7ee1-119">-SubscriptionId</span></span>
<span data-ttu-id="f7ee1-120">ID da assinatura do Azure na qual migrar projeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-120">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="f7ee1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7ee1-121">CommonParameters</span></span>
<span data-ttu-id="f7ee1-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7ee1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7ee1-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7ee1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7ee1-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f7ee1-124">INPUTS</span></span>

## <span data-ttu-id="f7ee1-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f7ee1-125">OUTPUTS</span></span>

### <span data-ttu-id="f7ee1-126">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180901Preview. ISolution</span><span class="sxs-lookup"><span data-stu-id="f7ee1-126">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.ISolution</span></span>

## <span data-ttu-id="f7ee1-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f7ee1-127">NOTES</span></span>

<span data-ttu-id="f7ee1-128">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f7ee1-128">ALIASES</span></span>

## <span data-ttu-id="f7ee1-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f7ee1-129">RELATED LINKS</span></span>

