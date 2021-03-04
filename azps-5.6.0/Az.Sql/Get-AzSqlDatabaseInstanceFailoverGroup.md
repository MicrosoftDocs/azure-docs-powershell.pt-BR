---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 2b8ddc8b15ca9fa7322de231f9688548c4073708
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901423"
---
# <span data-ttu-id="189b2-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="189b2-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="189b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="189b2-102">SYNOPSIS</span></span>
<span data-ttu-id="189b2-103">Obtém ou lista Grupos de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="189b2-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="189b2-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="189b2-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="189b2-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="189b2-105">DESCRIPTION</span></span>
<span data-ttu-id="189b2-106">Obtém um Grupo de Failover de Instância específico ou lista os Grupos de Failover de Instância em uma região sob a assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="189b2-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="189b2-107">Qualquer região no Grupo de Failover de Instância pode ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="189b2-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="189b2-108">Os valores retornados refletirão o estado das Instâncias Gerenciadas nessa região em relação ao Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="189b2-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="189b2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="189b2-109">EXAMPLES</span></span>

### <span data-ttu-id="189b2-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="189b2-110">Example 1</span></span>
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

<span data-ttu-id="189b2-111">Lista todos os Grupos de Failover na região</span><span class="sxs-lookup"><span data-stu-id="189b2-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="189b2-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="189b2-112">Example 2</span></span>
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

<span data-ttu-id="189b2-113">Obter um Grupo de Failover de Instância específico.</span><span class="sxs-lookup"><span data-stu-id="189b2-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="189b2-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="189b2-114">PARAMETERS</span></span>

### <span data-ttu-id="189b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="189b2-115">-DefaultProfile</span></span>
<span data-ttu-id="189b2-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="189b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="189b2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="189b2-117">-Location</span></span>
<span data-ttu-id="189b2-118">O nome da Região Local da qual recuperar o Grupo de Failover de Instância.</span><span class="sxs-lookup"><span data-stu-id="189b2-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="189b2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="189b2-119">-Name</span></span>
<span data-ttu-id="189b2-120">O nome do Grupo de Failover de Instância a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="189b2-120">The name of the Instance Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="189b2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="189b2-121">-ResourceGroupName</span></span>
<span data-ttu-id="189b2-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="189b2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="189b2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="189b2-123">CommonParameters</span></span>
<span data-ttu-id="189b2-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="189b2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="189b2-125">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="189b2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="189b2-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="189b2-126">INPUTS</span></span>

### <span data-ttu-id="189b2-127">System.String</span><span class="sxs-lookup"><span data-stu-id="189b2-127">System.String</span></span>

## <span data-ttu-id="189b2-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="189b2-128">OUTPUTS</span></span>

### <span data-ttu-id="189b2-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="189b2-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="189b2-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="189b2-130">NOTES</span></span>

## <span data-ttu-id="189b2-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="189b2-131">RELATED LINKS</span></span>
