---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbFirewallRule.md
ms.openlocfilehash: 00da9023a7ed6607993af3faadccfbddbb784526
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114273"
---
# <span data-ttu-id="9c6ba-101">New-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9c6ba-101">New-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="9c6ba-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c6ba-102">SYNOPSIS</span></span>
<span data-ttu-id="9c6ba-103">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-103">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="9c6ba-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c6ba-104">SYNTAX</span></span>

### <span data-ttu-id="9c6ba-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="9c6ba-105">CreateExpanded (Default)</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -EndIPAddress <String>
 -StartIPAddress <String> [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9c6ba-106">AllowAll</span><span class="sxs-lookup"><span data-stu-id="9c6ba-106">AllowAll</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -AllowAll [-Name <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9c6ba-107">ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9c6ba-107">ClientIPAddress</span></span>
```
New-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> -ClientIPAddress <String>
 [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c6ba-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c6ba-108">DESCRIPTION</span></span>
<span data-ttu-id="9c6ba-109">Cria uma nova regra de firewall ou atualiza uma regra de firewall existente.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-109">Creates a new firewall rule or updates an existing firewall rule.</span></span>

## <span data-ttu-id="9c6ba-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9c6ba-110">EXAMPLES</span></span>

### <span data-ttu-id="9c6ba-111">Exemplo 1: Criar uma regra de firewall sob um MariaDB</span><span class="sxs-lookup"><span data-stu-id="9c6ba-111">Example 1: Create a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -Name firewall-101 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -EndIPAddress 0.0.2.255 -StartIPAddress 0.0.2.1

Name         StartIPAddress EndIPAddress
----         -------------- ------------
firewall-101 0.0.2.1        0.0.2.255
```

<span data-ttu-id="9c6ba-112">Esse comando cria uma regra de firewall sob um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-112">This command creates a firewall rule under a MariaDB.</span></span>

### <span data-ttu-id="9c6ba-113">Exemplo 2: Crie uma nova Regra de Firewall MariaDB usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-113">Example 2: Create a new MariaDB Firewall Rule using -ClientIPAddress.</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -ClientIPAddress 0.0.0.1

Name                                StartIPAddress EndIPAddress
----                                -------------- ------------
ClientIPAddress_2020-08-11_18-19-27 0.0.0.1        0.0.0.1
```

<span data-ttu-id="9c6ba-114">Esse cmdlets criam uma Regra de Firewall mariadb usando -ClientIPAddress.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-114">This cmdlets create a MariaDB Firewall Rule using -ClientIPAddress.</span></span>

### <span data-ttu-id="9c6ba-115">Exemplo 3: Criar uma nova Regra de Firewall do MariaDB para permitir todos os IPs</span><span class="sxs-lookup"><span data-stu-id="9c6ba-115">Example 3: Create a new MariaDB Firewall Rule to allow all IPs</span></span>
```powershell
PS C:\> New-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-asd-01 -AllowAll

Name                         StartIPAddress EndIPAddress
----                         -------------- ------------
AllowAll_2020-08-11_18-19-27 0.0.0.0        255.255.255.255
```

<span data-ttu-id="9c6ba-116">Esses cmdlets criam uma nova Regra de Firewall de MariaDB para permitir todos os IPs.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-116">This cmdlets create a new MariaDB Firewall Rule to allow all IPs.</span></span>

## <span data-ttu-id="9c6ba-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c6ba-117">PARAMETERS</span></span>

### <span data-ttu-id="9c6ba-118">-AllowAll</span><span class="sxs-lookup"><span data-stu-id="9c6ba-118">-AllowAll</span></span>
<span data-ttu-id="9c6ba-119">Apresentar para permitir todos os IPs de intervalo, de 0.0.0.0 a 255.255.255.255.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-119">Present to allow all range IPs, from 0.0.0.0 to 255.255.255.255.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AllowAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c6ba-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c6ba-120">-AsJob</span></span>
<span data-ttu-id="9c6ba-121">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="9c6ba-121">Run the command as a job</span></span>

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

### <span data-ttu-id="9c6ba-122">-ClientIPAddress</span><span class="sxs-lookup"><span data-stu-id="9c6ba-122">-ClientIPAddress</span></span>
<span data-ttu-id="9c6ba-123">O cliente especificou um ÚNICO IP da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-123">Client specified single IP of the server firewall rule.</span></span>
<span data-ttu-id="9c6ba-124">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-124">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: ClientIPAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c6ba-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c6ba-125">-DefaultProfile</span></span>
<span data-ttu-id="9c6ba-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c6ba-127">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="9c6ba-127">-EndIPAddress</span></span>
<span data-ttu-id="9c6ba-128">O endereço IP final da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-128">The end IP address of the server firewall rule.</span></span>
<span data-ttu-id="9c6ba-129">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c6ba-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c6ba-130">-Name</span></span>
<span data-ttu-id="9c6ba-131">O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-131">The name of the server firewall rule.</span></span>
<span data-ttu-id="9c6ba-132">Se não especificado, o padrão será indefinido.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-132">If not specified, the default is undefined.</span></span>
<span data-ttu-id="9c6ba-133">Se AllowAll estiver presente, o nome padrão será AllowAll_yyyy-MM-dd_HH-mm-ss.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-133">If AllowAll is present, the default name is AllowAll_yyyy-MM-dd_HH-mm-ss.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c6ba-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9c6ba-134">-NoWait</span></span>
<span data-ttu-id="9c6ba-135">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="9c6ba-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9c6ba-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c6ba-136">-ResourceGroupName</span></span>
<span data-ttu-id="9c6ba-137">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-137">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9c6ba-138">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-138">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c6ba-139">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9c6ba-139">-ServerName</span></span>
<span data-ttu-id="9c6ba-140">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-140">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c6ba-141">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="9c6ba-141">-StartIPAddress</span></span>
<span data-ttu-id="9c6ba-142">O endereço IP inicial da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-142">The start IP address of the server firewall rule.</span></span>
<span data-ttu-id="9c6ba-143">Deve ser o formato IPv4.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-143">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c6ba-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c6ba-144">-SubscriptionId</span></span>
<span data-ttu-id="9c6ba-145">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-145">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c6ba-146">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9c6ba-146">-Confirm</span></span>
<span data-ttu-id="9c6ba-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c6ba-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c6ba-148">-WhatIf</span></span>
<span data-ttu-id="9c6ba-149">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c6ba-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c6ba-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c6ba-151">CommonParameters</span></span>
<span data-ttu-id="9c6ba-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c6ba-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c6ba-153">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c6ba-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c6ba-154">Entradas</span><span class="sxs-lookup"><span data-stu-id="9c6ba-154">INPUTS</span></span>

## <span data-ttu-id="9c6ba-155">Saídas</span><span class="sxs-lookup"><span data-stu-id="9c6ba-155">OUTPUTS</span></span>

### <span data-ttu-id="9c6ba-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9c6ba-156">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="9c6ba-157">Notas</span><span class="sxs-lookup"><span data-stu-id="9c6ba-157">NOTES</span></span>

<span data-ttu-id="9c6ba-158">Aliases</span><span class="sxs-lookup"><span data-stu-id="9c6ba-158">ALIASES</span></span>

## <span data-ttu-id="9c6ba-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c6ba-159">RELATED LINKS</span></span>

