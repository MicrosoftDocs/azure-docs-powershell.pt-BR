---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 77b1dae0db73a9a90a2100edef893edabfe87d0b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433523"
---
# <span data-ttu-id="98b34-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="98b34-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="98b34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="98b34-102">SYNOPSIS</span></span>
<span data-ttu-id="98b34-103">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="98b34-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="98b34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98b34-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="98b34-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="98b34-105">DESCRIPTION</span></span>
<span data-ttu-id="98b34-106">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="98b34-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="98b34-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="98b34-107">EXAMPLES</span></span>

### <span data-ttu-id="98b34-108">Exemplo 1: obter a réplica do servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="98b34-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="98b34-109">Este cmdlet obtém a réplica do servidor MySql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="98b34-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="98b34-110">OS</span><span class="sxs-lookup"><span data-stu-id="98b34-110">PARAMETERS</span></span>

### <span data-ttu-id="98b34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b34-111">-DefaultProfile</span></span>
<span data-ttu-id="98b34-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="98b34-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98b34-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98b34-113">-ResourceGroupName</span></span>
<span data-ttu-id="98b34-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="98b34-114">The name of the resource group.</span></span>
<span data-ttu-id="98b34-115">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="98b34-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="98b34-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="98b34-116">-ServerName</span></span>
<span data-ttu-id="98b34-117">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="98b34-117">The name of the server.</span></span>

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

### <span data-ttu-id="98b34-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98b34-118">-SubscriptionId</span></span>
<span data-ttu-id="98b34-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="98b34-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="98b34-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b34-120">CommonParameters</span></span>
<span data-ttu-id="98b34-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98b34-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b34-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98b34-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b34-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="98b34-123">INPUTS</span></span>

## <span data-ttu-id="98b34-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="98b34-124">OUTPUTS</span></span>

### <span data-ttu-id="98b34-125">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20200701Preview. IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="98b34-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="98b34-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="98b34-126">NOTES</span></span>

<span data-ttu-id="98b34-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="98b34-127">ALIASES</span></span>

## <span data-ttu-id="98b34-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="98b34-128">RELATED LINKS</span></span>

