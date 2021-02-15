---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 12e43eeb22151df8569e068933036fe29749ed1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115284"
---
# <span data-ttu-id="febad-101">Remove-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="febad-101">Remove-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="febad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="febad-102">SYNOPSIS</span></span>
<span data-ttu-id="febad-103">Remover permissões de entidades de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="febad-103">Remove Database principals permissions.</span></span>

## <span data-ttu-id="febad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="febad-104">SYNTAX</span></span>

### <span data-ttu-id="febad-105">RemoveExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="febad-105">RemoveExpanded (Default)</span></span>
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="febad-106">RemoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="febad-106">RemoveViaIdentityExpanded</span></span>
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="febad-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="febad-107">DESCRIPTION</span></span>
<span data-ttu-id="febad-108">Remover permissões de entidades de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="febad-108">Remove Database principals permissions.</span></span>

## <span data-ttu-id="febad-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="febad-109">EXAMPLES</span></span>

### <span data-ttu-id="febad-110">Exemplo 1: Remover permissões de entidades de banco de dados</span><span class="sxs-lookup"><span data-stu-id="febad-110">Example 1: Remove Database principals permissions</span></span>
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="febad-111">O comando acima remove permissões de entidades de banco de dados</span><span class="sxs-lookup"><span data-stu-id="febad-111">The above command removes Database principals permissions</span></span>

## <span data-ttu-id="febad-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="febad-112">PARAMETERS</span></span>

### <span data-ttu-id="febad-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="febad-113">-ClusterName</span></span>
<span data-ttu-id="febad-114">O nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="febad-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="febad-115">-Nomedo Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="febad-115">-DatabaseName</span></span>
<span data-ttu-id="febad-116">O nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="febad-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="febad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febad-117">-DefaultProfile</span></span>
<span data-ttu-id="febad-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="febad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="febad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="febad-119">-InputObject</span></span>
<span data-ttu-id="febad-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="febad-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="febad-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="febad-121">-ResourceGroupName</span></span>
<span data-ttu-id="febad-122">O nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="febad-122">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="febad-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="febad-123">-SubscriptionId</span></span>
<span data-ttu-id="febad-124">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="febad-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="febad-125">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="febad-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="febad-126">-Valor</span><span class="sxs-lookup"><span data-stu-id="febad-126">-Value</span></span>
<span data-ttu-id="febad-127">A lista de entidades de banco de dados do Kusto.</span><span class="sxs-lookup"><span data-stu-id="febad-127">The list of Kusto database principals.</span></span>
<span data-ttu-id="febad-128">Para construir, confira a seção ANOTAÇÕES das propriedades VALOR e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="febad-128">To construct, see NOTES section for VALUE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="febad-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="febad-129">-Confirm</span></span>
<span data-ttu-id="febad-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="febad-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="febad-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="febad-131">-WhatIf</span></span>
<span data-ttu-id="febad-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="febad-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="febad-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="febad-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="febad-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febad-134">CommonParameters</span></span>
<span data-ttu-id="febad-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="febad-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febad-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="febad-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febad-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="febad-137">INPUTS</span></span>

### <span data-ttu-id="febad-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="febad-138">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="febad-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="febad-139">OUTPUTS</span></span>

### <span data-ttu-id="febad-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="febad-140">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="febad-141">Notas</span><span class="sxs-lookup"><span data-stu-id="febad-141">NOTES</span></span>

<span data-ttu-id="febad-142">Aliases</span><span class="sxs-lookup"><span data-stu-id="febad-142">ALIASES</span></span>

<span data-ttu-id="febad-143">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="febad-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="febad-144">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="febad-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="febad-145">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="febad-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="febad-146">INPUTOBJECT: <IKustoIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="febad-146">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="febad-147">`[AttachedDatabaseConfigurationName <String>]`: o nome da configuração de banco de dados anexada.</span><span class="sxs-lookup"><span data-stu-id="febad-147">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="febad-148">`[ClusterName <String>]`: o nome do cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="febad-148">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="febad-149">`[DataConnectionName <String>]`: o nome da conexão de dados.</span><span class="sxs-lookup"><span data-stu-id="febad-149">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="febad-150">`[DatabaseName <String>]`: o nome do banco de dados no cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="febad-150">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="febad-151">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="febad-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="febad-152">`[Location <String>]`: local do Azure.</span><span class="sxs-lookup"><span data-stu-id="febad-152">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="febad-153">`[PrincipalAssignmentName <String>]`: o nome do kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="febad-153">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="febad-154">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o cluster de Kusto.</span><span class="sxs-lookup"><span data-stu-id="febad-154">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="febad-155">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="febad-155">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="febad-156">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="febad-156">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="febad-157">VALUE <IDatabasePrincipal[]>: a lista de entidades de banco de dados do Kusto.</span><span class="sxs-lookup"><span data-stu-id="febad-157">VALUE <IDatabasePrincipal[]>: The list of Kusto database principals.</span></span>
  - <span data-ttu-id="febad-158">`Name <String>`: Nome principal do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="febad-158">`Name <String>`: Database principal name.</span></span>
  - <span data-ttu-id="febad-159">`Role <DatabasePrincipalRole>`: Função principal do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="febad-159">`Role <DatabasePrincipalRole>`: Database principal role.</span></span>
  - <span data-ttu-id="febad-160">`Type <DatabasePrincipalType>`: tipo de entidade de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="febad-160">`Type <DatabasePrincipalType>`: Database principal type.</span></span>
  - <span data-ttu-id="febad-161">`[AppId <String>]`: ID do aplicativo – relevante somente para o tipo de entidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="febad-161">`[AppId <String>]`: Application id - relevant only for application principal type.</span></span>
  - <span data-ttu-id="febad-162">`[Email <String>]`: Email principal do banco de dados se existir.</span><span class="sxs-lookup"><span data-stu-id="febad-162">`[Email <String>]`: Database principal email if exists.</span></span>
  - <span data-ttu-id="febad-163">`[Fqn <String>]`: Nome totalmente qualificado do capital do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="febad-163">`[Fqn <String>]`: Database principal fully qualified name.</span></span>

## <span data-ttu-id="febad-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="febad-164">RELATED LINKS</span></span>

