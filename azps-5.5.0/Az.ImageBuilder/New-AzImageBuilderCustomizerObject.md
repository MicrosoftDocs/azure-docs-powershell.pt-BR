---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 3e67452a5d5e11fa4aa96d1b38b80a4284c21f00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113803"
---
# <span data-ttu-id="3072c-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="3072c-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="3072c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3072c-102">SYNOPSIS</span></span>
<span data-ttu-id="3072c-103">Descreve uma unidade de personalização de imagem</span><span class="sxs-lookup"><span data-stu-id="3072c-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="3072c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3072c-104">SYNTAX</span></span>

### <span data-ttu-id="3072c-105">ShellCus ltd (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3072c-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="3072c-106">FileCus ltda</span><span class="sxs-lookup"><span data-stu-id="3072c-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="3072c-107">PowerShellCus ltda</span><span class="sxs-lookup"><span data-stu-id="3072c-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="3072c-108">RestartCus rebootzer</span><span class="sxs-lookup"><span data-stu-id="3072c-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="3072c-109">WindowsUpdateCus ltd</span><span class="sxs-lookup"><span data-stu-id="3072c-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3072c-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="3072c-110">DESCRIPTION</span></span>
<span data-ttu-id="3072c-111">Descreve uma unidade de personalização de imagem</span><span class="sxs-lookup"><span data-stu-id="3072c-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="3072c-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3072c-112">EXAMPLES</span></span>

### <span data-ttu-id="3072c-113">Exemplo 1: Criar um personalização de atualização do Windows</span><span class="sxs-lookup"><span data-stu-id="3072c-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="3072c-114">Esse comando cria um personalização de atualização do Windows.</span><span class="sxs-lookup"><span data-stu-id="3072c-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="3072c-115">Exemplo 2: Criar um personalização de arquivo</span><span class="sxs-lookup"><span data-stu-id="3072c-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="3072c-116">Esse comando cria um personalização de arquivo.</span><span class="sxs-lookup"><span data-stu-id="3072c-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="3072c-117">Exemplo 3: Criar um personalização do PowerShell</span><span class="sxs-lookup"><span data-stu-id="3072c-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="3072c-118">Esse comando cria um personalização do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3072c-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="3072c-119">Exemplo 4: Criar um personalização de reinicialização</span><span class="sxs-lookup"><span data-stu-id="3072c-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="3072c-120">Esse comando cria um personalização de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="3072c-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="3072c-121">Exemplo 5: Criar um personalização de shell</span><span class="sxs-lookup"><span data-stu-id="3072c-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="3072c-122">Esse comando cria um personalização de shell.</span><span class="sxs-lookup"><span data-stu-id="3072c-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="3072c-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3072c-123">PARAMETERS</span></span>

