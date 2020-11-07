---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 956B60BE-D978-4682-BA11-4EE9296B77B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2d21d1b9609c160bdb2b4b3b8477a4b1b9bea991
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945882"
---
# <span data-ttu-id="f0a24-101">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f0a24-101">Publish-AzureVMDscConfiguration</span></span>

## <span data-ttu-id="f0a24-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f0a24-102">SYNOPSIS</span></span>
<span data-ttu-id="f0a24-103">Publica um script de configuração de estado desejado no armazenamento de BLOBs do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0a24-103">Publishes a desired state configuration script to Azure blob storage.</span></span>

## <span data-ttu-id="f0a24-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0a24-104">SYNTAX</span></span>

### <span data-ttu-id="f0a24-105">UploadArchive (padrão)</span><span class="sxs-lookup"><span data-stu-id="f0a24-105">UploadArchive (Default)</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-ContainerName <String>] [-Force]
 [-StorageContext <AzureStorageContext>] [-StorageEndpointSuffix <String>] [-SkipDependencyDetection]
 [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0a24-106">Createarchive</span><span class="sxs-lookup"><span data-stu-id="f0a24-106">CreateArchive</span></span>
```
Publish-AzureVMDscConfiguration [-ConfigurationPath] <String> [-Force] [-ConfigurationArchivePath <String>]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>] [-PassThru]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0a24-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f0a24-107">DESCRIPTION</span></span>
<span data-ttu-id="f0a24-108">O cmdlet **Publish-AzureVMDscConfiguration** publica um script de configuração de estado desejado para o armazenamento de blob do Azure, que posteriormente pode ser aplicado às máquinas virtuais do Azure usando o cmdlet **set-AzureVMDscExtension** .</span><span class="sxs-lookup"><span data-stu-id="f0a24-108">The **Publish-AzureVMDscConfiguration** cmdlet publishes a desired state configuration script to Azure blob storage, which later can be applied to Azure virtual machines using the **Set-AzureVMDscExtension** cmdlet.</span></span>

## <span data-ttu-id="f0a24-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f0a24-109">EXAMPLES</span></span>

### <span data-ttu-id="f0a24-110">Exemplo 1: publicar um script de configuração de estado no armazenamento de BLOB</span><span class="sxs-lookup"><span data-stu-id="f0a24-110">Example 1: Publish a state configuration script to blob storage</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1
```

<span data-ttu-id="f0a24-111">Esse comando cria um pacote. zip para o script fornecido e quaisquer módulos de recursos dependentes e o carrega no armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="f0a24-111">This command creates a .zip package for the given script and any dependent resource modules and uploads it to Azure storage.</span></span>

### <span data-ttu-id="f0a24-112">Exemplo 2: publicar um script de configuração de estado em um arquivo local</span><span class="sxs-lookup"><span data-stu-id="f0a24-112">Example 2: Publish a state configuration script to a local file</span></span>
```
PS C:\> Publish-AzureVMDscConfiguration .\MyConfiguration.ps1 -ConfigurationArchivePath .\MyConfiguration.ps1.zip
```

<span data-ttu-id="f0a24-113">Esse comando cria um pacote. zip para o script fornecido e todos os módulos de recursos dependentes e os armazena no arquivo .\MyConfiguration.ps1.zip local.</span><span class="sxs-lookup"><span data-stu-id="f0a24-113">This command creates a .zip package for the given script and any dependent resource modules and stores it in the local file .\MyConfiguration.ps1.zip.</span></span>

## <span data-ttu-id="f0a24-114">OS</span><span class="sxs-lookup"><span data-stu-id="f0a24-114">PARAMETERS</span></span>

### <span data-ttu-id="f0a24-115">-AdditionalPath</span><span class="sxs-lookup"><span data-stu-id="f0a24-115">-AdditionalPath</span></span>
<span data-ttu-id="f0a24-116">Especifica uma matriz de caminhos adicionais.</span><span class="sxs-lookup"><span data-stu-id="f0a24-116">Specifies an array of additional paths.</span></span>

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

### <span data-ttu-id="f0a24-117">-ConfigurationArchivePath</span><span class="sxs-lookup"><span data-stu-id="f0a24-117">-ConfigurationArchivePath</span></span>
<span data-ttu-id="f0a24-118">Especifica o caminho de um arquivo. zip local que esse cmdlet grava o arquivo morto de configuração.</span><span class="sxs-lookup"><span data-stu-id="f0a24-118">Specifies the path of a local .zip file that this cmdlet writes the configuration archive.</span></span>
<span data-ttu-id="f0a24-119">O script de configuração não é carregado no armazenamento de BLOBs do Azure se você usar esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f0a24-119">The configuration script is not uploaded to Azure blob storage if you use this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a24-120">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="f0a24-120">-ConfigurationDataPath</span></span>
<span data-ttu-id="f0a24-121">Especifica um caminho de dados de configuração.</span><span class="sxs-lookup"><span data-stu-id="f0a24-121">Specifies a configuration data path.</span></span>

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

### <span data-ttu-id="f0a24-122">-ConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="f0a24-122">-ConfigurationPath</span></span>
<span data-ttu-id="f0a24-123">Especifica o caminho de um arquivo que contém uma ou mais configurações.</span><span class="sxs-lookup"><span data-stu-id="f0a24-123">Specifies the path of a file that contains one or more configurations.</span></span>
<span data-ttu-id="f0a24-124">O arquivo pode ser um script do Windows PowerShell (arquivo. ps1), um módulo (arquivo. psm1) ou um arquivo morto (arquivo. zip) que contém um conjunto de módulos do Windows PowerShell, com cada módulo em um diretório separado.</span><span class="sxs-lookup"><span data-stu-id="f0a24-124">The file can be a Windows PowerShell script (.ps1 file), module (.psm1 file), or an archive (.zip file) that contains a set of Windows PowerShell modules, with each module in a separate directory.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a24-125">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f0a24-125">-ContainerName</span></span>
<span data-ttu-id="f0a24-126">Especifica o nome do contêiner de armazenamento do Azure no qual a configuração é carregada.</span><span class="sxs-lookup"><span data-stu-id="f0a24-126">Specifies the name of the Azure storage container the configuration is uploaded to.</span></span>

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

### <span data-ttu-id="f0a24-127">-Force</span><span class="sxs-lookup"><span data-stu-id="f0a24-127">-Force</span></span>
<span data-ttu-id="f0a24-128">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f0a24-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f0a24-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="f0a24-129">-InformationAction</span></span>
<span data-ttu-id="f0a24-130">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="f0a24-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f0a24-131">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="f0a24-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f0a24-132">Contínuo</span><span class="sxs-lookup"><span data-stu-id="f0a24-132">Continue</span></span>
- <span data-ttu-id="f0a24-133">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f0a24-133">Ignore</span></span>
- <span data-ttu-id="f0a24-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="f0a24-134">Inquire</span></span>
- <span data-ttu-id="f0a24-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f0a24-135">SilentlyContinue</span></span>
- <span data-ttu-id="f0a24-136">Finaliza</span><span class="sxs-lookup"><span data-stu-id="f0a24-136">Stop</span></span>
- <span data-ttu-id="f0a24-137">Suspensão</span><span class="sxs-lookup"><span data-stu-id="f0a24-137">Suspend</span></span>

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

### <span data-ttu-id="f0a24-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f0a24-138">-InformationVariable</span></span>
<span data-ttu-id="f0a24-139">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="f0a24-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f0a24-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0a24-140">-PassThru</span></span>
<span data-ttu-id="f0a24-141">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f0a24-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f0a24-142">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f0a24-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0a24-143">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f0a24-143">-Profile</span></span>
<span data-ttu-id="f0a24-144">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f0a24-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f0a24-145">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f0a24-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f0a24-146">-SkipDependencyDetection</span><span class="sxs-lookup"><span data-stu-id="f0a24-146">-SkipDependencyDetection</span></span>
<span data-ttu-id="f0a24-147">Indica que esse cmdlet ignora a detecção de dependências.</span><span class="sxs-lookup"><span data-stu-id="f0a24-147">Indicates that this cmdlet skips dependency detection.</span></span>

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

### <span data-ttu-id="f0a24-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="f0a24-148">-StorageContext</span></span>
<span data-ttu-id="f0a24-149">Especifica o contexto de armazenamento do Azure que fornece as configurações de segurança usadas para carregar o script de configuração para o contêiner especificado pelo parâmetro *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="f0a24-149">Specifies the Azure storage context that provides the security settings used to upload the configuration script to the container specified by the *ContainerName* parameter.</span></span>
<span data-ttu-id="f0a24-150">Esse contexto fornece acesso de gravação ao contêiner.</span><span class="sxs-lookup"><span data-stu-id="f0a24-150">This context provides write access to the container.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: UploadArchive
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0a24-151">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="f0a24-151">-StorageEndpointSuffix</span></span>
<span data-ttu-id="f0a24-152">Especifica o sufixo para o ponto de extremidade do armazenamento, por exemplo, core.contoso.net</span><span class="sxs-lookup"><span data-stu-id="f0a24-152">Specifies the suffix for the storage end-point, for instance, core.contoso.net</span></span>

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

### <span data-ttu-id="f0a24-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f0a24-153">-Confirm</span></span>
<span data-ttu-id="f0a24-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0a24-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0a24-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0a24-155">-WhatIf</span></span>
<span data-ttu-id="f0a24-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f0a24-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0a24-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f0a24-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0a24-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0a24-158">CommonParameters</span></span>
<span data-ttu-id="f0a24-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0a24-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0a24-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0a24-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0a24-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f0a24-161">INPUTS</span></span>

## <span data-ttu-id="f0a24-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f0a24-162">OUTPUTS</span></span>

## <span data-ttu-id="f0a24-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f0a24-163">NOTES</span></span>

## <span data-ttu-id="f0a24-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f0a24-164">RELATED LINKS</span></span>

[<span data-ttu-id="f0a24-165">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f0a24-165">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


