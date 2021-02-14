---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 977621a3f92a8239925494102aed8c672509b222
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100110867"
---
# <span data-ttu-id="4fffb-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="4fffb-101">New-AzADDomainService</span></span>

## <span data-ttu-id="4fffb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4fffb-102">SYNOPSIS</span></span>
<span data-ttu-id="4fffb-103">A operação Criar Serviço de Domínio cria um novo serviço de domínio com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="4fffb-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="4fffb-104">Se o serviço específico já existir, todas as propriedades patcháveis serão atualizadas e todas as propriedades imutáveis permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="4fffb-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="4fffb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4fffb-105">SYNTAX</span></span>

```
New-AzADDomainService -Name <String> -ResourceGroupName <String> -DomainName <String>
 -ReplicaSet <IReplicaSet[]> [-SubscriptionId <String>] [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4fffb-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="4fffb-106">DESCRIPTION</span></span>
<span data-ttu-id="4fffb-107">A operação Criar Serviço de Domínio cria um novo serviço de domínio com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="4fffb-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="4fffb-108">Se o serviço específico já existir, todas as propriedades patcháveis serão atualizadas e todas as propriedades imutáveis permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="4fffb-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="4fffb-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4fffb-109">EXAMPLES</span></span>

### <span data-ttu-id="4fffb-110">Exemplo 1: Criar novo ADDomainService</span><span class="sxs-lookup"><span data-stu-id="4fffb-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="4fffb-111">Criar novo ADDomainService</span><span class="sxs-lookup"><span data-stu-id="4fffb-111">Create new ADDomainService</span></span>

## <span data-ttu-id="4fffb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4fffb-112">PARAMETERS</span></span>

### <span data-ttu-id="4fffb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fffb-113">-AsJob</span></span>
<span data-ttu-id="4fffb-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="4fffb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4fffb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fffb-115">-DefaultProfile</span></span>
<span data-ttu-id="4fffb-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4fffb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fffb-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="4fffb-117">-DomainConfigurationType</span></span>
<span data-ttu-id="4fffb-118">Tipo de Configuração de Domínio</span><span class="sxs-lookup"><span data-stu-id="4fffb-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="4fffb-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="4fffb-119">-DomainName</span></span>
<span data-ttu-id="4fffb-120">O nome do domínio do Azure para o quais o usuário gostaria de implantar os Serviços de Domínio.</span><span class="sxs-lookup"><span data-stu-id="4fffb-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

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

### <span data-ttu-id="4fffb-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="4fffb-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="4fffb-122">Um sinalizador para determinar se ntlmV1 está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="4fffb-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="4fffb-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="4fffb-124">Um sinalizador para determinar se o SyncKerberosPasswords está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="4fffb-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="4fffb-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="4fffb-126">Um sinalizador para determinar se o SyncNtlmPasswords está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="4fffb-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="4fffb-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="4fffb-128">Um sinalizador para determinar se o SyncOnPremPasswords está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="4fffb-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="4fffb-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="4fffb-130">Um sinalizador para determinar se o TlsV1 está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="4fffb-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="4fffb-131">-FilteredSync</span></span>
<span data-ttu-id="4fffb-132">Sinalizador habilitado ou desabilitado para ativar a sincronização filtrada baseada em grupo</span><span class="sxs-lookup"><span data-stu-id="4fffb-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="4fffb-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="4fffb-133">-ForestTrust</span></span>
<span data-ttu-id="4fffb-134">Lista de configurações para a floresta de recursos para construir, consulte a seção ANOTAÇÕES para propriedades FORESTTRUST e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4fffb-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="4fffb-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="4fffb-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="4fffb-136">Um sinalizador para determinar se o acesso LDAP seguro pela Internet está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="4fffb-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="4fffb-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="4fffb-138">Um sinalizador para determinar se o LDAP Seguro está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="4fffb-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="4fffb-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="4fffb-140">O certificado necessário para configurar o LDAP Seguro.</span><span class="sxs-lookup"><span data-stu-id="4fffb-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="4fffb-141">O parâmetro passado aqui deve ser uma representação de base64encoded do arquivo pfx de certificado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="4fffb-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4fffb-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="4fffb-143">A senha para descriptografar o arquivo pfx de certificado LDAP seguro fornecido.</span><span class="sxs-lookup"><span data-stu-id="4fffb-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="4fffb-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fffb-144">-Name</span></span>
<span data-ttu-id="4fffb-145">O nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="4fffb-145">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fffb-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="4fffb-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="4fffb-147">A lista de destinatários adicionais</span><span class="sxs-lookup"><span data-stu-id="4fffb-147">The list of additional recipients</span></span>

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

### <span data-ttu-id="4fffb-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="4fffb-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="4fffb-149">Os administradores do controlador de domínio devem ser notificados</span><span class="sxs-lookup"><span data-stu-id="4fffb-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="4fffb-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="4fffb-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="4fffb-151">Os administradores globais devem ser notificados</span><span class="sxs-lookup"><span data-stu-id="4fffb-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="4fffb-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4fffb-152">-NoWait</span></span>
<span data-ttu-id="4fffb-153">Executar o comando assíncrona</span><span class="sxs-lookup"><span data-stu-id="4fffb-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4fffb-154">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="4fffb-154">-ReplicaSet</span></span>
<span data-ttu-id="4fffb-155">Lista de Conjuntos de Replicações para construir, consulte a seção ANOTAÇÕES para propriedades REPLICASET e crie uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="4fffb-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fffb-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="4fffb-156">-ResourceForest</span></span>
<span data-ttu-id="4fffb-157">Floresta de Recursos</span><span class="sxs-lookup"><span data-stu-id="4fffb-157">Resource Forest</span></span>

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

### <span data-ttu-id="4fffb-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fffb-158">-ResourceGroupName</span></span>
<span data-ttu-id="4fffb-159">O nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="4fffb-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="4fffb-160">O nome não é sensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4fffb-160">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4fffb-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="4fffb-161">-Sku</span></span>
<span data-ttu-id="4fffb-162">Tipo de SKU</span><span class="sxs-lookup"><span data-stu-id="4fffb-162">Sku Type</span></span>

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

### <span data-ttu-id="4fffb-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4fffb-163">-SubscriptionId</span></span>
<span data-ttu-id="4fffb-164">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4fffb-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4fffb-165">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4fffb-165">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4fffb-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="4fffb-166">-Tag</span></span>
<span data-ttu-id="4fffb-167">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="4fffb-167">Resource tags</span></span>

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

### <span data-ttu-id="4fffb-168">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4fffb-168">-Confirm</span></span>
<span data-ttu-id="4fffb-169">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fffb-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fffb-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fffb-170">-WhatIf</span></span>
<span data-ttu-id="4fffb-171">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fffb-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4fffb-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fffb-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fffb-173">CommonParameters</span></span>
<span data-ttu-id="4fffb-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fffb-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fffb-175">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4fffb-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fffb-176">Entradas</span><span class="sxs-lookup"><span data-stu-id="4fffb-176">INPUTS</span></span>

## <span data-ttu-id="4fffb-177">Saídas</span><span class="sxs-lookup"><span data-stu-id="4fffb-177">OUTPUTS</span></span>

### <span data-ttu-id="4fffb-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="4fffb-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="4fffb-179">Notas</span><span class="sxs-lookup"><span data-stu-id="4fffb-179">NOTES</span></span>

<span data-ttu-id="4fffb-180">Aliases</span><span class="sxs-lookup"><span data-stu-id="4fffb-180">ALIASES</span></span>

<span data-ttu-id="4fffb-181">PROPRIEDADES DE PARÂMETRO COMPLEXOS</span><span class="sxs-lookup"><span data-stu-id="4fffb-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4fffb-182">Para criar os parâmetros descritos abaixo, construa uma tabela hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="4fffb-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4fffb-183">Para obter informações sobre tabelas hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4fffb-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4fffb-184">FORESTTRUST <IForestTrust[]>: Lista de configurações para a Floresta de Recursos</span><span class="sxs-lookup"><span data-stu-id="4fffb-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="4fffb-185">`[FriendlyName <String>]`: Nome amigável</span><span class="sxs-lookup"><span data-stu-id="4fffb-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="4fffb-186">`[RemoteDnsIP <String>]`: ips dns remotos</span><span class="sxs-lookup"><span data-stu-id="4fffb-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="4fffb-187">`[TrustDirection <String>]`: Direção da Confiança</span><span class="sxs-lookup"><span data-stu-id="4fffb-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="4fffb-188">`[TrustPassword <String>]`: Confiar na Senha</span><span class="sxs-lookup"><span data-stu-id="4fffb-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="4fffb-189">`[TrustedDomainFqdn <String>]`: FQDN de domínio confiável</span><span class="sxs-lookup"><span data-stu-id="4fffb-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="4fffb-190">REPLICASET <IReplicaSet[]>: Lista de ReplicaSets</span><span class="sxs-lookup"><span data-stu-id="4fffb-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="4fffb-191">`[Location <String>]`: Local de rede virtual</span><span class="sxs-lookup"><span data-stu-id="4fffb-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="4fffb-192">`[SubnetId <String>]`: o nome da rede virtual na quais os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="4fffb-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="4fffb-193">A id da sub-rede na quais os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="4fffb-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="4fffb-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="4fffb-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="4fffb-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4fffb-195">RELATED LINKS</span></span>

