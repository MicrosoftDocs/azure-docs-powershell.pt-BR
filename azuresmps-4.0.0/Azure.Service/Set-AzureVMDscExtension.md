---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947351"
---
# <span data-ttu-id="9d901-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9d901-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="9d901-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d901-102">SYNOPSIS</span></span>
<span data-ttu-id="9d901-103">Configura a extensão DSC em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d901-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="9d901-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d901-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d901-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9d901-105">DESCRIPTION</span></span>
<span data-ttu-id="9d901-106">O cmdlet **set-AzureVMDscExtension** configura a extensão da configuração de estado desejada (DSC) em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d901-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="9d901-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9d901-107">EXAMPLES</span></span>

### <span data-ttu-id="9d901-108">Exemplo 1: configurar a extensão DSC em uma máquina virtual</span><span class="sxs-lookup"><span data-stu-id="9d901-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="9d901-109">Esse comando configura a extensão DSC em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d901-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="9d901-110">O pacote MyConfiguration.ps1.zip deve ter sido previamente carregado no armazenamento do Azure usando o comando **Publish-AzureVMDscConfiguration** e inclui o script MyConfiguration.ps1 e os módulos dos quais ele depende.</span><span class="sxs-lookup"><span data-stu-id="9d901-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="9d901-111">O argumento myconfiguration indica a configuração DSC específica dentro do script a ser executada.</span><span class="sxs-lookup"><span data-stu-id="9d901-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="9d901-112">O parâmetro- *ConfigurationArgument* especifica uma Hashtable com os argumentos que são passados para a função de configuração.</span><span class="sxs-lookup"><span data-stu-id="9d901-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="9d901-113">Exemplo 2: configurar a extensão DSC em uma máquina virtual usando um caminho para os dados de configuração</span><span class="sxs-lookup"><span data-stu-id="9d901-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="9d901-114">Esse comando configura a extensão DSC em uma máquina virtual usando um caminho para os dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="9d901-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="9d901-115">OS</span><span class="sxs-lookup"><span data-stu-id="9d901-115">PARAMETERS</span></span>

### <span data-ttu-id="9d901-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="9d901-116">-ConfigurationArchive</span></span>
<span data-ttu-id="9d901-117">Especifica o nome do pacote de configuração (arquivo. zip) que foi carregado anteriormente por Publish-AzureVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9d901-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="9d901-118">Esse parâmetro deve especificar somente o nome do arquivo, sem qualquer caminho.</span><span class="sxs-lookup"><span data-stu-id="9d901-118">This parameter must specify only the name of the file, without any path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d901-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="9d901-119">-ConfigurationArgument</span></span>
<span data-ttu-id="9d901-120">Especifica uma Hashtable especificando os argumentos para a função de configuração.</span><span class="sxs-lookup"><span data-stu-id="9d901-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="9d901-121">As chaves correspondem aos nomes de parâmetro e aos valores para os valores de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="9d901-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="9d901-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9d901-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d901-123">tipos primitivos</span><span class="sxs-lookup"><span data-stu-id="9d901-123">primitive types</span></span>
- <span data-ttu-id="9d901-124">String</span><span class="sxs-lookup"><span data-stu-id="9d901-124">string</span></span>
- <span data-ttu-id="9d901-125">matriz</span><span class="sxs-lookup"><span data-stu-id="9d901-125">array</span></span>
- <span data-ttu-id="9d901-126">PSCredential</span><span class="sxs-lookup"><span data-stu-id="9d901-126">PSCredential</span></span>

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

### <span data-ttu-id="9d901-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="9d901-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="9d901-128">Especifica o caminho de um arquivo. psd1 que especifica os dados para a função de configuração.</span><span class="sxs-lookup"><span data-stu-id="9d901-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="9d901-129">Esse arquivo deve conter uma Hashtable, conforme descrito em separando os dados de configuração e de ambiente https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .</span><span class="sxs-lookup"><span data-stu-id="9d901-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

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

### <span data-ttu-id="9d901-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9d901-130">-ConfigurationName</span></span>
<span data-ttu-id="9d901-131">Especifica o nome do script de configuração ou do módulo que é invocado pela extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="9d901-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="9d901-132">O valor desse parâmetro deve ser o nome de uma das funções de configuração contidas nos scripts ou módulos empacotados em *ConfigurationArchive*.</span><span class="sxs-lookup"><span data-stu-id="9d901-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="9d901-133">Esse cmdlet usa como padrão o nome do arquivo fornecido pelo parâmetro *ConfigurationArchive* se você omitir esse parâmetro, excluindo qualquer extensão.</span><span class="sxs-lookup"><span data-stu-id="9d901-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="9d901-134">Por exemplo, se *ConfigurationArchive* for "SalesWebSite.ps1.zip", o valor padrão para *ConfigurationName* será "SalesWebSite".</span><span class="sxs-lookup"><span data-stu-id="9d901-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

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

### <span data-ttu-id="9d901-135">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9d901-135">-ContainerName</span></span>
<span data-ttu-id="9d901-136">Especifica o nome do contêiner de armazenamento do Azure em que o *ConfigurationArchive* está localizado.</span><span class="sxs-lookup"><span data-stu-id="9d901-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

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

### <span data-ttu-id="9d901-137">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="9d901-137">-DataCollection</span></span>
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

### <span data-ttu-id="9d901-138">-Force</span><span class="sxs-lookup"><span data-stu-id="9d901-138">-Force</span></span>
<span data-ttu-id="9d901-139">Indica que esse cmdlet substitui BLOBs existentes.</span><span class="sxs-lookup"><span data-stu-id="9d901-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

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

