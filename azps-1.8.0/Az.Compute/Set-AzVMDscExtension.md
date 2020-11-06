---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 75cd5e76fe4ebce1479525aba2c36e6741b6094b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601227"
---
# <span data-ttu-id="e73d0-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e73d0-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="e73d0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e73d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e73d0-103">Configura a extensão DSC em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e73d0-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="e73d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e73d0-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e73d0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e73d0-105">DESCRIPTION</span></span>
<span data-ttu-id="e73d0-106">O cmdlet **set-AzVMDscExtension** configura a extensão de estado desejado (DSC) do Windows PowerShell em uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e73d0-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="e73d0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e73d0-107">EXAMPLES</span></span>

### <span data-ttu-id="e73d0-108">Exemplo 1: definir uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="e73d0-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="e73d0-109">Esse comando define a extensão DSC na máquina virtual nomeada VM07 para baixar Sample.ps1.zip da conta de armazenamento chamada STG e o contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="e73d0-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="e73d0-110">O comando invoca a configuração chamada configname.</span><span class="sxs-lookup"><span data-stu-id="e73d0-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="e73d0-111">O arquivo Sample.ps1.zip foi carregado anteriormente usando **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e73d0-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="e73d0-112">Exemplo 2: definir uma extensão DSC com dados de configuração</span><span class="sxs-lookup"><span data-stu-id="e73d0-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="e73d0-113">Esse comando define a extensão na máquina virtual nomeada VM13 para baixar Sample.ps1.zip da conta de armazenamento chamada STG e o contêiner chamado WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="e73d0-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="e73d0-114">O comando a configuração nomeada ConfigName e especifica os dados de configuração e os argumentos.</span><span class="sxs-lookup"><span data-stu-id="e73d0-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="e73d0-115">O arquivo Sample.ps1.zip foi carregado anteriormente usando **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e73d0-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="e73d0-116">Exemplo 3: definir uma extensão DSC com dados de configuração com atualização automática</span><span class="sxs-lookup"><span data-stu-id="e73d0-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="e73d0-117">Esse comando define a extensão na máquina virtual nomeada VM22 para baixar Sample.ps1.zip da conta de armazenamento chamada STG e o contêiner chamado WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="e73d0-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="e73d0-118">O comando invoca a configuração nomeada ConfigName e especifica dados de configuração e argumentos.</span><span class="sxs-lookup"><span data-stu-id="e73d0-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="e73d0-119">Esse comando também habilita a atualização automática do manipulador de extensão para a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="e73d0-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="e73d0-120">O Sample.ps1.zip foi carregado anteriormente usando **Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e73d0-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="e73d0-121">OS</span><span class="sxs-lookup"><span data-stu-id="e73d0-121">PARAMETERS</span></span>

