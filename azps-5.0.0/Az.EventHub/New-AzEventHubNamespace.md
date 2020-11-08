---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: a51fffe36102b05121e52054103357bd26f56d51
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115464"
---
# <span data-ttu-id="a79ce-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="a79ce-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="a79ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a79ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a79ce-103">Cria um namespace de hubs de eventos.</span><span class="sxs-lookup"><span data-stu-id="a79ce-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="a79ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a79ce-104">SYNTAX</span></span>

### <span data-ttu-id="a79ce-105">NamespaceParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="a79ce-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a79ce-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="a79ce-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a79ce-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a79ce-107">DESCRIPTION</span></span>
<span data-ttu-id="a79ce-108">O cmdlet New-AzEventHubNamespace cria um novo namespace de hubs de eventos de tipo.</span><span class="sxs-lookup"><span data-stu-id="a79ce-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="a79ce-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a79ce-109">EXAMPLES</span></span>
### <span data-ttu-id="a79ce-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a79ce-110">Example 1</span></span>                                           
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

<span data-ttu-id="a79ce-111">Cria um namespace de hubs \` de evento Mynamespacename \` na localização geográfica especificada \` MyLocation \` , na MyResourceGroupName do grupo de recursos \` \` .</span><span class="sxs-lookup"><span data-stu-id="a79ce-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="a79ce-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a79ce-112">Example 2</span></span>
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

<span data-ttu-id="a79ce-113">Cria um namespace de hubs de evento \` Mynamespacename \` na localização geográfica especificada \` MyLocation \` , no grupo de recursos \` MyResourceGroupName \` e autoinflate são habilitados com MaximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="a79ce-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="a79ce-114">Exemplo 3: namespace habilitado para Kafka</span><span class="sxs-lookup"><span data-stu-id="a79ce-114">Example 3: Kafka enabled namespace</span></span>
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

<span data-ttu-id="a79ce-115">Cria um namespace de hubs \` de evento Mynamespacename \` na localização geográfica especificada \` MyLocation \` , no grupo de recursos \` MyResourceGroupName \` com Kafka e autoinflate habilitado.</span><span class="sxs-lookup"><span data-stu-id="a79ce-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="a79ce-116">Exemplo 4: namespace habilitado para ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a79ce-116">Example 4: ZoneRedundant enabled namespace</span></span>
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

<span data-ttu-id="a79ce-117">Cria um namespace de hubs \` de evento Mynamespacename \` na localização geográfica especificada \` MyLocation \` , no grupo de recursos \` MyResourceGroupName \` com Kafka e autoinflate habilitado.</span><span class="sxs-lookup"><span data-stu-id="a79ce-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="a79ce-118">Exemplo 5: criando namespace com gerenciar identidade em um cluster</span><span class="sxs-lookup"><span data-stu-id="a79ce-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
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

## <span data-ttu-id="a79ce-119">OS</span><span class="sxs-lookup"><span data-stu-id="a79ce-119">PARAMETERS</span></span>

### <span data-ttu-id="a79ce-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="a79ce-120">-ClusterARMId</span></span>
<span data-ttu-id="a79ce-121">ID do braço do cluster onde o namespace deve ser criado</span><span class="sxs-lookup"><span data-stu-id="a79ce-121">ARM ID of Cluster where namespace is to be created</span></span>

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

### <span data-ttu-id="a79ce-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a79ce-122">-DefaultProfile</span></span>
<span data-ttu-id="a79ce-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a79ce-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a79ce-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="a79ce-124">-EnableAutoInflate</span></span>
<span data-ttu-id="a79ce-125">Indica se o autoinflar está habilitado</span><span class="sxs-lookup"><span data-stu-id="a79ce-125">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="a79ce-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="a79ce-126">-EnableKafka</span></span>
<span data-ttu-id="a79ce-127">Habilitando ou desabilitando o Kafka para namespace</span><span class="sxs-lookup"><span data-stu-id="a79ce-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="a79ce-128">-Identidade</span><span class="sxs-lookup"><span data-stu-id="a79ce-128">-Identity</span></span>
<span data-ttu-id="a79ce-129">habilitar ou desabilitar a identidade do namespace</span><span class="sxs-lookup"><span data-stu-id="a79ce-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="a79ce-130">-Local</span><span class="sxs-lookup"><span data-stu-id="a79ce-130">-Location</span></span>
<span data-ttu-id="a79ce-131">Localização do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="a79ce-131">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="a79ce-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="a79ce-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="a79ce-133">Limite superior de unidades de produtividade quando o autoinflar está habilitado, o valor deve estar entre 0 e 20 unidades de produtividade.</span><span class="sxs-lookup"><span data-stu-id="a79ce-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="a79ce-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="a79ce-134">-Name</span></span>
<span data-ttu-id="a79ce-135">Nome do namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="a79ce-135">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="a79ce-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a79ce-136">-ResourceGroupName</span></span>
<span data-ttu-id="a79ce-137">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a79ce-137">Resource Group Name</span></span>

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

### <span data-ttu-id="a79ce-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="a79ce-138">-SkuCapacity</span></span>
<span data-ttu-id="a79ce-139">As unidades de produtividade do eventhub.</span><span class="sxs-lookup"><span data-stu-id="a79ce-139">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="a79ce-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a79ce-140">-SkuName</span></span>
<span data-ttu-id="a79ce-141">Nome SKU do namespace.</span><span class="sxs-lookup"><span data-stu-id="a79ce-141">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="a79ce-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="a79ce-142">-Tag</span></span>
<span data-ttu-id="a79ce-143">Hashtables que representam marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="a79ce-143">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="a79ce-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a79ce-144">-ZoneRedundant</span></span>
<span data-ttu-id="a79ce-145">Habilitando ou desabilitando a zona redundante para namespace</span><span class="sxs-lookup"><span data-stu-id="a79ce-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="a79ce-146">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a79ce-146">-Confirm</span></span>
<span data-ttu-id="a79ce-147">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a79ce-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a79ce-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a79ce-148">-WhatIf</span></span>
<span data-ttu-id="a79ce-149">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a79ce-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a79ce-150">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a79ce-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a79ce-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a79ce-151">CommonParameters</span></span>
<span data-ttu-id="a79ce-152">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a79ce-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a79ce-153">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a79ce-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a79ce-154">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a79ce-154">INPUTS</span></span>

### <span data-ttu-id="a79ce-155">System. String</span><span class="sxs-lookup"><span data-stu-id="a79ce-155">System.String</span></span>

### <span data-ttu-id="a79ce-156">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a79ce-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a79ce-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a79ce-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a79ce-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a79ce-158">OUTPUTS</span></span>

### <span data-ttu-id="a79ce-159">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="a79ce-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="a79ce-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a79ce-160">NOTES</span></span>

## <span data-ttu-id="a79ce-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a79ce-161">RELATED LINKS</span></span>