### <span data-ttu-id="3072c-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="3072c-124">-CustomizerName</span></span>
<span data-ttu-id="3072c-125">Nome amigável para fornecer contexto sobre o que essa etapa de personalização faz.</span><span class="sxs-lookup"><span data-stu-id="3072c-125">Friendly Name to provide context on what this customization step does.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-126">-Destino</span><span class="sxs-lookup"><span data-stu-id="3072c-126">-Destination</span></span>
<span data-ttu-id="3072c-127">O caminho absoluto para um arquivo (com estruturas de diretório aninhadas já criadas) em que o arquivo (do sourceUri) será carregado no VM.</span><span class="sxs-lookup"><span data-stu-id="3072c-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-128">-FileCus ltda</span><span class="sxs-lookup"><span data-stu-id="3072c-128">-FileCustomizer</span></span>
<span data-ttu-id="3072c-129">Carrega arquivos em VMs (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="3072c-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="3072c-130">Corresponde ao provisionador de arquivos Desarmado.</span><span class="sxs-lookup"><span data-stu-id="3072c-130">Corresponds to Packer file provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-131">-Filtro</span><span class="sxs-lookup"><span data-stu-id="3072c-131">-Filter</span></span>
<span data-ttu-id="3072c-132">Matriz de filtros para selecionar atualizações a aplicar.</span><span class="sxs-lookup"><span data-stu-id="3072c-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="3072c-133">Omitir ou especificar matriz vazia para usar a matriz padrão (sem filtro).</span><span class="sxs-lookup"><span data-stu-id="3072c-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="3072c-134">Consulte o link acima para ver exemplos e descrição detalhada desse campo.</span><span class="sxs-lookup"><span data-stu-id="3072c-134">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String[]
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-135">-Em linha</span><span class="sxs-lookup"><span data-stu-id="3072c-135">-Inline</span></span>
<span data-ttu-id="3072c-136">Matriz de comandos de shell a ser executada.</span><span class="sxs-lookup"><span data-stu-id="3072c-136">Array of shell commands to execute.</span></span>

```yaml
Type: System.String[]
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-137">-PowerShellCus ltda</span><span class="sxs-lookup"><span data-stu-id="3072c-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="3072c-138">Executa o PowerShell especificado no VM (Windows).</span><span class="sxs-lookup"><span data-stu-id="3072c-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="3072c-139">Corresponde ao provisionador do PowerShell Deslúm.</span><span class="sxs-lookup"><span data-stu-id="3072c-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="3072c-140">É possível especificar exatamente um de "scriptUri" ou "em linha".</span><span class="sxs-lookup"><span data-stu-id="3072c-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PowerShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="3072c-141">-RestartCheckCommand</span></span>
<span data-ttu-id="3072c-142">Comando para verificar se a reinicialização foi bem-sucedida [Padrão: ''].</span><span class="sxs-lookup"><span data-stu-id="3072c-142">Command to check if restart succeeded [Default: ''].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="3072c-143">-RestartCommand</span></span>
<span data-ttu-id="3072c-144">Comando para executar a reinicialização [Padrão: 'parada total /r /f /t 0 /c reinicialização']</span><span class="sxs-lookup"><span data-stu-id="3072c-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-145">-RestartCus rebootzer</span><span class="sxs-lookup"><span data-stu-id="3072c-145">-RestartCustomizer</span></span>
<span data-ttu-id="3072c-146">Reinicia um VM e espera que ele volte a ficar online (Windows).</span><span class="sxs-lookup"><span data-stu-id="3072c-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="3072c-147">Corresponde ao provisionador de reinicialização de janelas do Windows.</span><span class="sxs-lookup"><span data-stu-id="3072c-147">Corresponds to Packer windows-restart provisioner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestartCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="3072c-148">-RestartTimeout</span></span>
<span data-ttu-id="3072c-149">Reinicie o tempo especificado como uma cadeia de caracteres de magnitude e unidade, por exemplo, '5m' (5 minutos) ou '2h' (2 horas) [Padrão: '5m'].</span><span class="sxs-lookup"><span data-stu-id="3072c-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

```yaml
Type: System.String
Parameter Sets: RestartCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="3072c-150">-RunElevated</span></span>
<span data-ttu-id="3072c-151">Se especificado, o script do PowerShell será executado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="3072c-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="3072c-152">-ScriptUri</span></span>
<span data-ttu-id="3072c-153">URI do script de shell a ser executado para personalização.</span><span class="sxs-lookup"><span data-stu-id="3072c-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="3072c-154">Pode ser um link do github, URI SAS para Armazenamento do Azure, etc.</span><span class="sxs-lookup"><span data-stu-id="3072c-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="3072c-155">-SearchCriterion</span></span>
<span data-ttu-id="3072c-156">Critérios para pesquisar atualizações.</span><span class="sxs-lookup"><span data-stu-id="3072c-156">Criteria to search updates.</span></span>
<span data-ttu-id="3072c-157">Omita ou especifique a cadeia de caracteres vazia para usar o padrão (pesquisar tudo).</span><span class="sxs-lookup"><span data-stu-id="3072c-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="3072c-158">Consulte o link acima para ver exemplos e descrição detalhada desse campo.</span><span class="sxs-lookup"><span data-stu-id="3072c-158">Refer to above link for examples and detailed description of this field.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="3072c-159">-Sha256Checksum</span></span>
<span data-ttu-id="3072c-160">SHA256 verifica o script de shell fornecido no campo scriptUri.</span><span class="sxs-lookup"><span data-stu-id="3072c-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer, PowerShellCustomizer, ShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-161">-ShellCus ltda</span><span class="sxs-lookup"><span data-stu-id="3072c-161">-ShellCustomizer</span></span>
<span data-ttu-id="3072c-162">Executa um script shell durante a fase de personalização (Linux).</span><span class="sxs-lookup"><span data-stu-id="3072c-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="3072c-163">Corresponde ao provisionador de shell Descarada.</span><span class="sxs-lookup"><span data-stu-id="3072c-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="3072c-164">É possível especificar exatamente um de "scriptUri" ou "em linha".</span><span class="sxs-lookup"><span data-stu-id="3072c-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShellCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="3072c-165">-SourceUri</span></span>
<span data-ttu-id="3072c-166">O URI do arquivo a ser carregado para personalizar o VM.</span><span class="sxs-lookup"><span data-stu-id="3072c-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="3072c-167">Pode ser um link do github, URI SAS para Armazenamento do Azure, etc.</span><span class="sxs-lookup"><span data-stu-id="3072c-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

```yaml
Type: System.String
Parameter Sets: FileCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="3072c-168">-UpdateLimit</span></span>
<span data-ttu-id="3072c-169">Número máximo de atualizações a aplicar por vez.</span><span class="sxs-lookup"><span data-stu-id="3072c-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="3072c-170">Omita ou especifique 0 para usar o padrão (1000).</span><span class="sxs-lookup"><span data-stu-id="3072c-170">Omit or specify 0 to use the default (1000).</span></span>

```yaml
Type: System.Int32
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="3072c-171">-ValidExitCode</span></span>
<span data-ttu-id="3072c-172">Códigos de saída válidos para o script do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3072c-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="3072c-173">[Padrão: 0].</span><span class="sxs-lookup"><span data-stu-id="3072c-173">[Default: 0].</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: PowerShellCustomizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-174">-WindowsUpdateCus ltd</span><span class="sxs-lookup"><span data-stu-id="3072c-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="3072c-175">Instala o Windows Updates.</span><span class="sxs-lookup"><span data-stu-id="3072c-175">Installs Windows Updates.</span></span>
<span data-ttu-id="3072c-176">Corresponde ao Provisionador de Atualização do Windows ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="3072c-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsUpdateCustomizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3072c-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3072c-177">CommonParameters</span></span>
<span data-ttu-id="3072c-178">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3072c-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3072c-179">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3072c-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3072c-180">Entradas</span><span class="sxs-lookup"><span data-stu-id="3072c-180">INPUTS</span></span>

## <span data-ttu-id="3072c-181">Saídas</span><span class="sxs-lookup"><span data-stu-id="3072c-181">OUTPUTS</span></span>

### <span data-ttu-id="3072c-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCus model</span><span class="sxs-lookup"><span data-stu-id="3072c-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="3072c-183">Notas</span><span class="sxs-lookup"><span data-stu-id="3072c-183">NOTES</span></span>

<span data-ttu-id="3072c-184">Aliases</span><span class="sxs-lookup"><span data-stu-id="3072c-184">ALIASES</span></span>

## <span data-ttu-id="3072c-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3072c-185">RELATED LINKS</span></span>

