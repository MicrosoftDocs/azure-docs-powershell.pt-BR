---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257925"
---
# <span data-ttu-id="f2fcc-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="f2fcc-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="f2fcc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2fcc-102">SYNOPSIS</span></span>
<span data-ttu-id="f2fcc-103">Obtém um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="f2fcc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2fcc-104">SYNTAX</span></span>

### <span data-ttu-id="f2fcc-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="f2fcc-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2fcc-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f2fcc-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2fcc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2fcc-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f2fcc-108">Programação</span><span class="sxs-lookup"><span data-stu-id="f2fcc-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2fcc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2fcc-109">DESCRIPTION</span></span>
<span data-ttu-id="f2fcc-110">Obtém um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="f2fcc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2fcc-111">EXAMPLES</span></span>

### <span data-ttu-id="f2fcc-112">Exemplo 1: listar todos os clusters do Kusto em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f2fcc-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="f2fcc-113">O comando acima lista todos os clusters do Kusto no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="f2fcc-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="f2fcc-114">Exemplo 2: obter um cluster Kusto específico por nome</span><span class="sxs-lookup"><span data-stu-id="f2fcc-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="f2fcc-115">O comando acima retorna o cluster Kusto chamado "testnewkustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="f2fcc-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="f2fcc-116">OS</span><span class="sxs-lookup"><span data-stu-id="f2fcc-116">PARAMETERS</span></span>

### <span data-ttu-id="f2fcc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2fcc-117">-DefaultProfile</span></span>
<span data-ttu-id="f2fcc-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2fcc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2fcc-119">-InputObject</span></span>
<span data-ttu-id="f2fcc-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f2fcc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2fcc-121">-Name</span></span>
<span data-ttu-id="f2fcc-122">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2fcc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2fcc-123">-ResourceGroupName</span></span>
<span data-ttu-id="f2fcc-124">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f2fcc-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2fcc-125">-SubscriptionId</span></span>
<span data-ttu-id="f2fcc-126">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f2fcc-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2fcc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2fcc-128">CommonParameters</span></span>
<span data-ttu-id="f2fcc-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2fcc-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2fcc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2fcc-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2fcc-131">INPUTS</span></span>

### <span data-ttu-id="f2fcc-132">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f2fcc-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f2fcc-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2fcc-133">OUTPUTS</span></span>

### <span data-ttu-id="f2fcc-134">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="f2fcc-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="f2fcc-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2fcc-135">NOTES</span></span>

<span data-ttu-id="f2fcc-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f2fcc-136">ALIASES</span></span>

<span data-ttu-id="f2fcc-137">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f2fcc-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2fcc-138">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2fcc-139">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2fcc-140">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f2fcc-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2fcc-141">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f2fcc-142">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f2fcc-143">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f2fcc-144">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f2fcc-145">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f2fcc-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2fcc-146">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f2fcc-147">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f2fcc-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f2fcc-149">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f2fcc-150">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f2fcc-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f2fcc-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2fcc-151">RELATED LINKS</span></span>

