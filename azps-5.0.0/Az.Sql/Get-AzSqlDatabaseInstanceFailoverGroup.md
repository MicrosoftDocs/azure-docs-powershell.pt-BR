---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: bd2a157a1fb05baf0fa6e02b061462718ffad314
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115668"
---
# <span data-ttu-id="07771-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="07771-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="07771-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07771-102">SYNOPSIS</span></span>
<span data-ttu-id="07771-103">Obtém ou lista grupos de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="07771-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="07771-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07771-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07771-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07771-105">DESCRIPTION</span></span>
<span data-ttu-id="07771-106">Obtém um grupo de failover de instância específica ou lista os grupos de failover de instância em uma região sob a assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="07771-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="07771-107">Qualquer região no grupo de failover de instância pode ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="07771-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="07771-108">Os valores retornados refletirão o estado das instâncias gerenciadas nessa região em relação ao grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="07771-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="07771-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07771-109">EXAMPLES</span></span>

### <span data-ttu-id="07771-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07771-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
    ResourceGroupName                     : rg
    Location                              : East US
    Name                                  : fg
    PartnerResourceGroupName              : rg
    PartnerRegion                         : West US
    PrimaryManagedInstanceName            : managedInstance1
    PartnerManagedInstanceName            : managedInstance2
    ReplicationRole                       : Primary
    ReplicationState                      : CATCH_UP
    ReadWriteFailoverPolicy               : Automatic
    FailoverWithDataLossGracePeriodHours  : 1
    ReadOnlyFailoverPolicy                : Disabled
    Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
}
```

<span data-ttu-id="07771-111">Lista todos os grupos de failover na região</span><span class="sxs-lookup"><span data-stu-id="07771-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="07771-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="07771-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="07771-113">Obter um grupo de failover de instância específico.</span><span class="sxs-lookup"><span data-stu-id="07771-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="07771-114">OS</span><span class="sxs-lookup"><span data-stu-id="07771-114">PARAMETERS</span></span>

### <span data-ttu-id="07771-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07771-115">-DefaultProfile</span></span>
<span data-ttu-id="07771-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07771-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07771-117">-Local</span><span class="sxs-lookup"><span data-stu-id="07771-117">-Location</span></span>
<span data-ttu-id="07771-118">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="07771-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07771-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="07771-119">-Name</span></span>
<span data-ttu-id="07771-120">O nome do grupo de failover de instância a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="07771-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07771-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07771-121">-ResourceGroupName</span></span>
<span data-ttu-id="07771-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="07771-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07771-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07771-123">CommonParameters</span></span>
<span data-ttu-id="07771-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07771-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07771-125">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07771-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07771-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07771-126">INPUTS</span></span>

### <span data-ttu-id="07771-127">System. String</span><span class="sxs-lookup"><span data-stu-id="07771-127">System.String</span></span>

## <span data-ttu-id="07771-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07771-128">OUTPUTS</span></span>

### <span data-ttu-id="07771-129">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="07771-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="07771-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07771-130">NOTES</span></span>

## <span data-ttu-id="07771-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07771-131">RELATED LINKS</span></span>
