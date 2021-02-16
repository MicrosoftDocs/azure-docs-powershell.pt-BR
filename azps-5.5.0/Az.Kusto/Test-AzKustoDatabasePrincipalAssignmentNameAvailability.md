---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: b4a670046403aafb4b40740c34f27d7c81bcf8e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117584"
---
# <span data-ttu-id="4e35c-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="4e35c-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="4e35c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4e35c-102">SYNOPSIS</span></span>
<span data-ttu-id="4e35c-103">Verifica se a atribuição principal do banco de dados é válida e se ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="4e35c-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="4e35c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4e35c-104">SYNTAX</span></span>

### <span data-ttu-id="4e35c-105">CheckExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4e35c-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e35c-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4e35c-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e35c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e35c-107">DESCRIPTION</span></span>
<span data-ttu-id="4e35c-108">Verifica se a atribuição principal do banco de dados é válida e se ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="4e35c-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="4e35c-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4e35c-109">EXAMPLES</span></span>

### <span data-ttu-id="4e35c-110">Exemplo 1: Verificar a disponibilidade de um nome de nome de entidade de banco de dados que está em uso</span><span class="sxs-lookup"><span data-stu-id="4e35c-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="4e35c-111">O comando acima retorna se existe ou não um PrincipalAssignment chamado "myprincipal" no banco de dados "mykustodatabase" do cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="4e35c-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="4e35c-112">Exemplo 2: Verificar a disponibilidade de um nome de nome de entidade de banco de dados que não está em uso</span><span class="sxs-lookup"><span data-stu-id="4e35c-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="4e35c-113">O comando acima retorna se existe ou não um PrincipalAssignment chamado "myprincipal" no banco de dados "mykustodatabase" do cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="4e35c-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="4e35c-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e35c-114">PARAMETERS</span></span>

### <span data-ttu-id="4e35c-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4e35c-115">-ClusterName</span></span>
<span data-ttu-id="4e35c-116">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e35c-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4e35c-117">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="4e35c-117">-DatabaseName</span></span>
<span data-ttu-id="4e35c-118">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e35c-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="4e35c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e35c-119">-DefaultProfile</span></span>
<span data-ttu-id="4e35c-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4e35c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e35c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e35c-121">-InputObject</span></span>
<span data-ttu-id="4e35c-122">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4e35c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e35c-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e35c-123">-Name</span></span>
<span data-ttu-id="4e35c-124">Nome do recurso de Atribuição Principal.</span><span class="sxs-lookup"><span data-stu-id="4e35c-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="4e35c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e35c-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e35c-126">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e35c-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4e35c-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e35c-127">-SubscriptionId</span></span>
<span data-ttu-id="4e35c-128">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e35c-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e35c-129">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4e35c-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4e35c-130">-Tipo</span><span class="sxs-lookup"><span data-stu-id="4e35c-130">-Type</span></span>
<span data-ttu-id="4e35c-131">O tipo de recurso, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="4e35c-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="4e35c-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4e35c-132">-Confirm</span></span>
<span data-ttu-id="4e35c-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e35c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e35c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e35c-134">-WhatIf</span></span>
<span data-ttu-id="4e35c-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4e35c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e35c-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4e35c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e35c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e35c-137">CommonParameters</span></span>
<span data-ttu-id="4e35c-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e35c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e35c-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e35c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e35c-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="4e35c-140">INPUTS</span></span>

### <span data-ttu-id="4e35c-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="4e35c-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4e35c-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="4e35c-142">OUTPUTS</span></span>

### <span data-ttu-id="4e35c-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="4e35c-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="4e35c-144">Notas</span><span class="sxs-lookup"><span data-stu-id="4e35c-144">NOTES</span></span>

<span data-ttu-id="4e35c-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="4e35c-145">ALIASES</span></span>

<span data-ttu-id="4e35c-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4e35c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e35c-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4e35c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e35c-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e35c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e35c-149">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="4e35c-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e35c-150">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="4e35c-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4e35c-151">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e35c-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4e35c-152">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="4e35c-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4e35c-153">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e35c-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4e35c-154">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="4e35c-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e35c-155">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="4e35c-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4e35c-156">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="4e35c-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4e35c-157">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e35c-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4e35c-158">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e35c-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4e35c-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4e35c-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4e35c-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4e35c-160">RELATED LINKS</span></span>

