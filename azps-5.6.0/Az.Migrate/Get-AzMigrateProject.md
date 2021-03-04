---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 4176b07f8a19538a05899b526d21f21cfcc20c9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889254"
---
# <span data-ttu-id="13139-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="13139-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="13139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13139-102">SYNOPSIS</span></span>
<span data-ttu-id="13139-103">Método para obter um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="13139-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="13139-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="13139-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="13139-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="13139-105">DESCRIPTION</span></span>
<span data-ttu-id="13139-106">Método para obter um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="13139-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="13139-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="13139-107">EXAMPLES</span></span>

### <span data-ttu-id="13139-108">Exemplo 1: Obter</span><span class="sxs-lookup"><span data-stu-id="13139-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="13139-109">Método para obter um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="13139-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="13139-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="13139-110">PARAMETERS</span></span>

### <span data-ttu-id="13139-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13139-111">-DefaultProfile</span></span>
<span data-ttu-id="13139-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="13139-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13139-113">-Name</span><span class="sxs-lookup"><span data-stu-id="13139-113">-Name</span></span>
<span data-ttu-id="13139-114">Nome do projeto migrar do Azure.</span><span class="sxs-lookup"><span data-stu-id="13139-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="13139-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13139-115">-ResourceGroupName</span></span>
<span data-ttu-id="13139-116">O nome do Grupo de Recursos do Azure que migra o projeto faz parte.</span><span class="sxs-lookup"><span data-stu-id="13139-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="13139-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13139-117">-SubscriptionId</span></span>
<span data-ttu-id="13139-118">ID de Assinatura do Azure no qual o projeto de migração foi criado.</span><span class="sxs-lookup"><span data-stu-id="13139-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="13139-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13139-119">CommonParameters</span></span>
<span data-ttu-id="13139-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13139-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13139-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13139-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13139-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="13139-122">INPUTS</span></span>

## <span data-ttu-id="13139-123">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="13139-123">OUTPUTS</span></span>

### <span data-ttu-id="13139-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="13139-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="13139-125">NOTES</span><span class="sxs-lookup"><span data-stu-id="13139-125">NOTES</span></span>

<span data-ttu-id="13139-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="13139-126">ALIASES</span></span>

## <span data-ttu-id="13139-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="13139-127">RELATED LINKS</span></span>

