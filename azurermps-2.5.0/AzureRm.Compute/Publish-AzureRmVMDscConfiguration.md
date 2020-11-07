---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/publish-azurermvmdscconfiguration
schema: 2.0.0
ms.openlocfilehash: c9a778638a0ca86198079227cfa0021a96ac138b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786156"
---
# <span data-ttu-id="27705-101">Publish-AzureRmVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="27705-101">Publish-AzureRmVMDscConfiguration</span></span>

## <span data-ttu-id="27705-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="27705-102">SYNOPSIS</span></span>
<span data-ttu-id="27705-103">Carrega um script DSC para o armazenamento de BLOBs do Azure.</span><span class="sxs-lookup"><span data-stu-id="27705-103">Uploads a DSC script to Azure blob storage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27705-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="27705-104">SYNTAX</span></span>

### <span data-ttu-id="27705-105">UploadArchive (padrão)</span><span class="sxs-lookup"><span data-stu-id="27705-105">UploadArchive (Default)</span></span>
```
Publish-AzureRmVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27705-106">Createarchive</span><span class="sxs-lookup"><span data-stu-id="27705-106">CreateArchive</span></span>
```
Publish-AzureRmVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27705-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="27705-107">DESCRIPTION</span></span>
<span data-ttu-id="27705-108">O cmdlet **Publish-AzureRmVMDscConfiguration** carrega um script de configuração de estado desejado (DSC) no armazenamento de blob do Azure, que posteriormente pode ser aplicado às máquinas virtuais do Azure usando o cmdlet Set-AzureRmVMDscExtension.</span><span class="sxs-lookup"><span data-stu-id="27705-108">The **Publish-AzureRmVMDscConfiguration** cmdlet uploads a Desired State Configuration (DSC) script to Azure blob storage, which later can be applied to Azure virtual machines using the Set-AzureRmVMDscExtension cmdlet.</span></span>

## <span data-ttu-id="27705-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="27705-109">EXAMPLES</span></span>

### <span data-ttu-id="27705-110">Exemplo 1: criar um pacote. zip em carregá-lo para armazenamento do Azure</span><span class="sxs-lookup"><span data-stu-id="27705-110">Example 1: Create a .zip package an upload it to Azure storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1"
```

<span data-ttu-id="27705-111">Esse comando cria um pacote. zip para o script fornecido e quaisquer módulos de recursos dependentes e o carrega no armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="27705-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="27705-112">Exemplo 2: criar um pacote. zip e armazená-lo em um arquivo local</span><span class="sxs-lookup"><span data-stu-id="27705-112">Example 2: Create a .zip package and store it to a local file</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

<span data-ttu-id="27705-113">Esse comando cria um pacote. zip para o script fornecido e todos os módulos de recursos dependentes e os armazena no arquivo local que é chamado .\MyConfiguration.ps1.zip.</span><span class="sxs-lookup"><span data-stu-id="27705-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file that is named .\MyConfiguration.ps1.zip.</span></span>

### <span data-ttu-id="27705-114">Exemplo 3: adicionar configuração ao arquivo morto e, em seguida, carregá-lo para armazenamento</span><span class="sxs-lookup"><span data-stu-id="27705-114">Example 3: Add configuration to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

<span data-ttu-id="27705-115">Esse comando adiciona uma configuração chamada Sample.ps1 ao arquivo morto de configuração para carregar no Azure Storage e ignora módulos de recursos dependentes.</span><span class="sxs-lookup"><span data-stu-id="27705-115">This command adds configuration named Sample.ps1 to the configuration archive to upload to Azure storage and skips dependent resource modules.</span></span>

### <span data-ttu-id="27705-116">Exemplo 4: adicionar dados de configuração e configuração ao arquivo morto e, em seguida, carregá-los para armazenamento</span><span class="sxs-lookup"><span data-stu-id="27705-116">Example 4: Add configuration and configuration data to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="27705-117">Esse comando adiciona uma configuração chamada Sample.ps1 e dados de configuração chamados SampleData.psd1 para o arquivo morto de configuração para carregar no armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="27705-117">This command adds configuration named Sample.ps1 and configuration data named SampleData.psd1 to the configuration archive to upload to Azure storage.</span></span>

### <span data-ttu-id="27705-118">Exemplo 5: adicionar configuração, dados de configuração e conteúdo adicional ao arquivo morto e, em seguida, carregá-lo para armazenamento</span><span class="sxs-lookup"><span data-stu-id="27705-118">Example 5: Add configuration, configuration data, and additional content to the archive and then upload it to storage</span></span>
```
PS C:\> Publish-AzureRmVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

<span data-ttu-id="27705-119">Esse comando adiciona uma configuração chamada Sample.ps1, dados de configuração SampleData.psd1 e conteúdo adicional para o arquivamento de configuração para carregar no armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="27705-119">This command adds configuration named Sample.ps1, configuration data SampleData.psd1, and additional content to configuration archive to upload to Azure storage.</span></span>

## <span data-ttu-id="27705-120">OS</span><span class="sxs-lookup"><span data-stu-id="27705-120">PARAMETERS</span></span>

