---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: ab15d7a9da10e7e7a024d3af332f449cd011a290
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98264203"
---
# <span data-ttu-id="5fa04-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="5fa04-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="5fa04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fa04-102">SYNOPSIS</span></span>
<span data-ttu-id="5fa04-103">Verifica se o nome do banco de dados é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="5fa04-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="5fa04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fa04-104">SYNTAX</span></span>

### <span data-ttu-id="5fa04-105">CheckExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="5fa04-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="5fa04-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5fa04-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5fa04-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fa04-107">DESCRIPTION</span></span>
<span data-ttu-id="5fa04-108">Verifica se o nome do banco de dados é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="5fa04-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="5fa04-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fa04-109">EXAMPLES</span></span>

### <span data-ttu-id="5fa04-110">Exemplo 1: verificar a disponibilidade de um nome de banco de dados do Kusto que está em uso</span><span class="sxs-lookup"><span data-stu-id="5fa04-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="5fa04-111">O comando acima retorna se um banco de dados Kusto chamado "mykustodatabase" existe ou não no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="5fa04-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="5fa04-112">Exemplo 2: verificar a disponibilidade de um nome de banco de dados do Kusto que não está em uso</span><span class="sxs-lookup"><span data-stu-id="5fa04-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="5fa04-113">O comando acima retorna se um banco de dados Kusto chamado "mykustodatabase2" existe ou não no cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="5fa04-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="5fa04-114">OS</span><span class="sxs-lookup"><span data-stu-id="5fa04-114">PARAMETERS</span></span>

### <span data-ttu-id="5fa04-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5fa04-115">-ClusterName</span></span>
<span data-ttu-id="5fa04-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5fa04-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="5fa04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fa04-117">-DefaultProfile</span></span>
<span data-ttu-id="5fa04-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fa04-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fa04-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fa04-119">-InputObject</span></span>
<span data-ttu-id="5fa04-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="5fa04-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5fa04-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fa04-121">-Name</span></span>
<span data-ttu-id="5fa04-122">Nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="5fa04-122">Resource name.</span></span>

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

### <span data-ttu-id="5fa04-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fa04-123">-ResourceGroupName</span></span>
<span data-ttu-id="5fa04-124">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5fa04-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="5fa04-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fa04-125">-SubscriptionId</span></span>
<span data-ttu-id="5fa04-126">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5fa04-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5fa04-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="5fa04-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5fa04-128">-Digite</span><span class="sxs-lookup"><span data-stu-id="5fa04-128">-Type</span></span>
<span data-ttu-id="5fa04-129">O tipo de recurso, por exemplo, Microsoft. Kusto/clusters/bancos de dados.</span><span class="sxs-lookup"><span data-stu-id="5fa04-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="5fa04-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5fa04-130">-Confirm</span></span>
<span data-ttu-id="5fa04-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fa04-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fa04-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fa04-132">-WhatIf</span></span>
<span data-ttu-id="5fa04-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5fa04-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fa04-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fa04-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fa04-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fa04-135">CommonParameters</span></span>
<span data-ttu-id="5fa04-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fa04-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fa04-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fa04-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fa04-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fa04-138">INPUTS</span></span>

### <span data-ttu-id="5fa04-139">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="5fa04-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="5fa04-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fa04-140">OUTPUTS</span></span>

### <span data-ttu-id="5fa04-141">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="5fa04-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="5fa04-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fa04-142">NOTES</span></span>

<span data-ttu-id="5fa04-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="5fa04-143">ALIASES</span></span>

<span data-ttu-id="5fa04-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="5fa04-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5fa04-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="5fa04-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5fa04-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5fa04-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5fa04-147">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="5fa04-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5fa04-148">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="5fa04-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="5fa04-149">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5fa04-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="5fa04-150">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="5fa04-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="5fa04-151">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5fa04-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="5fa04-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="5fa04-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5fa04-153">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="5fa04-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="5fa04-154">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="5fa04-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="5fa04-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="5fa04-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="5fa04-156">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5fa04-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5fa04-157">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="5fa04-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5fa04-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fa04-158">RELATED LINKS</span></span>

