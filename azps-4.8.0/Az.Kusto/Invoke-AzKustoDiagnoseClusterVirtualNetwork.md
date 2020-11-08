---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: 682de416a4aba61e1f287661c88faee9e20d248c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113552"
---
# <span data-ttu-id="9ce90-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9ce90-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="9ce90-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9ce90-102">SYNOPSIS</span></span>
<span data-ttu-id="9ce90-103">Diagnostica o status de conectividade de rede para recursos externos dos quais o serviço depende.</span><span class="sxs-lookup"><span data-stu-id="9ce90-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="9ce90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9ce90-104">SYNTAX</span></span>

### <span data-ttu-id="9ce90-105">Diagnosticar (padrão)</span><span class="sxs-lookup"><span data-stu-id="9ce90-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9ce90-106">DiagnoseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9ce90-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9ce90-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9ce90-107">DESCRIPTION</span></span>
<span data-ttu-id="9ce90-108">Diagnostica o status de conectividade de rede para recursos externos dos quais o serviço depende.</span><span class="sxs-lookup"><span data-stu-id="9ce90-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="9ce90-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9ce90-109">EXAMPLES</span></span>

### <span data-ttu-id="9ce90-110">Exemplo 1: mostrar o diagnóstico de conectividade de rede para recursos externos</span><span class="sxs-lookup"><span data-stu-id="9ce90-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="9ce90-111">O comando acima diagnostica o status de conectividade de rede para recursos externos nos quais o "testnewkustocluster" do cluster depende</span><span class="sxs-lookup"><span data-stu-id="9ce90-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="9ce90-112">OS</span><span class="sxs-lookup"><span data-stu-id="9ce90-112">PARAMETERS</span></span>

### <span data-ttu-id="9ce90-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ce90-113">-AsJob</span></span>
<span data-ttu-id="9ce90-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9ce90-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce90-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9ce90-115">-ClusterName</span></span>
<span data-ttu-id="9ce90-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ce90-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ce90-117">-DefaultProfile</span></span>
<span data-ttu-id="9ce90-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9ce90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ce90-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ce90-119">-InputObject</span></span>
<span data-ttu-id="9ce90-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="9ce90-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DiagnoseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ce90-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9ce90-121">-NoWait</span></span>
<span data-ttu-id="9ce90-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="9ce90-122">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ce90-123">-ResourceGroupName</span></span>
<span data-ttu-id="9ce90-124">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ce90-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce90-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9ce90-125">-SubscriptionId</span></span>
<span data-ttu-id="9ce90-126">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ce90-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9ce90-127">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ce90-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Diagnose
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ce90-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9ce90-128">-Confirm</span></span>
<span data-ttu-id="9ce90-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ce90-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ce90-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ce90-130">-WhatIf</span></span>
<span data-ttu-id="9ce90-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9ce90-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ce90-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9ce90-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ce90-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ce90-133">CommonParameters</span></span>
<span data-ttu-id="9ce90-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ce90-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ce90-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ce90-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ce90-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9ce90-136">INPUTS</span></span>

### <span data-ttu-id="9ce90-137">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9ce90-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9ce90-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9ce90-138">OUTPUTS</span></span>

### <span data-ttu-id="9ce90-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9ce90-139">System.String</span></span>

## <span data-ttu-id="9ce90-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9ce90-140">NOTES</span></span>

<span data-ttu-id="9ce90-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9ce90-141">ALIASES</span></span>

<span data-ttu-id="9ce90-142">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="9ce90-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9ce90-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="9ce90-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9ce90-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9ce90-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9ce90-145">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="9ce90-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9ce90-146">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="9ce90-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9ce90-147">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ce90-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9ce90-148">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="9ce90-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9ce90-149">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ce90-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9ce90-150">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="9ce90-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9ce90-151">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="9ce90-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9ce90-152">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ce90-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9ce90-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="9ce90-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9ce90-154">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9ce90-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9ce90-155">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="9ce90-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9ce90-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9ce90-156">RELATED LINKS</span></span>

