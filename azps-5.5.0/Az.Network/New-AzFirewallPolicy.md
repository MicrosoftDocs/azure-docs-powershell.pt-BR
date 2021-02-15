---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 0e3a9b99a23715b63eb42c83ba112776272969ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111642"
---
# <span data-ttu-id="004c7-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="004c7-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="004c7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="004c7-102">SYNOPSIS</span></span>
<span data-ttu-id="004c7-103">Cria uma nova Política de Firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="004c7-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="004c7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="004c7-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-IntrusionDetection <PSAzureFirewallPolicyIntrusionDetection>] [-TransportSecurityName <String>]
 [-TransportSecurityKeyVaultSecretId <String>] [-SkuTier <String>] [-UserAssignedIdentityId <String>]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="004c7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="004c7-105">DESCRIPTION</span></span>
<span data-ttu-id="004c7-106">O **cmdlet New-AzFirewallPolicy** cria uma Política de Firewall do Azure.</span><span class="sxs-lookup"><span data-stu-id="004c7-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="004c7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="004c7-107">EXAMPLES</span></span>

### <span data-ttu-id="004c7-108">Exemplo 1: 1.</span><span class="sxs-lookup"><span data-stu-id="004c7-108">Example 1: 1.</span></span> <span data-ttu-id="004c7-109">Criar uma política vazia</span><span class="sxs-lookup"><span data-stu-id="004c7-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="004c7-110">Este exemplo cria uma política de firewall do Azure</span><span class="sxs-lookup"><span data-stu-id="004c7-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="004c7-111">Exemplo 2: 2.</span><span class="sxs-lookup"><span data-stu-id="004c7-111">Example 2: 2.</span></span> <span data-ttu-id="004c7-112">Criar uma política vazia com o Modo ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="004c7-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="004c7-113">Este exemplo cria uma política de firewall do Azure com um modo intel de ameaças</span><span class="sxs-lookup"><span data-stu-id="004c7-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="004c7-114">Exemplo 3: 3.</span><span class="sxs-lookup"><span data-stu-id="004c7-114">Example 3: 3.</span></span> <span data-ttu-id="004c7-115">Criar uma política vazia com o ThreatIntel Whitelist</span><span class="sxs-lookup"><span data-stu-id="004c7-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="004c7-116">Este exemplo cria uma política de firewall do Azure com uma lista de ameaças da Intel Whitelist</span><span class="sxs-lookup"><span data-stu-id="004c7-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

