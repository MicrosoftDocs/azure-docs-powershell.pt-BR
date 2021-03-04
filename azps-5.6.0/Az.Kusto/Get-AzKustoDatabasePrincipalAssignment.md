---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 038db26826c4f3f37dcba42e1ccd435512ecd88b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889780"
---
# <span data-ttu-id="3d41b-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="3d41b-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="3d41b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d41b-102">SYNOPSIS</span></span>
<span data-ttu-id="3d41b-103">Obtém um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="3d41b-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="3d41b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3d41b-104">SYNTAX</span></span>

### <span data-ttu-id="3d41b-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3d41b-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d41b-106">Obter</span><span class="sxs-lookup"><span data-stu-id="3d41b-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3d41b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3d41b-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d41b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3d41b-108">DESCRIPTION</span></span>
<span data-ttu-id="3d41b-109">Obtém um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="3d41b-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="3d41b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3d41b-110">EXAMPLES</span></span>

### <span data-ttu-id="3d41b-111">Exemplo 1: Listar todos os PrincipaisAssignment em um banco de dados pelo nome</span><span class="sxs-lookup"><span data-stu-id="3d41b-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="3d41b-112">O comando acima retorna todos os PrincipaisAssignment no banco de dados "mykustodatabase" encontrado no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="3d41b-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="3d41b-113">Exemplo 2: Obter um PrincipalAssignment específico em um banco de dados pelo nome</span><span class="sxs-lookup"><span data-stu-id="3d41b-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="3d41b-114">O comando acima retorna todos os PrincipaisAssignment denominados "kustoprincipal1" no banco de dados "mykustodatabase" encontrado no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="3d41b-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="3d41b-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3d41b-115">PARAMETERS</span></span>

### <span data-ttu-id="3d41b-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3d41b-116">-ClusterName</span></span>
<span data-ttu-id="3d41b-117">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3d41b-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d41b-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3d41b-118">-DatabaseName</span></span>
<span data-ttu-id="3d41b-119">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3d41b-119">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d41b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d41b-120">-DefaultProfile</span></span>
<span data-ttu-id="3d41b-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3d41b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d41b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d41b-122">-InputObject</span></span>
<span data-ttu-id="3d41b-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3d41b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d41b-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="3d41b-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="3d41b-125">O nome da entidade KustoAssignment.</span><span class="sxs-lookup"><span data-stu-id="3d41b-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d41b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d41b-126">-ResourceGroupName</span></span>
<span data-ttu-id="3d41b-127">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3d41b-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d41b-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d41b-128">-SubscriptionId</span></span>
<span data-ttu-id="3d41b-129">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3d41b-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3d41b-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3d41b-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d41b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d41b-131">CommonParameters</span></span>
<span data-ttu-id="3d41b-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d41b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d41b-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d41b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d41b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d41b-134">INPUTS</span></span>

### <span data-ttu-id="3d41b-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3d41b-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3d41b-136">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3d41b-136">OUTPUTS</span></span>

### <span data-ttu-id="3d41b-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="3d41b-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="3d41b-138">NOTES</span><span class="sxs-lookup"><span data-stu-id="3d41b-138">NOTES</span></span>

<span data-ttu-id="3d41b-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3d41b-139">ALIASES</span></span>

<span data-ttu-id="3d41b-140">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="3d41b-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3d41b-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3d41b-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3d41b-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3d41b-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3d41b-143">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="3d41b-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3d41b-144">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="3d41b-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3d41b-145">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3d41b-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3d41b-146">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="3d41b-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3d41b-147">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3d41b-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3d41b-148">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3d41b-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3d41b-149">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="3d41b-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3d41b-150">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="3d41b-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3d41b-151">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3d41b-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3d41b-152">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3d41b-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3d41b-153">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3d41b-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3d41b-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3d41b-154">RELATED LINKS</span></span>