### <span data-ttu-id="9d901-140">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="9d901-140">-InformationAction</span></span>
<span data-ttu-id="9d901-141">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="9d901-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9d901-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9d901-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d901-143">Contínuo</span><span class="sxs-lookup"><span data-stu-id="9d901-143">Continue</span></span>
- <span data-ttu-id="9d901-144">Ignorar</span><span class="sxs-lookup"><span data-stu-id="9d901-144">Ignore</span></span>
- <span data-ttu-id="9d901-145">Inquire</span><span class="sxs-lookup"><span data-stu-id="9d901-145">Inquire</span></span>
- <span data-ttu-id="9d901-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9d901-146">SilentlyContinue</span></span>
- <span data-ttu-id="9d901-147">Finaliza</span><span class="sxs-lookup"><span data-stu-id="9d901-147">Stop</span></span>
- <span data-ttu-id="9d901-148">Suspensão</span><span class="sxs-lookup"><span data-stu-id="9d901-148">Suspend</span></span>

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

### <span data-ttu-id="9d901-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9d901-149">-InformationVariable</span></span>
<span data-ttu-id="9d901-150">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="9d901-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9d901-151">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9d901-151">-Profile</span></span>
<span data-ttu-id="9d901-152">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="9d901-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d901-153">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9d901-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d901-154">-Referencename</span><span class="sxs-lookup"><span data-stu-id="9d901-154">-ReferenceName</span></span>
<span data-ttu-id="9d901-155">Especifica uma cadeia de caracteres definida pelo usuário que pode ser usada para fazer referência a uma extensão.</span><span class="sxs-lookup"><span data-stu-id="9d901-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="9d901-156">Esse parâmetro é especificado quando a extensão é adicionada à máquina virtual pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="9d901-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="9d901-157">Para atualizações subsequentes, você deve especificar o nome de referência usado anteriormente enquanto atualiza a extensão.</span><span class="sxs-lookup"><span data-stu-id="9d901-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="9d901-158">O *referencename* atribuído a uma extensão é retornado usando o cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="9d901-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="9d901-159">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="9d901-159">-StorageContext</span></span>
<span data-ttu-id="9d901-160">Especifica o contexto de armazenamento do Azure que fornece as configurações de segurança usadas para acessar o script de configuração.</span><span class="sxs-lookup"><span data-stu-id="9d901-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="9d901-161">Esse contexto fornece acesso de leitura ao contêiner especificado pelo parâmetro *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="9d901-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d901-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9d901-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="9d901-163">Especifica o sufixo de ponto de extremidade DNS para todos os serviços de armazenamento, por exemplo, "core.contoso.net".</span><span class="sxs-lookup"><span data-stu-id="9d901-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

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

### <span data-ttu-id="9d901-164">-Versão</span><span class="sxs-lookup"><span data-stu-id="9d901-164">-Version</span></span>
<span data-ttu-id="9d901-165">Especifica a versão específica da extensão DSC a ser usada.</span><span class="sxs-lookup"><span data-stu-id="9d901-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="9d901-166">O valor padrão é definido como "1. \*" se esse parâmetro não for especificado.</span><span class="sxs-lookup"><span data-stu-id="9d901-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

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

### <span data-ttu-id="9d901-167">-VM</span><span class="sxs-lookup"><span data-stu-id="9d901-167">-VM</span></span>
<span data-ttu-id="9d901-168">Especifica o objeto da máquina virtual persistente.</span><span class="sxs-lookup"><span data-stu-id="9d901-168">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d901-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="9d901-169">-WmfVersion</span></span>
<span data-ttu-id="9d901-170">Especifica a versão da Windows Management Framework (WMF) a ser instalada na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d901-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="9d901-171">A extensão DSC depende dos recursos DSC disponíveis apenas nas atualizações do WMF.</span><span class="sxs-lookup"><span data-stu-id="9d901-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="9d901-172">Esse parâmetro especifica qual versão da atualização instalar na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9d901-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="9d901-173">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="9d901-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9d901-174">4,0.</span><span class="sxs-lookup"><span data-stu-id="9d901-174">4.0.</span></span>
<span data-ttu-id="9d901-175">Instala o WMF 4,0, a menos que uma versão mais recente já esteja instalada.</span><span class="sxs-lookup"><span data-stu-id="9d901-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="9d901-176">5,0.</span><span class="sxs-lookup"><span data-stu-id="9d901-176">5.0.</span></span>
<span data-ttu-id="9d901-177">Instala a versão mais recente do WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="9d901-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="9d901-178">novidades.</span><span class="sxs-lookup"><span data-stu-id="9d901-178">latest.</span></span>
<span data-ttu-id="9d901-179">Instala o WMF mais recente, no momento, o WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="9d901-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="9d901-180">O valor padrão é mais recente.</span><span class="sxs-lookup"><span data-stu-id="9d901-180">The default value is latest.</span></span>

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

### <span data-ttu-id="9d901-181">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9d901-181">-Confirm</span></span>
<span data-ttu-id="9d901-182">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d901-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d901-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d901-183">-WhatIf</span></span>
<span data-ttu-id="9d901-184">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9d901-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d901-185">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9d901-185">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d901-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d901-186">CommonParameters</span></span>
<span data-ttu-id="9d901-187">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d901-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d901-188">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d901-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d901-189">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9d901-189">INPUTS</span></span>

## <span data-ttu-id="9d901-190">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9d901-190">OUTPUTS</span></span>

## <span data-ttu-id="9d901-191">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9d901-191">NOTES</span></span>

## <span data-ttu-id="9d901-192">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d901-192">RELATED LINKS</span></span>

[<span data-ttu-id="9d901-193">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9d901-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="9d901-194">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9d901-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="9d901-195">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9d901-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="9d901-196">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="9d901-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="9d901-197">Publicar-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d901-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)


