---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlReplica.md
ms.openlocfilehash: 5d27610924fe0b4a92acfb5f7d1e678742d5b5c7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111504"
---
# <span data-ttu-id="4c62c-101">Get-AzPostgreSqlReplica</span><span class="sxs-lookup"><span data-stu-id="4c62c-101">Get-AzPostgreSqlReplica</span></span>

## <span data-ttu-id="4c62c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c62c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c62c-103">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="4c62c-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="4c62c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c62c-104">SYNTAX</span></span>

```
Get-AzPostgreSqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4c62c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4c62c-105">DESCRIPTION</span></span>
<span data-ttu-id="4c62c-106">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="4c62c-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="4c62c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4c62c-107">EXAMPLES</span></span>

### <span data-ttu-id="4c62c-108">Exemplo 1: Obter a replica do servidor PostgreSql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="4c62c-108">Example 1: Get PostgreSql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlReplica -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserverreplica eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="4c62c-109">Este cmdlet obtém a réplica do servidor PostgreSql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4c62c-109">This cmdlet gets PostgreSql server replica by resource group and server name.</span></span>

## <span data-ttu-id="4c62c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c62c-110">PARAMETERS</span></span>

### <span data-ttu-id="4c62c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c62c-111">-DefaultProfile</span></span>
<span data-ttu-id="4c62c-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4c62c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c62c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c62c-113">-ResourceGroupName</span></span>
<span data-ttu-id="4c62c-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c62c-114">The name of the resource group.</span></span>
<span data-ttu-id="4c62c-115">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4c62c-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4c62c-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4c62c-116">-ServerName</span></span>
<span data-ttu-id="4c62c-117">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="4c62c-117">The name of the server.</span></span>

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

### <span data-ttu-id="4c62c-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c62c-118">-SubscriptionId</span></span>
<span data-ttu-id="4c62c-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="4c62c-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4c62c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c62c-120">CommonParameters</span></span>
<span data-ttu-id="4c62c-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c62c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c62c-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c62c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c62c-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="4c62c-123">INPUTS</span></span>

## <span data-ttu-id="4c62c-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="4c62c-124">OUTPUTS</span></span>

### <span data-ttu-id="4c62c-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="4c62c-125">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="4c62c-126">Notas</span><span class="sxs-lookup"><span data-stu-id="4c62c-126">NOTES</span></span>

<span data-ttu-id="4c62c-127">Aliases</span><span class="sxs-lookup"><span data-stu-id="4c62c-127">ALIASES</span></span>

## <span data-ttu-id="4c62c-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c62c-128">RELATED LINKS</span></span>

