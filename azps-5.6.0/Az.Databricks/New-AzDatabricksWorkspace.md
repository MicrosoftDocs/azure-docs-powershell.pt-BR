---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: c49056da040e7259c1cbc0964335f157e00cbecd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886666"
---
# <span data-ttu-id="a8bdb-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="a8bdb-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="a8bdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="a8bdb-103">Cria um novo espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-103">Creates a new workspace.</span></span>

## <span data-ttu-id="a8bdb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a8bdb-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-EnableNoPublicIP] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a8bdb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a8bdb-105">DESCRIPTION</span></span>
<span data-ttu-id="a8bdb-106">Cria um novo espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-106">Creates a new workspace.</span></span>

## <span data-ttu-id="a8bdb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8bdb-107">EXAMPLES</span></span>

### <span data-ttu-id="a8bdb-108">Exemplo 1: Criar um espaço de trabalho Databricks</span><span class="sxs-lookup"><span data-stu-id="a8bdb-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="a8bdb-109">Este comando cria um espaço de trabalho Databricks.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="a8bdb-110">Exemplo 2: Criar um espaço de trabalho Databricks com uma rede virtual personalizada</span><span class="sxs-lookup"><span data-stu-id="a8bdb-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="a8bdb-111">Este comando cria um espaço de trabalho Databricks com rede virtual personalizada em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="a8bdb-112">Exemplo 3: Criar um espaço de trabalho Databricks com criptografia habilitada</span><span class="sxs-lookup"><span data-stu-id="a8bdb-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="a8bdb-113">Este comando cria um espaço de trabalho Databricks e o define para se preparar para criptografia.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="a8bdb-114">Consulte os exemplos de Update-AzDatabricksWorkspace para obter mais configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="a8bdb-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a8bdb-115">PARAMETERS</span></span>

### <span data-ttu-id="a8bdb-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8bdb-116">-AsJob</span></span>
<span data-ttu-id="a8bdb-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a8bdb-117">Run the command as a job</span></span>

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

### <span data-ttu-id="a8bdb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8bdb-118">-DefaultProfile</span></span>
<span data-ttu-id="a8bdb-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8bdb-120">-EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="a8bdb-120">-EnableNoPublicIP</span></span>
<span data-ttu-id="a8bdb-121">O valor que deve ser usado para este campo.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-121">The value which should be used for this field.</span></span>

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

### <span data-ttu-id="a8bdb-122">-Location</span><span class="sxs-lookup"><span data-stu-id="a8bdb-122">-Location</span></span>
<span data-ttu-id="a8bdb-123">A localização geográfica onde o recurso mora</span><span class="sxs-lookup"><span data-stu-id="a8bdb-123">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="a8bdb-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8bdb-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="a8bdb-125">O nome do grupo de recursos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="a8bdb-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a8bdb-126">-Name</span></span>
<span data-ttu-id="a8bdb-127">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-127">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8bdb-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a8bdb-128">-NoWait</span></span>
<span data-ttu-id="a8bdb-129">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a8bdb-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a8bdb-130">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="a8bdb-130">-PrepareEncryption</span></span>
<span data-ttu-id="a8bdb-131">Preparar o espaço de trabalho para criptografia.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-131">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="a8bdb-132">Habilita a Identidade Gerenciada para conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-132">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="a8bdb-133">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="a8bdb-133">-PrivateSubnetName</span></span>
<span data-ttu-id="a8bdb-134">O nome da Sub-rede Privada na Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-134">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="a8bdb-135">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="a8bdb-135">-PublicSubnetName</span></span>
<span data-ttu-id="a8bdb-136">O nome de uma sub-rede pública na Rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-136">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="a8bdb-137">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="a8bdb-137">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="a8bdb-138">Um booleano indicando se o sistema de arquivos raiz DBFS será ou não habilitado com camada secundária de criptografia com chaves gerenciadas da plataforma para dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-138">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="a8bdb-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8bdb-139">-ResourceGroupName</span></span>
<span data-ttu-id="a8bdb-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-140">The name of the resource group.</span></span>
<span data-ttu-id="a8bdb-141">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-141">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a8bdb-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="a8bdb-142">-Sku</span></span>
<span data-ttu-id="a8bdb-143">O nome SKU.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-143">The SKU name.</span></span>

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

### <span data-ttu-id="a8bdb-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8bdb-144">-SubscriptionId</span></span>
<span data-ttu-id="a8bdb-145">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a8bdb-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8bdb-146">-Tag</span></span>
<span data-ttu-id="a8bdb-147">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-147">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8bdb-148">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="a8bdb-148">-VirtualNetworkId</span></span>
<span data-ttu-id="a8bdb-149">A ID de uma Rede Virtual onde esse Cluster databricks deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-149">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="a8bdb-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8bdb-150">-Confirm</span></span>
<span data-ttu-id="a8bdb-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8bdb-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8bdb-152">-WhatIf</span></span>
<span data-ttu-id="a8bdb-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8bdb-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8bdb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8bdb-155">CommonParameters</span></span>
<span data-ttu-id="a8bdb-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8bdb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8bdb-157">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8bdb-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8bdb-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8bdb-158">INPUTS</span></span>

## <span data-ttu-id="a8bdb-159">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a8bdb-159">OUTPUTS</span></span>

### <span data-ttu-id="a8bdb-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="a8bdb-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="a8bdb-161">NOTES</span><span class="sxs-lookup"><span data-stu-id="a8bdb-161">NOTES</span></span>

<span data-ttu-id="a8bdb-162">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a8bdb-162">ALIASES</span></span>

## <span data-ttu-id="a8bdb-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8bdb-163">RELATED LINKS</span></span>

