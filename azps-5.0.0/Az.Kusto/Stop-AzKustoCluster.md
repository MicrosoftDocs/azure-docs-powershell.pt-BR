---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94126126"
---
# <span data-ttu-id="fe915-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="fe915-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="fe915-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe915-102">SYNOPSIS</span></span>
<span data-ttu-id="fe915-103">Interrompe um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fe915-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="fe915-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe915-104">SYNTAX</span></span>

### <span data-ttu-id="fe915-105">Parar (padrão)</span><span class="sxs-lookup"><span data-stu-id="fe915-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fe915-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fe915-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fe915-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe915-107">DESCRIPTION</span></span>
<span data-ttu-id="fe915-108">Interrompe um cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fe915-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="fe915-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe915-109">EXAMPLES</span></span>

### <span data-ttu-id="fe915-110">Exemplo 1: parar um cluster Kusto</span><span class="sxs-lookup"><span data-stu-id="fe915-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="fe915-111">O comando acima interrompe um cluster Kusto</span><span class="sxs-lookup"><span data-stu-id="fe915-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="fe915-112">OS</span><span class="sxs-lookup"><span data-stu-id="fe915-112">PARAMETERS</span></span>

### <span data-ttu-id="fe915-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe915-113">-AsJob</span></span>
<span data-ttu-id="fe915-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="fe915-114">Run the command as a job</span></span>

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

### <span data-ttu-id="fe915-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe915-115">-DefaultProfile</span></span>
<span data-ttu-id="fe915-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe915-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe915-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe915-117">-InputObject</span></span>
<span data-ttu-id="fe915-118">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="fe915-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe915-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe915-119">-Name</span></span>
<span data-ttu-id="fe915-120">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fe915-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe915-121">-Nowait</span><span class="sxs-lookup"><span data-stu-id="fe915-121">-NoWait</span></span>
<span data-ttu-id="fe915-122">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="fe915-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fe915-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe915-123">-PassThru</span></span>
<span data-ttu-id="fe915-124">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="fe915-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fe915-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe915-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe915-126">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fe915-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe915-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe915-127">-SubscriptionId</span></span>
<span data-ttu-id="fe915-128">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fe915-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fe915-129">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fe915-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe915-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe915-130">-Confirm</span></span>
<span data-ttu-id="fe915-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe915-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe915-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe915-132">-WhatIf</span></span>
<span data-ttu-id="fe915-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe915-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe915-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe915-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe915-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe915-135">CommonParameters</span></span>
<span data-ttu-id="fe915-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe915-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe915-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe915-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe915-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe915-138">INPUTS</span></span>

### <span data-ttu-id="fe915-139">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="fe915-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="fe915-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe915-140">OUTPUTS</span></span>

### <span data-ttu-id="fe915-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe915-141">System.Boolean</span></span>

## <span data-ttu-id="fe915-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe915-142">NOTES</span></span>

<span data-ttu-id="fe915-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fe915-143">ALIASES</span></span>

<span data-ttu-id="fe915-144">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="fe915-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fe915-145">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="fe915-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fe915-146">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fe915-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fe915-147">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="fe915-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fe915-148">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="fe915-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="fe915-149">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fe915-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="fe915-150">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="fe915-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="fe915-151">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fe915-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="fe915-152">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="fe915-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fe915-153">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="fe915-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="fe915-154">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="fe915-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="fe915-155">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="fe915-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="fe915-156">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fe915-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="fe915-157">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="fe915-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="fe915-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe915-158">RELATED LINKS</span></span>

