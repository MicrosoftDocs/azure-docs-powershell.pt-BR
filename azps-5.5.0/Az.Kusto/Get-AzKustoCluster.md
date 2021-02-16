---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 99afad24d33cfd6a614100b5bc53406f04965ba9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113039"
---
# <span data-ttu-id="49032-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="49032-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="49032-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="49032-102">SYNOPSIS</span></span>
<span data-ttu-id="49032-103">Obtém um cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="49032-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="49032-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49032-104">SYNTAX</span></span>

### <span data-ttu-id="49032-105">Lista1 (Padrão)</span><span class="sxs-lookup"><span data-stu-id="49032-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49032-106">Obter</span><span class="sxs-lookup"><span data-stu-id="49032-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49032-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="49032-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="49032-108">Lista</span><span class="sxs-lookup"><span data-stu-id="49032-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="49032-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="49032-109">DESCRIPTION</span></span>
<span data-ttu-id="49032-110">Obtém um cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="49032-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="49032-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="49032-111">EXAMPLES</span></span>

### <span data-ttu-id="49032-112">Exemplo 1: Listar todos os clusters kusto em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="49032-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="49032-113">O comando acima lista todos os clusters Kusto no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="49032-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="49032-114">Exemplo 2: Obter um cluster Kusto específico por nome</span><span class="sxs-lookup"><span data-stu-id="49032-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="49032-115">O comando acima retorna o cluster Kusto chamado "testnewkustocluster" no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="49032-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="49032-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49032-116">PARAMETERS</span></span>

### <span data-ttu-id="49032-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49032-117">-DefaultProfile</span></span>
<span data-ttu-id="49032-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="49032-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49032-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49032-119">-InputObject</span></span>
<span data-ttu-id="49032-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="49032-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="49032-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="49032-121">-Name</span></span>
<span data-ttu-id="49032-122">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="49032-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="49032-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49032-123">-ResourceGroupName</span></span>
<span data-ttu-id="49032-124">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="49032-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="49032-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="49032-125">-SubscriptionId</span></span>
<span data-ttu-id="49032-126">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49032-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="49032-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="49032-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="49032-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49032-128">CommonParameters</span></span>
<span data-ttu-id="49032-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49032-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49032-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49032-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49032-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="49032-131">INPUTS</span></span>

### <span data-ttu-id="49032-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="49032-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="49032-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="49032-133">OUTPUTS</span></span>

### <span data-ttu-id="49032-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="49032-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="49032-135">Notas</span><span class="sxs-lookup"><span data-stu-id="49032-135">NOTES</span></span>

<span data-ttu-id="49032-136">Aliases</span><span class="sxs-lookup"><span data-stu-id="49032-136">ALIASES</span></span>

<span data-ttu-id="49032-137">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="49032-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="49032-138">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="49032-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="49032-139">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="49032-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="49032-140">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="49032-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="49032-141">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="49032-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="49032-142">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="49032-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="49032-143">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="49032-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="49032-144">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="49032-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="49032-145">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="49032-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="49032-146">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="49032-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="49032-147">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="49032-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="49032-148">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="49032-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="49032-149">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="49032-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="49032-150">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="49032-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="49032-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="49032-151">RELATED LINKS</span></span>