### <span data-ttu-id="27705-121">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="27705-121">-AdditionalPath</span></span>
<span data-ttu-id="27705-122">Especifica o caminho de um arquivo ou diretório a ser incluído no arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="27705-122">Specifies the path of a file or a directory to include in the configuration archive.</span></span>
<span data-ttu-id="27705-123">Ele é baixado para a máquina virtual juntamente com a configuração.</span><span class="sxs-lookup"><span data-stu-id="27705-123">It gets downloaded to the virtual machine together with the configuration.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27705-124">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="27705-124">-ConfigurationDataPath</span></span>
<span data-ttu-id="27705-125">Especifica o caminho de um arquivo. psd1 que especifica os dados para a configuração.</span><span class="sxs-lookup"><span data-stu-id="27705-125">Specifies the path of a .psd1 file that specifies the data for the configuration.</span></span>
<span data-ttu-id="27705-126">Isso é adicionado ao arquivo de configuração e, em seguida, passado para a função de configuração.</span><span class="sxs-lookup"><span data-stu-id="27705-126">This is added to the configuration archive and then passed to the configuration function.</span></span>
<span data-ttu-id="27705-127">Ele é substituído pelo caminho de dados de configuração fornecido pelo cmdlet Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="27705-127">It gets overwritten by the configuration data path provided through the Set-AzureRmVMDscExtension cmdlet</span></span>

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

### <span data-ttu-id="27705-128">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="27705-128">-ConfigurationPath</span></span>
<span data-ttu-id="27705-129">Especifica o caminho de um arquivo que contém uma ou mais configurações.</span><span class="sxs-lookup"><span data-stu-id="27705-129">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="27705-130">O arquivo pode ser um arquivo de script do Windows PowerShell (. ps1) ou um arquivo de módulo do Windows PowerShell (. psm1).</span><span class="sxs-lookup"><span data-stu-id="27705-130">The file can be a Windows PowerShell script (.ps1) file or a Windows PowerShell module (.psm1) file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27705-131">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="27705-131">-ContainerName</span></span>
<span data-ttu-id="27705-132">Especifica o nome do contêiner de armazenamento do Azure no qual a configuração é carregada.</span><span class="sxs-lookup"><span data-stu-id="27705-132">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27705-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27705-133">-DefaultProfile</span></span>
<span data-ttu-id="27705-134">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="27705-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27705-135">-Force</span><span class="sxs-lookup"><span data-stu-id="27705-135">-Force</span></span>
<span data-ttu-id="27705-136">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="27705-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27705-137">-OutputArchivePath</span><span class="sxs-lookup"><span data-stu-id="27705-137">-OutputArchivePath</span></span>
<span data-ttu-id="27705-138">Especifica o caminho de um arquivo. zip local no qual gravar o arquivo morto de configuração.</span><span class="sxs-lookup"><span data-stu-id="27705-138">Specifies the path of a local .zip file to write the configuration archive to.</span></span>
<span data-ttu-id="27705-139">Quando esse parâmetro é usado, o script de configuração não é carregado no armazenamento do blob do Azure.</span><span class="sxs-lookup"><span data-stu-id="27705-139">When this parameter is used, the configuration script is not uploaded to Azure blob storage.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27705-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27705-140">-ResourceGroupName</span></span>
<span data-ttu-id="27705-141">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="27705-141">Specifies the name of the resource group that contains the storage account.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27705-142">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="27705-142">-SkipDependencyDetection</span></span>
<span data-ttu-id="27705-143">Indica que esse cmdlet exclui dependências do recurso DSC do arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="27705-143">Indicates that this cmdlet excludes DSC resource dependencies from the configuration archive.</span></span>

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

### <span data-ttu-id="27705-144">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="27705-144">-StorageAccountName</span></span>
<span data-ttu-id="27705-145">Especifica o nome da conta de armazenamento do Azure que é usado para carregar o script de configuração para o contêiner especificado pelo parâmetro *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="27705-145">Specifies the Azure storage account name that is used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27705-146">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="27705-146">-StorageEndpointSuffix</span></span>
<span data-ttu-id="27705-147">Especifica o sufixo para o ponto de extremidade de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="27705-147">Specifies the suffix for the storage end point.</span></span>

```yaml
Type: String
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27705-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="27705-148">-Confirm</span></span>
<span data-ttu-id="27705-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27705-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27705-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27705-150">-WhatIf</span></span>
<span data-ttu-id="27705-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="27705-151">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="27705-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="27705-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27705-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27705-153">CommonParameters</span></span>
<span data-ttu-id="27705-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27705-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27705-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27705-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27705-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="27705-156">INPUTS</span></span>

### <span data-ttu-id="27705-157">String</span><span class="sxs-lookup"><span data-stu-id="27705-157">String</span></span>
<span data-ttu-id="27705-158">O parâmetro ' ConfigurationPath ' aceita o valor do tipo ' String ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="27705-158">Parameter 'ConfigurationPath' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="27705-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="27705-159">OUTPUTS</span></span>

### <span data-ttu-id="27705-160">System. String</span><span class="sxs-lookup"><span data-stu-id="27705-160">System.String</span></span>

## <span data-ttu-id="27705-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="27705-161">NOTES</span></span>

## <span data-ttu-id="27705-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="27705-162">RELATED LINKS</span></span>

[<span data-ttu-id="27705-163">Get-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="27705-163">Get-AzureRmVMDscExtension</span></span>](./Get-AzureRmVMDscExtension.md)

[<span data-ttu-id="27705-164">Remove-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="27705-164">Remove-AzureRmVMDscExtension</span></span>](./Remove-AzureRmVMDscExtension.md)

[<span data-ttu-id="27705-165">Set-AzureRmVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="27705-165">Set-AzureRmVMDscExtension</span></span>](./Set-AzureRmVMDscExtension.md)


