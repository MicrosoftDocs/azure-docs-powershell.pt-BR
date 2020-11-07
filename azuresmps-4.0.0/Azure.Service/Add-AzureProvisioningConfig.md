---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946382"
---
# <span data-ttu-id="9fb3f-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="9fb3f-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="9fb3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9fb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb3f-103">Adiciona a configuração de provisionamento para uma máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="9fb3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fb3f-104">SYNTAX</span></span>

### <span data-ttu-id="9fb3f-105">Windows (padrão)</span><span class="sxs-lookup"><span data-stu-id="9fb3f-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9fb3f-106">Linux</span><span class="sxs-lookup"><span data-stu-id="9fb3f-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9fb3f-107">WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="9fb3f-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9fb3f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9fb3f-108">DESCRIPTION</span></span>
<span data-ttu-id="9fb3f-109">O cmdlet **Add-AzureProvisioningConfig** adiciona informações de configuração de provisionamento a uma configuração de máquina virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="9fb3f-110">Você pode usar o objeto de configuração para criar uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="9fb3f-111">Esse cmdlet dá suporte a diferentes configurações de provisionamento, incluindo servidores autônomos do Windows, Windows Servers associados a um domínio do Active Directory e servidores baseados em Linux.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="9fb3f-112">Para criar um servidor associado a um domínio do Active Directory, especifique o nome de domínio totalmente qualificado do domínio do Active Directory e as credenciais de domínio de um usuário que tenha permissão para ingressar na máquina virtual no domínio.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="9fb3f-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9fb3f-113">EXAMPLES</span></span>

### <span data-ttu-id="9fb3f-114">Exemplo 1: criar uma máquina virtual autônoma</span><span class="sxs-lookup"><span data-stu-id="9fb3f-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="9fb3f-115">Esse comando cria um objeto de configuração de máquina virtual usando o cmdlet **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="9fb3f-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="9fb3f-116">O comando passa o objeto para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9fb3f-117">O cmdlet atual adiciona a configuração de provisionamento para uma máquina virtual que executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="9fb3f-118">A configuração inclui o nome de usuário e a senha de administrador.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="9fb3f-119">O comando passa a configuração para o cmdlet **New-AzureVM** , que cria a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="9fb3f-120">Exemplo 2: criar uma máquina virtual unida ao domínio</span><span class="sxs-lookup"><span data-stu-id="9fb3f-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="9fb3f-121">Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9fb3f-122">O cmdlet atual adiciona a configuração de provisionamento de uma máquina virtual para ingressar no domínio contoso.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="9fb3f-123">O comando inclui o nome de usuário e a senha necessários para ingressar na máquina virtual no domínio.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="9fb3f-124">A configuração exige que o usuário altere a senha do usuário no primeiro logon.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="9fb3f-125">O comando cria a máquina virtual com base no objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="9fb3f-126">Exemplo 3: criar uma máquina virtual baseada em Linux</span><span class="sxs-lookup"><span data-stu-id="9fb3f-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="9fb3f-127">Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9fb3f-128">O cmdlet atual adiciona a configuração de provisionamento para uma máquina virtual que executa o sistema operacional Linux.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="9fb3f-129">A configuração inclui o nome de usuário e a senha raiz.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="9fb3f-130">O comando cria a máquina virtual com base no objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="9fb3f-131">Exemplo 4: criar uma máquina virtual que inclua certificados para WinRM</span><span class="sxs-lookup"><span data-stu-id="9fb3f-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="9fb3f-132">O primeiro comando obtém certificados de um repositório de certificados e, em seguida, os armazena na variável de matriz de $certs.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="9fb3f-133">O segundo comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9fb3f-134">O cmdlet atual adiciona configuração de provisionamento que inclui certificados para WinRM.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="9fb3f-135">O comando cria a máquina virtual com base no objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="9fb3f-136">Exemplo 5: criar uma máquina virtual com o WinRM habilitado em HTTP</span><span class="sxs-lookup"><span data-stu-id="9fb3f-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="9fb3f-137">Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9fb3f-138">O cmdlet atual adiciona configuração de provisionamento que tem o WinRM habilitado em HTTP.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="9fb3f-139">O comando cria a máquina virtual com base no objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="9fb3f-140">Exemplo 6: criar uma máquina virtual que tenha o WinRM desabilitado em HTTPS</span><span class="sxs-lookup"><span data-stu-id="9fb3f-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="9fb3f-141">Esse comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9fb3f-142">O cmdlet atual adiciona uma configuração de provisionamento que desabilita o WinRM em HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="9fb3f-143">O comando cria a máquina virtual com base no objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="9fb3f-144">Exemplo 7: criar uma máquina virtual sem exportação de chave</span><span class="sxs-lookup"><span data-stu-id="9fb3f-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="9fb3f-145">O primeiro comando obtém certificados de um repositório de certificados e, em seguida, os armazena na variável de matriz de $certs.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="9fb3f-146">O segundo comando cria um objeto de configuração de máquina virtual e, em seguida, passa-o para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="9fb3f-147">O cmdlet atual adiciona a configuração de provisionamento para uma máquina virtual que inclui certificados e não exporta chaves privadas.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="9fb3f-148">O comando cria a máquina virtual com base no objeto de configuração.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="9fb3f-149">OS</span><span class="sxs-lookup"><span data-stu-id="9fb3f-149">PARAMETERS</span></span>

