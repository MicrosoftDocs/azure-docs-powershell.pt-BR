---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: a39578ffb7a0f3a5ecc6abc873f659b5d170aff5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113026"
---
# <span data-ttu-id="71748-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="71748-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="71748-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71748-102">SYNOPSIS</span></span>
<span data-ttu-id="71748-103">Retorna um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71748-103">Returns a database.</span></span>

## <span data-ttu-id="71748-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71748-104">SYNTAX</span></span>

### <span data-ttu-id="71748-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="71748-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71748-106">Obter</span><span class="sxs-lookup"><span data-stu-id="71748-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="71748-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="71748-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="71748-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="71748-108">DESCRIPTION</span></span>
<span data-ttu-id="71748-109">Retorna um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="71748-109">Returns a database.</span></span>

## <span data-ttu-id="71748-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71748-110">EXAMPLES</span></span>

### <span data-ttu-id="71748-111">Exemplo 1: Listar todos os bancos de dados do Kusto em um cluster por nome</span><span class="sxs-lookup"><span data-stu-id="71748-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="71748-112">O comando acima retorna todos os bancos de dados do Kusto no cluster "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="71748-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="71748-113">Exemplo 2: Obter um banco de dados Kusto específico por nome</span><span class="sxs-lookup"><span data-stu-id="71748-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="71748-114">O comando acima retorna o banco de dados Kusto chamado "mykustodatabase" no cluster "testnewkustocluster" encontrado no grupo de recursos "testrg".</span><span class="sxs-lookup"><span data-stu-id="71748-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="71748-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71748-115">PARAMETERS</span></span>

### <span data-ttu-id="71748-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="71748-116">-ClusterName</span></span>
<span data-ttu-id="71748-117">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="71748-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="71748-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71748-118">-DefaultProfile</span></span>
<span data-ttu-id="71748-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71748-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71748-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71748-120">-InputObject</span></span>
<span data-ttu-id="71748-121">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="71748-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="71748-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="71748-122">-Name</span></span>
<span data-ttu-id="71748-123">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="71748-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="71748-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71748-124">-ResourceGroupName</span></span>
<span data-ttu-id="71748-125">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="71748-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="71748-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71748-126">-SubscriptionId</span></span>
<span data-ttu-id="71748-127">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="71748-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="71748-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="71748-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="71748-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71748-129">CommonParameters</span></span>
<span data-ttu-id="71748-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71748-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71748-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="71748-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71748-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="71748-132">INPUTS</span></span>

### <span data-ttu-id="71748-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="71748-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="71748-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="71748-134">OUTPUTS</span></span>

### <span data-ttu-id="71748-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="71748-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="71748-136">Notas</span><span class="sxs-lookup"><span data-stu-id="71748-136">NOTES</span></span>

<span data-ttu-id="71748-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="71748-137">ALIASES</span></span>

<span data-ttu-id="71748-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="71748-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71748-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="71748-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71748-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71748-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71748-141">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="71748-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71748-142">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="71748-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="71748-143">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="71748-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="71748-144">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="71748-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="71748-145">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="71748-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="71748-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="71748-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71748-147">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="71748-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="71748-148">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="71748-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="71748-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="71748-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="71748-150">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="71748-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="71748-151">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="71748-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="71748-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71748-152">RELATED LINKS</span></span>

