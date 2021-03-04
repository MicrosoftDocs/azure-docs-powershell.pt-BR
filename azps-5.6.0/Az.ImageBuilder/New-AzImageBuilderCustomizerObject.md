---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/powershell/module/az.imagebuilder/new-AzImageBuilderCustomizerObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderCustomizerObject.md
ms.openlocfilehash: 97e59efcc20f8ce025b2e90285ef051edc8272dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893284"
---
# <span data-ttu-id="3ec91-101">New-AzImageBuilderCustomizerObject</span><span class="sxs-lookup"><span data-stu-id="3ec91-101">New-AzImageBuilderCustomizerObject</span></span>

## <span data-ttu-id="3ec91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ec91-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec91-103">Descreve uma unidade de personalização de imagem</span><span class="sxs-lookup"><span data-stu-id="3ec91-103">Describes a unit of image customization</span></span>

## <span data-ttu-id="3ec91-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ec91-104">SYNTAX</span></span>

### <span data-ttu-id="3ec91-105">ShellCustomizer (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3ec91-105">ShellCustomizer (Default)</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -ShellCustomizer [-Inline <String[]>]
 [-ScriptUri <String>] [-Sha256Checksum <String>] [<CommonParameters>]
```

### <span data-ttu-id="3ec91-106">FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-106">FileCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -FileCustomizer [-Destination <String>]
 [-Sha256Checksum <String>] [-SourceUri <String>] [<CommonParameters>]
```

### <span data-ttu-id="3ec91-107">PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-107">PowerShellCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -PowerShellCustomizer [-Inline <String[]>]
 [-RunElevated <Boolean>] [-ScriptUri <String>] [-Sha256Checksum <String>] [-ValidExitCode <Int32[]>]
 [<CommonParameters>]
```

### <span data-ttu-id="3ec91-108">RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-108">RestartCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -RestartCustomizer [-RestartCheckCommand <String>]
 [-RestartCommand <String>] [-RestartTimeout <String>] [<CommonParameters>]
```

### <span data-ttu-id="3ec91-109">WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-109">WindowsUpdateCustomizer</span></span>
```
New-AzImageBuilderCustomizerObject -CustomizerName <String> -WindowsUpdateCustomizer [-Filter <String[]>]
 [-SearchCriterion <String>] [-UpdateLimit <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="3ec91-110">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ec91-110">DESCRIPTION</span></span>
<span data-ttu-id="3ec91-111">Descreve uma unidade de personalização de imagem</span><span class="sxs-lookup"><span data-stu-id="3ec91-111">Describes a unit of image customization</span></span>

## <span data-ttu-id="3ec91-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ec91-112">EXAMPLES</span></span>

### <span data-ttu-id="3ec91-113">Exemplo 1: Criar um personalizador de atualização do Windows</span><span class="sxs-lookup"><span data-stu-id="3ec91-113">Example 1: Create a windows update customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -WindowsUpdateCustomizer -Filter ("BrowseOnly", "IsInstalled") -SearchCriterion "BrowseOnly=0 and IsInstalled=0"  -UpdateLimit 100 -CustomizerName 'WindUpdate'

Name       Type          Filter                    SearchCriterion                UpdateLimit
----       ----          ------                    ---------------                -----------
WindUpdate WindowsUpdate {BrowseOnly, IsInstalled} BrowseOnly=0 and IsInstalled=0 100
```

<span data-ttu-id="3ec91-114">Este comando cria um personalizador de atualização do Windows.</span><span class="sxs-lookup"><span data-stu-id="3ec91-114">This command creates a windows update customizer.</span></span>

### <span data-ttu-id="3ec91-115">Exemplo 2: Criar um personalizador de arquivos</span><span class="sxs-lookup"><span data-stu-id="3ec91-115">Example 2: Create a file customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -FileCustomizer -CustomizerName 'filecus' -Destination 'c:\\buildArtifacts\\index.html' -SourceUri 'https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/index.html'

Name    Type Destination                    Sha256Checksum SourceUri
----    ---- -----------                    -------------- ---------
filecus File c:\\buildArtifacts\\index.html                https://github.com/danielsollondon/azvmimagebuilder/blob/master/quickquickstarts/exampleArtifacts/buildArtifacts/…

```

<span data-ttu-id="3ec91-116">Este comando cria um personalizador de arquivos.</span><span class="sxs-lookup"><span data-stu-id="3ec91-116">This command creates a file customizer.</span></span>

### <span data-ttu-id="3ec91-117">Exemplo 3: Criar um personalizador do PowerShell</span><span class="sxs-lookup"><span data-stu-id="3ec91-117">Example 3: Create a powershell customizer</span></span>
```powershell
PS C:\> $inline = @("mkdir c:\\buildActions", "echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt")
PS C:\> New-AzImageBuilderCustomizerObject -PowerShellCustomizer -CustomizerName settingUpMgmtAgtPath -RunElevated $false -Inline $inline

