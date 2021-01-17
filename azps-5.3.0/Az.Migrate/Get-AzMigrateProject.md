---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427133"
---
# <span data-ttu-id="7f7d5-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7f7d5-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="7f7d5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7f7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7d5-103">Método para obter um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="7f7d5-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="7f7d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7f7d5-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7f7d5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7f7d5-105">DESCRIPTION</span></span>
<span data-ttu-id="7f7d5-106">Método para obter um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="7f7d5-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="7f7d5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7f7d5-107">EXAMPLES</span></span>

### <span data-ttu-id="7f7d5-108">Exemplo 1: obter</span><span class="sxs-lookup"><span data-stu-id="7f7d5-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="7f7d5-109">Método para obter um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="7f7d5-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="7f7d5-110">OS</span><span class="sxs-lookup"><span data-stu-id="7f7d5-110">PARAMETERS</span></span>

### <span data-ttu-id="7f7d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f7d5-111">-DefaultProfile</span></span>
<span data-ttu-id="7f7d5-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7f7d5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f7d5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f7d5-113">-Name</span></span>
<span data-ttu-id="7f7d5-114">Nome do projeto de migração do Azure.</span><span class="sxs-lookup"><span data-stu-id="7f7d5-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="7f7d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f7d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="7f7d5-116">Nome do grupo de recursos do Azure do qual a migração do Project faz parte.</span><span class="sxs-lookup"><span data-stu-id="7f7d5-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="7f7d5-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f7d5-117">-SubscriptionId</span></span>
<span data-ttu-id="7f7d5-118">ID da assinatura do Azure na qual migrar projeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="7f7d5-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="7f7d5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7d5-119">CommonParameters</span></span>
<span data-ttu-id="7f7d5-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f7d5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7d5-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f7d5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7d5-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7f7d5-122">INPUTS</span></span>

## <span data-ttu-id="7f7d5-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7f7d5-123">OUTPUTS</span></span>

### <span data-ttu-id="7f7d5-124">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180901Preview. IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="7f7d5-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="7f7d5-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7f7d5-125">NOTES</span></span>

<span data-ttu-id="7f7d5-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="7f7d5-126">ALIASES</span></span>

## <span data-ttu-id="7f7d5-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7f7d5-127">RELATED LINKS</span></span>

