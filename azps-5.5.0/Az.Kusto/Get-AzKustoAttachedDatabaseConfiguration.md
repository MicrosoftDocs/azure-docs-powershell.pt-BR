---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b1a042eb96c1fa6acbcc22fbdd33aefd9d4d46b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113040"
---
# <span data-ttu-id="a104e-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="a104e-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="a104e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a104e-102">SYNOPSIS</span></span>
<span data-ttu-id="a104e-103">Retorna uma configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="a104e-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="a104e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a104e-104">SYNTAX</span></span>

### <span data-ttu-id="a104e-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a104e-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a104e-106">Obter</span><span class="sxs-lookup"><span data-stu-id="a104e-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a104e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a104e-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a104e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a104e-108">DESCRIPTION</span></span>
<span data-ttu-id="a104e-109">Retorna uma configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="a104e-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="a104e-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a104e-110">EXAMPLES</span></span>

### <span data-ttu-id="a104e-111">Exemplo 1: Listar todas as AnexadasDatabaseConfigurações em um cluster</span><span class="sxs-lookup"><span data-stu-id="a104e-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="a104e-112">O comando acima lista todas as AttachedDatabaseConfigurações no cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="a104e-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="a104e-113">Exemplo 2: Obter uma Configuração AnexadaDatabase específica em um cluster</span><span class="sxs-lookup"><span data-stu-id="a104e-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="a104e-114">O comando acima retorna as AnexadasDatabaseConfigurações chamadas "myfollowerconfiguration" no cluster "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="a104e-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="a104e-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a104e-115">PARAMETERS</span></span>

### <span data-ttu-id="a104e-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a104e-116">-ClusterName</span></span>
<span data-ttu-id="a104e-117">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="a104e-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a104e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a104e-118">-DefaultProfile</span></span>
<span data-ttu-id="a104e-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a104e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a104e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a104e-120">-InputObject</span></span>
<span data-ttu-id="a104e-121">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="a104e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a104e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a104e-122">-Name</span></span>
<span data-ttu-id="a104e-123">O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="a104e-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a104e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a104e-124">-ResourceGroupName</span></span>
<span data-ttu-id="a104e-125">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="a104e-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a104e-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a104e-126">-SubscriptionId</span></span>
<span data-ttu-id="a104e-127">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a104e-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a104e-128">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a104e-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a104e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a104e-129">CommonParameters</span></span>
<span data-ttu-id="a104e-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a104e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a104e-131">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a104e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a104e-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="a104e-132">INPUTS</span></span>

### <span data-ttu-id="a104e-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a104e-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a104e-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="a104e-134">OUTPUTS</span></span>

### <span data-ttu-id="a104e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="a104e-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="a104e-136">Notas</span><span class="sxs-lookup"><span data-stu-id="a104e-136">NOTES</span></span>

<span data-ttu-id="a104e-137">Aliases</span><span class="sxs-lookup"><span data-stu-id="a104e-137">ALIASES</span></span>

<span data-ttu-id="a104e-138">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="a104e-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a104e-139">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a104e-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a104e-140">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a104e-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a104e-141">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="a104e-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a104e-142">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="a104e-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a104e-143">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="a104e-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a104e-144">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="a104e-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a104e-145">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="a104e-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a104e-146">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="a104e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a104e-147">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="a104e-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a104e-148">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="a104e-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a104e-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="a104e-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a104e-150">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a104e-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a104e-151">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a104e-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a104e-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a104e-152">RELATED LINKS</span></span>