### <span data-ttu-id="9fb3f-150">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="9fb3f-150">-AdminUsername</span></span>
<span data-ttu-id="9fb3f-151">Especifica o nome de usuário da conta de administrador que essa configuração cria na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-152">-Certificados</span><span class="sxs-lookup"><span data-stu-id="9fb3f-152">-Certificates</span></span>
<span data-ttu-id="9fb3f-153">Especifica um conjunto de certificados que essa configuração instala na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-154">-CustomDatafile</span><span class="sxs-lookup"><span data-stu-id="9fb3f-154">-CustomDataFile</span></span>
<span data-ttu-id="9fb3f-155">Especifica um arquivo de dados para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="9fb3f-156">Esse cmdlet codifica o conteúdo do arquivo como Base64.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="9fb3f-157">O arquivo deve ter menos de 64 kilobytes de comprimento.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="9fb3f-158">Se o sistema operacional convidado for o sistema operacional do Windows, essa configuração salvará esses dados como um arquivo binário denominado%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="9fb3f-159">Se o sistema operacional convidado for Linux, essa configuração passará os dados usando o arquivo ovf-env.xml.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="9fb3f-160">A configuração copia o arquivo para o diretório/var/lib/waagent.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="9fb3f-161">O agente também armazena os dados codificados em base64 no/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="9fb3f-162">-DisableAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="9fb3f-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="9fb3f-163">Indica que essa configuração desabilita as atualizações automáticas.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-163">Indicates that this configuration disables automatic updates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="9fb3f-164">-DisableGuestAgent</span></span>
<span data-ttu-id="9fb3f-165">Indica que essa configuração desabilita o agente convidado de infraestrutura como serviço (IaaS).</span><span class="sxs-lookup"><span data-stu-id="9fb3f-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

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

