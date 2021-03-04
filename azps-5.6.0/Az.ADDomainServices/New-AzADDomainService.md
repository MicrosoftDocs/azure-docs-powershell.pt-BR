---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 61918dd4bce5279a2528e94c4e46fbe1c8813aff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889711"
---
# <span data-ttu-id="a8a1d-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="a8a1d-101">New-AzADDomainService</span></span>

## <span data-ttu-id="a8a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a1d-103">A operação Criar Serviço de Domínio cria um novo serviço de domínio com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="a8a1d-104">Se o serviço específico já existir, todas as propriedades remendáveis serão atualizadas e quaisquer propriedades imutáveis permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="a8a1d-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a8a1d-105">SYNTAX</span></span>

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

## <span data-ttu-id="a8a1d-106">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a8a1d-106">DESCRIPTION</span></span>
<span data-ttu-id="a8a1d-107">A operação Criar Serviço de Domínio cria um novo serviço de domínio com os parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="a8a1d-108">Se o serviço específico já existir, todas as propriedades remendáveis serão atualizadas e quaisquer propriedades imutáveis permanecerão inalteradas.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="a8a1d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a8a1d-109">EXAMPLES</span></span>

### <span data-ttu-id="a8a1d-110">Exemplo 1: Criar novo ADDomainService</span><span class="sxs-lookup"><span data-stu-id="a8a1d-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="a8a1d-111">Criar novo ADDomainService</span><span class="sxs-lookup"><span data-stu-id="a8a1d-111">Create new ADDomainService</span></span>

## <span data-ttu-id="a8a1d-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a8a1d-112">PARAMETERS</span></span>

### <span data-ttu-id="a8a1d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8a1d-113">-AsJob</span></span>
<span data-ttu-id="a8a1d-114">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="a8a1d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a8a1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a1d-115">-DefaultProfile</span></span>
<span data-ttu-id="a8a1d-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8a1d-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="a8a1d-117">-DomainConfigurationType</span></span>
<span data-ttu-id="a8a1d-118">Tipo de Configuração de Domínio</span><span class="sxs-lookup"><span data-stu-id="a8a1d-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="a8a1d-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="a8a1d-119">-DomainName</span></span>
<span data-ttu-id="a8a1d-120">O nome do domínio do Azure para o quais o usuário gostaria de implantar os Serviços de Domínio.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

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

### <span data-ttu-id="a8a1d-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="a8a1d-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="a8a1d-122">Um sinalizador para determinar se o NtlmV1 está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="a8a1d-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="a8a1d-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="a8a1d-124">Um sinalizador para determinar se SyncKerberosPasswords está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="a8a1d-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="a8a1d-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="a8a1d-126">Um sinalizador para determinar se SyncNtlmPasswords está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="a8a1d-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="a8a1d-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="a8a1d-128">Um sinalizador para determinar se SyncOnPremPasswords está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="a8a1d-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="a8a1d-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="a8a1d-130">Um sinalizador para determinar se o TlsV1 está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="a8a1d-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="a8a1d-131">-FilteredSync</span></span>
<span data-ttu-id="a8a1d-132">Sinalizador habilitado ou desabilitado para ativar a sincronização filtrada baseada em grupo</span><span class="sxs-lookup"><span data-stu-id="a8a1d-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="a8a1d-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="a8a1d-133">-ForestTrust</span></span>
<span data-ttu-id="a8a1d-134">Lista de configurações para Floresta de Recursos a ser construída, consulte a seção NOTES para propriedades FORESTTRUST e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="a8a1d-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="a8a1d-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="a8a1d-136">Um sinalizador para determinar se o acesso seguro LDAP pela Internet está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="a8a1d-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="a8a1d-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="a8a1d-138">Um sinalizador para determinar se o LDAP seguro está habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="a8a1d-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="a8a1d-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="a8a1d-140">O certificado necessário para configurar o LDAP seguro.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="a8a1d-141">O parâmetro passado aqui deve ser uma representação base64encoded do arquivo pfx do certificado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="a8a1d-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a8a1d-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="a8a1d-143">A senha para descriptografar o arquivo pfx de certificado LDAP seguro fornecido.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="a8a1d-144">-Name</span><span class="sxs-lookup"><span data-stu-id="a8a1d-144">-Name</span></span>
<span data-ttu-id="a8a1d-145">O nome do serviço de domínio.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-145">The name of the domain service.</span></span>

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

### <span data-ttu-id="a8a1d-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="a8a1d-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="a8a1d-147">A lista de destinatários adicionais</span><span class="sxs-lookup"><span data-stu-id="a8a1d-147">The list of additional recipients</span></span>

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

