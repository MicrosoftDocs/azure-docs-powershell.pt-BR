---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbReplica.md
ms.openlocfilehash: c6fef537c3a0cc01bd2de01e00b69c1a69f81e3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887718"
---
# <span data-ttu-id="c9013-101">Get-AzMariaDbReplica</span><span class="sxs-lookup"><span data-stu-id="c9013-101">Get-AzMariaDbReplica</span></span>

## <span data-ttu-id="c9013-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9013-102">SYNOPSIS</span></span>
<span data-ttu-id="c9013-103">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="c9013-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="c9013-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c9013-104">SYNTAX</span></span>

```
Get-AzMariaDbReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c9013-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c9013-105">DESCRIPTION</span></span>
<span data-ttu-id="c9013-106">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="c9013-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="c9013-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9013-107">EXAMPLES</span></span>

### <span data-ttu-id="c9013-108">Exemplo 1: Listar todas as réplicas DB em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="c9013-108">Example 1: List all replica DB under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbReplica -ServerName mariadb-test-szp6dt -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------   -------        --------------
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
mariadb-test-szp6dt-rep154 eastus   zcsxhpasdc         10.2    5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="c9013-109">Este comando lista todas as réplicas DB em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="c9013-109">This command lists all replica DB under a MariaDB.</span></span>

## <span data-ttu-id="c9013-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c9013-110">PARAMETERS</span></span>

### <span data-ttu-id="c9013-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9013-111">-DefaultProfile</span></span>
<span data-ttu-id="c9013-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9013-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9013-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9013-113">-ResourceGroupName</span></span>
<span data-ttu-id="c9013-114">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="c9013-114">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c9013-115">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="c9013-115">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c9013-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c9013-116">-ServerName</span></span>
<span data-ttu-id="c9013-117">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="c9013-117">The name of the server.</span></span>

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

### <span data-ttu-id="c9013-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c9013-118">-SubscriptionId</span></span>
<span data-ttu-id="c9013-119">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="c9013-119">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="c9013-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9013-120">CommonParameters</span></span>
<span data-ttu-id="c9013-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9013-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9013-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9013-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9013-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9013-123">INPUTS</span></span>

## <span data-ttu-id="c9013-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c9013-124">OUTPUTS</span></span>

### <span data-ttu-id="c9013-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="c9013-125">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="c9013-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="c9013-126">NOTES</span></span>

<span data-ttu-id="c9013-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c9013-127">ALIASES</span></span>

## <span data-ttu-id="c9013-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9013-128">RELATED LINKS</span></span>

