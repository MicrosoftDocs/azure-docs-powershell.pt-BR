---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94124846"
---
# <span data-ttu-id="64182-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="64182-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="64182-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64182-102">SYNOPSIS</span></span>
<span data-ttu-id="64182-103">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="64182-103">Gets information about a server.</span></span>

## <span data-ttu-id="64182-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64182-104">SYNTAX</span></span>

### <span data-ttu-id="64182-105">List1 (padrão)</span><span class="sxs-lookup"><span data-stu-id="64182-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64182-106">Obter</span><span class="sxs-lookup"><span data-stu-id="64182-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64182-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="64182-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="64182-108">Programação</span><span class="sxs-lookup"><span data-stu-id="64182-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="64182-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64182-109">DESCRIPTION</span></span>
<span data-ttu-id="64182-110">Obtém informações sobre um servidor.</span><span class="sxs-lookup"><span data-stu-id="64182-110">Gets information about a server.</span></span>

## <span data-ttu-id="64182-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64182-111">EXAMPLES</span></span>

### <span data-ttu-id="64182-112">Exemplo 1: listar todas as MariaDB em assinaturas</span><span class="sxs-lookup"><span data-stu-id="64182-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="64182-113">Esse comando lista todas as MariaDB em uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="64182-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="64182-114">Exemplo 2: listar todas as MariaDB em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="64182-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="64182-115">Esse comando lista todas as MariaDB em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64182-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="64182-116">Exemplo 3: obter um MariaDB</span><span class="sxs-lookup"><span data-stu-id="64182-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="64182-117">Esse comando obtém um MariaDB.</span><span class="sxs-lookup"><span data-stu-id="64182-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="64182-118">OS</span><span class="sxs-lookup"><span data-stu-id="64182-118">PARAMETERS</span></span>

### <span data-ttu-id="64182-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64182-119">-DefaultProfile</span></span>
<span data-ttu-id="64182-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64182-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64182-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64182-121">-InputObject</span></span>
<span data-ttu-id="64182-122">Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="64182-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="64182-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="64182-123">-Name</span></span>
<span data-ttu-id="64182-124">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="64182-124">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64182-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64182-125">-ResourceGroupName</span></span>
<span data-ttu-id="64182-126">O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="64182-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="64182-127">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="64182-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="64182-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="64182-128">-SubscriptionId</span></span>
<span data-ttu-id="64182-129">A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="64182-129">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64182-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64182-130">CommonParameters</span></span>
<span data-ttu-id="64182-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64182-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64182-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64182-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64182-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64182-133">INPUTS</span></span>

### <span data-ttu-id="64182-134">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="64182-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="64182-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64182-135">OUTPUTS</span></span>

### <span data-ttu-id="64182-136">Microsoft. Azure. PowerShell. cmdlets. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="64182-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="64182-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64182-137">NOTES</span></span>

<span data-ttu-id="64182-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="64182-138">ALIASES</span></span>

<span data-ttu-id="64182-139">PROPRIEDADES DE PARÂMETROS COMPLEXAS</span><span class="sxs-lookup"><span data-stu-id="64182-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="64182-140">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="64182-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="64182-141">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="64182-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="64182-142">INPUTobject <IMariaDbIdentity> : parâmetro de identidade</span><span class="sxs-lookup"><span data-stu-id="64182-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="64182-143">`[ConfigurationName <String>]`: O nome da configuração do servidor.</span><span class="sxs-lookup"><span data-stu-id="64182-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="64182-144">`[DatabaseName <String>]`: O nome do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="64182-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="64182-145">`[FirewallRuleName <String>]`: O nome da regra de firewall do servidor.</span><span class="sxs-lookup"><span data-stu-id="64182-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="64182-146">`[Id <String>]`: Caminho de identidade do recurso</span><span class="sxs-lookup"><span data-stu-id="64182-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="64182-147">`[LocationName <String>]`: O nome do local.</span><span class="sxs-lookup"><span data-stu-id="64182-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="64182-148">`[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso.</span><span class="sxs-lookup"><span data-stu-id="64182-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="64182-149">Você pode obter esse valor da API do Azure Resource Manager ou do Portal.</span><span class="sxs-lookup"><span data-stu-id="64182-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="64182-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: O nome da política de alerta de segurança.</span><span class="sxs-lookup"><span data-stu-id="64182-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="64182-151">`[ServerName <String>]`: O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="64182-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="64182-152">`[SubscriptionId <String>]`: A ID da assinatura que identifica uma assinatura do Azure.</span><span class="sxs-lookup"><span data-stu-id="64182-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="64182-153">`[VirtualNetworkRuleName <String>]`: O nome da regra de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="64182-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="64182-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64182-154">RELATED LINKS</span></span>

