---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114277"
---
# <span data-ttu-id="f2044-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f2044-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="f2044-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2044-102">SYNOPSIS</span></span>
<span data-ttu-id="f2044-103">Recebe uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f2044-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="f2044-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2044-104">SYNTAX</span></span>

### <span data-ttu-id="f2044-105">Lista (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f2044-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f2044-106">Obter</span><span class="sxs-lookup"><span data-stu-id="f2044-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f2044-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f2044-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="f2044-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f2044-108">DESCRIPTION</span></span>
<span data-ttu-id="f2044-109">Recebe uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f2044-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="f2044-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f2044-110">EXAMPLES</span></span>

### <span data-ttu-id="f2044-111">Exemplo 1: Listar todas as regras de rede virtual sob um MariaDB</span><span class="sxs-lookup"><span data-stu-id="f2044-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="f2044-112">Esse comando lista todas as regras de rede virtual sob um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f2044-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="f2044-113">Exemplo 2: Obter regra de rede virtual sob um MariaDB</span><span class="sxs-lookup"><span data-stu-id="f2044-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="f2044-114">Esse comando obtém uma regra de rede virtual sob um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="f2044-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="f2044-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2044-115">PARAMETERS</span></span>

### <span data-ttu-id="f2044-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2044-116">-DefaultProfile</span></span>
<span data-ttu-id="f2044-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2044-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2044-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2044-118">-InputObject</span></span>
<span data-ttu-id="f2044-119">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="f2044-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2044-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2044-120">-Name</span></span>
<span data-ttu-id="f2044-121">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f2044-121">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2044-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2044-122">-PassThru</span></span>
<span data-ttu-id="f2044-123">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="f2044-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f2044-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2044-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2044-125">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f2044-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="f2044-126">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="f2044-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2044-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f2044-127">-ServerName</span></span>
<span data-ttu-id="f2044-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f2044-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2044-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f2044-129">-SubscriptionId</span></span>
<span data-ttu-id="f2044-130">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2044-130">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2044-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2044-131">CommonParameters</span></span>
<span data-ttu-id="f2044-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2044-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2044-133">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2044-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2044-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="f2044-134">INPUTS</span></span>

### <span data-ttu-id="f2044-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="f2044-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="f2044-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="f2044-136">OUTPUTS</span></span>

### <span data-ttu-id="f2044-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f2044-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="f2044-138">Notas</span><span class="sxs-lookup"><span data-stu-id="f2044-138">NOTES</span></span>

<span data-ttu-id="f2044-139">Aliases</span><span class="sxs-lookup"><span data-stu-id="f2044-139">ALIASES</span></span>

<span data-ttu-id="f2044-140">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="f2044-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f2044-141">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="f2044-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f2044-142">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f2044-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f2044-143">INPUTOBJECT: <IMariaDbIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="f2044-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f2044-144">`[ConfigurationName <String>]`: o nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="f2044-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="f2044-145">`[DatabaseName <String>]`: o nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="f2044-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="f2044-146">`[FirewallRuleName <String>]`: o nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="f2044-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="f2044-147">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="f2044-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f2044-148">`[LocationName <String>]`: o nome do local.</span><span class="sxs-lookup"><span data-stu-id="f2044-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="f2044-149">`[ResourceGroupName <String>]`: o nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="f2044-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="f2044-150">Você pode obter esse valor da API do Gerenciador de Recursos do Azure ou do portal.</span><span class="sxs-lookup"><span data-stu-id="f2044-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="f2044-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: o nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="f2044-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="f2044-152">`[ServerName <String>]`: o nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="f2044-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="f2044-153">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2044-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="f2044-154">`[VirtualNetworkRuleName <String>]`: o nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f2044-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="f2044-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2044-155">RELATED LINKS</span></span>

