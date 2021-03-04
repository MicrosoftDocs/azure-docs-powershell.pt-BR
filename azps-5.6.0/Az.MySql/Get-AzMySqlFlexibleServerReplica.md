---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 25444df39945527d1bc574283e397407e0218633
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886741"
---
# <span data-ttu-id="81be1-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="81be1-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="81be1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81be1-102">SYNOPSIS</span></span>
<span data-ttu-id="81be1-103">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="81be1-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="81be1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="81be1-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="81be1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="81be1-105">DESCRIPTION</span></span>
<span data-ttu-id="81be1-106">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="81be1-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="81be1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="81be1-107">EXAMPLES</span></span>

### <span data-ttu-id="81be1-108">Exemplo 1: Obter réplica do servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="81be1-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="81be1-109">Este cmdlet obtém a réplica do servidor MySql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="81be1-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="81be1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="81be1-110">PARAMETERS</span></span>

### <span data-ttu-id="81be1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81be1-111">-DefaultProfile</span></span>
<span data-ttu-id="81be1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="81be1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81be1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81be1-113">-ResourceGroupName</span></span>
<span data-ttu-id="81be1-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="81be1-114">The name of the resource group.</span></span>
<span data-ttu-id="81be1-115">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="81be1-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="81be1-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81be1-116">-ServerName</span></span>
<span data-ttu-id="81be1-117">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="81be1-117">The name of the server.</span></span>

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

### <span data-ttu-id="81be1-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="81be1-118">-SubscriptionId</span></span>
<span data-ttu-id="81be1-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="81be1-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="81be1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81be1-120">CommonParameters</span></span>
<span data-ttu-id="81be1-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81be1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81be1-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81be1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81be1-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81be1-123">INPUTS</span></span>

## <span data-ttu-id="81be1-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="81be1-124">OUTPUTS</span></span>

### <span data-ttu-id="81be1-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="81be1-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="81be1-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="81be1-126">NOTES</span></span>

<span data-ttu-id="81be1-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="81be1-127">ALIASES</span></span>

## <span data-ttu-id="81be1-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="81be1-128">RELATED LINKS</span></span>