### <span data-ttu-id="004c7-117">Exemplo 4: 4.</span><span class="sxs-lookup"><span data-stu-id="004c7-117">Example 4: 4.</span></span> <span data-ttu-id="004c7-118">Criar política com detecção de invasão, identidade e segurança de transporte</span><span class="sxs-lookup"><span data-stu-id="004c7-118">Create policy with intrusion detection, identity and transport security</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride -BypassTraffic $bypass
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/TestRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/user-assign-identity'
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection -TransportSecurityName tsName -TransportSecurityKeyVaultSecretId "https://<keyvaultname>.vault.azure.net/secrets/cacert"  -UserAssignedIdentityId $userAssignedIdentity
```

<span data-ttu-id="004c7-119">Este exemplo cria uma política de firewall do Azure com uma detecção de invasão no modo de alerta, identidade atribuída pelo usuário e segurança de transporte</span><span class="sxs-lookup"><span data-stu-id="004c7-119">This example creates an azure firewall policy with a intrusion detection in mode alert, user assigned identity and transport security</span></span>

## <span data-ttu-id="004c7-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="004c7-120">PARAMETERS</span></span>

### <span data-ttu-id="004c7-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="004c7-121">-AsJob</span></span>
<span data-ttu-id="004c7-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="004c7-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-123">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="004c7-123">-BasePolicy</span></span>
<span data-ttu-id="004c7-124">A política base a ser herdado</span><span class="sxs-lookup"><span data-stu-id="004c7-124">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004c7-125">-DefaultProfile</span></span>
<span data-ttu-id="004c7-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="004c7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-127">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="004c7-127">-DnsSetting</span></span>
<span data-ttu-id="004c7-128">A configuração DNS</span><span class="sxs-lookup"><span data-stu-id="004c7-128">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-129">-Forçar</span><span class="sxs-lookup"><span data-stu-id="004c7-129">-Force</span></span>
<span data-ttu-id="004c7-130">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="004c7-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-131">-Identidade</span><span class="sxs-lookup"><span data-stu-id="004c7-131">-Identity</span></span>
<span data-ttu-id="004c7-132">Identidade de Política de Firewall a ser atribuída à Política de Firewall.</span><span class="sxs-lookup"><span data-stu-id="004c7-132">Firewall Policy Identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-133">-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="004c7-133">-IntrusionDetection</span></span>
<span data-ttu-id="004c7-134">A configuração de detecção de invasão</span><span class="sxs-lookup"><span data-stu-id="004c7-134">The Intrusion Detection Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-135">-Local</span><span class="sxs-lookup"><span data-stu-id="004c7-135">-Location</span></span>
<span data-ttu-id="004c7-136">Localização.</span><span class="sxs-lookup"><span data-stu-id="004c7-136">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="004c7-137">-Name</span></span>
<span data-ttu-id="004c7-138">O nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="004c7-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="004c7-139">-ResourceGroupName</span></span>
<span data-ttu-id="004c7-140">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="004c7-140">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-141">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="004c7-141">-SkuTier</span></span>
<span data-ttu-id="004c7-142">Nível de SKU da política de firewall</span><span class="sxs-lookup"><span data-stu-id="004c7-142">Firewall policy sku tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="004c7-143">-Tag</span></span>
<span data-ttu-id="004c7-144">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="004c7-144">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-145">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="004c7-145">-ThreatIntelMode</span></span>
<span data-ttu-id="004c7-146">O modo de operação para Inteligência contra Ameaças.</span><span class="sxs-lookup"><span data-stu-id="004c7-146">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-147">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="004c7-147">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="004c7-148">A lista de whitelist para Inteligência contra Ameaças</span><span class="sxs-lookup"><span data-stu-id="004c7-148">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-149">-TransportSecurityKeyVaultSecntesId</span><span class="sxs-lookup"><span data-stu-id="004c7-149">-TransportSecurityKeyVaultSecretId</span></span>
<span data-ttu-id="004c7-150">ID Secreta do objeto 'Secret' ou 'Certificate' (pfx não criptografado de base 64) armazenado no KeyVault</span><span class="sxs-lookup"><span data-stu-id="004c7-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-151">-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="004c7-151">-TransportSecurityName</span></span>
<span data-ttu-id="004c7-152">Nome da segurança do transporte</span><span class="sxs-lookup"><span data-stu-id="004c7-152">Transport security name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-153">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="004c7-153">-UserAssignedIdentityId</span></span>
<span data-ttu-id="004c7-154">ResourceId da identidade atribuída pelo usuário a ser atribuída à Política de Firewall.</span><span class="sxs-lookup"><span data-stu-id="004c7-154">ResourceId of the user assigned identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-155">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="004c7-155">-Confirm</span></span>
<span data-ttu-id="004c7-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="004c7-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004c7-157">-WhatIf</span></span>
<span data-ttu-id="004c7-158">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="004c7-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="004c7-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="004c7-159">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="004c7-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004c7-160">CommonParameters</span></span>
<span data-ttu-id="004c7-161">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004c7-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004c7-162">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="004c7-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004c7-163">Entradas</span><span class="sxs-lookup"><span data-stu-id="004c7-163">INPUTS</span></span>

### <span data-ttu-id="004c7-164">System.String</span><span class="sxs-lookup"><span data-stu-id="004c7-164">System.String</span></span>

### <span data-ttu-id="004c7-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="004c7-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="004c7-166">Saídas</span><span class="sxs-lookup"><span data-stu-id="004c7-166">OUTPUTS</span></span>

### <span data-ttu-id="004c7-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="004c7-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="004c7-168">Notas</span><span class="sxs-lookup"><span data-stu-id="004c7-168">NOTES</span></span>

## <span data-ttu-id="004c7-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="004c7-169">RELATED LINKS</span></span>
