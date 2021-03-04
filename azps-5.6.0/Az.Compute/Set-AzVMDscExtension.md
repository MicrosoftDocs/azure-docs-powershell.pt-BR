---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: facd5a3637dcb1a8a392171468dd890279ba0f74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886074"
---
# <span data-ttu-id="94331-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="94331-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="94331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94331-102">SYNOPSIS</span></span>
<span data-ttu-id="94331-103">Configura a extensão DSC em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="94331-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="94331-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="94331-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94331-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="94331-105">DESCRIPTION</span></span>
<span data-ttu-id="94331-106">O cmdlet **Set-AzVMDscExtension** configura a extensão Windows PowerShell DSC (Configuração de Estado Desejado) em uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="94331-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="94331-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94331-107">EXAMPLES</span></span>

### <span data-ttu-id="94331-108">Exemplo 1: Definir uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="94331-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="94331-109">Este comando define a extensão DSC na máquina virtual chamada VM07 para baixar Sample.ps1.zip da conta de armazenamento chamada Stg e do contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="94331-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="94331-110">O comando invoca a configuração chamada ConfigName.</span><span class="sxs-lookup"><span data-stu-id="94331-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="94331-111">O Sample.ps1.zip arquivo foi carregado anteriormente **usando Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="94331-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="94331-112">Exemplo 2: definir uma extensão DSC com dados de configuração</span><span class="sxs-lookup"><span data-stu-id="94331-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="94331-113">Este comando define a extensão na máquina virtual chamada VM13 para baixar Sample.ps1.zip da conta de armazenamento chamada Stg e do contêiner chamado WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="94331-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="94331-114">O comando a configuração denominada ConfigName e especifica dados e argumentos de configuração.</span><span class="sxs-lookup"><span data-stu-id="94331-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="94331-115">O Sample.ps1.zip arquivo foi carregado anteriormente **usando Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="94331-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="94331-116">Exemplo 3: definir uma extensão DSC com dados de configuração que têm atualização automática</span><span class="sxs-lookup"><span data-stu-id="94331-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="94331-117">Este comando define a extensão na máquina virtual chamada VM22 para baixar Sample.ps1.zip da conta de armazenamento chamada Stg e do contêiner chamado WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="94331-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="94331-118">O comando invoca a configuração chamada ConfigName e especifica dados e argumentos de configuração.</span><span class="sxs-lookup"><span data-stu-id="94331-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="94331-119">Esse comando também habilita a atualização automática do manipulador de extensão para a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="94331-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="94331-120">O Sample.ps1.zip foi carregado anteriormente **usando Publish-AzVMDscConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="94331-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="94331-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="94331-121">PARAMETERS</span></span>

