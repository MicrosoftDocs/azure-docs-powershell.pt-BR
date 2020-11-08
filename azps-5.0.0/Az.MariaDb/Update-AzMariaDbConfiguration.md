---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124838"
---
# <span data-ttu-id="f4b2e-101">Update-AzMariaDbConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4b2e-101">Update-AzMariaDbConfiguration</span></span>

## <span data-ttu-id="f4b2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f4b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b2e-103">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-103">Updates a configuration of a server.</span></span>
<span data-ttu-id="f4b2e-104">Use Update-AzMariaDbServer em vez disso, se quiser atualizar AdministratorLoginPassword, SKU, etc.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-104">Use Update-AzMariaDbServer instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="f4b2e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4b2e-105">SYNTAX</span></span>

### <span data-ttu-id="f4b2e-106">UpdateExpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="f4b2e-106">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f4b2e-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f4b2e-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f4b2e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f4b2e-108">DESCRIPTION</span></span>
<span data-ttu-id="f4b2e-109">Atualiza uma configuração de um servidor.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-109">Updates a configuration of a server.</span></span>
<span data-ttu-id="f4b2e-110">Use Update-AzMariaDberver em vez disso, se quiser atualizar AdministratorLoginPassword, SKU, etc.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-110">Use Update-AzMariaDberver instead if you want update AdministratorLoginPassword, sku, etc.</span></span>

## <span data-ttu-id="f4b2e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4b2e-111">EXAMPLES</span></span>

### <span data-ttu-id="f4b2e-112">Exemplo 1: atualizar a configuração do MariaDB</span><span class="sxs-lookup"><span data-stu-id="f4b2e-112">Example 1: Update MariaDB configuration</span></span>
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

<span data-ttu-id="f4b2e-113">Esse comando atualiza uma configuração do MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-113">This command updates a MariaDB configuration.</span></span>

## <span data-ttu-id="f4b2e-114">OS</span><span class="sxs-lookup"><span data-stu-id="f4b2e-114">PARAMETERS</span></span>

### <span data-ttu-id="f4b2e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4b2e-115">-AsJob</span></span>
<span data-ttu-id="f4b2e-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="f4b2e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f4b2e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b2e-117">-DefaultProfile</span></span>
<span data-ttu-id="f4b2e-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b2e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4b2e-119">-InputObject</span></span>
<span data-ttu-id="f4b2e-120">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f4b2e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4b2e-121">-Name</span></span>
<span data-ttu-id="f4b2e-122">O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-122">The name of the server configuration.</span></span>

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

### <span data-ttu-id="f4b2e-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f4b2e-123">-NoWait</span></span>
<span data-ttu-id="f4b2e-124">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="f4b2e-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f4b2e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b2e-125">-ResourceGroupName</span></span>
<span data-ttu-id="f4b2e-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f4b2e-127">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="f4b2e-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="f4b2e-128">-ServerName</span></span>
<span data-ttu-id="f4b2e-129">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-129">The name of the server.</span></span>

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

### <span data-ttu-id="f4b2e-130">-Fonte</span><span class="sxs-lookup"><span data-stu-id="f4b2e-130">-Source</span></span>
<span data-ttu-id="f4b2e-131">Fonte da configuração.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-131">Source of the configuration.</span></span>

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

### <span data-ttu-id="f4b2e-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f4b2e-132">-SubscriptionId</span></span>
<span data-ttu-id="f4b2e-133">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-133">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="f4b2e-134">-Valor</span><span class="sxs-lookup"><span data-stu-id="f4b2e-134">-Value</span></span>
<span data-ttu-id="f4b2e-135">Valor da configuração.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-135">Value of the configuration.</span></span>

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

### <span data-ttu-id="f4b2e-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f4b2e-136">-Confirm</span></span>
<span data-ttu-id="f4b2e-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4b2e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b2e-138">-WhatIf</span></span>
<span data-ttu-id="f4b2e-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4b2e-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4b2e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b2e-141">CommonParameters</span></span>
<span data-ttu-id="f4b2e-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b2e-143">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4b2e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b2e-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f4b2e-144">INPUTS</span></span>

### <span data-ttu-id="f4b2e-145">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="f4b2e-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="f4b2e-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f4b2e-146">OUTPUTS</span></span>

### <span data-ttu-id="f4b2e-147">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4b2e-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IConfiguration</span></span>

## <span data-ttu-id="f4b2e-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f4b2e-148">NOTES</span></span>

<span data-ttu-id="f4b2e-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="f4b2e-149">ALIASES</span></span>

<span data-ttu-id="f4b2e-150">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="f4b2e-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f4b2e-151">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4b2e-152">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f4b2e-153">INPUTobject <IMariaDbIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="f4b2e-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4b2e-154">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f4b2e-155">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f4b2e-156">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f4b2e-157">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="f4b2e-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4b2e-158">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f4b2e-159">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f4b2e-160">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f4b2e-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f4b2e-162">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f4b2e-163">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="f4b2e-164">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f4b2e-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f4b2e-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4b2e-165">RELATED LINKS</span></span>