### <span data-ttu-id="9fb3f-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="9fb3f-166">-DisableSSH</span></span>
<span data-ttu-id="9fb3f-167">Indica que essa configuração desabilita o SSH.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-167">Indicates that this configuration disables SSH.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="9fb3f-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="9fb3f-169">Indica que essa configuração desabilita o gerenciamento remoto do Windows (WinRM) em HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="9fb3f-170">Por padrão, o WinRM está habilitado no HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-170">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-171">-Domain</span><span class="sxs-lookup"><span data-stu-id="9fb3f-171">-Domain</span></span>
<span data-ttu-id="9fb3f-172">Especifica o nome do domínio da conta que tem permissão para adicionar o computador a um domínio.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="9fb3f-173">-DomainPassword</span></span>
<span data-ttu-id="9fb3f-174">Especifica a senha da conta de usuário que tem permissão para adicionar o computador a um domínio.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-175">-DomainUserName</span><span class="sxs-lookup"><span data-stu-id="9fb3f-175">-DomainUserName</span></span>
<span data-ttu-id="9fb3f-176">Especifica o nome da conta de usuário que tem permissão para adicionar o computador a um domínio.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="9fb3f-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="9fb3f-178">Indica que essa configuração habilita o WinRM sobre HTTP.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-179">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9fb3f-179">-InformationAction</span></span>
<span data-ttu-id="9fb3f-180">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9fb3f-181">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9fb3f-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9fb3f-182">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9fb3f-182">Continue</span></span>
- <span data-ttu-id="9fb3f-183">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9fb3f-183">Ignore</span></span>
- <span data-ttu-id="9fb3f-184">Inquire</span><span class="sxs-lookup"><span data-stu-id="9fb3f-184">Inquire</span></span>
- <span data-ttu-id="9fb3f-185">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9fb3f-185">SilentlyContinue</span></span>
- <span data-ttu-id="9fb3f-186">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9fb3f-186">Stop</span></span>
- <span data-ttu-id="9fb3f-187">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9fb3f-187">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-188">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9fb3f-188">-InformationVariable</span></span>
<span data-ttu-id="9fb3f-189">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-189">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="9fb3f-190">-JoinDomain</span></span>
<span data-ttu-id="9fb3f-191">Especifica o nome de domínio totalmente qualificado (FQDN) do domínio para ingressar.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="9fb3f-192">-Linux</span></span>
<span data-ttu-id="9fb3f-193">Indica que essa configuração cria uma configuração Linux.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-193">Indicates that this configuration creates a Linux configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="9fb3f-194">-LinuxUser</span></span>
<span data-ttu-id="9fb3f-195">Especifica o nome de usuário da conta administrativa do Linux que essa configuração cria na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="9fb3f-196">-MachineObjectOU</span></span>
<span data-ttu-id="9fb3f-197">Especifica o nome totalmente qualificado da unidade organizacional (UO) na qual a configuração cria a conta do computador.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="9fb3f-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="9fb3f-199">Indica que essa configuração não carrega a chave privada.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-199">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-200">-NoRDPEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fb3f-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="9fb3f-201">Indica que essa configuração cria uma máquina virtual sem um ponto de extremidade da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fb3f-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="9fb3f-203">Indica que essa configuração cria uma máquina virtual sem um ponto de extremidade SSH.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="9fb3f-204">-NoSSHPassword</span></span>
<span data-ttu-id="9fb3f-205">Indica que essa configuração cria uma máquina virtual sem uma senha SSH.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-206">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="9fb3f-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="9fb3f-207">Indica que essa configuração não adiciona um ponto de extremidade WinRM para a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-208">-Senha</span><span class="sxs-lookup"><span data-stu-id="9fb3f-208">-Password</span></span>
<span data-ttu-id="9fb3f-209">Especifica a senha da conta de administrador.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-209">Specifies the password of the administrator account.</span></span>

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

### <span data-ttu-id="9fb3f-210">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9fb3f-210">-Profile</span></span>
<span data-ttu-id="9fb3f-211">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9fb3f-212">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="9fb3f-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="9fb3f-214">Indica que a máquina virtual exige que o usuário altere a senha no primeiro logon.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="9fb3f-215">-SSHKeyPairs</span></span>
<span data-ttu-id="9fb3f-216">Especifica os pares de chaves SSH.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-216">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="9fb3f-217">-SSHPublicKeys</span></span>
<span data-ttu-id="9fb3f-218">Especifica as chaves públicas SSH.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-218">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-219">-Fuso horário</span><span class="sxs-lookup"><span data-stu-id="9fb3f-219">-TimeZone</span></span>
<span data-ttu-id="9fb3f-220">Especifica o fuso horário da máquina virtual, por exemplo, hora padrão do Pacífico ou horário padrão central do Canadá.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-221">-VM</span><span class="sxs-lookup"><span data-stu-id="9fb3f-221">-VM</span></span>
<span data-ttu-id="9fb3f-222">Especifica um objeto de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-222">Specifies a virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="9fb3f-223">-Windows</span></span>
<span data-ttu-id="9fb3f-224">Indica que essa configuração cria uma máquina virtual autônoma que executa o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-225">-WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="9fb3f-225">-WindowsDomain</span></span>
<span data-ttu-id="9fb3f-226">Indica que essa configuração cria o Windows Server que ingressou em um domínio do Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-227">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="9fb3f-227">-WinRMCertificate</span></span>
<span data-ttu-id="9fb3f-228">Especifica um certificado que essa configuração associa a um ponto de extremidade WinRM.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-229">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="9fb3f-229">-X509Certificates</span></span>
<span data-ttu-id="9fb3f-230">Especifica uma matriz de certificados X509 que são implantados em um serviço hospedado.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb3f-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb3f-231">CommonParameters</span></span>
<span data-ttu-id="9fb3f-232">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fb3f-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb3f-233">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fb3f-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb3f-234">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9fb3f-234">INPUTS</span></span>

## <span data-ttu-id="9fb3f-235">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9fb3f-235">OUTPUTS</span></span>

## <span data-ttu-id="9fb3f-236">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9fb3f-236">NOTES</span></span>

## <span data-ttu-id="9fb3f-237">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9fb3f-237">RELATED LINKS</span></span>

[<span data-ttu-id="9fb3f-238">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="9fb3f-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="9fb3f-239">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="9fb3f-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


