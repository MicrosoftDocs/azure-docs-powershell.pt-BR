---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 7abc847bebf5baeea1bf12db6d930bd2daa34d7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885465"
---
# <span data-ttu-id="7774f-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="7774f-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="7774f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7774f-102">SYNOPSIS</span></span>
<span data-ttu-id="7774f-103">Cria um namespace de Hubs de Eventos.</span><span class="sxs-lookup"><span data-stu-id="7774f-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="7774f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7774f-104">SYNTAX</span></span>

### <span data-ttu-id="7774f-105">NamespaceParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7774f-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7774f-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="7774f-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7774f-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7774f-107">DESCRIPTION</span></span>
<span data-ttu-id="7774f-108">O New-AzEventHubNamespace cmdlet cria um novo namespace do tipo Hubs de Eventos.</span><span class="sxs-lookup"><span data-stu-id="7774f-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="7774f-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7774f-109">EXAMPLES</span></span>
### <span data-ttu-id="7774f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7774f-110">Example 1</span></span>                                           
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/14/2020 9:02:16 PM
UpdatedAt                     : 6/14/2020 9:03:04 PM
ServiceBusEndpoint            : https://testingnew2018.servicebus.windows.net:443/
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : False
MaximumThroughputUnits        : 0
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7774f-111">Cria um namespace De hubs de eventos MyNamespaceName na localização geográfica especificada MyLocation , no grupo de recursos \` \` \` \` \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7774f-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7774f-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7774f-112">Example 2</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7774f-113">Cria um namespace de Hubs de Eventos MyNamespaceName na localização geográfica especificada MyLocation , no grupo de recursos \` \` \` \` \` MyResourceGroupName e AutoInflate está habilitado com \` MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="7774f-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="7774f-114">Exemplo 3: namespace habilitado para Kafka</span><span class="sxs-lookup"><span data-stu-id="7774f-114">Example 3: Kafka enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7774f-115">Cria um namespace de Hubs de Eventos MyNamespaceName na localização geográfica especificada MyLocation , no grupo de recursos \` \` \` \` \` MyResourceGroupName com \` Kafka e AutoInflate habilitados.</span><span class="sxs-lookup"><span data-stu-id="7774f-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="7774f-116">Exemplo 4: Namespace habilitado para ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7774f-116">Example 4: ZoneRedundant enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -ZoneRedundant

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : True
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="7774f-117">Cria um namespace de Hubs de Eventos MyNamespaceName na localização geográfica especificada MyLocation , no grupo de recursos \` \` \` \` \` MyResourceGroupName com \` Kafka e AutoInflate habilitados.</span><span class="sxs-lookup"><span data-stu-id="7774f-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="7774f-118">Exemplo 5: Criando Namespace com Gerenciar Identidade em um cluster</span><span class="sxs-lookup"><span data-stu-id="7774f-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
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
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
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
PS C:\>$getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
PS C:\> $key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperties @(@($key.Name, $keyvault.VaultUri,""))

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

## <span data-ttu-id="7774f-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7774f-119">PARAMETERS</span></span>

### <span data-ttu-id="7774f-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="7774f-120">-ClusterARMId</span></span>
<span data-ttu-id="7774f-121">ARM ID do Cluster onde o namespace deve ser criado</span><span class="sxs-lookup"><span data-stu-id="7774f-121">ARM ID of Cluster where namespace is to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7774f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7774f-122">-DefaultProfile</span></span>
<span data-ttu-id="7774f-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7774f-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7774f-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="7774f-124">-EnableAutoInflate</span></span>
<span data-ttu-id="7774f-125">Indica se a AutoInflate está habilitada</span><span class="sxs-lookup"><span data-stu-id="7774f-125">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7774f-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="7774f-126">-EnableKafka</span></span>
<span data-ttu-id="7774f-127">habilitando ou desabilitando o Kafka para namespace</span><span class="sxs-lookup"><span data-stu-id="7774f-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="7774f-128">-Identity</span><span class="sxs-lookup"><span data-stu-id="7774f-128">-Identity</span></span>
<span data-ttu-id="7774f-129">habilitando ou desabilitando a Identidade para namespace</span><span class="sxs-lookup"><span data-stu-id="7774f-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="7774f-130">-Location</span><span class="sxs-lookup"><span data-stu-id="7774f-130">-Location</span></span>
<span data-ttu-id="7774f-131">Local do Namespace EventHub.</span><span class="sxs-lookup"><span data-stu-id="7774f-131">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="7774f-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="7774f-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="7774f-133">Limite superior de unidades de transferência quando AutoInflate estiver habilitado, o valor deve estar dentro de 0 a 20 unidades de transferência.</span><span class="sxs-lookup"><span data-stu-id="7774f-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7774f-134">-Name</span><span class="sxs-lookup"><span data-stu-id="7774f-134">-Name</span></span>
<span data-ttu-id="7774f-135">Nome do Namespace EventHub.</span><span class="sxs-lookup"><span data-stu-id="7774f-135">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="7774f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7774f-136">-ResourceGroupName</span></span>
<span data-ttu-id="7774f-137">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7774f-137">Resource Group Name</span></span>

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

### <span data-ttu-id="7774f-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="7774f-138">-SkuCapacity</span></span>
<span data-ttu-id="7774f-139">As unidades de transferência eventhub.</span><span class="sxs-lookup"><span data-stu-id="7774f-139">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="7774f-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7774f-140">-SkuName</span></span>
<span data-ttu-id="7774f-141">Namespace Sku Name.</span><span class="sxs-lookup"><span data-stu-id="7774f-141">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="7774f-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="7774f-142">-Tag</span></span>
<span data-ttu-id="7774f-143">Hashtables que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="7774f-143">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7774f-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="7774f-144">-ZoneRedundant</span></span>
<span data-ttu-id="7774f-145">habilitando ou desabilitando Zona Redundante para namespace</span><span class="sxs-lookup"><span data-stu-id="7774f-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="7774f-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7774f-146">-Confirm</span></span>
<span data-ttu-id="7774f-147">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7774f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7774f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7774f-148">-WhatIf</span></span>
<span data-ttu-id="7774f-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7774f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7774f-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7774f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7774f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7774f-151">CommonParameters</span></span>
<span data-ttu-id="7774f-152">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7774f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7774f-153">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7774f-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7774f-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7774f-154">INPUTS</span></span>

### <span data-ttu-id="7774f-155">System.String</span><span class="sxs-lookup"><span data-stu-id="7774f-155">System.String</span></span>

### <span data-ttu-id="7774f-156">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7774f-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7774f-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7774f-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7774f-158">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7774f-158">OUTPUTS</span></span>

### <span data-ttu-id="7774f-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="7774f-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="7774f-160">NOTES</span><span class="sxs-lookup"><span data-stu-id="7774f-160">NOTES</span></span>

## <span data-ttu-id="7774f-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7774f-161">RELATED LINKS</span></span>
