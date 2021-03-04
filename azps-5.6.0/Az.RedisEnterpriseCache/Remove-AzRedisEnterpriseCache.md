---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/remove-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Remove-AzRedisEnterpriseCache.md
ms.openlocfilehash: d6b030cfbc6233d917d252f2d271eb7d4bfe65bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891744"
---
# <span data-ttu-id="4a5d0-101">Remove-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="4a5d0-101">Remove-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="4a5d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a5d0-102">SYNOPSIS</span></span>
<span data-ttu-id="4a5d0-103">Exclui um cluster de cache RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-103">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="4a5d0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4a5d0-104">SYNTAX</span></span>

### <span data-ttu-id="4a5d0-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4a5d0-105">Delete (Default)</span></span>
```
Remove-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4a5d0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a5d0-106">DeleteViaIdentity</span></span>
```
Remove-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4a5d0-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4a5d0-107">DESCRIPTION</span></span>
<span data-ttu-id="4a5d0-108">Exclui um cluster de cache RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-108">Deletes a RedisEnterprise cache cluster.</span></span>

## <span data-ttu-id="4a5d0-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4a5d0-109">EXAMPLES</span></span>

### <span data-ttu-id="4a5d0-110">Exemplo 1: Remover um Cache da Empresa Redis e retornar o resultado</span><span class="sxs-lookup"><span data-stu-id="4a5d0-110">Example 1: Remove a Redis Enterprise Cache and return the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -PassThru
True
```

<span data-ttu-id="4a5d0-111">Este comando remove um Cache da Empresa Redis e exibe se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-111">This command removes a Redis Enterprise Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="4a5d0-112">Exemplo 2: Remover um Cache da Empresa Redis e não exibir o resultado</span><span class="sxs-lookup"><span data-stu-id="4a5d0-112">Example 2: Remove a Redis Enterprise Cache and do not display the result</span></span>
```powershell
PS C:\> Remove-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup"
```

<span data-ttu-id="4a5d0-113">Este comando remove um Cache da Empresa Redis.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-113">This command removes a Redis Enterprise Cache.</span></span>
<span data-ttu-id="4a5d0-114">Como o parâmetro PassThru não é especificado, o resultado da operação não é exibido.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-114">Because the PassThru parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="4a5d0-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4a5d0-115">PARAMETERS</span></span>

### <span data-ttu-id="4a5d0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a5d0-116">-AsJob</span></span>
<span data-ttu-id="4a5d0-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="4a5d0-117">Run the command as a job</span></span>

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

### <span data-ttu-id="4a5d0-118">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4a5d0-118">-ClusterName</span></span>
<span data-ttu-id="4a5d0-119">O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-119">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="4a5d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a5d0-120">-DefaultProfile</span></span>
<span data-ttu-id="4a5d0-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a5d0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a5d0-122">-InputObject</span></span>
<span data-ttu-id="4a5d0-123">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a5d0-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4a5d0-124">-NoWait</span></span>
<span data-ttu-id="4a5d0-125">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="4a5d0-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4a5d0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4a5d0-126">-PassThru</span></span>
<span data-ttu-id="4a5d0-127">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="4a5d0-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4a5d0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a5d0-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a5d0-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a5d0-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a5d0-130">-SubscriptionId</span></span>
<span data-ttu-id="4a5d0-131">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-131">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4a5d0-132">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4a5d0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a5d0-133">-Confirm</span></span>
<span data-ttu-id="4a5d0-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a5d0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a5d0-135">-WhatIf</span></span>
<span data-ttu-id="4a5d0-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a5d0-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a5d0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a5d0-138">CommonParameters</span></span>
<span data-ttu-id="4a5d0-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a5d0-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a5d0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a5d0-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a5d0-141">INPUTS</span></span>

### <span data-ttu-id="4a5d0-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="4a5d0-142">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="4a5d0-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4a5d0-143">OUTPUTS</span></span>

### <span data-ttu-id="4a5d0-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4a5d0-144">System.Boolean</span></span>

## <span data-ttu-id="4a5d0-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="4a5d0-145">NOTES</span></span>

<span data-ttu-id="4a5d0-146">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4a5d0-146">ALIASES</span></span>

<span data-ttu-id="4a5d0-147">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="4a5d0-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a5d0-148">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a5d0-149">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a5d0-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="4a5d0-150">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a5d0-151">`[ClusterName <String>]`: O nome do cluster RedisEnterprise.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-151">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="4a5d0-152">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-152">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4a5d0-153">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="4a5d0-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a5d0-154">`[Location <String>]`: A região em que a operação está.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-154">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="4a5d0-155">`[OperationId <String>]`: Identificador exclusivo da operação.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-155">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="4a5d0-156">`[PrivateEndpointConnectionName <String>]`: O nome da conexão de ponto de extremidade privada associada ao recurso do Azure</span><span class="sxs-lookup"><span data-stu-id="4a5d0-156">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="4a5d0-157">`[ResourceGroupName <String>]`: O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="4a5d0-158">`[SubscriptionId <String>]`: Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="4a5d0-159">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4a5d0-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4a5d0-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4a5d0-160">RELATED LINKS</span></span>

