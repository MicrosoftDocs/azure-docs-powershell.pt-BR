---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: d7dc3a154049e486490edddd5fbda52a552d32c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111826"
---
# <span data-ttu-id="679df-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="679df-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="679df-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="679df-102">SYNOPSIS</span></span>
<span data-ttu-id="679df-103">Verifica se o nome do cluster é válido e se ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="679df-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="679df-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="679df-104">SYNTAX</span></span>

### <span data-ttu-id="679df-105">CheckExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="679df-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="679df-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="679df-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="679df-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="679df-107">DESCRIPTION</span></span>
<span data-ttu-id="679df-108">Verifica se o nome do cluster é válido e se ainda não está em uso.</span><span class="sxs-lookup"><span data-stu-id="679df-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="679df-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="679df-109">EXAMPLES</span></span>

### <span data-ttu-id="679df-110">Exemplo 1: Verificar a disponibilidade de um nome de cluster Kusto que está em uso</span><span class="sxs-lookup"><span data-stu-id="679df-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="679df-111">O comando acima retorna se existe ou não um cluster Kusto chamado "testnewkustocluster" na região "Leste dos EUA".</span><span class="sxs-lookup"><span data-stu-id="679df-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="679df-112">Exemplo 2: Verificar a disponibilidade de um nome de cluster Kusto que não está em uso</span><span class="sxs-lookup"><span data-stu-id="679df-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="679df-113">O comando acima retorna se existe ou não um cluster Kusto chamado "availablekustocluster" na região "Leste dos EUA".</span><span class="sxs-lookup"><span data-stu-id="679df-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="679df-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="679df-114">PARAMETERS</span></span>

### <span data-ttu-id="679df-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679df-115">-DefaultProfile</span></span>
<span data-ttu-id="679df-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="679df-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="679df-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="679df-117">-InputObject</span></span>
<span data-ttu-id="679df-118">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="679df-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="679df-119">-Local</span><span class="sxs-lookup"><span data-stu-id="679df-119">-Location</span></span>
<span data-ttu-id="679df-120">Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="679df-120">Azure location.</span></span>

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

### <span data-ttu-id="679df-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="679df-121">-Name</span></span>
<span data-ttu-id="679df-122">Nome do cluster.</span><span class="sxs-lookup"><span data-stu-id="679df-122">Cluster name.</span></span>

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

### <span data-ttu-id="679df-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="679df-123">-SubscriptionId</span></span>
<span data-ttu-id="679df-124">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="679df-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="679df-125">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="679df-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="679df-126">-Tipo</span><span class="sxs-lookup"><span data-stu-id="679df-126">-Type</span></span>
<span data-ttu-id="679df-127">O tipo de recurso, Microsoft.Kusto/clusters.</span><span class="sxs-lookup"><span data-stu-id="679df-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="679df-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="679df-128">-Confirm</span></span>
<span data-ttu-id="679df-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="679df-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679df-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679df-130">-WhatIf</span></span>
<span data-ttu-id="679df-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="679df-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679df-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="679df-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679df-133">CommonParameters</span></span>
<span data-ttu-id="679df-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="679df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679df-135">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="679df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679df-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="679df-136">INPUTS</span></span>

### <span data-ttu-id="679df-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="679df-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="679df-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="679df-138">OUTPUTS</span></span>

### <span data-ttu-id="679df-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="679df-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="679df-140">Notas</span><span class="sxs-lookup"><span data-stu-id="679df-140">NOTES</span></span>

<span data-ttu-id="679df-141">Aliases</span><span class="sxs-lookup"><span data-stu-id="679df-141">ALIASES</span></span>

<span data-ttu-id="679df-142">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="679df-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="679df-143">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="679df-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="679df-144">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="679df-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="679df-145">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="679df-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="679df-146">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="679df-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="679df-147">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="679df-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="679df-148">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="679df-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="679df-149">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="679df-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="679df-150">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="679df-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="679df-151">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="679df-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="679df-152">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="679df-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="679df-153">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="679df-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="679df-154">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="679df-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="679df-155">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="679df-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="679df-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="679df-156">RELATED LINKS</span></span>

