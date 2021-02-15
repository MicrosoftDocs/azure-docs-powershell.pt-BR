---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 533e247ed2a0b9682e2fe87699d0a77b51ed06ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113021"
---
# <span data-ttu-id="531d4-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="531d4-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="531d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="531d4-102">SYNOPSIS</span></span>
<span data-ttu-id="531d4-103">Obtém um principal de banco de dados de cluster Kusto, Assignment.</span><span class="sxs-lookup"><span data-stu-id="531d4-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="531d4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="531d4-104">SYNTAX</span></span>

### <span data-ttu-id="531d4-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="531d4-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="531d4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="531d4-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="531d4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="531d4-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="531d4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="531d4-108">DESCRIPTION</span></span>
<span data-ttu-id="531d4-109">Obtém um principal de banco de dados de cluster Kusto, Assignment.</span><span class="sxs-lookup"><span data-stu-id="531d4-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="531d4-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="531d4-110">EXAMPLES</span></span>

### <span data-ttu-id="531d4-111">Exemplo 1: Listar todas as PrincipaisAssignação em um banco de dados por nome</span><span class="sxs-lookup"><span data-stu-id="531d4-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="531d4-112">O comando acima retorna todas as PrincipaisAssignment no banco de dados "mykustodatabase" encontrado no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="531d4-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="531d4-113">Exemplo 2: Obter um nome específico do PrincipalAssignment em um banco de dados</span><span class="sxs-lookup"><span data-stu-id="531d4-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="531d4-114">O comando acima retorna todos os PrincipaisAssignment chamados "kustoprincipal1" no banco de dados "mykustodatabase" encontrado no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="531d4-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="531d4-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="531d4-115">PARAMETERS</span></span>

### <span data-ttu-id="531d4-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="531d4-116">-ClusterName</span></span>
<span data-ttu-id="531d4-117">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="531d4-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="531d4-118">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="531d4-118">-DatabaseName</span></span>
<span data-ttu-id="531d4-119">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="531d4-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="531d4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531d4-120">-DefaultProfile</span></span>
<span data-ttu-id="531d4-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="531d4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="531d4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="531d4-122">-InputObject</span></span>
<span data-ttu-id="531d4-123">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="531d4-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="531d4-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="531d4-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="531d4-125">O nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="531d4-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="531d4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="531d4-126">-ResourceGroupName</span></span>
<span data-ttu-id="531d4-127">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="531d4-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="531d4-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="531d4-128">-SubscriptionId</span></span>
<span data-ttu-id="531d4-129">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="531d4-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="531d4-130">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="531d4-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="531d4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531d4-131">CommonParameters</span></span>
<span data-ttu-id="531d4-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="531d4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531d4-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="531d4-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531d4-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="531d4-134">INPUTS</span></span>

### <span data-ttu-id="531d4-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="531d4-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="531d4-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="531d4-136">OUTPUTS</span></span>

### <span data-ttu-id="531d4-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="531d4-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="531d4-138">Notas</span><span class="sxs-lookup"><span data-stu-id="531d4-138">NOTES</span></span>

<span data-ttu-id="531d4-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="531d4-139">ALIASES</span></span>

<span data-ttu-id="531d4-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="531d4-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="531d4-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="531d4-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="531d4-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="531d4-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="531d4-143">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="531d4-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="531d4-144">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="531d4-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="531d4-145">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="531d4-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="531d4-146">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="531d4-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="531d4-147">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="531d4-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="531d4-148">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="531d4-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="531d4-149">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="531d4-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="531d4-150">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="531d4-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="531d4-151">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="531d4-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="531d4-152">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="531d4-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="531d4-153">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="531d4-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="531d4-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="531d4-154">RELATED LINKS</span></span>

