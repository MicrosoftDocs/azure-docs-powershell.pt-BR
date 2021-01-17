---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: a39578ffb7a0f3a5ecc6abc873f659b5d170aff5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427162"
---
# <span data-ttu-id="f36c4-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="f36c4-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="f36c4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f36c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f36c4-103">Retorna um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f36c4-103">Returns a database.</span></span>

## <span data-ttu-id="f36c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f36c4-104">SYNTAX</span></span>

### <span data-ttu-id="f36c4-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="f36c4-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f36c4-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f36c4-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f36c4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f36c4-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f36c4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f36c4-108">DESCRIPTION</span></span>
<span data-ttu-id="f36c4-109">Retorna um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f36c4-109">Returns a database.</span></span>

## <span data-ttu-id="f36c4-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f36c4-110">EXAMPLES</span></span>

### <span data-ttu-id="f36c4-111">Exemplo 1: listar todos os bancos de dados do Kusto em um cluster por nome</span><span class="sxs-lookup"><span data-stu-id="f36c4-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="f36c4-112">O comando acima retorna todos os bancos de dados do Kusto no cluster "testnewkustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="f36c4-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="f36c4-113">Exemplo 2: obter um banco de dados Kusto específico por nome</span><span class="sxs-lookup"><span data-stu-id="f36c4-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="f36c4-114">O comando acima retorna o banco de dados Kusto chamado "mykustodatabase" no cluster "testnewkustocluster" localizado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="f36c4-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="f36c4-115">OS</span><span class="sxs-lookup"><span data-stu-id="f36c4-115">PARAMETERS</span></span>

### <span data-ttu-id="f36c4-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f36c4-116">-ClusterName</span></span>
<span data-ttu-id="f36c4-117">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f36c4-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f36c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36c4-118">-DefaultProfile</span></span>
<span data-ttu-id="f36c4-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f36c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f36c4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f36c4-120">-InputObject</span></span>
<span data-ttu-id="f36c4-121">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f36c4-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f36c4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="f36c4-122">-Name</span></span>
<span data-ttu-id="f36c4-123">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f36c4-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f36c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="f36c4-125">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f36c4-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f36c4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f36c4-126">-SubscriptionId</span></span>
<span data-ttu-id="f36c4-127">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f36c4-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f36c4-128">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f36c4-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f36c4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36c4-129">CommonParameters</span></span>
<span data-ttu-id="f36c4-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f36c4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36c4-131">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f36c4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36c4-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f36c4-132">INPUTS</span></span>

### <span data-ttu-id="f36c4-133">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f36c4-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f36c4-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f36c4-134">OUTPUTS</span></span>

### <span data-ttu-id="f36c4-135">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200918. IDatabase</span><span class="sxs-lookup"><span data-stu-id="f36c4-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="f36c4-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f36c4-136">NOTES</span></span>

<span data-ttu-id="f36c4-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f36c4-137">ALIASES</span></span>

<span data-ttu-id="f36c4-138">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f36c4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f36c4-139">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f36c4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f36c4-140">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f36c4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f36c4-141">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f36c4-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f36c4-142">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="f36c4-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f36c4-143">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f36c4-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f36c4-144">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="f36c4-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f36c4-145">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f36c4-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f36c4-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f36c4-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f36c4-147">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="f36c4-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f36c4-148">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="f36c4-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f36c4-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f36c4-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f36c4-150">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f36c4-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f36c4-151">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f36c4-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f36c4-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f36c4-152">RELATED LINKS</span></span>