Name                 Type       Inline                                                                                                  RunElevated ScriptUri Sha256Checksum
----                 ----       ------                                                                                                  ----------- --------- --------------
settingUpMgmtAgtPath PowerShell {mkdir c:\\buildActions, echo Azure-Image-Builder-Was-Here  > c:\\buildActions\\buildActionsOutput.txt} False

```

<span data-ttu-id="3ec91-118">Este comando cria um personalizador do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3ec91-118">This command creates a powershell customizer.</span></span>

### <span data-ttu-id="3ec91-119">Exemplo 4: Criar um personalizador de reinicialização</span><span class="sxs-lookup"><span data-stu-id="3ec91-119">Example 4: Create a restart customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -RestartCustomizer -CustomizerName 'restcus' -RestartCommand 'shutdown /f /r /t 0 /c \"packer restart\"' -RestartCheckCommand 'powershell -command "& {Write-Output "restarted."}"' -RestartTimeout '10m'

Name    Type           RestartCheckCommand                                 RestartCommand                            RestartTimeout
----    ----           -------------------                                 --------------                            --------------
restcus WindowsRestart powershell -command "& {Write-Output "restarted."}" shutdown /f /r /t 0 /c \"packer restart\" 10m
```

<span data-ttu-id="3ec91-120">Este comando cria um personalizador de reinicialização.</span><span class="sxs-lookup"><span data-stu-id="3ec91-120">This command creates a restart customizer.</span></span>

### <span data-ttu-id="3ec91-121">Exemplo 5: Criar um personalizador de shell</span><span class="sxs-lookup"><span data-stu-id="3ec91-121">Example 5: Create a shell customizer</span></span>
```powershell
PS C:\> New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName downloadBuildArtifacts -ScriptUri "https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh" 

Name                   Type  Inline ScriptUri                                                                                                      Sha256Checksum
----                   ----  ------ ---------                                                                                                      --------------
downloadBuildArtifacts Shell        https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh
```

<span data-ttu-id="3ec91-122">Este comando cria um personalizador de shell.</span><span class="sxs-lookup"><span data-stu-id="3ec91-122">This command creates a shell customizer.</span></span>

## <span data-ttu-id="3ec91-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ec91-123">PARAMETERS</span></span>

### <span data-ttu-id="3ec91-124">-CustomizerName</span><span class="sxs-lookup"><span data-stu-id="3ec91-124">-CustomizerName</span></span>
<span data-ttu-id="3ec91-125">Nome Amigável para fornecer contexto sobre o que essa etapa de personalização faz.</span><span class="sxs-lookup"><span data-stu-id="3ec91-125">Friendly Name to provide context on what this customization step does.</span></span>

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

### <span data-ttu-id="3ec91-126">-Destination</span><span class="sxs-lookup"><span data-stu-id="3ec91-126">-Destination</span></span>
<span data-ttu-id="3ec91-127">O caminho absoluto para um arquivo (com estruturas de diretório aninhadas já criadas) para o qual o arquivo (de sourceUri) será carregado na VM.</span><span class="sxs-lookup"><span data-stu-id="3ec91-127">The absolute path to a file (with nested directory structures already created) where the file (from sourceUri) will be uploaded to in the VM.</span></span>

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

### <span data-ttu-id="3ec91-128">-FileCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-128">-FileCustomizer</span></span>
<span data-ttu-id="3ec91-129">Carrega arquivos em VMs (Linux, Windows).</span><span class="sxs-lookup"><span data-stu-id="3ec91-129">Uploads files to VMs (Linux, Windows).</span></span>
<span data-ttu-id="3ec91-130">Corresponde ao provisionador de arquivos do Empacotador.</span><span class="sxs-lookup"><span data-stu-id="3ec91-130">Corresponds to Packer file provisioner.</span></span>

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

### <span data-ttu-id="3ec91-131">-Filter</span><span class="sxs-lookup"><span data-stu-id="3ec91-131">-Filter</span></span>
<span data-ttu-id="3ec91-132">Matriz de filtros para selecionar atualizações a aplicar.</span><span class="sxs-lookup"><span data-stu-id="3ec91-132">Array of filters to select updates to apply.</span></span>
<span data-ttu-id="3ec91-133">Omitir ou especificar matriz vazia para usar o padrão (sem filtro).</span><span class="sxs-lookup"><span data-stu-id="3ec91-133">Omit or specify empty array to use the default (no filter).</span></span>
<span data-ttu-id="3ec91-134">Consulte o link acima para ver exemplos e descrição detalhada deste campo.</span><span class="sxs-lookup"><span data-stu-id="3ec91-134">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="3ec91-135">-Inline</span><span class="sxs-lookup"><span data-stu-id="3ec91-135">-Inline</span></span>
<span data-ttu-id="3ec91-136">Matriz de comandos de shell a ser executada.</span><span class="sxs-lookup"><span data-stu-id="3ec91-136">Array of shell commands to execute.</span></span>

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

