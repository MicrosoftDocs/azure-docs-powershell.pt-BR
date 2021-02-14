---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: 22d0fed7c72aa5754b7393cdf06fb58a4bfc0db3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117205"
---
# <span data-ttu-id="44e0f-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="44e0f-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="44e0f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44e0f-102">SYNOPSIS</span></span>
<span data-ttu-id="44e0f-103">Exclui um cluster de cache RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="44e0f-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="44e0f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44e0f-104">SYNTAX</span></span>

### <span data-ttu-id="44e0f-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="44e0f-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44e0f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44e0f-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44e0f-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="44e0f-107">DESCRIPTION</span></span>
<span data-ttu-id="44e0f-108">Exclui um cluster de cache RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="44e0f-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="44e0f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44e0f-109">EXAMPLES</span></span>

### <span data-ttu-id="44e0f-110">Exemplo 1: Remover um Cache Corporativo Redis e retornar o resultado</span><span class="sxs-lookup"><span data-stu-id="44e0f-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="44e0f-111">Esse comando remove um Cache Corporativo Redis e exibe se a operação é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="44e0f-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="44e0f-112">Exemplo 2: Remover um Cache Corporativo Redis e não exibir o resultado</span><span class="sxs-lookup"><span data-stu-id="44e0f-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="44e0f-113">Esse comando remove um Cache Corporativo Redis.</span><span class="sxs-lookup"><span data-stu-id="44e0f-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="44e0f-114">Como o parâmetro PassThru não é especificado, o resultado da operação não é exibido.</span><span class="sxs-lookup"><span data-stu-id="44e0f-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="44e0f-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44e0f-115">PARAMETERS</span></span>

### <span data-ttu-id="44e0f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44e0f-116">-AsJob</span></span>
<span data-ttu-id="44e0f-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="44e0f-117">Run the command as a job</span></span>

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

### <span data-ttu-id="44e0f-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="44e0f-118">-ClusterName</span></span>
<span data-ttu-id="44e0f-119">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="44e0f-119">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e0f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44e0f-120">-DefaultProfile</span></span>
<span data-ttu-id="44e0f-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44e0f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44e0f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44e0f-122">-InputObject</span></span>
<span data-ttu-id="44e0f-123">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="44e0f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44e0f-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="44e0f-124">-NoWait</span></span>
<span data-ttu-id="44e0f-125">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="44e0f-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="44e0f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44e0f-126">-PassThru</span></span>
<span data-ttu-id="44e0f-127">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="44e0f-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44e0f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44e0f-128">-ResourceGroupName</span></span>
<span data-ttu-id="44e0f-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44e0f-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e0f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44e0f-130">-SubscriptionId</span></span>
<span data-ttu-id="44e0f-131">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44e0f-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="44e0f-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="44e0f-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44e0f-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="44e0f-133">-Confirm</span></span>
<span data-ttu-id="44e0f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44e0f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44e0f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44e0f-135">-WhatIf</span></span>
<span data-ttu-id="44e0f-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="44e0f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44e0f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44e0f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44e0f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44e0f-138">CommonParameters</span></span>
<span data-ttu-id="44e0f-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44e0f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44e0f-140">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44e0f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44e0f-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="44e0f-141">INPUTS</span></span>

### <span data-ttu-id="44e0f-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="44e0f-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="44e0f-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="44e0f-143">OUTPUTS</span></span>

### <span data-ttu-id="44e0f-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44e0f-144">System.Boolean</span></span>

## <span data-ttu-id="44e0f-145">Notas</span><span class="sxs-lookup"><span data-stu-id="44e0f-145">NOTES</span></span>

<span data-ttu-id="44e0f-146">Aliases</span><span class="sxs-lookup"><span data-stu-id="44e0f-146">ALIASES</span></span>

<span data-ttu-id="44e0f-147">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="44e0f-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44e0f-148">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="44e0f-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44e0f-149">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44e0f-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44e0f-150">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="44e0f-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44e0f-151">`[ClusterName <String>]`: o nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="44e0f-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="44e0f-152">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="44e0f-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="44e0f-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="44e0f-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44e0f-154">`[Location <String>]`: a região em que a operação está.</span><span class="sxs-lookup"><span data-stu-id="44e0f-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="44e0f-155">`[OperationId <String>]`: identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="44e0f-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="44e0f-156">`[PrivateEndpointConnectionName <String>]`: o nome da conexão de ponto de extremidade particular associada ao recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="44e0f-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="44e0f-157">`[ResourceGroupName <String>]`: o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44e0f-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="44e0f-158">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="44e0f-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="44e0f-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="44e0f-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="44e0f-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44e0f-160">RELATED LINKS</span></span>

