---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 04F58D88-53D6-42CA-852C-9E2A129898C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDscExtension.md
ms.openlocfilehash: 7b4c416b8a083b1cf64e9e23ccdf08f153a76261
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116507"
---
# <span data-ttu-id="1de6a-101">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1de6a-101">Set-AzVMDscExtension</span></span>

## <span data-ttu-id="1de6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1de6a-102">SYNOPSIS</span></span>
<span data-ttu-id="1de6a-103">Configura a extensão DSC em uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1de6a-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="1de6a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1de6a-104">SYNTAX</span></span>

```
Set-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-ArchiveBlobName] <String> [-ArchiveStorageAccountName] <String> [-ArchiveResourceGroupName <String>]
 [-ArchiveStorageEndpointSuffix <String>] [-ArchiveContainerName <String>] [-ConfigurationName <String>]
 [-ConfigurationArgument <Hashtable>] [-ConfigurationData <String>] [-Version] <String> [-Force]
 [-Location <String>] [-AutoUpdate] [-WmfVersion <String>] [-DataCollection <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1de6a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1de6a-105">DESCRIPTION</span></span>
<span data-ttu-id="1de6a-106">O cmdlet **Set-AzVMDscExtension** configura a extensão DSC (Configuração de Estado Desejada) do Windows PowerShell em uma máquina virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1de6a-106">The **Set-AzVMDscExtension** cmdlet configures the Windows PowerShell Desired State Configuration (DSC) extension on a virtual machine in a resource group.</span></span>

## <span data-ttu-id="1de6a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1de6a-107">EXAMPLES</span></span>

### <span data-ttu-id="1de6a-108">Exemplo 1: Definir uma extensão DSC</span><span class="sxs-lookup"><span data-stu-id="1de6a-108">Example 1: Set a DSC extension</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -Version "1.10" -Location "West US"
```