### <span data-ttu-id="3ec91-137">-PowerShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-137">-PowerShellCustomizer</span></span>
<span data-ttu-id="3ec91-138">Executa o PowerShell especificado na VM (Windows).</span><span class="sxs-lookup"><span data-stu-id="3ec91-138">Runs the specified PowerShell on the VM (Windows).</span></span>
<span data-ttu-id="3ec91-139">Corresponde ao provisionador do PowerShell do Empacotador.</span><span class="sxs-lookup"><span data-stu-id="3ec91-139">Corresponds to Packer powershell provisioner.</span></span>
<span data-ttu-id="3ec91-140">É possível especificar exatamente um de 'scriptUri' ou 'em linha'.</span><span class="sxs-lookup"><span data-stu-id="3ec91-140">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="3ec91-141">-RestartCheckCommand</span><span class="sxs-lookup"><span data-stu-id="3ec91-141">-RestartCheckCommand</span></span>
<span data-ttu-id="3ec91-142">Comando para verificar se a reinicialização foi bem-sucedida [Padrão: ''].</span><span class="sxs-lookup"><span data-stu-id="3ec91-142">Command to check if restart succeeded [Default: ''].</span></span>

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

### <span data-ttu-id="3ec91-143">-RestartCommand</span><span class="sxs-lookup"><span data-stu-id="3ec91-143">-RestartCommand</span></span>
<span data-ttu-id="3ec91-144">Comando para executar a reinicialização [Padrão: 'desligamento /r /f /t 0 /c reinício do empacotador']</span><span class="sxs-lookup"><span data-stu-id="3ec91-144">Command to execute the restart [Default: 'shutdown /r /f /t 0 /c packer restart']</span></span>

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

### <span data-ttu-id="3ec91-145">-RestartCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-145">-RestartCustomizer</span></span>
<span data-ttu-id="3ec91-146">Reinicia uma VM e aguarda que ela volte online (Windows).</span><span class="sxs-lookup"><span data-stu-id="3ec91-146">Reboots a VM and waits for it to come back online (Windows).</span></span>
<span data-ttu-id="3ec91-147">Corresponde ao provisionador de reinicialização do windows do Empacotador.</span><span class="sxs-lookup"><span data-stu-id="3ec91-147">Corresponds to Packer windows-restart provisioner.</span></span>

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

### <span data-ttu-id="3ec91-148">-RestartTimeout</span><span class="sxs-lookup"><span data-stu-id="3ec91-148">-RestartTimeout</span></span>
<span data-ttu-id="3ec91-149">Tempo de reinicialização especificado como uma cadeia de caracteres de magnitude e unidade, por exemplo, '5m' (5 minutos) ou '2h' (2 horas) [Padrão: '5m'].</span><span class="sxs-lookup"><span data-stu-id="3ec91-149">Restart timeout specified as a string of magnitude and unit, e.g. '5m' (5 minutes) or '2h' (2 hours) [Default: '5m'].</span></span>

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

### <span data-ttu-id="3ec91-150">-RunElevated</span><span class="sxs-lookup"><span data-stu-id="3ec91-150">-RunElevated</span></span>
<span data-ttu-id="3ec91-151">Se especificado, o script do PowerShell será executado com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="3ec91-151">If specified, the PowerShell script will be run with elevated privileges.</span></span>

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

### <span data-ttu-id="3ec91-152">-ScriptUri</span><span class="sxs-lookup"><span data-stu-id="3ec91-152">-ScriptUri</span></span>
<span data-ttu-id="3ec91-153">URI do script de shell a ser executado para personalização.</span><span class="sxs-lookup"><span data-stu-id="3ec91-153">URI of the shell script to be run for customizing.</span></span>
<span data-ttu-id="3ec91-154">Pode ser um link github, URI SAS para Armazenamento do Azure, etc.</span><span class="sxs-lookup"><span data-stu-id="3ec91-154">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="3ec91-155">-SearchCriterion</span><span class="sxs-lookup"><span data-stu-id="3ec91-155">-SearchCriterion</span></span>
<span data-ttu-id="3ec91-156">Critérios para pesquisar atualizações.</span><span class="sxs-lookup"><span data-stu-id="3ec91-156">Criteria to search updates.</span></span>
<span data-ttu-id="3ec91-157">Omita ou especifique a cadeia de caracteres vazia para usar o padrão (pesquisar tudo).</span><span class="sxs-lookup"><span data-stu-id="3ec91-157">Omit or specify empty string to use the default (search all).</span></span>
<span data-ttu-id="3ec91-158">Consulte o link acima para ver exemplos e descrição detalhada deste campo.</span><span class="sxs-lookup"><span data-stu-id="3ec91-158">Refer to above link for examples and detailed description of this field.</span></span>

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