### <span data-ttu-id="94331-122">-ArchiveBlobName</span><span class="sxs-lookup"><span data-stu-id="94331-122">-ArchiveBlobName</span></span>
<span data-ttu-id="94331-123">Especifica o nome do arquivo de configuração que foi carregado anteriormente pelo cmdlet Publish-AzVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="94331-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="94331-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="94331-124">-ArchiveContainerName</span></span>
<span data-ttu-id="94331-125">Nome da espécie do contêiner de armazenamento do Azure onde o arquivo de configuração está localizado.</span><span class="sxs-lookup"><span data-stu-id="94331-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="94331-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94331-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="94331-127">Especifica o nome do grupo de recursos que contém a conta de armazenamento que contém o arquivo morto de configuração.</span><span class="sxs-lookup"><span data-stu-id="94331-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="94331-128">Esse parâmetro é opcional se a conta de armazenamento e a máquina virtual estão no mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="94331-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="94331-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="94331-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="94331-130">Especifica o nome da conta de armazenamento do Azure usada para baixar ArchiveBlobName.</span><span class="sxs-lookup"><span data-stu-id="94331-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="94331-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="94331-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="94331-132">Especifica o sufixo do ponto de extremidade de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="94331-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="94331-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="94331-133">-AutoUpdate</span></span>
<span data-ttu-id="94331-134">Especifica a versão do manipulador de extensão especificada pelo parâmetro *Version.*</span><span class="sxs-lookup"><span data-stu-id="94331-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="94331-135">Por padrão, o manipulador de extensão não é autoupdated.</span><span class="sxs-lookup"><span data-stu-id="94331-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="94331-136">Use o *parâmetro AutoUpdate* para habilitar a atualização automática do manipulador de extensão para a versão mais recente como e quando ela está disponível.</span><span class="sxs-lookup"><span data-stu-id="94331-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="94331-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="94331-137">-ConfigurationArgument</span></span>
<span data-ttu-id="94331-138">Especifica uma tabela de hash que contém os argumentos para a função de configuração.</span><span class="sxs-lookup"><span data-stu-id="94331-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="94331-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="94331-139">-ConfigurationData</span></span>
<span data-ttu-id="94331-140">Especifica o caminho de um arquivo .psd1 que especifica os dados para a configuração.</span><span class="sxs-lookup"><span data-stu-id="94331-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="94331-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="94331-141">-ConfigurationName</span></span>
<span data-ttu-id="94331-142">Especifica o nome da configuração invocada pela Extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="94331-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="94331-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="94331-143">-DataCollection</span></span>
<span data-ttu-id="94331-144">Especifica o tipo de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="94331-144">Specifies the data collection type.</span></span>
<span data-ttu-id="94331-145">Os valores aceitáveis para este parâmetro são: Habilitar e Desabilitar.</span><span class="sxs-lookup"><span data-stu-id="94331-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="94331-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94331-146">-DefaultProfile</span></span>
<span data-ttu-id="94331-147">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="94331-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94331-148">-Force</span><span class="sxs-lookup"><span data-stu-id="94331-148">-Force</span></span>
<span data-ttu-id="94331-149">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="94331-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94331-150">-Location</span><span class="sxs-lookup"><span data-stu-id="94331-150">-Location</span></span>
<span data-ttu-id="94331-151">Especifica o caminho da extensão do recurso.</span><span class="sxs-lookup"><span data-stu-id="94331-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="94331-152">-Name</span><span class="sxs-lookup"><span data-stu-id="94331-152">-Name</span></span>
<span data-ttu-id="94331-153">Especifica o nome do recurso Gerenciador de Recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="94331-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="94331-154">O valor padrão é Microsoft.Powershell.DSC.</span><span class="sxs-lookup"><span data-stu-id="94331-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="94331-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="94331-155">-NoWait</span></span>
<span data-ttu-id="94331-156">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="94331-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="94331-157">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="94331-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="94331-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94331-158">-ResourceGroupName</span></span>
<span data-ttu-id="94331-159">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="94331-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="94331-160">-Version</span><span class="sxs-lookup"><span data-stu-id="94331-160">-Version</span></span>
<span data-ttu-id="94331-161">Especifica a versão da extensão DSC à Set-AzVMDscExtension aplica as configurações.</span><span class="sxs-lookup"><span data-stu-id="94331-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="94331-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="94331-162">-VMName</span></span>
<span data-ttu-id="94331-163">Especifica o nome da máquina virtual onde o manipulador de extensão DSC está instalado.</span><span class="sxs-lookup"><span data-stu-id="94331-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="94331-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="94331-164">-WmfVersion</span></span>
<span data-ttu-id="94331-165">Especifica a versão WMF.</span><span class="sxs-lookup"><span data-stu-id="94331-165">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="94331-166">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94331-166">-Confirm</span></span>
<span data-ttu-id="94331-167">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94331-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94331-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94331-168">-WhatIf</span></span>
<span data-ttu-id="94331-169">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94331-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94331-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94331-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94331-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94331-171">CommonParameters</span></span>
<span data-ttu-id="94331-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94331-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94331-173">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94331-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94331-174">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94331-174">INPUTS</span></span>

### <span data-ttu-id="94331-175">System.String</span><span class="sxs-lookup"><span data-stu-id="94331-175">System.String</span></span>

### <span data-ttu-id="94331-176">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="94331-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="94331-177">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="94331-177">OUTPUTS</span></span>

### <span data-ttu-id="94331-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="94331-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="94331-179">NOTES</span><span class="sxs-lookup"><span data-stu-id="94331-179">NOTES</span></span>

## <span data-ttu-id="94331-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94331-180">RELATED LINKS</span></span>

[<span data-ttu-id="94331-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="94331-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="94331-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="94331-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="94331-183">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="94331-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


