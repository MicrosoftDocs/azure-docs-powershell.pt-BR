---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280655"
---
# <span data-ttu-id="8d7e0-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d7e0-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="8d7e0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8d7e0-102">SYNOPSIS</span></span>
<span data-ttu-id="8d7e0-103">Cria um novo espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-103">Creates a new workspace.</span></span>

## <span data-ttu-id="8d7e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d7e0-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d7e0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8d7e0-105">DESCRIPTION</span></span>
<span data-ttu-id="8d7e0-106">Cria um novo espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-106">Creates a new workspace.</span></span>

## <span data-ttu-id="8d7e0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8d7e0-107">EXAMPLES</span></span>

### <span data-ttu-id="8d7e0-108">Exemplo 1: criar um espaço de trabalho databricks</span><span class="sxs-lookup"><span data-stu-id="8d7e0-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="8d7e0-109">Esse comando cria um espaço de trabalho databricks.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="8d7e0-110">Exemplo 2: criar um espaço de trabalho databricks com uma rede virtual personalizada</span><span class="sxs-lookup"><span data-stu-id="8d7e0-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="8d7e0-111">Esse comando cria um espaço de trabalho databricks com uma rede virtual personalizada em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="8d7e0-112">Exemplo 3: criar um espaço de trabalho databricks com habilitar criptografia</span><span class="sxs-lookup"><span data-stu-id="8d7e0-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="8d7e0-113">Esse comando cria um espaço de trabalho databricks e o define para se preparar para a criptografia.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="8d7e0-114">Consulte os exemplos de Update-AzDatabricksWorkspace para obter mais configurações de criptografia.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="8d7e0-115">OS</span><span class="sxs-lookup"><span data-stu-id="8d7e0-115">PARAMETERS</span></span>

### <span data-ttu-id="8d7e0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d7e0-116">-AsJob</span></span>
<span data-ttu-id="8d7e0-117">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="8d7e0-117">Run the command as a job</span></span>

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

### <span data-ttu-id="8d7e0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d7e0-118">-DefaultProfile</span></span>
<span data-ttu-id="8d7e0-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d7e0-120">-Local</span><span class="sxs-lookup"><span data-stu-id="8d7e0-120">-Location</span></span>
<span data-ttu-id="8d7e0-121">A localização geográfica onde reside o recurso</span><span class="sxs-lookup"><span data-stu-id="8d7e0-121">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="8d7e0-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d7e0-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="8d7e0-123">O nome do grupo de recursos gerenciado.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-123">The managed resource group name.</span></span>

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

### <span data-ttu-id="8d7e0-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8d7e0-124">-Name</span></span>
<span data-ttu-id="8d7e0-125">O nome do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-125">The name of the workspace.</span></span>

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

### <span data-ttu-id="8d7e0-126">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8d7e0-126">-NoWait</span></span>
<span data-ttu-id="8d7e0-127">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="8d7e0-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8d7e0-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="8d7e0-128">-PrepareEncryption</span></span>
<span data-ttu-id="8d7e0-129">Preparar o espaço de trabalho para criptografia.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="8d7e0-130">Habilita a identidade gerenciada para a conta de armazenamento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="8d7e0-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="8d7e0-131">-PrivateSubnetName</span></span>
<span data-ttu-id="8d7e0-132">O nome da sub-rede particular dentro da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-132">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="8d7e0-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="8d7e0-133">-PublicSubnetName</span></span>
<span data-ttu-id="8d7e0-134">O nome de uma sub-rede pública na rede virtual.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-134">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="8d7e0-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="8d7e0-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="8d7e0-136">Um booliano que indica se o sistema de arquivos raiz DBFS será habilitado com camada secundária de criptografia com chaves gerenciadas pela plataforma para dados em repouso.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="8d7e0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d7e0-137">-ResourceGroupName</span></span>
<span data-ttu-id="8d7e0-138">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-138">The name of the resource group.</span></span>
<span data-ttu-id="8d7e0-139">O nome não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="8d7e0-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="8d7e0-140">-Sku</span></span>
<span data-ttu-id="8d7e0-141">O nome do SKU.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-141">The SKU name.</span></span>

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

### <span data-ttu-id="8d7e0-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d7e0-142">-SubscriptionId</span></span>
<span data-ttu-id="8d7e0-143">A ID da assinatura de destino.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-143">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="8d7e0-144">-Marca</span><span class="sxs-lookup"><span data-stu-id="8d7e0-144">-Tag</span></span>
<span data-ttu-id="8d7e0-145">Marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-145">Resource tags.</span></span>

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

### <span data-ttu-id="8d7e0-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8d7e0-146">-VirtualNetworkId</span></span>
<span data-ttu-id="8d7e0-147">A ID de uma rede virtual na qual esse cluster de databricks deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="8d7e0-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8d7e0-148">-Confirm</span></span>
<span data-ttu-id="8d7e0-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d7e0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d7e0-150">-WhatIf</span></span>
<span data-ttu-id="8d7e0-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d7e0-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d7e0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d7e0-153">CommonParameters</span></span>
<span data-ttu-id="8d7e0-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d7e0-155">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d7e0-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d7e0-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8d7e0-156">INPUTS</span></span>

## <span data-ttu-id="8d7e0-157">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8d7e0-157">OUTPUTS</span></span>

### <span data-ttu-id="8d7e0-158">Microsoft. Azure. PowerShell. cmdlets. databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="8d7e0-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="8d7e0-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8d7e0-159">NOTES</span></span>

<span data-ttu-id="8d7e0-160">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8d7e0-160">ALIASES</span></span>

## <span data-ttu-id="8d7e0-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8d7e0-161">RELATED LINKS</span></span>

