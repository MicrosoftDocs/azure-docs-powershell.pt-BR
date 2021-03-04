---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodiagnoseclustervirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDiagnoseClusterVirtualNetwork.md
ms.openlocfilehash: d2530404774c3cb735dedb6eb233979fe602fe4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893158"
---
# <span data-ttu-id="3ad7f-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3ad7f-101">Invoke-AzKustoDiagnoseClusterVirtualNetwork</span></span>

## <span data-ttu-id="3ad7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ad7f-102">SYNOPSIS</span></span>
<span data-ttu-id="3ad7f-103">Diagnostica o status de conectividade de rede para recursos externos dos quais o serviço depende.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-103">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="3ad7f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ad7f-104">SYNTAX</span></span>

### <span data-ttu-id="3ad7f-105">Diagnóstico (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3ad7f-105">Diagnose (Default)</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3ad7f-106">DiagnosticViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3ad7f-106">DiagnoseViaIdentity</span></span>
```
Invoke-AzKustoDiagnoseClusterVirtualNetwork -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ad7f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ad7f-107">DESCRIPTION</span></span>
<span data-ttu-id="3ad7f-108">Diagnostica o status de conectividade de rede para recursos externos dos quais o serviço depende.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-108">Diagnoses network connectivity status for external resources on which the service is dependent on.</span></span>

## <span data-ttu-id="3ad7f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ad7f-109">EXAMPLES</span></span>

### <span data-ttu-id="3ad7f-110">Exemplo 1: Mostrar diagnóstico de conectividade de rede para recursos externos</span><span class="sxs-lookup"><span data-stu-id="3ad7f-110">Example 1: Show network connectivity diagnosis for external resources</span></span> 
```powershell
PS C:\> Invoke-AzKustoDiagnoseClusterVirtualNetwork -ResourceGroupName "testrg" -ClusterName "testnewkustocluster"

```

<span data-ttu-id="3ad7f-111">O comando acima diagnostica o status de conectividade de rede para recursos externos nos quais o cluster "testnewkustocluster" depende</span><span class="sxs-lookup"><span data-stu-id="3ad7f-111">The above command diagnoses network connectivity status for external resources on which the cluster "testnewkustocluster" is dependent on</span></span>

## <span data-ttu-id="3ad7f-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ad7f-112">PARAMETERS</span></span>

### <span data-ttu-id="3ad7f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ad7f-113">-AsJob</span></span>
<span data-ttu-id="3ad7f-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="3ad7f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="3ad7f-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="3ad7f-115">-ClusterName</span></span>
<span data-ttu-id="3ad7f-116">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="3ad7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ad7f-117">-DefaultProfile</span></span>
<span data-ttu-id="3ad7f-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ad7f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ad7f-119">-InputObject</span></span>
<span data-ttu-id="3ad7f-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ad7f-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3ad7f-121">-NoWait</span></span>
<span data-ttu-id="3ad7f-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="3ad7f-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3ad7f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ad7f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ad7f-124">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="3ad7f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ad7f-125">-SubscriptionId</span></span>
<span data-ttu-id="3ad7f-126">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3ad7f-127">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3ad7f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ad7f-128">-Confirm</span></span>
<span data-ttu-id="3ad7f-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ad7f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ad7f-130">-WhatIf</span></span>
<span data-ttu-id="3ad7f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ad7f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ad7f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ad7f-133">CommonParameters</span></span>
<span data-ttu-id="3ad7f-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ad7f-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ad7f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ad7f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ad7f-136">INPUTS</span></span>

### <span data-ttu-id="3ad7f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3ad7f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3ad7f-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ad7f-138">OUTPUTS</span></span>

### <span data-ttu-id="3ad7f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3ad7f-139">System.String</span></span>

## <span data-ttu-id="3ad7f-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ad7f-140">NOTES</span></span>

<span data-ttu-id="3ad7f-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3ad7f-141">ALIASES</span></span>

<span data-ttu-id="3ad7f-142">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="3ad7f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ad7f-143">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ad7f-144">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ad7f-145">INPUTOBJECT <IKustoIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="3ad7f-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ad7f-146">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3ad7f-147">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3ad7f-148">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3ad7f-149">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3ad7f-150">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="3ad7f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ad7f-151">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3ad7f-152">`[PrincipalAssignmentName <String>]`: O nome do Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3ad7f-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3ad7f-154">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3ad7f-155">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="3ad7f-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3ad7f-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ad7f-156">RELATED LINKS</span></span>

