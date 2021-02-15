---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: f13a92bef4bfbafc67beec6d99cf02d8d1d63c31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111884"
---
# <span data-ttu-id="17830-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="17830-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="17830-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="17830-102">SYNOPSIS</span></span>
<span data-ttu-id="17830-103">Atualiza o namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="17830-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="17830-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17830-104">SYNTAX</span></span>

### <span data-ttu-id="17830-105">NamespaceParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="17830-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17830-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="17830-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17830-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="17830-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17830-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="17830-108">DESCRIPTION</span></span>
<span data-ttu-id="17830-109">O Set-AzEventHubNamespace cmdlet atualiza as propriedades do namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="17830-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="17830-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="17830-110">EXAMPLES</span></span>

### <span data-ttu-id="17830-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="17830-111">Example 1</span></span>
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

<span data-ttu-id="17830-112">Atualiza as Marcas do namespace \` MyNamespaceName \` para Criado.</span><span class="sxs-lookup"><span data-stu-id="17830-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="17830-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="17830-113">Example 2</span></span>
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

<span data-ttu-id="17830-114">Atualiza o estado do namespace \` MyNamespaceName \` com AutoInflate = habilitado e MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="17830-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="17830-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="17830-115">Example 3</span></span>

<span data-ttu-id="17830-116">Atualiza o namespace de Hubs de Eventos especificado.</span><span class="sxs-lookup"><span data-stu-id="17830-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="17830-117">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="17830-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="17830-118">Exemplo 5: Criar e atualizar o Namespace com Gerenciar Identidade em um cluster</span><span class="sxs-lookup"><span data-stu-id="17830-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
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

## <span data-ttu-id="17830-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17830-119">PARAMETERS</span></span>

### <span data-ttu-id="17830-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17830-120">-DefaultProfile</span></span>
<span data-ttu-id="17830-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="17830-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17830-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="17830-122">-EnableAutoInflate</span></span>
<span data-ttu-id="17830-123">Indica se a AutoInflate está habilitada</span><span class="sxs-lookup"><span data-stu-id="17830-123">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="17830-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="17830-124">-EnableKafka</span></span>
<span data-ttu-id="17830-125">habilitando ou desabilitando o Kafka para namespace</span><span class="sxs-lookup"><span data-stu-id="17830-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="17830-126">-Identidade</span><span class="sxs-lookup"><span data-stu-id="17830-126">-Identity</span></span>
<span data-ttu-id="17830-127">habilitando ou desabilitando a Identidade para namespace</span><span class="sxs-lookup"><span data-stu-id="17830-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="17830-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="17830-128">-IdentityUserDefined</span></span>
<span data-ttu-id="17830-129">Identidade definida pelo usuário ou Nenhum</span><span class="sxs-lookup"><span data-stu-id="17830-129">User defined Identity or None</span></span>

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

### <span data-ttu-id="17830-130">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="17830-130">-KeyProperty</span></span>
<span data-ttu-id="17830-131">Lista de propriedades de chave, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span><span class="sxs-lookup"><span data-stu-id="17830-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

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

### <span data-ttu-id="17830-132">-KeySource</span><span class="sxs-lookup"><span data-stu-id="17830-132">-KeySource</span></span>
<span data-ttu-id="17830-133">Fonte de Chave</span><span class="sxs-lookup"><span data-stu-id="17830-133">Key Source</span></span>

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

### <span data-ttu-id="17830-134">-Local</span><span class="sxs-lookup"><span data-stu-id="17830-134">-Location</span></span>
<span data-ttu-id="17830-135">Local do Namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="17830-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="17830-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="17830-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="17830-137">Limite superior de unidades de produtividade quando o AutoInflate está habilitado, o valor deve estar dentro de 0 a 20 unidades de produtividade.</span><span class="sxs-lookup"><span data-stu-id="17830-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="17830-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="17830-138">-Name</span></span>
<span data-ttu-id="17830-139">Nome do Namespace do EventHub.</span><span class="sxs-lookup"><span data-stu-id="17830-139">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="17830-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17830-140">-ResourceGroupName</span></span>
<span data-ttu-id="17830-141">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="17830-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="17830-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="17830-142">-SkuCapacity</span></span>
<span data-ttu-id="17830-143">As unidades de produtividade do eventhub.</span><span class="sxs-lookup"><span data-stu-id="17830-143">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="17830-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="17830-144">-SkuName</span></span>
<span data-ttu-id="17830-145">Nome da SKU name namespace.</span><span class="sxs-lookup"><span data-stu-id="17830-145">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="17830-146">-Estado</span><span class="sxs-lookup"><span data-stu-id="17830-146">-State</span></span>
<span data-ttu-id="17830-147">Desabilitar/Habilitar Namespace.</span><span class="sxs-lookup"><span data-stu-id="17830-147">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="17830-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="17830-148">-Tag</span></span>
<span data-ttu-id="17830-149">Hashtables que representa a marca de recurso.</span><span class="sxs-lookup"><span data-stu-id="17830-149">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="17830-150">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="17830-150">-Confirm</span></span>
<span data-ttu-id="17830-151">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17830-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17830-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17830-152">-WhatIf</span></span>
<span data-ttu-id="17830-153">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="17830-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17830-154">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="17830-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17830-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17830-155">CommonParameters</span></span>
<span data-ttu-id="17830-156">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17830-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17830-157">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17830-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17830-158">Entradas</span><span class="sxs-lookup"><span data-stu-id="17830-158">INPUTS</span></span>

### <span data-ttu-id="17830-159">System.String</span><span class="sxs-lookup"><span data-stu-id="17830-159">System.String</span></span>

### <span data-ttu-id="17830-160">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="17830-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="17830-161">System.Nullable'1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="17830-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="17830-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="17830-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="17830-163">Saídas</span><span class="sxs-lookup"><span data-stu-id="17830-163">OUTPUTS</span></span>

### <span data-ttu-id="17830-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="17830-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="17830-165">Notas</span><span class="sxs-lookup"><span data-stu-id="17830-165">NOTES</span></span>

## <span data-ttu-id="17830-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="17830-166">RELATED LINKS</span></span>
