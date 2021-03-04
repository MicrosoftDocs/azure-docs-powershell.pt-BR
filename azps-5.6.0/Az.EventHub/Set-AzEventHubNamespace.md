---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 6afbd081eca842e2185428f90a18932e05c3bbe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889472"
---
# <span data-ttu-id="476a0-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="476a0-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="476a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="476a0-102">SYNOPSIS</span></span>
<span data-ttu-id="476a0-103">Atualiza o namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="476a0-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="476a0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="476a0-104">SYNTAX</span></span>

### <span data-ttu-id="476a0-105">NamespaceParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="476a0-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476a0-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="476a0-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="476a0-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="476a0-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="476a0-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="476a0-108">DESCRIPTION</span></span>
<span data-ttu-id="476a0-109">O Set-AzEventHubNamespace cmdlet atualiza as propriedades do namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="476a0-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="476a0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="476a0-110">EXAMPLES</span></span>

### <span data-ttu-id="476a0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="476a0-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="476a0-112">Atualiza as Marcas do namespace \` MyNamespaceName \` para Created .</span><span class="sxs-lookup"><span data-stu-id="476a0-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="476a0-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="476a0-113">Example 2</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10 

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="476a0-114">Atualiza o estado do namespace \` MyNamespaceName \` com AutoInflate = habilitado e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="476a0-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="476a0-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="476a0-115">Example 3</span></span>

<span data-ttu-id="476a0-116">Atualiza o namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="476a0-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="476a0-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="476a0-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="476a0-118">Exemplo 5: Criar e atualizar Namespace com Gerenciar Identidade em um cluster</span><span class="sxs-lookup"><span data-stu-id="476a0-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation --EnableAutoInflate -MaximumThroughputUnits 12 -EnableKafka -ZoneRedundant -Identity

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 12
ZoneRedundant                 : True
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity.PrincipalId          : ##########
Identity.TenantId             : ##########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :

# Get created namespace
PS C:\> $getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
$key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperty @(@($key.Name, $keyvault.VaultUri,""))

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          : #########
Identity.TenantId             : #########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          : MicrosoftKeyVault
Encryption.KeyVaultProperties : {testkey, https://myvaultname.vault.azure.net, }
```

## <span data-ttu-id="476a0-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="476a0-119">PARAMETERS</span></span>

### <span data-ttu-id="476a0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476a0-120">-DefaultProfile</span></span>
<span data-ttu-id="476a0-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="476a0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="476a0-122">-EnableAutoInflate</span></span>
<span data-ttu-id="476a0-123">Indica se a AutoInflate está habilitada</span><span class="sxs-lookup"><span data-stu-id="476a0-123">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="476a0-124">-EnableKafka</span></span>
<span data-ttu-id="476a0-125">habilitando ou desabilitando o Kafka para namespace</span><span class="sxs-lookup"><span data-stu-id="476a0-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="476a0-126">-Identity</span><span class="sxs-lookup"><span data-stu-id="476a0-126">-Identity</span></span>
<span data-ttu-id="476a0-127">habilitando ou desabilitando a Identidade para namespace</span><span class="sxs-lookup"><span data-stu-id="476a0-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="476a0-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="476a0-128">-IdentityUserDefined</span></span>
<span data-ttu-id="476a0-129">Identidade definida pelo usuário ou Nenhuma</span><span class="sxs-lookup"><span data-stu-id="476a0-129">User defined Identity or None</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-130">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="476a0-130">-KeyProperty</span></span>
<span data-ttu-id="476a0-131">Lista de propriedades de chave, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span><span class="sxs-lookup"><span data-stu-id="476a0-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String[]]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-132">-KeySource</span><span class="sxs-lookup"><span data-stu-id="476a0-132">-KeySource</span></span>
<span data-ttu-id="476a0-133">Origem da chave</span><span class="sxs-lookup"><span data-stu-id="476a0-133">Key Source</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-134">-Location</span><span class="sxs-lookup"><span data-stu-id="476a0-134">-Location</span></span>
<span data-ttu-id="476a0-135">Local do Namespace EventHub.</span><span class="sxs-lookup"><span data-stu-id="476a0-135">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="476a0-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="476a0-137">Limite superior de unidades de transferência quando AutoInflate estiver habilitado, o valor deve estar dentro de 0 a 20 unidades de transferência.</span><span class="sxs-lookup"><span data-stu-id="476a0-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-138">-Name</span><span class="sxs-lookup"><span data-stu-id="476a0-138">-Name</span></span>
<span data-ttu-id="476a0-139">Nome do Namespace EventHub.</span><span class="sxs-lookup"><span data-stu-id="476a0-139">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="476a0-140">-ResourceGroupName</span></span>
<span data-ttu-id="476a0-141">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="476a0-141">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="476a0-142">-SkuCapacity</span></span>
<span data-ttu-id="476a0-143">As unidades de transferência eventhub.</span><span class="sxs-lookup"><span data-stu-id="476a0-143">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="476a0-144">-SkuName</span></span>
<span data-ttu-id="476a0-145">Namespace Sku Name.</span><span class="sxs-lookup"><span data-stu-id="476a0-145">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-146">-State</span><span class="sxs-lookup"><span data-stu-id="476a0-146">-State</span></span>
<span data-ttu-id="476a0-147">Desabilitar/Habilitar Namespace.</span><span class="sxs-lookup"><span data-stu-id="476a0-147">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="476a0-148">-Tag</span></span>
<span data-ttu-id="476a0-149">Hashtables que representa a marca de recurso.</span><span class="sxs-lookup"><span data-stu-id="476a0-149">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="476a0-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="476a0-150">-Confirm</span></span>
<span data-ttu-id="476a0-151">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="476a0-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="476a0-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="476a0-152">-WhatIf</span></span>
<span data-ttu-id="476a0-153">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="476a0-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="476a0-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="476a0-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="476a0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476a0-155">CommonParameters</span></span>
<span data-ttu-id="476a0-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476a0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476a0-157">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="476a0-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476a0-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="476a0-158">INPUTS</span></span>

### <span data-ttu-id="476a0-159">System.String</span><span class="sxs-lookup"><span data-stu-id="476a0-159">System.String</span></span>

### <span data-ttu-id="476a0-160">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="476a0-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="476a0-161">System.Nullable'1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="476a0-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="476a0-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="476a0-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="476a0-163">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="476a0-163">OUTPUTS</span></span>

### <span data-ttu-id="476a0-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="476a0-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="476a0-165">NOTES</span><span class="sxs-lookup"><span data-stu-id="476a0-165">NOTES</span></span>

## <span data-ttu-id="476a0-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="476a0-166">RELATED LINKS</span></span>
