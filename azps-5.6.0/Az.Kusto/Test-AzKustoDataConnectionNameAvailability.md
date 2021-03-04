---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: b33f496845cf03a31a90203d5a4d10076d156e59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892631"
---
# <span data-ttu-id="a482c-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="a482c-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="a482c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a482c-102">SYNOPSIS</span></span>
<span data-ttu-id="a482c-103">Verifica se o nome da conexão de dados é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="a482c-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="a482c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a482c-104">SYNTAX</span></span>

### <span data-ttu-id="a482c-105">CheckExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a482c-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a482c-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a482c-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a482c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a482c-107">DESCRIPTION</span></span>
<span data-ttu-id="a482c-108">Verifica se o nome da conexão de dados é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="a482c-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="a482c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a482c-109">EXAMPLES</span></span>

### <span data-ttu-id="a482c-110">Exemplo 1: Verificar a disponibilidade de um nome de conexão de dados que está em uso</span><span class="sxs-lookup"><span data-stu-id="a482c-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="a482c-111">O comando acima retorna se existe ou não uma Conexão de Dados chamada "mykustodataconnection" no banco de dados "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="a482c-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="a482c-112">Exemplo 2: Verifique a disponibilidade de um nome de conexão de dados que não está em uso</span><span class="sxs-lookup"><span data-stu-id="a482c-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="a482c-113">O comando acima retorna se existe ou não uma Conexão de Dados chamada "mydataconnection" no banco de dados "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="a482c-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="a482c-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a482c-114">PARAMETERS</span></span>

### <span data-ttu-id="a482c-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a482c-115">-ClusterName</span></span>
<span data-ttu-id="a482c-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a482c-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a482c-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a482c-117">-DatabaseName</span></span>
<span data-ttu-id="a482c-118">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a482c-118">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a482c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a482c-119">-DefaultProfile</span></span>
<span data-ttu-id="a482c-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a482c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a482c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a482c-121">-InputObject</span></span>
<span data-ttu-id="a482c-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a482c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a482c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a482c-123">-Name</span></span>
<span data-ttu-id="a482c-124">Nome da Conexão de Dados.</span><span class="sxs-lookup"><span data-stu-id="a482c-124">Data Connection name.</span></span>

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

### <span data-ttu-id="a482c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a482c-125">-ResourceGroupName</span></span>
<span data-ttu-id="a482c-126">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a482c-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a482c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a482c-127">-SubscriptionId</span></span>
<span data-ttu-id="a482c-128">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a482c-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a482c-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a482c-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a482c-130">-Type</span><span class="sxs-lookup"><span data-stu-id="a482c-130">-Type</span></span>
<span data-ttu-id="a482c-131">O tipo de recurso, Microsoft.Kusto/Clusters/Databases/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="a482c-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a482c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a482c-132">-Confirm</span></span>
<span data-ttu-id="a482c-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a482c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a482c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a482c-134">-WhatIf</span></span>
<span data-ttu-id="a482c-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a482c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a482c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a482c-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a482c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a482c-137">CommonParameters</span></span>
<span data-ttu-id="a482c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a482c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a482c-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a482c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a482c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a482c-140">INPUTS</span></span>

### <span data-ttu-id="a482c-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a482c-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a482c-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a482c-142">OUTPUTS</span></span>

### <span data-ttu-id="a482c-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="a482c-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="a482c-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="a482c-144">NOTES</span></span>

<span data-ttu-id="a482c-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a482c-145">ALIASES</span></span>

<span data-ttu-id="a482c-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a482c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a482c-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a482c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a482c-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a482c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a482c-149">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="a482c-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a482c-150">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="a482c-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a482c-151">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a482c-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a482c-152">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="a482c-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a482c-153">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a482c-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a482c-154">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="a482c-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a482c-155">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="a482c-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a482c-156">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a482c-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a482c-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="a482c-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a482c-158">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a482c-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a482c-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a482c-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a482c-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a482c-160">RELATED LINKS</span></span>