<span data-ttu-id="1de6a-109">Esse comando define a extensão DSC na máquina virtual chamada VM07 para baixar Sample.ps1.zip da conta de armazenamento chamada Stg e do contêiner padrão.</span><span class="sxs-lookup"><span data-stu-id="1de6a-109">This command sets the DSC extension on the virtual machine named VM07 to download Sample.ps1.zip from the storage account named Stg and the default container.</span></span>
<span data-ttu-id="1de6a-110">O comando invocará a configuração chamada ConfigName.</span><span class="sxs-lookup"><span data-stu-id="1de6a-110">The command invokes the configuration named ConfigName.</span></span>
<span data-ttu-id="1de6a-111">O Sample.ps1.zip arquivo foi carregado anteriormente **usando Publish-AzVMDscConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="1de6a-111">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="1de6a-112">Exemplo 2: Definir uma extensão DSC com dados de configuração</span><span class="sxs-lookup"><span data-stu-id="1de6a-112">Example 2: Set a DSC extension with configuration data</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM13" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName "WindowsPowerShellDSC" -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US"
```

<span data-ttu-id="1de6a-113">Esse comando define a extensão na máquina virtual chamada VM13 para baixar Sample.ps1.zip da conta de armazenamento chamada Stg e do contêiner chamado WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="1de6a-113">This command sets the extension on the virtual machine named VM13 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="1de6a-114">O comando da configuração chamado ConfigName e especifica dados e argumentos de configuração.</span><span class="sxs-lookup"><span data-stu-id="1de6a-114">The command the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="1de6a-115">O Sample.ps1.zip arquivo foi carregado anteriormente **usando Publish-AzVMDscConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="1de6a-115">The Sample.ps1.zip file was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

### <span data-ttu-id="1de6a-116">Exemplo 3: Definir uma extensão DSC com dados de configuração que têm atualização automática</span><span class="sxs-lookup"><span data-stu-id="1de6a-116">Example 3: Set a DSC extension with configuration data that has auto update</span></span>
```
PS C:\> Set-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM22" -ArchiveBlobName "Sample.ps1.zip" -ArchiveStorageAccountName "Stg" -ConfigurationName "ConfigName" -ConfigurationArgument "@{arg="val"}" -ArchiveContainerName WindowsPowerShellDSC -ConfigurationData "SampleData.psd1" -Version "1.10" -Location "West US" -AutoUpdate
```

<span data-ttu-id="1de6a-117">Esse comando define a extensão na máquina virtual chamada VM22 para baixar Sample.ps1.zip da conta de armazenamento chamada Stg e do contêiner chamado WindowsPowerShellDSC.</span><span class="sxs-lookup"><span data-stu-id="1de6a-117">This command sets the extension on the virtual machine named VM22 to download Sample.ps1.zip from the storage account named Stg and the container named WindowsPowerShellDSC.</span></span>
<span data-ttu-id="1de6a-118">O comando invocará a configuração chamada ConfigName e especificará dados e argumentos de configuração.</span><span class="sxs-lookup"><span data-stu-id="1de6a-118">The command invokes the configuration named ConfigName and specifies configuration data and arguments.</span></span>
<span data-ttu-id="1de6a-119">Esse comando também habilita a atualização automática do manipulador de extensão para a versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="1de6a-119">This command also enables auto update of extension handler to the latest version.</span></span>
<span data-ttu-id="1de6a-120">O Sample.ps1.zip foi carregado anteriormente **usando Publish-AzVMDscConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="1de6a-120">The Sample.ps1.zip was previously uploaded by using **Publish-AzVMDscConfiguration**.</span></span>

## <span data-ttu-id="1de6a-121">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1de6a-121">PARAMETERS</span></span>

### <span data-ttu-id="1de6a-122">-ArchiveBname</span><span class="sxs-lookup"><span data-stu-id="1de6a-122">-ArchiveBlobName</span></span>
<span data-ttu-id="1de6a-123">Especifica o nome do arquivo de configuração que foi carregado anteriormente pelo cmdlet Publish-AzVMDscConfiguration usuário.</span><span class="sxs-lookup"><span data-stu-id="1de6a-123">Specifies the name of the configuration file that was previously uploaded by the Publish-AzVMDscConfiguration cmdlet.</span></span>

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

### <span data-ttu-id="1de6a-124">-ArchiveContainerName</span><span class="sxs-lookup"><span data-stu-id="1de6a-124">-ArchiveContainerName</span></span>
<span data-ttu-id="1de6a-125">Nome da espécies do contêiner de armazenamento do Azure onde o arquivo de configuração está localizado.</span><span class="sxs-lookup"><span data-stu-id="1de6a-125">Species name of the Azure storage container where the configuration archive is located.</span></span>

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

### <span data-ttu-id="1de6a-126">-ArchiveResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1de6a-126">-ArchiveResourceGroupName</span></span>
<span data-ttu-id="1de6a-127">Especifica o nome do grupo de recursos que contém a conta de armazenamento que contém o arquivo morto de configuração.</span><span class="sxs-lookup"><span data-stu-id="1de6a-127">Specifies the name of the resource group that contains the storage account that contains the configuration archive.</span></span>
<span data-ttu-id="1de6a-128">Esse parâmetro é opcional se a conta de armazenamento e a máquina virtual estão no mesmo grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1de6a-128">This parameter is optional if the storage account and virtual machine are both in the same resource group.</span></span>

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

### <span data-ttu-id="1de6a-129">-ArchiveStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1de6a-129">-ArchiveStorageAccountName</span></span>
<span data-ttu-id="1de6a-130">Especifica o nome da conta de armazenamento do Azure usada para baixar o ArchiveBname.</span><span class="sxs-lookup"><span data-stu-id="1de6a-130">Specifies the Azure storage account name that is used to download the ArchiveBlobName.</span></span>

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

### <span data-ttu-id="1de6a-131">-ArchiveStorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="1de6a-131">-ArchiveStorageEndpointSuffix</span></span>
<span data-ttu-id="1de6a-132">Especifica o sufixo do ponto de extremidade de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1de6a-132">Specifies the storage endpoint suffix.</span></span>

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

### <span data-ttu-id="1de6a-133">-AutoUpdate</span><span class="sxs-lookup"><span data-stu-id="1de6a-133">-AutoUpdate</span></span>
<span data-ttu-id="1de6a-134">Especifica a versão do manipulador de extensão especificada pelo parâmetro *Versão.*</span><span class="sxs-lookup"><span data-stu-id="1de6a-134">Specifies the extension handler version specified by the *Version* parameter.</span></span>
<span data-ttu-id="1de6a-135">Por padrão, o manipulador de extensão não é autoupedado.</span><span class="sxs-lookup"><span data-stu-id="1de6a-135">By default extension handler is not autoupdated.</span></span>
<span data-ttu-id="1de6a-136">Use o *parâmetro AutoUpdate* para habilitar a atualização automática do manipulador de extensão para a versão mais recente, como e quando ele está disponível.</span><span class="sxs-lookup"><span data-stu-id="1de6a-136">Use the *AutoUpdate* parameter to enable auto update of the extension handler to the latest version as and when it is available.</span></span>

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

### <span data-ttu-id="1de6a-137">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="1de6a-137">-ConfigurationArgument</span></span>
<span data-ttu-id="1de6a-138">Especifica uma tabela hash que contém os argumentos para a função de configuração.</span><span class="sxs-lookup"><span data-stu-id="1de6a-138">Specifies a hash table that contains the arguments to the configuration function.</span></span>

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

### <span data-ttu-id="1de6a-139">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="1de6a-139">-ConfigurationData</span></span>
<span data-ttu-id="1de6a-140">Especifica o caminho de um arquivo .psd1 que especifica os dados para a configuração.</span><span class="sxs-lookup"><span data-stu-id="1de6a-140">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>

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

### <span data-ttu-id="1de6a-141">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1de6a-141">-ConfigurationName</span></span>
<span data-ttu-id="1de6a-142">Especifica o nome da configuração invocada pela Extensão DSC.</span><span class="sxs-lookup"><span data-stu-id="1de6a-142">Specifies the name of the configuration that the DSC Extension invokes.</span></span>

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

### <span data-ttu-id="1de6a-143">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="1de6a-143">-DataCollection</span></span>
<span data-ttu-id="1de6a-144">Especifica o tipo de coleta de dados.</span><span class="sxs-lookup"><span data-stu-id="1de6a-144">Specifies the data collection type.</span></span>
<span data-ttu-id="1de6a-145">Os valores aceitáveis para este parâmetro são: Habilitar e Desabilitar.</span><span class="sxs-lookup"><span data-stu-id="1de6a-145">The acceptable values for this parameter are: Enable and Disable.</span></span>

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

### <span data-ttu-id="1de6a-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1de6a-146">-DefaultProfile</span></span>
<span data-ttu-id="1de6a-147">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1de6a-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1de6a-148">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1de6a-148">-Force</span></span>
<span data-ttu-id="1de6a-149">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1de6a-149">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1de6a-150">-Local</span><span class="sxs-lookup"><span data-stu-id="1de6a-150">-Location</span></span>
<span data-ttu-id="1de6a-151">Especifica o caminho da extensão do recurso.</span><span class="sxs-lookup"><span data-stu-id="1de6a-151">Specifies the path of the resource extension.</span></span>

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

### <span data-ttu-id="1de6a-152">-Nome</span><span class="sxs-lookup"><span data-stu-id="1de6a-152">-Name</span></span>
<span data-ttu-id="1de6a-153">Especifica o nome do recurso gerenciador de recursos do Azure que representa a extensão.</span><span class="sxs-lookup"><span data-stu-id="1de6a-153">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="1de6a-154">O valor padrão é Microsoft.Powershell.DSC.</span><span class="sxs-lookup"><span data-stu-id="1de6a-154">The default value is Microsoft.Powershell.DSC.</span></span>

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

### <span data-ttu-id="1de6a-155">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1de6a-155">-NoWait</span></span>
<span data-ttu-id="1de6a-156">Inicia a operação e retorna imediatamente, antes que a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="1de6a-156">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1de6a-157">Para determinar se a operação foi concluída com êxito, use algum outro mecanismo.</span><span class="sxs-lookup"><span data-stu-id="1de6a-157">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1de6a-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1de6a-158">-ResourceGroupName</span></span>
<span data-ttu-id="1de6a-159">Especifica o nome do grupo de recursos da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1de6a-159">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1de6a-160">-Versão</span><span class="sxs-lookup"><span data-stu-id="1de6a-160">-Version</span></span>
<span data-ttu-id="1de6a-161">Especifica a versão da extensão DSC à Set-AzVMDscExtension aplica as configurações.</span><span class="sxs-lookup"><span data-stu-id="1de6a-161">Specifies the version of the DSC extension that Set-AzVMDscExtension applies the settings to.</span></span>

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

### <span data-ttu-id="1de6a-162">-VMName</span><span class="sxs-lookup"><span data-stu-id="1de6a-162">-VMName</span></span>
<span data-ttu-id="1de6a-163">Especifica o nome da máquina virtual onde o manipulador de extensão DSC está instalado.</span><span class="sxs-lookup"><span data-stu-id="1de6a-163">Specifies the name of the virtual machine where DSC extension handler is installed.</span></span>

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

### <span data-ttu-id="1de6a-164">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="1de6a-164">-WmfVersion</span></span>
<span data-ttu-id="1de6a-165">Especifica a versão WMF.</span><span class="sxs-lookup"><span data-stu-id="1de6a-165">Specifies the WMF version.</span></span>

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

### <span data-ttu-id="1de6a-166">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1de6a-166">-Confirm</span></span>
<span data-ttu-id="1de6a-167">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1de6a-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1de6a-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1de6a-168">-WhatIf</span></span>
<span data-ttu-id="1de6a-169">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1de6a-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1de6a-170">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1de6a-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1de6a-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1de6a-171">CommonParameters</span></span>
<span data-ttu-id="1de6a-172">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1de6a-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1de6a-173">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1de6a-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1de6a-174">Entradas</span><span class="sxs-lookup"><span data-stu-id="1de6a-174">INPUTS</span></span>

### <span data-ttu-id="1de6a-175">System.String</span><span class="sxs-lookup"><span data-stu-id="1de6a-175">System.String</span></span>

### <span data-ttu-id="1de6a-176">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1de6a-176">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1de6a-177">Saídas</span><span class="sxs-lookup"><span data-stu-id="1de6a-177">OUTPUTS</span></span>

### <span data-ttu-id="1de6a-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1de6a-178">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1de6a-179">Notas</span><span class="sxs-lookup"><span data-stu-id="1de6a-179">NOTES</span></span>

## <span data-ttu-id="1de6a-180">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1de6a-180">RELATED LINKS</span></span>

[<span data-ttu-id="1de6a-181">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1de6a-181">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="1de6a-182">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="1de6a-182">Remove-AzVMDscExtension</span></span>](./Remove-AzVMDscExtension.md)

[<span data-ttu-id="1de6a-183">Publish-AzVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1de6a-183">Publish-AzVMDscConfiguration</span></span>](./Publish-AzVMDscConfiguration.md)


