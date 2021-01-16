---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260915"
---
# <span data-ttu-id="41c86-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="41c86-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="41c86-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41c86-102">SYNOPSIS</span></span>
<span data-ttu-id="41c86-103">Obtém um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="41c86-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="41c86-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41c86-104">SYNTAX</span></span>

### <span data-ttu-id="41c86-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="41c86-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41c86-106">Obter</span><span class="sxs-lookup"><span data-stu-id="41c86-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="41c86-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41c86-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="41c86-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41c86-108">DESCRIPTION</span></span>
<span data-ttu-id="41c86-109">Obtém um banco de dados de cluster Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="41c86-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="41c86-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41c86-110">EXAMPLES</span></span>

### <span data-ttu-id="41c86-111">Exemplo 1: listar todos os PrincipalAssignment em um banco de dados por nome</span><span class="sxs-lookup"><span data-stu-id="41c86-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="41c86-112">O comando acima retorna todos os PrincipalAssignment no banco de dados "mykustodatabase" encontrado no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="41c86-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="41c86-113">Exemplo 2: obter um PrincipalAssignment específico em um banco de dados por nome</span><span class="sxs-lookup"><span data-stu-id="41c86-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="41c86-114">O comando acima retorna todos os PrincipalAssignment chamados "kustoprincipal1" no banco de dados "mykustodatabase" localizado no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="41c86-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="41c86-115">OS</span><span class="sxs-lookup"><span data-stu-id="41c86-115">PARAMETERS</span></span>

### <span data-ttu-id="41c86-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="41c86-116">-ClusterName</span></span>
<span data-ttu-id="41c86-117">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="41c86-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="41c86-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="41c86-118">-DatabaseName</span></span>
<span data-ttu-id="41c86-119">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="41c86-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="41c86-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c86-120">-DefaultProfile</span></span>
<span data-ttu-id="41c86-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41c86-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41c86-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41c86-122">-InputObject</span></span>
<span data-ttu-id="41c86-123">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="41c86-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="41c86-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="41c86-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="41c86-125">O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="41c86-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="41c86-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41c86-126">-ResourceGroupName</span></span>
<span data-ttu-id="41c86-127">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="41c86-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="41c86-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41c86-128">-SubscriptionId</span></span>
<span data-ttu-id="41c86-129">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="41c86-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="41c86-130">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="41c86-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="41c86-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c86-131">CommonParameters</span></span>
<span data-ttu-id="41c86-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c86-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c86-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41c86-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c86-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41c86-134">INPUTS</span></span>

### <span data-ttu-id="41c86-135">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="41c86-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="41c86-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41c86-136">OUTPUTS</span></span>

### <span data-ttu-id="41c86-137">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="41c86-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="41c86-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41c86-138">NOTES</span></span>

<span data-ttu-id="41c86-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="41c86-139">ALIASES</span></span>

<span data-ttu-id="41c86-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="41c86-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41c86-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="41c86-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41c86-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="41c86-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41c86-143">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="41c86-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41c86-144">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="41c86-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="41c86-145">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="41c86-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="41c86-146">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="41c86-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="41c86-147">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="41c86-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="41c86-148">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="41c86-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41c86-149">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="41c86-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="41c86-150">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="41c86-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="41c86-151">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="41c86-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="41c86-152">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="41c86-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="41c86-153">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="41c86-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="41c86-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41c86-154">RELATED LINKS</span></span>

