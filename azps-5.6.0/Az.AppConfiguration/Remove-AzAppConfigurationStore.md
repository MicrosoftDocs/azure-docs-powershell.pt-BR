---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: 4babe23fbddbc11838cad6307117884c3bb14ae8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890319"
---
# <span data-ttu-id="125fd-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="125fd-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="125fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="125fd-102">SYNOPSIS</span></span>
<span data-ttu-id="125fd-103">Exclui um armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="125fd-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="125fd-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="125fd-104">SYNTAX</span></span>

### <span data-ttu-id="125fd-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="125fd-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="125fd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="125fd-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="125fd-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="125fd-107">DESCRIPTION</span></span>
<span data-ttu-id="125fd-108">Exclui um armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="125fd-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="125fd-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="125fd-109">EXAMPLES</span></span>

### <span data-ttu-id="125fd-110">Exemplo 1: Remover um armazenamento de configuração de aplicativo</span><span class="sxs-lookup"><span data-stu-id="125fd-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="125fd-111">Este comando remove um armazenamento de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="125fd-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="125fd-112">Exemplo 2: Remover um armazenamento de configuração de aplicativo</span><span class="sxs-lookup"><span data-stu-id="125fd-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="125fd-113">Este comando remove um armazenamento de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="125fd-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="125fd-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="125fd-114">PARAMETERS</span></span>

### <span data-ttu-id="125fd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="125fd-115">-AsJob</span></span>
<span data-ttu-id="125fd-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="125fd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="125fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125fd-117">-DefaultProfile</span></span>
<span data-ttu-id="125fd-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="125fd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="125fd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="125fd-119">-InputObject</span></span>
<span data-ttu-id="125fd-120">Parâmetro Identity Para construir, consulte a seção NOTES para propriedades INPUTOBJECT e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="125fd-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="125fd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="125fd-121">-Name</span></span>
<span data-ttu-id="125fd-122">O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="125fd-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="125fd-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="125fd-123">-NoWait</span></span>
<span data-ttu-id="125fd-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="125fd-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="125fd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="125fd-125">-PassThru</span></span>
<span data-ttu-id="125fd-126">Retorna true quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="125fd-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="125fd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125fd-127">-ResourceGroupName</span></span>
<span data-ttu-id="125fd-128">O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="125fd-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="125fd-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="125fd-129">-SubscriptionId</span></span>
<span data-ttu-id="125fd-130">A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="125fd-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="125fd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="125fd-131">-Confirm</span></span>
<span data-ttu-id="125fd-132">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="125fd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="125fd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="125fd-133">-WhatIf</span></span>
<span data-ttu-id="125fd-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="125fd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="125fd-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="125fd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="125fd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125fd-136">CommonParameters</span></span>
<span data-ttu-id="125fd-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="125fd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125fd-138">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="125fd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125fd-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="125fd-139">INPUTS</span></span>

### <span data-ttu-id="125fd-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="125fd-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="125fd-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="125fd-141">OUTPUTS</span></span>

### <span data-ttu-id="125fd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="125fd-142">System.Boolean</span></span>

## <span data-ttu-id="125fd-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="125fd-143">NOTES</span></span>

<span data-ttu-id="125fd-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="125fd-144">ALIASES</span></span>

<span data-ttu-id="125fd-145">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="125fd-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="125fd-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="125fd-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="125fd-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="125fd-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="125fd-148">INPUTOBJECT <IAppConfigurationIdentity> : Parâmetro Identity</span><span class="sxs-lookup"><span data-stu-id="125fd-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="125fd-149">`[ConfigStoreName <String>]`: O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="125fd-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="125fd-150">`[GroupName <String>]`: O nome do grupo de recursos de link privado.</span><span class="sxs-lookup"><span data-stu-id="125fd-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="125fd-151">`[Id <String>]`: Caminho da identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="125fd-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="125fd-152">`[PrivateEndpointConnectionName <String>]`: Nome da conexão do ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="125fd-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="125fd-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="125fd-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="125fd-154">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="125fd-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="125fd-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="125fd-155">RELATED LINKS</span></span>

