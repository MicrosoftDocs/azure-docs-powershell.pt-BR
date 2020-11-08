---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateProject.md
ms.openlocfilehash: 1e3fdb2eabd986907a4b702a62caa3a0d9c34e85
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126012"
---
# <span data-ttu-id="91980-101">Get-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="91980-101">Get-AzMigrateProject</span></span>

## <span data-ttu-id="91980-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="91980-102">SYNOPSIS</span></span>
<span data-ttu-id="91980-103">Método para obter um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="91980-103">Method to get a migrate project.</span></span>

## <span data-ttu-id="91980-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="91980-104">SYNTAX</span></span>

```
Get-AzMigrateProject -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="91980-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="91980-105">DESCRIPTION</span></span>
<span data-ttu-id="91980-106">Método para obter um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="91980-106">Method to get a migrate project.</span></span>

## <span data-ttu-id="91980-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="91980-107">EXAMPLES</span></span>

### <span data-ttu-id="91980-108">Exemplo 1: obter</span><span class="sxs-lookup"><span data-stu-id="91980-108">Example 1: Get</span></span>
```powershell
PS C:\> Get-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName BugBashAVSVMware -Name BugBashAVSVMware

ETag Location      Name             Type
---- --------      ----             ----
     southeastasia BugBashAVSVMware Microsoft.Migrate/MigrateProjects
```

<span data-ttu-id="91980-109">Método para obter um projeto de migração.</span><span class="sxs-lookup"><span data-stu-id="91980-109">Method to get a migrate project.</span></span>

## <span data-ttu-id="91980-110">OS</span><span class="sxs-lookup"><span data-stu-id="91980-110">PARAMETERS</span></span>

### <span data-ttu-id="91980-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91980-111">-DefaultProfile</span></span>
<span data-ttu-id="91980-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="91980-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91980-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="91980-113">-Name</span></span>
<span data-ttu-id="91980-114">Nome do projeto de migração do Azure.</span><span class="sxs-lookup"><span data-stu-id="91980-114">Name of the Azure Migrate project.</span></span>

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

### <span data-ttu-id="91980-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91980-115">-ResourceGroupName</span></span>
<span data-ttu-id="91980-116">Nome do grupo de recursos do Azure do qual a migração do Project faz parte.</span><span class="sxs-lookup"><span data-stu-id="91980-116">Name of the Azure Resource Group that migrate project is part of.</span></span>

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

### <span data-ttu-id="91980-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91980-117">-SubscriptionId</span></span>
<span data-ttu-id="91980-118">ID da assinatura do Azure na qual migrar projeto foi criado.</span><span class="sxs-lookup"><span data-stu-id="91980-118">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="91980-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91980-119">CommonParameters</span></span>
<span data-ttu-id="91980-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91980-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91980-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91980-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91980-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="91980-122">INPUTS</span></span>

## <span data-ttu-id="91980-123">EXIBE</span><span class="sxs-lookup"><span data-stu-id="91980-123">OUTPUTS</span></span>

### <span data-ttu-id="91980-124">Microsoft. Azure. PowerShell. cmdlets. Migrate. Models. Api20180901Preview. IMigrateProject</span><span class="sxs-lookup"><span data-stu-id="91980-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProject</span></span>

## <span data-ttu-id="91980-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="91980-125">NOTES</span></span>

<span data-ttu-id="91980-126">ALIASES</span><span class="sxs-lookup"><span data-stu-id="91980-126">ALIASES</span></span>

## <span data-ttu-id="91980-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="91980-127">RELATED LINKS</span></span>

