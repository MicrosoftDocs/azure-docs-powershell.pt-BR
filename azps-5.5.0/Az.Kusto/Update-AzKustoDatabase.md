---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: b7638780dc4fa360998d7d974d74c93ccd5c2afe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111821"
---
# <span data-ttu-id="767c2-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="767c2-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="767c2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="767c2-102">SYNOPSIS</span></span>
<span data-ttu-id="767c2-103">Atualiza um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="767c2-103">Updates a database.</span></span>

## <span data-ttu-id="767c2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="767c2-104">SYNTAX</span></span>

### <span data-ttu-id="767c2-105">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="767c2-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="767c2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="767c2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="767c2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="767c2-107">DESCRIPTION</span></span>
<span data-ttu-id="767c2-108">Atualiza um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="767c2-108">Updates a database.</span></span>

## <span data-ttu-id="767c2-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="767c2-109">EXAMPLES</span></span>

### <span data-ttu-id="767c2-110">Exemplo 1: Atualizar um banco de dados existente por nome</span><span class="sxs-lookup"><span data-stu-id="767c2-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="767c2-111">O comando acima atualiza o período de exclusão suave e o período de hot cache do banco de dados de Kusto "mykustodatabase" no cluster "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="767c2-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="767c2-112">Exemplo 2: Atualizar um banco de dados existente por meio de identidade</span><span class="sxs-lookup"><span data-stu-id="767c2-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="767c2-113">O comando acima atualiza o período de exclusão suave e o período de hot cache do banco de dados de Kusto "mykustodatabase" no cluster "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="767c2-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="767c2-114">Exemplo 3: Atualizar um banco de dados ReadOnly existente por nome</span><span class="sxs-lookup"><span data-stu-id="767c2-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="767c2-115">O comando acima atualiza o período de hot cache do banco de dados kusto "mykustodatabase" no cluster "myfollowercluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="767c2-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="767c2-116">Exemplo 4: Atualizar um banco de dados do ReadOnly existente por meio de identidade</span><span class="sxs-lookup"><span data-stu-id="767c2-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="767c2-117">O comando acima atualiza o período de hot cache do banco de dados kusto "mykustodatabase" no cluster "myfollowercluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="767c2-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="767c2-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="767c2-118">PARAMETERS</span></span>

### <span data-ttu-id="767c2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="767c2-119">-AsJob</span></span>
<span data-ttu-id="767c2-120">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="767c2-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="767c2-121">-ClusterName</span></span>
<span data-ttu-id="767c2-122">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="767c2-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="767c2-123">-DefaultProfile</span></span>
<span data-ttu-id="767c2-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="767c2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="767c2-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="767c2-125">-HotCachePeriod</span></span>
<span data-ttu-id="767c2-126">O tempo em que os dados devem ser mantidos em cache para consultas rápidas no TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="767c2-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="767c2-127">-InputObject</span></span>
<span data-ttu-id="767c2-128">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="767c2-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-129">-Tipo</span><span class="sxs-lookup"><span data-stu-id="767c2-129">-Kind</span></span>
<span data-ttu-id="767c2-130">Tipo de banco de dados</span><span class="sxs-lookup"><span data-stu-id="767c2-130">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-131">-Local</span><span class="sxs-lookup"><span data-stu-id="767c2-131">-Location</span></span>
<span data-ttu-id="767c2-132">Local do recurso.</span><span class="sxs-lookup"><span data-stu-id="767c2-132">Resource location.</span></span>

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

### <span data-ttu-id="767c2-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="767c2-133">-Name</span></span>
<span data-ttu-id="767c2-134">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="767c2-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="767c2-135">-NoWait</span></span>
<span data-ttu-id="767c2-136">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="767c2-136">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="767c2-137">-ResourceGroupName</span></span>
<span data-ttu-id="767c2-138">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="767c2-138">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="767c2-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="767c2-140">O tempo em que os dados devem ser mantidos antes de deixar de ser acessíveis para consultas no TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="767c2-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="767c2-141">-SubscriptionId</span></span>
<span data-ttu-id="767c2-142">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="767c2-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="767c2-143">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="767c2-143">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767c2-144">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="767c2-144">-Confirm</span></span>
<span data-ttu-id="767c2-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="767c2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="767c2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="767c2-146">-WhatIf</span></span>
<span data-ttu-id="767c2-147">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="767c2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="767c2-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="767c2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="767c2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="767c2-149">CommonParameters</span></span>
<span data-ttu-id="767c2-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="767c2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="767c2-151">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="767c2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="767c2-152">Entradas</span><span class="sxs-lookup"><span data-stu-id="767c2-152">INPUTS</span></span>

### <span data-ttu-id="767c2-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="767c2-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="767c2-154">Saídas</span><span class="sxs-lookup"><span data-stu-id="767c2-154">OUTPUTS</span></span>

### <span data-ttu-id="767c2-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="767c2-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="767c2-156">Notas</span><span class="sxs-lookup"><span data-stu-id="767c2-156">NOTES</span></span>

<span data-ttu-id="767c2-157">Aliases</span><span class="sxs-lookup"><span data-stu-id="767c2-157">ALIASES</span></span>

<span data-ttu-id="767c2-158">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="767c2-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="767c2-159">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="767c2-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="767c2-160">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="767c2-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="767c2-161">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="767c2-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="767c2-162">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="767c2-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="767c2-163">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="767c2-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="767c2-164">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="767c2-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="767c2-165">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="767c2-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="767c2-166">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="767c2-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="767c2-167">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="767c2-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="767c2-168">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="767c2-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="767c2-169">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="767c2-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="767c2-170">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="767c2-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="767c2-171">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="767c2-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="767c2-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="767c2-172">RELATED LINKS</span></span>