### <span data-ttu-id="3ec91-159">-Sha256Checksum</span><span class="sxs-lookup"><span data-stu-id="3ec91-159">-Sha256Checksum</span></span>
<span data-ttu-id="3ec91-160">Sha256 verifica o script de shell fornecido no campo scriptUri.</span><span class="sxs-lookup"><span data-stu-id="3ec91-160">SHA256 checksum of the shell script provided in the scriptUri field.</span></span>

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

### <span data-ttu-id="3ec91-161">-ShellCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-161">-ShellCustomizer</span></span>
<span data-ttu-id="3ec91-162">Executa um script de shell durante a fase de personalização (Linux).</span><span class="sxs-lookup"><span data-stu-id="3ec91-162">Runs a shell script during the customization phase (Linux).</span></span>
<span data-ttu-id="3ec91-163">Corresponde ao provisionador de shell do Empacotador.</span><span class="sxs-lookup"><span data-stu-id="3ec91-163">Corresponds to Packer shell provisioner.</span></span>
<span data-ttu-id="3ec91-164">É possível especificar exatamente um de 'scriptUri' ou 'em linha'.</span><span class="sxs-lookup"><span data-stu-id="3ec91-164">Exactly one of 'scriptUri' or 'inline' can be specified.</span></span>

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

### <span data-ttu-id="3ec91-165">-SourceUri</span><span class="sxs-lookup"><span data-stu-id="3ec91-165">-SourceUri</span></span>
<span data-ttu-id="3ec91-166">O URI do arquivo a ser carregado para personalizar a VM.</span><span class="sxs-lookup"><span data-stu-id="3ec91-166">The URI of the file to be uploaded for customizing the VM.</span></span>
<span data-ttu-id="3ec91-167">Pode ser um link github, URI SAS para Armazenamento do Azure, etc.</span><span class="sxs-lookup"><span data-stu-id="3ec91-167">It can be a github link, SAS URI for Azure Storage, etc.</span></span>

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

### <span data-ttu-id="3ec91-168">-UpdateLimit</span><span class="sxs-lookup"><span data-stu-id="3ec91-168">-UpdateLimit</span></span>
<span data-ttu-id="3ec91-169">Número máximo de atualizações a aplicar por vez.</span><span class="sxs-lookup"><span data-stu-id="3ec91-169">Maximum number of updates to apply at a time.</span></span>
<span data-ttu-id="3ec91-170">Omita ou especifique 0 para usar o padrão (1000).</span><span class="sxs-lookup"><span data-stu-id="3ec91-170">Omit or specify 0 to use the default (1000).</span></span>

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

### <span data-ttu-id="3ec91-171">-ValidExitCode</span><span class="sxs-lookup"><span data-stu-id="3ec91-171">-ValidExitCode</span></span>
<span data-ttu-id="3ec91-172">Códigos de saída válidos para o script do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3ec91-172">Valid exit codes for the PowerShell script.</span></span>
<span data-ttu-id="3ec91-173">[Padrão: 0].</span><span class="sxs-lookup"><span data-stu-id="3ec91-173">[Default: 0].</span></span>

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

### <span data-ttu-id="3ec91-174">-WindowsUpdateCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-174">-WindowsUpdateCustomizer</span></span>
<span data-ttu-id="3ec91-175">Instala o Windows Updates.</span><span class="sxs-lookup"><span data-stu-id="3ec91-175">Installs Windows Updates.</span></span>
<span data-ttu-id="3ec91-176">Corresponde ao Provisionador de Atualizações do Windows do Empacotador ( https://github.com/rgl/packer-provisioner-windows-update) .</span><span class="sxs-lookup"><span data-stu-id="3ec91-176">Corresponds to Packer Windows Update Provisioner (https://github.com/rgl/packer-provisioner-windows-update).</span></span>

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

### <span data-ttu-id="3ec91-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec91-177">CommonParameters</span></span>
<span data-ttu-id="3ec91-178">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec91-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec91-179">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ec91-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec91-180">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ec91-180">INPUTS</span></span>

## <span data-ttu-id="3ec91-181">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ec91-181">OUTPUTS</span></span>

### <span data-ttu-id="3ec91-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span><span class="sxs-lookup"><span data-stu-id="3ec91-182">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer</span></span>

## <span data-ttu-id="3ec91-183">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ec91-183">NOTES</span></span>

<span data-ttu-id="3ec91-184">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3ec91-184">ALIASES</span></span>

## <span data-ttu-id="3ec91-185">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ec91-185">RELATED LINKS</span></span>

