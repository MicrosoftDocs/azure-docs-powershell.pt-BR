---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114777"
---
# <span data-ttu-id="264e9-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="264e9-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="264e9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="264e9-102">SYNOPSIS</span></span>
<span data-ttu-id="264e9-103">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="264e9-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="264e9-104">Use Update-AzMariaDbServer em vez disso, se quiser atualizar o AdministratorLoginPassword, sku etc.</span><span class="sxs-lookup"><span data-stu-id="264e9-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="264e9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="264e9-105">SYNTAX</span></span>

### <span data-ttu-id="264e9-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="264e9-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="264e9-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="264e9-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="264e9-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="264e9-108">DESCRIPTION</span></span>
<span data-ttu-id="264e9-109">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="264e9-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="264e9-110">Use Update-AzMariaDberver em vez disso, se quiser atualizar o AdministratorLoginPassword, sku etc.</span><span class="sxs-lookup"><span data-stu-id="264e9-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="264e9-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="264e9-111">EXAMPLES</span></span>

### <span data-ttu-id="264e9-112">Exemplo 1: Atualizar configuração de MariaDB</span><span class="sxs-lookup"><span data-stu-id="264e9-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="264e9-113">Este comando atualiza uma configuração mariadb.</span><span class="sxs-lookup"><span data-stu-id="264e9-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="264e9-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="264e9-114">PARAMETERS</span></span>

### <span data-ttu-id="264e9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="264e9-115">-AsJob</span></span>
<span data-ttu-id="264e9-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="264e9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="264e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="264e9-117">-DefaultProfile</span></span>
<span data-ttu-id="264e9-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="264e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="264e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="264e9-119">-InputObject</span></span>
<span data-ttu-id="264e9-120">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="264e9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="264e9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="264e9-121">-Name</span></span>
<span data-ttu-id="264e9-122">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="264e9-122">The name of the server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="264e9-123">-NoWait</span></span>
<span data-ttu-id="264e9-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="264e9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="264e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="264e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="264e9-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="264e9-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="264e9-127">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="264e9-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e9-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="264e9-128">-ServerName</span></span>
<span data-ttu-id="264e9-129">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="264e9-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e9-130">-Origem</span><span class="sxs-lookup"><span data-stu-id="264e9-130">-Source</span></span>
<span data-ttu-id="264e9-131">Origem da configuração.</span><span class="sxs-lookup"><span data-stu-id="264e9-131">Source of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e9-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="264e9-132">-SubscriptionId</span></span>
<span data-ttu-id="264e9-133">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="264e9-133">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e9-134">-Valor</span><span class="sxs-lookup"><span data-stu-id="264e9-134">-Value</span></span>
<span data-ttu-id="264e9-135">Valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="264e9-135">Value of the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="264e9-136">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="264e9-136">-Confirm</span></span>
<span data-ttu-id="264e9-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="264e9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="264e9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="264e9-138">-WhatIf</span></span>
<span data-ttu-id="264e9-139">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="264e9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="264e9-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="264e9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="264e9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="264e9-141">CommonParameters</span></span>
<span data-ttu-id="264e9-142">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="264e9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="264e9-143">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="264e9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="264e9-144">Entradas</span><span class="sxs-lookup"><span data-stu-id="264e9-144">INPUTS</span></span>

### <span data-ttu-id="264e9-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="264e9-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="264e9-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="264e9-146">OUTPUTS</span></span>

### <span data-ttu-id="264e9-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span><span class="sxs-lookup"><span data-stu-id="264e9-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="264e9-148">Notas</span><span class="sxs-lookup"><span data-stu-id="264e9-148">NOTES</span></span>

<span data-ttu-id="264e9-149">Aliases</span><span class="sxs-lookup"><span data-stu-id="264e9-149">ALIASES</span></span>

<span data-ttu-id="264e9-150">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="264e9-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="264e9-151">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="264e9-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="264e9-152">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="264e9-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="264e9-153">INPUTOBJECT: <IMariaDbIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="264e9-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="264e9-154">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="264e9-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="264e9-155">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="264e9-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="264e9-156">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="264e9-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="264e9-157">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="264e9-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="264e9-158">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="264e9-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="264e9-159">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="264e9-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="264e9-160">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="264e9-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="264e9-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="264e9-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="264e9-162">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="264e9-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="264e9-163">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="264e9-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="264e9-164">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="264e9-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="264e9-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="264e9-165">RELATED LINKS</span></span>

