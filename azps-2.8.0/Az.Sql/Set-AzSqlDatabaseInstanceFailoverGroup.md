---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 38e19e764e7a9d272db777a295f05016f0ef95af
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93773719"
---
# <span data-ttu-id="d025c-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d025c-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="d025c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d025c-102">SYNOPSIS</span></span>
<span data-ttu-id="d025c-103">Modifica a configuração de um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="d025c-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="d025c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d025c-104">SYNTAX</span></span>

### <span data-ttu-id="d025c-105">SetIFGDefault (padrão)</span><span class="sxs-lookup"><span data-stu-id="d025c-105">SetIFGDefault (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d025c-106">Definir um grupo de failover de instância da ID do recurso</span><span class="sxs-lookup"><span data-stu-id="d025c-106">Set a Instance Failover Group from Resource Id</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d025c-107">Definir um grupo de failover de instância da definição de instância AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d025c-107">Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup -InputObject <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d025c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d025c-108">DESCRIPTION</span></span>
<span data-ttu-id="d025c-109">Esse comando modifica a configuração de um grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="d025c-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="d025c-110">A região primária do grupo de failover de instância deve ser usada para executar o comando.</span><span class="sxs-lookup"><span data-stu-id="d025c-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="d025c-111">Durante a visualização do recurso de grupos de failover de instância, somente os valores maiores que ou iguais a 1 hora têm suporte para o parâmetro '-GracePeriodWithDataLossHours '.</span><span class="sxs-lookup"><span data-stu-id="d025c-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="d025c-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d025c-112">EXAMPLES</span></span>

### <span data-ttu-id="d025c-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d025c-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
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
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="d025c-114">Define a política de failover do grupo de failover de instância como ' manual ' por tubulação no grupo de failover.</span><span class="sxs-lookup"><span data-stu-id="d025c-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="d025c-115">OS</span><span class="sxs-lookup"><span data-stu-id="d025c-115">PARAMETERS</span></span>

### <span data-ttu-id="d025c-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="d025c-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="d025c-117">Se as paralisações no servidor secundário devem disparar o failover automático do ponto de extremidade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d025c-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="d025c-118">Este recurso ainda não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="d025c-118">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d025c-119">-DefaultProfile</span></span>
<span data-ttu-id="d025c-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d025c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d025c-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="d025c-121">-FailoverPolicy</span></span>
<span data-ttu-id="d025c-122">A política de failover do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="d025c-122">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="d025c-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="d025c-124">Intervalo antes do failover automático será iniciado se ocorrer uma falha no servidor primário e o failover não puder ser concluído sem perda de dados.</span><span class="sxs-lookup"><span data-stu-id="d025c-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d025c-125">-InputObject</span></span>
<span data-ttu-id="d025c-126">O objeto de grupo de failover de instância a ser definido</span><span class="sxs-lookup"><span data-stu-id="d025c-126">The Instance Failover Group object to set</span></span>

```yaml
Type: AzureSqlInstanceFailoverGroupModel
Parameter Sets: Set a Instance Failover Group from AzureSqlInstanceFailoverGroupModel instance definition
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-127">-Local</span><span class="sxs-lookup"><span data-stu-id="d025c-127">-Location</span></span>
<span data-ttu-id="d025c-128">O nome da região local a partir da qual recuperar o grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="d025c-128">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault, Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="d025c-129">-Name</span></span>
<span data-ttu-id="d025c-130">O nome do grupo de failover de instância.</span><span class="sxs-lookup"><span data-stu-id="d025c-130">The name of the Instance Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d025c-131">-ResourceGroupName</span></span>
<span data-ttu-id="d025c-132">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d025c-132">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetIFGDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d025c-133">-ResourceId</span></span>
<span data-ttu-id="d025c-134">A ID do recurso do grupo de failover de instância a ser definido.</span><span class="sxs-lookup"><span data-stu-id="d025c-134">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: String
Parameter Sets: Set a Instance Failover Group from Resource Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d025c-135">-Confirm</span></span>
<span data-ttu-id="d025c-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d025c-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d025c-137">-WhatIf</span></span>
<span data-ttu-id="d025c-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d025c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d025c-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d025c-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d025c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d025c-140">CommonParameters</span></span>
<span data-ttu-id="d025c-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d025c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d025c-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d025c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d025c-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d025c-143">INPUTS</span></span>

### <span data-ttu-id="d025c-144">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d025c-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="d025c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="d025c-145">System.String</span></span>

## <span data-ttu-id="d025c-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d025c-146">OUTPUTS</span></span>

### <span data-ttu-id="d025c-147">Microsoft. Azure. Commands. Sql. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d025c-147">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="d025c-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d025c-148">NOTES</span></span>

## <span data-ttu-id="d025c-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d025c-149">RELATED LINKS</span></span>
