---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280477"
---
# <span data-ttu-id="2beb6-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="2beb6-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="2beb6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2beb6-102">SYNOPSIS</span></span>
<span data-ttu-id="2beb6-103">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="2beb6-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="2beb6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2beb6-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2beb6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2beb6-105">DESCRIPTION</span></span>
<span data-ttu-id="2beb6-106">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="2beb6-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="2beb6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2beb6-107">EXAMPLES</span></span>

### <span data-ttu-id="2beb6-108">Exemplo 1: obter a réplica do servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="2beb6-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="2beb6-109">Este cmdlet obtém a réplica do servidor MySql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="2beb6-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="2beb6-110">OS</span><span class="sxs-lookup"><span data-stu-id="2beb6-110">PARAMETERS</span></span>

### <span data-ttu-id="2beb6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2beb6-111">-DefaultProfile</span></span>
<span data-ttu-id="2beb6-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2beb6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2beb6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2beb6-113">-ResourceGroupName</span></span>
<span data-ttu-id="2beb6-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2beb6-114">The name of the resource group.</span></span>
<span data-ttu-id="2beb6-115">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2beb6-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2beb6-116">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2beb6-116">-ServerName</span></span>
<span data-ttu-id="2beb6-117">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="2beb6-117">The name of the server.</span></span>

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

### <span data-ttu-id="2beb6-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2beb6-118">-SubscriptionId</span></span>
<span data-ttu-id="2beb6-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="2beb6-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2beb6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2beb6-120">CommonParameters</span></span>
<span data-ttu-id="2beb6-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2beb6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2beb6-122">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2beb6-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2beb6-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2beb6-123">INPUTS</span></span>

## <span data-ttu-id="2beb6-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2beb6-124">OUTPUTS</span></span>

### <span data-ttu-id="2beb6-125">Microsoft. Azure. PowerShell. cmdlets. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="2beb6-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="2beb6-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2beb6-126">NOTES</span></span>

<span data-ttu-id="2beb6-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2beb6-127">ALIASES</span></span>

## <span data-ttu-id="2beb6-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2beb6-128">RELATED LINKS</span></span>

