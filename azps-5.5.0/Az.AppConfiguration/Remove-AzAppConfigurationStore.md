---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112291"
---
# <span data-ttu-id="8f5ad-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="8f5ad-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="8f5ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8f5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5ad-103">Exclui um armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="8f5ad-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f5ad-104">SYNTAX</span></span>

### <span data-ttu-id="8f5ad-105">Excluir (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8f5ad-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8f5ad-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8f5ad-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f5ad-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f5ad-107">DESCRIPTION</span></span>
<span data-ttu-id="8f5ad-108">Exclui um armazenamento de configurações.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="8f5ad-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f5ad-109">EXAMPLES</span></span>

### <span data-ttu-id="8f5ad-110">Exemplo 1: Remover um armazenamento de configuração de aplicativos</span><span class="sxs-lookup"><span data-stu-id="8f5ad-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="8f5ad-111">Esse comando remove um armazenamento de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="8f5ad-112">Exemplo 2: Remover um armazenamento de configuração de aplicativos</span><span class="sxs-lookup"><span data-stu-id="8f5ad-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="8f5ad-113">Esse comando remove um armazenamento de configuração de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="8f5ad-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f5ad-114">PARAMETERS</span></span>

### <span data-ttu-id="8f5ad-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f5ad-115">-AsJob</span></span>
<span data-ttu-id="8f5ad-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8f5ad-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8f5ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5ad-117">-DefaultProfile</span></span>
<span data-ttu-id="8f5ad-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f5ad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f5ad-119">-InputObject</span></span>
<span data-ttu-id="8f5ad-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8f5ad-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f5ad-121">-Name</span></span>
<span data-ttu-id="8f5ad-122">O nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="8f5ad-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8f5ad-123">-NoWait</span></span>
<span data-ttu-id="8f5ad-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="8f5ad-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f5ad-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f5ad-125">-PassThru</span></span>
<span data-ttu-id="8f5ad-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="8f5ad-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8f5ad-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f5ad-127">-ResourceGroupName</span></span>
<span data-ttu-id="8f5ad-128">O nome do grupo de recursos ao qual o registro de contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="8f5ad-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f5ad-129">-SubscriptionId</span></span>
<span data-ttu-id="8f5ad-130">A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="8f5ad-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8f5ad-131">-Confirm</span></span>
<span data-ttu-id="8f5ad-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f5ad-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f5ad-133">-WhatIf</span></span>
<span data-ttu-id="8f5ad-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f5ad-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f5ad-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5ad-136">CommonParameters</span></span>
<span data-ttu-id="8f5ad-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5ad-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f5ad-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5ad-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="8f5ad-139">INPUTS</span></span>

### <span data-ttu-id="8f5ad-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="8f5ad-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="8f5ad-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="8f5ad-141">OUTPUTS</span></span>

### <span data-ttu-id="8f5ad-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8f5ad-142">System.Boolean</span></span>

## <span data-ttu-id="8f5ad-143">Notas</span><span class="sxs-lookup"><span data-stu-id="8f5ad-143">NOTES</span></span>

<span data-ttu-id="8f5ad-144">Aliases</span><span class="sxs-lookup"><span data-stu-id="8f5ad-144">ALIASES</span></span>

<span data-ttu-id="8f5ad-145">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="8f5ad-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f5ad-146">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f5ad-147">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f5ad-148">INPUTOBJECT: <IAppConfigurationIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="8f5ad-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f5ad-149">`[ConfigStoreName <String>]`: o nome do armazenamento de configuração.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="8f5ad-150">`[GroupName <String>]`: o nome do grupo de recursos de vínculo privado.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="8f5ad-151">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="8f5ad-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f5ad-152">`[PrivateEndpointConnectionName <String>]`: Nome de conexão do ponto de extremidade particular</span><span class="sxs-lookup"><span data-stu-id="8f5ad-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="8f5ad-153">`[ResourceGroupName <String>]`: o nome do grupo de recursos ao qual o registro de contêiner pertence.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="8f5ad-154">`[SubscriptionId <String>]`: A ID de assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f5ad-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="8f5ad-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8f5ad-155">RELATED LINKS</span></span>

