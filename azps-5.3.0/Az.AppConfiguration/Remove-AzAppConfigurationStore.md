---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272070"
---
# <span data-ttu-id="45c13-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="45c13-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="45c13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="45c13-102">SYNOPSIS</span></span>
<span data-ttu-id="45c13-103">Exclui um repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="45c13-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="45c13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45c13-104">SYNTAX</span></span>

### <span data-ttu-id="45c13-105">Excluir (padrão)</span><span class="sxs-lookup"><span data-stu-id="45c13-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="45c13-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45c13-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="45c13-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="45c13-107">DESCRIPTION</span></span>
<span data-ttu-id="45c13-108">Exclui um repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="45c13-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="45c13-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="45c13-109">EXAMPLES</span></span>

### <span data-ttu-id="45c13-110">Exemplo 1: remover um repositório de configuração de aplicativo</span><span class="sxs-lookup"><span data-stu-id="45c13-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="45c13-111">Esse comando Remove um repositório de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="45c13-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="45c13-112">Exemplo 2: remover um repositório de configuração de aplicativo</span><span class="sxs-lookup"><span data-stu-id="45c13-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="45c13-113">Esse comando Remove um repositório de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="45c13-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="45c13-114">OS</span><span class="sxs-lookup"><span data-stu-id="45c13-114">PARAMETERS</span></span>

### <span data-ttu-id="45c13-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45c13-115">-AsJob</span></span>
<span data-ttu-id="45c13-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="45c13-116">Run the command as a job</span></span>

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

### <span data-ttu-id="45c13-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c13-117">-DefaultProfile</span></span>
<span data-ttu-id="45c13-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="45c13-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c13-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45c13-119">-InputObject</span></span>
<span data-ttu-id="45c13-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="45c13-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45c13-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="45c13-121">-Name</span></span>
<span data-ttu-id="45c13-122">O nome do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="45c13-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="45c13-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="45c13-123">-NoWait</span></span>
<span data-ttu-id="45c13-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="45c13-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="45c13-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45c13-125">-PassThru</span></span>
<span data-ttu-id="45c13-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="45c13-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="45c13-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c13-127">-ResourceGroupName</span></span>
<span data-ttu-id="45c13-128">O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="45c13-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="45c13-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45c13-129">-SubscriptionId</span></span>
<span data-ttu-id="45c13-130">A ID da assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="45c13-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="45c13-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="45c13-131">-Confirm</span></span>
<span data-ttu-id="45c13-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45c13-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c13-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c13-133">-WhatIf</span></span>
<span data-ttu-id="45c13-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="45c13-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c13-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="45c13-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c13-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c13-136">CommonParameters</span></span>
<span data-ttu-id="45c13-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c13-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c13-138">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45c13-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c13-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="45c13-139">INPUTS</span></span>

### <span data-ttu-id="45c13-140">Microsoft. Azure. PowerShell. cmdlets. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="45c13-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="45c13-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="45c13-141">OUTPUTS</span></span>

### <span data-ttu-id="45c13-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="45c13-142">System.Boolean</span></span>

## <span data-ttu-id="45c13-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="45c13-143">NOTES</span></span>

<span data-ttu-id="45c13-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="45c13-144">ALIASES</span></span>

<span data-ttu-id="45c13-145">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="45c13-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="45c13-146">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="45c13-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45c13-147">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45c13-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="45c13-148">INPUTobject <IAppConfigurationIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="45c13-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45c13-149">`[ConfigStoreName <String>]`: O nome do repositório de configuração.</span><span class="sxs-lookup"><span data-stu-id="45c13-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="45c13-150">`[GroupName <String>]`: O nome do grupo de recursos de link privado.</span><span class="sxs-lookup"><span data-stu-id="45c13-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="45c13-151">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="45c13-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45c13-152">`[PrivateEndpointConnectionName <String>]`: Nome da conexão de ponto de extremidade privado</span><span class="sxs-lookup"><span data-stu-id="45c13-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="45c13-153">`[ResourceGroupName <String>]`: O nome do grupo de recursos ao qual o registro do contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="45c13-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="45c13-154">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="45c13-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="45c13-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="45c13-155">RELATED LINKS</span></span>

