---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 6a151119552ab4b0e42d247641248dd110af4994
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887988"
---
# <span data-ttu-id="12809-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="12809-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="12809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12809-102">SYNOPSIS</span></span>
<span data-ttu-id="12809-103">Verifica se a atribuição principal do banco de dados é válida e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="12809-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="12809-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="12809-104">SYNTAX</span></span>

### <span data-ttu-id="12809-105">CheckExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="12809-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12809-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="12809-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12809-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="12809-107">DESCRIPTION</span></span>
<span data-ttu-id="12809-108">Verifica se a atribuição principal do banco de dados é válida e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="12809-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="12809-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12809-109">EXAMPLES</span></span>

### <span data-ttu-id="12809-110">Exemplo 1: Verificar a disponibilidade de um nome de entidade de banco de dados que está em uso</span><span class="sxs-lookup"><span data-stu-id="12809-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="12809-111">O comando acima retorna se existe ou não um PrincipalAssignment chamado "myprincipal" no banco de dados "mykustodatabase" do cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="12809-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="12809-112">Exemplo 2: Verifique a disponibilidade de um nome de entidade de banco de dados que não está em uso</span><span class="sxs-lookup"><span data-stu-id="12809-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="12809-113">O comando acima retorna se existe ou não um PrincipalAssignment chamado "myprincipal" no banco de dados "mykustodatabase" do cluster "testnewkustocluster" .</span><span class="sxs-lookup"><span data-stu-id="12809-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="12809-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="12809-114">PARAMETERS</span></span>

### <span data-ttu-id="12809-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="12809-115">-ClusterName</span></span>
<span data-ttu-id="12809-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="12809-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="12809-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="12809-117">-DatabaseName</span></span>
<span data-ttu-id="12809-118">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="12809-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="12809-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12809-119">-DefaultProfile</span></span>
<span data-ttu-id="12809-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12809-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12809-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12809-121">-InputObject</span></span>
<span data-ttu-id="12809-122">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="12809-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="12809-123">-Name</span><span class="sxs-lookup"><span data-stu-id="12809-123">-Name</span></span>
<span data-ttu-id="12809-124">Nome do recurso Atribuição Principal.</span><span class="sxs-lookup"><span data-stu-id="12809-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="12809-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12809-125">-ResourceGroupName</span></span>
<span data-ttu-id="12809-126">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="12809-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="12809-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12809-127">-SubscriptionId</span></span>
<span data-ttu-id="12809-128">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12809-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="12809-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="12809-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="12809-130">-Type</span><span class="sxs-lookup"><span data-stu-id="12809-130">-Type</span></span>
<span data-ttu-id="12809-131">O tipo de recurso, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="12809-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="12809-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12809-132">-Confirm</span></span>
<span data-ttu-id="12809-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12809-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12809-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12809-134">-WhatIf</span></span>
<span data-ttu-id="12809-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12809-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12809-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12809-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12809-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12809-137">CommonParameters</span></span>
<span data-ttu-id="12809-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12809-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12809-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12809-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12809-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12809-140">INPUTS</span></span>

### <span data-ttu-id="12809-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="12809-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="12809-142">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="12809-142">OUTPUTS</span></span>

### <span data-ttu-id="12809-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="12809-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="12809-144">NOTES</span><span class="sxs-lookup"><span data-stu-id="12809-144">NOTES</span></span>

<span data-ttu-id="12809-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="12809-145">ALIASES</span></span>

<span data-ttu-id="12809-146">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="12809-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12809-147">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="12809-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12809-148">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12809-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12809-149">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="12809-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12809-150">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="12809-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="12809-151">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="12809-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="12809-152">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="12809-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="12809-153">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="12809-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="12809-154">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="12809-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12809-155">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="12809-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="12809-156">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="12809-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="12809-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="12809-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="12809-158">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12809-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="12809-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="12809-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="12809-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12809-160">RELATED LINKS</span></span>