### <span data-ttu-id="e73d0-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="e73d0-122">-ArchiveBlobName</span></span>
<span data-ttu-id="e73d0-123">Especifica o nome do arquivo de configuração que foi carregado anteriormente pelo cmdlet Publish-AzVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="e73d0-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationArchiveBlob

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="e73d0-124">-ArchiveContainerName</span></span>
<span data-ttu-id="e73d0-125">Nome da espécie do contêiner de armazenamento do Azure em que o arquivo morto de configuração está localizado.</span><span class="sxs-lookup"><span data-stu-id="e73d0-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e73d0-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="e73d0-127">Especifica o nome do grupo de recursos que contém a conta de armazenamento que contém o arquivo morto de configuração.</span><span class="sxs-lookup"><span data-stu-id="e73d0-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="e73d0-128">Esse parâmetro é opcional se a conta de armazenamento e a máquina virtual estiverem no mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e73d0-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e73d0-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="e73d0-130">Especifica o nome da conta de armazenamento do Azure que é usado para baixar o ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="e73d0-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="e73d0-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="e73d0-132">Especifica o sufixo de ponto de extremidade de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e73d0-132">Specifies the storage endpoint suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-133">-Atualização automática</span><span class="sxs-lookup"><span data-stu-id="e73d0-133">-AutoUpdate</span></span>
<span data-ttu-id="e73d0-134">Especifica a versão do manipulador de extensões especificada pelo parâmetro de *versão* .</span><span class="sxs-lookup"><span data-stu-id="e73d0-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="e73d0-135">Por padrão, o manipulador de extensão não é atualizado de acordo com o AutoUpdate.</span><span class="sxs-lookup"><span data-stu-id="e73d0-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="e73d0-136">Use o parâmetro *AutoUpdate* para habilitar a atualização automática do manipulador de extensão para a versão mais recente como e quando ela estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="e73d0-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="e73d0-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="e73d0-137">-ConfigurationArgument</span></span>
<span data-ttu-id="e73d0-138">Especifica uma tabela de hash que contém os argumentos para a função de configuração.</span><span class="sxs-lookup"><span data-stu-id="e73d0-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="e73d0-139">-ConfigurationData</span></span>
<span data-ttu-id="e73d0-140">Especifica o caminho de um arquivo. psd1 que especifica os dados para a configuração.</span><span class="sxs-lookup"><span data-stu-id="e73d0-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e73d0-141">-ConfigurationName</span></span>
<span data-ttu-id="e73d0-142">Especifica o nome da configuração invocada pela extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="e73d0-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="e73d0-143">-DataCollection</span></span>
<span data-ttu-id="e73d0-144">Especifica o tipo de coleção de dados.</span><span class="sxs-lookup"><span data-stu-id="e73d0-144">Specifies the data collection type.</span></span>
<span data-ttu-id="e73d0-145">Os valores aceitáveis para esse parâmetro são: Enable e Disable.</span><span class="sxs-lookup"><span data-stu-id="e73d0-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e73d0-146">-DefaultProfile</span></span>
<span data-ttu-id="e73d0-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e73d0-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e73d0-148">-Force</span><span class="sxs-lookup"><span data-stu-id="e73d0-148">-Force</span></span>
<span data-ttu-id="e73d0-149">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="e73d0-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e73d0-150">-Local</span><span class="sxs-lookup"><span data-stu-id="e73d0-150">-Location</span></span>
<span data-ttu-id="e73d0-151">Especifica o caminho da extensão do recurso.</span><span class="sxs-lookup"><span data-stu-id="e73d0-151">Specifies the path of the resource extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="e73d0-152">-Name</span></span>
<span data-ttu-id="e73d0-153">Especifica o nome do recurso do Gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="e73d0-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="e73d0-154">O valor padrão é Microsoft. PowerShell. DSC.</span><span class="sxs-lookup"><span data-stu-id="e73d0-154">The default value is Microsoft.Powershell.DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e73d0-155">-ResourceGroupName</span></span>
<span data-ttu-id="e73d0-156">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e73d0-156">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e73d0-157">-Versão</span><span class="sxs-lookup"><span data-stu-id="e73d0-157">-Version</span></span>
<span data-ttu-id="e73d0-158">Especifica a versão da extensão DSC à qual Set-AzVMDscExtension aplica as configurações.</span><span class="sxs-lookup"><span data-stu-id="e73d0-158">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-159">-VMName</span><span class="sxs-lookup"><span data-stu-id="e73d0-159">-VMName</span></span>
<span data-ttu-id="e73d0-160">Especifica o nome da máquina virtual na qual o manipulador de extensão DSC está instalado.</span><span class="sxs-lookup"><span data-stu-id="e73d0-160">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-161">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="e73d0-161">-WmfVersion</span></span>
<span data-ttu-id="e73d0-162">Especifica a versão do WMF.</span><span class="sxs-lookup"><span data-stu-id="e73d0-162">Specifies the WMF version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: 4.0, 5.0, 5.1, latest

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-163">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e73d0-163">-Confirm</span></span>
<span data-ttu-id="e73d0-164">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e73d0-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e73d0-165">-WhatIf</span></span>
<span data-ttu-id="e73d0-166">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e73d0-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e73d0-167">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e73d0-167">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e73d0-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e73d0-168">CommonParameters</span></span>
<span data-ttu-id="e73d0-169">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e73d0-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e73d0-170">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e73d0-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e73d0-171">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e73d0-171">INPUTS</span></span>

### <span data-ttu-id="e73d0-172">System. String</span><span class="sxs-lookup"><span data-stu-id="e73d0-172">System.String</span></span>

### <span data-ttu-id="e73d0-173">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e73d0-173">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e73d0-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e73d0-174">OUTPUTS</span></span>

### <span data-ttu-id="e73d0-175">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e73d0-175">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e73d0-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e73d0-176">NOTES</span></span>

## <span data-ttu-id="e73d0-177">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e73d0-177">RELATED LINKS</span></span>

[<span data-ttu-id="e73d0-178">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e73d0-178">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="e73d0-179">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="e73d0-179">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="e73d0-180">Publicar-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e73d0-180">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


