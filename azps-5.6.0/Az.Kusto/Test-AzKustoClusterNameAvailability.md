---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: dcc402b2db390403a6106953b3ecbdd6cc52a2b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885708"
---
# <span data-ttu-id="de968-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="de968-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="de968-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de968-102">SYNOPSIS</span></span>
<span data-ttu-id="de968-103">Verifica se o nome do cluster é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="de968-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="de968-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="de968-104">SYNTAX</span></span>

### <span data-ttu-id="de968-105">CheckExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="de968-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="de968-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="de968-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de968-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="de968-107">DESCRIPTION</span></span>
<span data-ttu-id="de968-108">Verifica se o nome do cluster é válido e ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="de968-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="de968-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="de968-109">EXAMPLES</span></span>

### <span data-ttu-id="de968-110">Exemplo 1: verificar a disponibilidade de um nome de cluster kusto que está em uso</span><span class="sxs-lookup"><span data-stu-id="de968-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="de968-111">O comando acima retorna se existe ou não um cluster Kusto chamado "testnewkustocluster" na região "East US".</span><span class="sxs-lookup"><span data-stu-id="de968-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="de968-112">Exemplo 2: Verifique a disponibilidade de um nome de cluster Kusto que não está em uso</span><span class="sxs-lookup"><span data-stu-id="de968-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="de968-113">O comando acima retorna se existe ou não um cluster Kusto chamado "availablekustocluster" na região "East US".</span><span class="sxs-lookup"><span data-stu-id="de968-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="de968-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="de968-114">PARAMETERS</span></span>

### <span data-ttu-id="de968-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de968-115">-DefaultProfile</span></span>
<span data-ttu-id="de968-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="de968-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de968-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de968-117">-InputObject</span></span>
<span data-ttu-id="de968-118">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="de968-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="de968-119">-Location</span><span class="sxs-lookup"><span data-stu-id="de968-119">-Location</span></span>
<span data-ttu-id="de968-120">Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="de968-120">Azure location.</span></span>

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

### <span data-ttu-id="de968-121">-Name</span><span class="sxs-lookup"><span data-stu-id="de968-121">-Name</span></span>
<span data-ttu-id="de968-122">Nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="de968-122">Cluster name.</span></span>

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

### <span data-ttu-id="de968-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de968-123">-SubscriptionId</span></span>
<span data-ttu-id="de968-124">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="de968-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="de968-125">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="de968-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="de968-126">-Type</span><span class="sxs-lookup"><span data-stu-id="de968-126">-Type</span></span>
<span data-ttu-id="de968-127">O tipo de recurso, Microsoft.Kusto/clusters.</span><span class="sxs-lookup"><span data-stu-id="de968-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="de968-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de968-128">-Confirm</span></span>
<span data-ttu-id="de968-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de968-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de968-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de968-130">-WhatIf</span></span>
<span data-ttu-id="de968-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="de968-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de968-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="de968-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de968-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de968-133">CommonParameters</span></span>
<span data-ttu-id="de968-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de968-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de968-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de968-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de968-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="de968-136">INPUTS</span></span>

### <span data-ttu-id="de968-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="de968-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="de968-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="de968-138">OUTPUTS</span></span>

### <span data-ttu-id="de968-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="de968-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="de968-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="de968-140">NOTES</span></span>

<span data-ttu-id="de968-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="de968-141">ALIASES</span></span>

<span data-ttu-id="de968-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="de968-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="de968-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="de968-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de968-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="de968-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="de968-145">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="de968-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="de968-146">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="de968-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="de968-147">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="de968-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="de968-148">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="de968-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="de968-149">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="de968-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="de968-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="de968-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="de968-151">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="de968-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="de968-152">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="de968-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="de968-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="de968-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="de968-154">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="de968-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="de968-155">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="de968-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="de968-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="de968-156">RELATED LINKS</span></span>

