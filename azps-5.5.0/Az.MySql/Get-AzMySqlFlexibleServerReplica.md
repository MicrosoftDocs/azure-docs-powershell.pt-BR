---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerReplica.md
ms.openlocfilehash: 77b1dae0db73a9a90a2100edef893edabfe87d0b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114749"
---
# <span data-ttu-id="02eb5-101">Get-AzMySqlFlexibleServerReplica</span><span class="sxs-lookup"><span data-stu-id="02eb5-101">Get-AzMySqlFlexibleServerReplica</span></span>

## <span data-ttu-id="02eb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="02eb5-102">SYNOPSIS</span></span>
<span data-ttu-id="02eb5-103">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="02eb5-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="02eb5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02eb5-104">SYNTAX</span></span>

```
Get-AzMySqlFlexibleServerReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="02eb5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="02eb5-105">DESCRIPTION</span></span>
<span data-ttu-id="02eb5-106">Listar todas as réplicas de um determinado servidor.</span><span class="sxs-lookup"><span data-stu-id="02eb5-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="02eb5-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="02eb5-107">EXAMPLES</span></span>

### <span data-ttu-id="02eb5-108">Exemplo 1: Obter a replica do servidor MySql por grupo de recursos e nome do servidor</span><span class="sxs-lookup"><span data-stu-id="02eb5-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="02eb5-109">Este cmdlet obtém a replicação do servidor MySql por grupo de recursos e nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="02eb5-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="02eb5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02eb5-110">PARAMETERS</span></span>

### <span data-ttu-id="02eb5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02eb5-111">-DefaultProfile</span></span>
<span data-ttu-id="02eb5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="02eb5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02eb5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02eb5-113">-ResourceGroupName</span></span>
<span data-ttu-id="02eb5-114">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="02eb5-114">The name of the resource group.</span></span>
<span data-ttu-id="02eb5-115">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="02eb5-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="02eb5-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="02eb5-116">-ServerName</span></span>
<span data-ttu-id="02eb5-117">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="02eb5-117">The name of the server.</span></span>

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

### <span data-ttu-id="02eb5-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02eb5-118">-SubscriptionId</span></span>
<span data-ttu-id="02eb5-119">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="02eb5-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="02eb5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02eb5-120">CommonParameters</span></span>
<span data-ttu-id="02eb5-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02eb5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02eb5-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02eb5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02eb5-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="02eb5-123">INPUTS</span></span>

## <span data-ttu-id="02eb5-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="02eb5-124">OUTPUTS</span></span>

### <span data-ttu-id="02eb5-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="02eb5-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="02eb5-126">Notas</span><span class="sxs-lookup"><span data-stu-id="02eb5-126">NOTES</span></span>

<span data-ttu-id="02eb5-127">Aliases</span><span class="sxs-lookup"><span data-stu-id="02eb5-127">ALIASES</span></span>

## <span data-ttu-id="02eb5-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="02eb5-128">RELATED LINKS</span></span>

