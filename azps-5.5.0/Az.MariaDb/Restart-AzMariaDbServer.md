---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114271"
---
# <span data-ttu-id="51be0-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="51be0-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="51be0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51be0-102">SYNOPSIS</span></span>
<span data-ttu-id="51be0-103">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="51be0-103">Restarts a server.</span></span>

## <span data-ttu-id="51be0-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51be0-104">SYNTAX</span></span>

### <span data-ttu-id="51be0-105">Nomedo Servidor (Padrão)</span><span class="sxs-lookup"><span data-stu-id="51be0-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="51be0-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="51be0-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51be0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="51be0-107">DESCRIPTION</span></span>
<span data-ttu-id="51be0-108">Reinicia um servidor.</span><span class="sxs-lookup"><span data-stu-id="51be0-108">Restarts a server.</span></span>

## <span data-ttu-id="51be0-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="51be0-109">EXAMPLES</span></span>

### <span data-ttu-id="51be0-110">Exemplo 1: Reiniciar um MariaDB</span><span class="sxs-lookup"><span data-stu-id="51be0-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="51be0-111">Este comando reinicia um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="51be0-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="51be0-112">Exemplo 2: Reiniciar um MariaDB</span><span class="sxs-lookup"><span data-stu-id="51be0-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="51be0-113">Este comando reinicia um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="51be0-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="51be0-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51be0-114">PARAMETERS</span></span>

### <span data-ttu-id="51be0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51be0-115">-AsJob</span></span>
<span data-ttu-id="51be0-116">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="51be0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="51be0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51be0-117">-DefaultProfile</span></span>
<span data-ttu-id="51be0-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="51be0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51be0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51be0-119">-InputObject</span></span>
<span data-ttu-id="51be0-120">Parâmetro de Identidade Para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="51be0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51be0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="51be0-121">-Name</span></span>
<span data-ttu-id="51be0-122">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="51be0-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51be0-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="51be0-123">-NoWait</span></span>
<span data-ttu-id="51be0-124">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="51be0-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="51be0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51be0-125">-PassThru</span></span>
<span data-ttu-id="51be0-126">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="51be0-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="51be0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51be0-127">-ResourceGroupName</span></span>
<span data-ttu-id="51be0-128">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="51be0-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="51be0-129">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="51be0-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51be0-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51be0-130">-SubscriptionId</span></span>
<span data-ttu-id="51be0-131">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="51be0-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51be0-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="51be0-132">-Confirm</span></span>
<span data-ttu-id="51be0-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51be0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51be0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51be0-134">-WhatIf</span></span>
<span data-ttu-id="51be0-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="51be0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51be0-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51be0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51be0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51be0-137">CommonParameters</span></span>
<span data-ttu-id="51be0-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51be0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51be0-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51be0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51be0-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="51be0-140">INPUTS</span></span>

### <span data-ttu-id="51be0-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="51be0-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="51be0-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="51be0-142">OUTPUTS</span></span>

### <span data-ttu-id="51be0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51be0-143">System.Boolean</span></span>

## <span data-ttu-id="51be0-144">Notas</span><span class="sxs-lookup"><span data-stu-id="51be0-144">NOTES</span></span>

<span data-ttu-id="51be0-145">Aliases</span><span class="sxs-lookup"><span data-stu-id="51be0-145">ALIASES</span></span>

<span data-ttu-id="51be0-146">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="51be0-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="51be0-147">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="51be0-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="51be0-148">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="51be0-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="51be0-149">INPUTOBJECT: <IMariaDbIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="51be0-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="51be0-150">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="51be0-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="51be0-151">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="51be0-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="51be0-152">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="51be0-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="51be0-153">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="51be0-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="51be0-154">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="51be0-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="51be0-155">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="51be0-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="51be0-156">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="51be0-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="51be0-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="51be0-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="51be0-158">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="51be0-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="51be0-159">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="51be0-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="51be0-160">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="51be0-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="51be0-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51be0-161">RELATED LINKS</span></span>

