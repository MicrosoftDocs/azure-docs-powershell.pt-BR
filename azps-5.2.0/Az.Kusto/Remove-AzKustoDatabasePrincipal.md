---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259756"
---
# <span data-ttu-id="f9c1e-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f9c1e-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="f9c1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f9c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c1e-103">Remover as permissões de entidades de segurança do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="f9c1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f9c1e-104">SYNTAX</span></span>

### <span data-ttu-id="f9c1e-105">RemoveExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="f9c1e-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f9c1e-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f9c1e-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f9c1e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f9c1e-107">DESCRIPTION</span></span>
<span data-ttu-id="f9c1e-108">Remover as permissões de entidades de segurança do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="f9c1e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f9c1e-109">EXAMPLES</span></span>

### <span data-ttu-id="f9c1e-110">Exemplo 1: remover as permissões dos objetos de banco de dados</span><span class="sxs-lookup"><span data-stu-id="f9c1e-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="f9c1e-111">O comando acima remove as permissões de entidades de segurança do banco de dados</span><span class="sxs-lookup"><span data-stu-id="f9c1e-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="f9c1e-112">OS</span><span class="sxs-lookup"><span data-stu-id="f9c1e-112">PARAMETERS</span></span>

### <span data-ttu-id="f9c1e-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f9c1e-113">-ClusterName</span></span>
<span data-ttu-id="f9c1e-114">O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c1e-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f9c1e-115">-DatabaseName</span></span>
<span data-ttu-id="f9c1e-116">O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-116">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c1e-117">-DefaultProfile</span></span>
<span data-ttu-id="f9c1e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9c1e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9c1e-119">-InputObject</span></span>
<span data-ttu-id="f9c1e-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9c1e-122">O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-122">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c1e-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9c1e-123">-SubscriptionId</span></span>
<span data-ttu-id="f9c1e-124">Obtém as credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f9c1e-125">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c1e-126">-Valor</span><span class="sxs-lookup"><span data-stu-id="f9c1e-126">-Value</span></span>
<span data-ttu-id="f9c1e-127">A lista de objetos Kusto do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="f9c1e-128">Para construir, consulte a seção observações para propriedades de valor e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9c1e-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f9c1e-129">-Confirm</span></span>
<span data-ttu-id="f9c1e-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9c1e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9c1e-131">-WhatIf</span></span>
<span data-ttu-id="f9c1e-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9c1e-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9c1e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c1e-134">CommonParameters</span></span>
<span data-ttu-id="f9c1e-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c1e-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9c1e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c1e-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f9c1e-137">INPUTS</span></span>

### <span data-ttu-id="f9c1e-138">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="f9c1e-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="f9c1e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f9c1e-139">OUTPUTS</span></span>

### <span data-ttu-id="f9c1e-140">Microsoft. Azure. PowerShell. cmdlets. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f9c1e-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="f9c1e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f9c1e-141">NOTES</span></span>

<span data-ttu-id="f9c1e-142">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f9c1e-142">ALIASES</span></span>

<span data-ttu-id="f9c1e-143">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f9c1e-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f9c1e-144">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f9c1e-145">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f9c1e-146">INPUTobject <IKustoIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f9c1e-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f9c1e-147">`[AttachedDatabaseConfigurationName <String>]`: O nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="f9c1e-148">`[ClusterName <String>]`: O nome do cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="f9c1e-149">`[DataConnectionName <String>]`: O nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="f9c1e-150">`[DatabaseName <String>]`: O nome do banco de dados no cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="f9c1e-151">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f9c1e-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f9c1e-152">`[Location <String>]`: Local do Azure.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="f9c1e-153">`[PrincipalAssignmentName <String>]`: O nome do principalAssignment Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="f9c1e-154">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o cluster Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="f9c1e-155">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f9c1e-156">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="f9c1e-157">VALOR <IDatabasePrincipal [] >: a lista de objetos de banco de dados do Kusto.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="f9c1e-158">`Name <String>`: Nome do banco de dados principal.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="f9c1e-159">`Role <DatabasePrincipalRole>`: Função de entidade do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="f9c1e-160">`Type <DatabasePrincipalType>`: Tipo de entidade de segurança do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="f9c1e-161">`[AppId <String>]`: ID do aplicativo-relevante somente para o tipo principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="f9c1e-162">`[Email <String>]`: Email principal do banco de dados se existe.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="f9c1e-163">`[Fqn <String>]`: Nome totalmente qualificado do banco de dados principal.</span><span class="sxs-lookup"><span data-stu-id="f9c1e-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="f9c1e-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f9c1e-164">RELATED LINKS</span></span>