### <span data-ttu-id="a8a1d-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="a8a1d-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="a8a1d-149">Os administradores do controlador de domínio devem ser notificados</span><span class="sxs-lookup"><span data-stu-id="a8a1d-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="a8a1d-150">-NotificationSettingNotifyGlobalAdmin</span><span class="sxs-lookup"><span data-stu-id="a8a1d-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="a8a1d-151">Caso os administradores globais sejam notificados</span><span class="sxs-lookup"><span data-stu-id="a8a1d-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="a8a1d-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a8a1d-152">-NoWait</span></span>
<span data-ttu-id="a8a1d-153">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="a8a1d-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a8a1d-154">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="a8a1d-154">-ReplicaSet</span></span>
<span data-ttu-id="a8a1d-155">Lista de ReplicaSets Para construir, consulte a seção NOTES para propriedades REPLICASET e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

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

### <span data-ttu-id="a8a1d-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="a8a1d-156">-ResourceForest</span></span>
<span data-ttu-id="a8a1d-157">Floresta de Recursos</span><span class="sxs-lookup"><span data-stu-id="a8a1d-157">Resource Forest</span></span>

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

### <span data-ttu-id="a8a1d-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a1d-158">-ResourceGroupName</span></span>
<span data-ttu-id="a8a1d-159">O nome do grupo de recursos dentro da assinatura do usuário.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="a8a1d-160">O nome é insensível a maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-160">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a8a1d-161">-Sku</span><span class="sxs-lookup"><span data-stu-id="a8a1d-161">-Sku</span></span>
<span data-ttu-id="a8a1d-162">Tipo Sku</span><span class="sxs-lookup"><span data-stu-id="a8a1d-162">Sku Type</span></span>

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

### <span data-ttu-id="a8a1d-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a8a1d-163">-SubscriptionId</span></span>
<span data-ttu-id="a8a1d-164">Obtém credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a8a1d-165">A ID da assinatura faz parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-165">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a8a1d-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8a1d-166">-Tag</span></span>
<span data-ttu-id="a8a1d-167">Marcas de recurso</span><span class="sxs-lookup"><span data-stu-id="a8a1d-167">Resource tags</span></span>

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

### <span data-ttu-id="a8a1d-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8a1d-168">-Confirm</span></span>
<span data-ttu-id="a8a1d-169">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8a1d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8a1d-170">-WhatIf</span></span>
<span data-ttu-id="a8a1d-171">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8a1d-172">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8a1d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a1d-173">CommonParameters</span></span>
<span data-ttu-id="a8a1d-174">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a1d-175">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8a1d-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a1d-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a8a1d-176">INPUTS</span></span>

## <span data-ttu-id="a8a1d-177">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a8a1d-177">OUTPUTS</span></span>

### <span data-ttu-id="a8a1d-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="a8a1d-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="a8a1d-179">NOTES</span><span class="sxs-lookup"><span data-stu-id="a8a1d-179">NOTES</span></span>

<span data-ttu-id="a8a1d-180">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a8a1d-180">ALIASES</span></span>

<span data-ttu-id="a8a1d-181">PROPRIEDADES DE PARÂMETRO COMPLEXO</span><span class="sxs-lookup"><span data-stu-id="a8a1d-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a8a1d-182">Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades apropriadas.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a8a1d-183">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a8a1d-184">FORESTTRUST <IForestTrust[]>: Lista de configurações para Floresta de Recursos</span><span class="sxs-lookup"><span data-stu-id="a8a1d-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="a8a1d-185">`[FriendlyName <String>]`: Nome Amigável</span><span class="sxs-lookup"><span data-stu-id="a8a1d-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="a8a1d-186">`[RemoteDnsIP <String>]`: IPs dns remotos</span><span class="sxs-lookup"><span data-stu-id="a8a1d-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="a8a1d-187">`[TrustDirection <String>]`: Direção de confiança</span><span class="sxs-lookup"><span data-stu-id="a8a1d-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="a8a1d-188">`[TrustPassword <String>]`: Senha de confiança</span><span class="sxs-lookup"><span data-stu-id="a8a1d-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="a8a1d-189">`[TrustedDomainFqdn <String>]`: FQDN de domínio confiável</span><span class="sxs-lookup"><span data-stu-id="a8a1d-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="a8a1d-190">REPLICASET <IReplicaSet[]>: Lista de ReplicaSets</span><span class="sxs-lookup"><span data-stu-id="a8a1d-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="a8a1d-191">`[Location <String>]`: Local da rede virtual</span><span class="sxs-lookup"><span data-stu-id="a8a1d-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="a8a1d-192">`[SubnetId <String>]`: O nome da rede virtual na quais os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="a8a1d-193">A id da sub-rede em que os Serviços de Domínio serão implantados.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="a8a1d-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="a8a1d-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="a8a1d-195">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a8a1d-195">RELATED LINKS</span></span>

