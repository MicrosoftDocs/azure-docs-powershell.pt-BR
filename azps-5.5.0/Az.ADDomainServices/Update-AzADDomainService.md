---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 7acebe247009c95f9d504dc09b2729eeb5aabbbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110863"
---
# <span data-ttu-id="6891a-101">Update-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="6891a-101">Update-AzADDomainService</span></span>

## <span data-ttu-id="6891a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6891a-102">SYNOPSIS</span></span>
<span data-ttu-id="6891a-103">A operação Atualizar Serviço de Domínio pode ser usada para atualizar a implantação existente.</span><span class="sxs-lookup"><span data-stu-id="6891a-103">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="6891a-104">A chamada de atualização só dá suporte às propriedades listadas no corpo do PATCH.</span><span class="sxs-lookup"><span data-stu-id="6891a-104">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="6891a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6891a-105">SYNTAX</span></span>

### <span data-ttu-id="6891a-106">UpdateExpanded (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6891a-106">UpdateExpanded (Default)</span></span>
```
Update-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DomainConfigurationType <String>] [-DomainSecuritySettingNtlmV1 <String>]
 [-DomainSecuritySettingSyncKerberosPassword <String>] [-DomainSecuritySettingSyncNtlmPassword <String>]
 [-DomainSecuritySettingSyncOnPremPassword <String>] [-DomainSecuritySettingTlsV1 <String>]
 [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>] [-LdapSettingExternalAccess <String>]
 [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6891a-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6891a-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6891a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="6891a-108">DESCRIPTION</span></span>
<span data-ttu-id="6891a-109">A operação Atualizar Serviço de Domínio pode ser usada para atualizar a implantação existente.</span><span class="sxs-lookup"><span data-stu-id="6891a-109">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="6891a-110">A chamada de atualização só dá suporte às propriedades listadas no corpo do PATCH.</span><span class="sxs-lookup"><span data-stu-id="6891a-110">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="6891a-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6891a-111">EXAMPLES</span></span>

### <span data-ttu-id="6891a-112">Exemplo 1: Atualizar AzADDomainService por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="6891a-112">Example 1: Update AzADDomainService By ResourceGroupName and Name</span></span>
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="6891a-113">Atualizar AzADDomainService por ResourceGroupName e Name</span><span class="sxs-lookup"><span data-stu-id="6891a-113">Update AzADDomainService By ResourceGroupName and Name</span></span>

### <span data-ttu-id="6891a-114">Exemplo 2: Atualizar AzADDomainService por Inputobject</span><span class="sxs-lookup"><span data-stu-id="6891a-114">Example 2: Update AzADDomainService By Inputobject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="6891a-115">Atualizar AzADDomainService por Inputobject</span><span class="sxs-lookup"><span data-stu-id="6891a-115">Update AzADDomainService By Inputobject</span></span>

## <span data-ttu-id="6891a-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6891a-116">PARAMETERS</span></span>

### <span data-ttu-id="6891a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6891a-117">-AsJob</span></span>
<span data-ttu-id="6891a-118">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="6891a-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6891a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6891a-119">-DefaultProfile</span></span>
<span data-ttu-id="6891a-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6891a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6891a-121">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="6891a-121">-DomainConfigurationType</span></span>
<span data-ttu-id="6891a-122">Tipo de Configuração de Domínio</span><span class="sxs-lookup"><span data-stu-id="6891a-122">Domain Configuration Type</span></span>

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

### <span data-ttu-id="6891a-123">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="6891a-123">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="6891a-124">Um sinalizador para determinar se ntlmV1 está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6891a-124">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="6891a-125">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="6891a-125">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="6891a-126">Um sinalizador para determinar se o SyncKerberosPasswords está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6891a-126">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="6891a-127">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="6891a-127">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="6891a-128">Um sinalizador para determinar se o SyncNtlmPasswords está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6891a-128">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="6891a-129">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="6891a-129">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="6891a-130">Um sinalizador para determinar se o SyncOnPremPasswords está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6891a-130">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="6891a-131">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="6891a-131">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="6891a-132">Um sinalizador para determinar se o TlsV1 está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6891a-132">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="6891a-133">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="6891a-133">-FilteredSync</span></span>
<span data-ttu-id="6891a-134">Sinalizador habilitado ou desabilitado para ativar a sincronização filtrada baseada em grupo</span><span class="sxs-lookup"><span data-stu-id="6891a-134">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="6891a-135">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="6891a-135">-ForestTrust</span></span>
<span data-ttu-id="6891a-136">Lista de configurações para a floresta de recursos para construir, consulte a seção ANOTAÇÕES para propriedades FORESTTRUST e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="6891a-136">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6891a-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6891a-137">-InputObject</span></span>
<span data-ttu-id="6891a-138">Parâmetro de Identidade para construir, consulte a seção ANOTAÇÕES para propriedades INPUTOBJECT e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="6891a-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6891a-139">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="6891a-139">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="6891a-140">Um sinalizador para determinar se o acesso LDAP seguro pela Internet está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6891a-140">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="6891a-141">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="6891a-141">-LdapSettingLdaps</span></span>
<span data-ttu-id="6891a-142">Um sinalizador para determinar se o LDAP Seguro está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6891a-142">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="6891a-143">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="6891a-143">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="6891a-144">O certificado necessário para configurar o LDAP Seguro.</span><span class="sxs-lookup"><span data-stu-id="6891a-144">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="6891a-145">O parâmetro passado aqui deve ser uma representação de base64encoded do arquivo pfx de certificado.</span><span class="sxs-lookup"><span data-stu-id="6891a-145">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="6891a-146">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6891a-146">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="6891a-147">A senha para descriptografar o arquivo pfx de certificado LDAP seguro fornecido.</span><span class="sxs-lookup"><span data-stu-id="6891a-147">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6891a-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="6891a-148">-Name</span></span>
<span data-ttu-id="6891a-149">O nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="6891a-149">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6891a-150">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="6891a-150">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="6891a-151">A lista de destinatários adicionais</span><span class="sxs-lookup"><span data-stu-id="6891a-151">The list of additional recipients</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6891a-152">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="6891a-152">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="6891a-153">Os administradores do controlador de domínio devem ser notificados</span><span class="sxs-lookup"><span data-stu-id="6891a-153">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="6891a-154">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="6891a-154">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="6891a-155">Os administradores globais devem ser notificados</span><span class="sxs-lookup"><span data-stu-id="6891a-155">Should global admins be notified</span></span>

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

### <span data-ttu-id="6891a-156">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6891a-156">-NoWait</span></span>
<span data-ttu-id="6891a-157">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="6891a-157">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6891a-158">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="6891a-158">-ReplicaSet</span></span>
<span data-ttu-id="6891a-159">Lista de Conjuntos de Replicações para construir, consulte a seção ANOTAÇÕES para propriedades REPLICASET e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="6891a-159">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6891a-160">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="6891a-160">-ResourceForest</span></span>
<span data-ttu-id="6891a-161">Floresta de Recursos</span><span class="sxs-lookup"><span data-stu-id="6891a-161">Resource Forest</span></span>

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

### <span data-ttu-id="6891a-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6891a-162">-ResourceGroupName</span></span>
<span data-ttu-id="6891a-163">O nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="6891a-163">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="6891a-164">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6891a-164">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6891a-165">-SKU</span><span class="sxs-lookup"><span data-stu-id="6891a-165">-Sku</span></span>
<span data-ttu-id="6891a-166">Tipo de SKU</span><span class="sxs-lookup"><span data-stu-id="6891a-166">Sku Type</span></span>

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

### <span data-ttu-id="6891a-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6891a-167">-SubscriptionId</span></span>
<span data-ttu-id="6891a-168">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6891a-168">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6891a-169">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6891a-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6891a-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="6891a-170">-Tag</span></span>
<span data-ttu-id="6891a-171">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="6891a-171">Resource tags</span></span>

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

### <span data-ttu-id="6891a-172">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6891a-172">-Confirm</span></span>
<span data-ttu-id="6891a-173">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6891a-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6891a-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6891a-174">-WhatIf</span></span>
<span data-ttu-id="6891a-175">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6891a-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6891a-176">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6891a-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6891a-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6891a-177">CommonParameters</span></span>
<span data-ttu-id="6891a-178">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6891a-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6891a-179">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6891a-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6891a-180">Entradas</span><span class="sxs-lookup"><span data-stu-id="6891a-180">INPUTS</span></span>

### <span data-ttu-id="6891a-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="6891a-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="6891a-182">Saídas</span><span class="sxs-lookup"><span data-stu-id="6891a-182">OUTPUTS</span></span>

### <span data-ttu-id="6891a-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="6891a-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="6891a-184">Notas</span><span class="sxs-lookup"><span data-stu-id="6891a-184">NOTES</span></span>

<span data-ttu-id="6891a-185">Aliases</span><span class="sxs-lookup"><span data-stu-id="6891a-185">ALIASES</span></span>

<span data-ttu-id="6891a-186">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="6891a-186">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6891a-187">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="6891a-187">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6891a-188">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6891a-188">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6891a-189">FORESTTRUST <IForestTrust[]>: Lista de configurações para a Floresta de Recursos</span><span class="sxs-lookup"><span data-stu-id="6891a-189">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="6891a-190">`[FriendlyName <String>]`: Nome amigável</span><span class="sxs-lookup"><span data-stu-id="6891a-190">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="6891a-191">`[RemoteDnsIP <String>]`: ips dns remotos</span><span class="sxs-lookup"><span data-stu-id="6891a-191">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="6891a-192">`[TrustDirection <String>]`: Direção da Confiança</span><span class="sxs-lookup"><span data-stu-id="6891a-192">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="6891a-193">`[TrustPassword <String>]`: Confiar na Senha</span><span class="sxs-lookup"><span data-stu-id="6891a-193">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="6891a-194">`[TrustedDomainFqdn <String>]`: FQDN de domínio confiável</span><span class="sxs-lookup"><span data-stu-id="6891a-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="6891a-195">INPUTOBJECT: <IAdDomainServicesIdentity> Parâmetro de Identidade</span><span class="sxs-lookup"><span data-stu-id="6891a-195">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6891a-196">`[DomainServiceName <String>]`: o nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="6891a-196">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="6891a-197">`[Id <String>]`: Caminho de identidade de recursos</span><span class="sxs-lookup"><span data-stu-id="6891a-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6891a-198">`[ResourceGroupName <String>]`: o nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="6891a-198">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="6891a-199">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6891a-199">The name is case insensitive.</span></span>
  - <span data-ttu-id="6891a-200">`[SubscriptionId <String>]`: obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6891a-200">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="6891a-201">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="6891a-201">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="6891a-202">REPLICASET <IReplicaSet[]>: Lista de ReplicaSets</span><span class="sxs-lookup"><span data-stu-id="6891a-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="6891a-203">`[Location <String>]`: Local de rede virtual</span><span class="sxs-lookup"><span data-stu-id="6891a-203">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="6891a-204">`[SubnetId <String>]`: o nome da rede virtual na quais os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="6891a-204">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="6891a-205">A id da sub-rede na quais os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="6891a-205">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="6891a-206">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="6891a-206">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="6891a-207">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6891a-207">RELATED LINKS</span></span>

