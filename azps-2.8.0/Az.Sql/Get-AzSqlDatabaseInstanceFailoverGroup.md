---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: dbb0cb56c50025e6b257d801957b1a75479220f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773669"
---
# <span data-ttu-id="8d586-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8d586-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="8d586-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d586-102">SYNOPSIS</span></span>
<span data-ttu-id="8d586-103">Obtém ou lista grupos de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="8d586-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="8d586-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d586-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d586-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d586-105">DESCRIPTION</span></span>
<span data-ttu-id="8d586-106">Obtém um grupo de failover de instância específica ou lista os grupos de failover de instância em uma região sob a assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d586-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="8d586-107">Qualquer região no grupo de failover de instância pode ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="8d586-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="8d586-108">Os valores retornados refletirão o estado das instâncias gerenciadas nessa região em relação ao grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="8d586-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="8d586-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d586-109">EXAMPLES</span></span>

### <span data-ttu-id="8d586-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8d586-110">Example 1</span></span>
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

<span data-ttu-id="8d586-111">Lista todos os grupos de failover na região</span><span class="sxs-lookup"><span data-stu-id="8d586-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="8d586-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8d586-112">Example 2</span></span>
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

<span data-ttu-id="8d586-113">Obter um grupo de failover de instância específico.</span><span class="sxs-lookup"><span data-stu-id="8d586-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="8d586-114">OS</span><span class="sxs-lookup"><span data-stu-id="8d586-114">PARAMETERS</span></span>

### <span data-ttu-id="8d586-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d586-115">-DefaultProfile</span></span>
<span data-ttu-id="8d586-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d586-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d586-117">-Local</span><span class="sxs-lookup"><span data-stu-id="8d586-117">-Location</span></span>
<span data-ttu-id="8d586-118">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="8d586-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d586-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d586-119">-Name</span></span>
<span data-ttu-id="8d586-120">O nome do grupo de failover de instância a ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="8d586-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d586-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d586-121">-ResourceGroupName</span></span>
<span data-ttu-id="8d586-122">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d586-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d586-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d586-123">CommonParameters</span></span>
<span data-ttu-id="8d586-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d586-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d586-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d586-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d586-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d586-126">INPUTS</span></span>

### <span data-ttu-id="8d586-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8d586-127">System.String</span></span>

## <span data-ttu-id="8d586-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d586-128">OUTPUTS</span></span>

### <span data-ttu-id="8d586-129">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8d586-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="8d586-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d586-130">NOTES</span></span>

## <span data-ttu-id="8d586-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d586-131">RELATED LINKS</span></span>
