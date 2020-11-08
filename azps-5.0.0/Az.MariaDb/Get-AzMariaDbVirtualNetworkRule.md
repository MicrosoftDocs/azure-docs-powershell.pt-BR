---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124844"
---
# <span data-ttu-id="48093-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="48093-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="48093-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48093-102">SYNOPSIS</span></span>
<span data-ttu-id="48093-103">Obtém uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="48093-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="48093-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48093-104">SYNTAX</span></span>

### <span data-ttu-id="48093-105">Lista (padrão)</span><span class="sxs-lookup"><span data-stu-id="48093-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="48093-106">Obter</span><span class="sxs-lookup"><span data-stu-id="48093-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="48093-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48093-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="48093-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48093-108">DESCRIPTION</span></span>
<span data-ttu-id="48093-109">Obtém uma regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="48093-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="48093-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48093-110">EXAMPLES</span></span>

### <span data-ttu-id="48093-111">Exemplo 1: listar todas as regras de rede virtual em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="48093-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="48093-112">Esse comando lista todas as regras de rede virtual em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="48093-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="48093-113">Exemplo 2: obter regra de rede virtual em um MariaDB</span><span class="sxs-lookup"><span data-stu-id="48093-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="48093-114">Esse comando obtém uma regra de rede virtual em um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="48093-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="48093-115">OS</span><span class="sxs-lookup"><span data-stu-id="48093-115">PARAMETERS</span></span>

### <span data-ttu-id="48093-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48093-116">-DefaultProfile</span></span>
<span data-ttu-id="48093-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48093-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48093-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48093-118">-InputObject</span></span>
<span data-ttu-id="48093-119">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="48093-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="48093-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="48093-120">-Name</span></span>
<span data-ttu-id="48093-121">O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="48093-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="48093-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48093-122">-PassThru</span></span>
<span data-ttu-id="48093-123">Retorna verdadeiro quando o comando é bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="48093-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="48093-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48093-124">-ResourceGroupName</span></span>
<span data-ttu-id="48093-125">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="48093-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="48093-126">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="48093-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="48093-127">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="48093-127">-ServerName</span></span>
<span data-ttu-id="48093-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="48093-128">The name of the server.</span></span>

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

### <span data-ttu-id="48093-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48093-129">-SubscriptionId</span></span>
<span data-ttu-id="48093-130">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="48093-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="48093-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48093-131">CommonParameters</span></span>
<span data-ttu-id="48093-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48093-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48093-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48093-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48093-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48093-134">INPUTS</span></span>

### <span data-ttu-id="48093-135">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="48093-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="48093-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48093-136">OUTPUTS</span></span>

### <span data-ttu-id="48093-137">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="48093-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="48093-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48093-138">NOTES</span></span>

<span data-ttu-id="48093-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="48093-139">ALIASES</span></span>

<span data-ttu-id="48093-140">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="48093-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="48093-141">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="48093-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48093-142">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="48093-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="48093-143">INPUTobject <IMariaDbIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="48093-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="48093-144">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="48093-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="48093-145">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="48093-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="48093-146">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="48093-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="48093-147">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="48093-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48093-148">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="48093-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="48093-149">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="48093-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="48093-150">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="48093-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="48093-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="48093-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="48093-152">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="48093-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="48093-153">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="48093-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="48093-154">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="48093-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="48093-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48093-155">RELATED LINKS</span></span>

