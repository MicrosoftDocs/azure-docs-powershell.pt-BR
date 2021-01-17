---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: 51882269c342e766a3b714f931486eca437b9e58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427665"
---
# <span data-ttu-id="4c51b-101">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="4c51b-101">Invoke-AzStorageSyncCompatibilityCheck</span></span>

## <span data-ttu-id="4c51b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c51b-102">SYNOPSIS</span></span>
<span data-ttu-id="4c51b-103">Verifica possíveis problemas de compatibilidade entre o sistema e a sincronização de arquivos do Azure.</span><span class="sxs-lookup"><span data-stu-id="4c51b-103">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

## <span data-ttu-id="4c51b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c51b-104">SYNTAX</span></span>

### <span data-ttu-id="4c51b-105">PathBased (padrão)</span><span class="sxs-lookup"><span data-stu-id="4c51b-105">PathBased (Default)</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### <span data-ttu-id="4c51b-106">ComputerNameBased</span><span class="sxs-lookup"><span data-stu-id="4c51b-106">ComputerNameBased</span></span>
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## <span data-ttu-id="4c51b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c51b-107">DESCRIPTION</span></span>
<span data-ttu-id="4c51b-108">O cmdlet **Invoke-AzStorageSyncCompatibilityCheck** verifica possíveis problemas de compatibilidade entre seu sistema e a sincronização de arquivos do Azure. Com um caminho local ou remoto, ele executa um conjunto de validações no namespace do sistema e do arquivo e, em seguida, retorna qualquer problema de compatibilidade encontrado.</span><span class="sxs-lookup"><span data-stu-id="4c51b-108">The **Invoke-AzStorageSyncCompatibilityCheck** cmdlet checks for potential compatibility issues between your system and Azure File Sync. Given a local or remote path, it performs a set of validations on the system and file namespace, and then returns any compatibility issues it finds.</span></span>
<span data-ttu-id="4c51b-109">Verificações do sistema:</span><span class="sxs-lookup"><span data-stu-id="4c51b-109">System checks:</span></span>
- <span data-ttu-id="4c51b-110">Verificações de namespace do arquivo de compatibilidade do so:</span><span class="sxs-lookup"><span data-stu-id="4c51b-110">OS compatibility File namespace checks:</span></span>
- <span data-ttu-id="4c51b-111">Caracteres sem suporte</span><span class="sxs-lookup"><span data-stu-id="4c51b-111">Unsupported characters</span></span>
- <span data-ttu-id="4c51b-112">Tamanho máximo de arquivo</span><span class="sxs-lookup"><span data-stu-id="4c51b-112">Maximum file size</span></span>
- <span data-ttu-id="4c51b-113">Comprimento máximo do caminho</span><span class="sxs-lookup"><span data-stu-id="4c51b-113">Maximum path length</span></span>
- <span data-ttu-id="4c51b-114">Tamanho máximo de arquivo</span><span class="sxs-lookup"><span data-stu-id="4c51b-114">Maximum file length</span></span>
- <span data-ttu-id="4c51b-115">Tamanho máximo do DataSet</span><span class="sxs-lookup"><span data-stu-id="4c51b-115">Maximum dataset size</span></span>
- <span data-ttu-id="4c51b-116">Profundidade máxima de diretório</span><span class="sxs-lookup"><span data-stu-id="4c51b-116">Maximum directory depth</span></span>

## <span data-ttu-id="4c51b-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c51b-117">EXAMPLES</span></span>

### <span data-ttu-id="4c51b-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4c51b-118">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

<span data-ttu-id="4c51b-119">Esse comando verifica a compatibilidade do sistema e também de arquivos e pastas no C:\DATA.</span><span class="sxs-lookup"><span data-stu-id="4c51b-119">This command checks the compatibility of the system and also of files and folders in C:\DATA.</span></span>

### <span data-ttu-id="4c51b-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4c51b-120">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

<span data-ttu-id="4c51b-121">Esse comando verifica a compatibilidade de arquivos e pastas no C:\DATA, mas não executa uma verificação de compatibilidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="4c51b-121">This command checks the compatibility of files and folders in C:\DATA, but does not perform a system compatibility check.</span></span>

### <span data-ttu-id="4c51b-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4c51b-122">Example 3</span></span>
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

<span data-ttu-id="4c51b-123">Esse comando verifica a compatibilidade do sistema e também de arquivos e pastas no C:\DATA e, em seguida, exporta os resultados como um arquivo CSV para C:\results.</span><span class="sxs-lookup"><span data-stu-id="4c51b-123">This command checks the compatibility of the system and also of files and folders in C:\DATA, and then exports the results as a CSV file to C:\results.</span></span>

## <span data-ttu-id="4c51b-124">OS</span><span class="sxs-lookup"><span data-stu-id="4c51b-124">PARAMETERS</span></span>

### <span data-ttu-id="4c51b-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="4c51b-125">-ComputerName</span></span>
<span data-ttu-id="4c51b-126">O computador em que você está executando essa verificação.</span><span class="sxs-lookup"><span data-stu-id="4c51b-126">The computer you are performing this check on.</span></span>

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c51b-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="4c51b-127">-Credential</span></span>
<span data-ttu-id="4c51b-128">Suas credenciais para o compartilhamento que você está validando.</span><span class="sxs-lookup"><span data-stu-id="4c51b-128">Your credentials for the share you are validating.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c51b-129">-Caminho</span><span class="sxs-lookup"><span data-stu-id="4c51b-129">-Path</span></span>
<span data-ttu-id="4c51b-130">O caminho UNC do compartilhamento que você está validando.</span><span class="sxs-lookup"><span data-stu-id="4c51b-130">The UNC path of the share you are validating.</span></span>

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c51b-131">-SkipNamespaceChecks</span><span class="sxs-lookup"><span data-stu-id="4c51b-131">-SkipNamespaceChecks</span></span>
<span data-ttu-id="4c51b-132">Defina esse sinalizador para ignorar validações de namespace de arquivo e executar somente validações de sistema.</span><span class="sxs-lookup"><span data-stu-id="4c51b-132">Set this flag to skip file namespace validations and only perform system validations.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c51b-133">-SkipSystemChecks</span><span class="sxs-lookup"><span data-stu-id="4c51b-133">-SkipSystemChecks</span></span>
<span data-ttu-id="4c51b-134">Defina esse sinalizador para ignorar validações do sistema e somente executar validações de namespace de arquivo.</span><span class="sxs-lookup"><span data-stu-id="4c51b-134">Set this flag to skip system validations and only perform file namespace validations.</span></span>

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

### <span data-ttu-id="4c51b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c51b-135">CommonParameters</span></span>
<span data-ttu-id="4c51b-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c51b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c51b-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c51b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c51b-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c51b-138">INPUTS</span></span>

### <span data-ttu-id="4c51b-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="4c51b-139">None</span></span>

## <span data-ttu-id="4c51b-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c51b-140">OUTPUTS</span></span>

### <span data-ttu-id="4c51b-141">Microsoft. Azure. Commands. StorageSync. Evaluation. Models. PSValidationResult</span><span class="sxs-lookup"><span data-stu-id="4c51b-141">Microsoft.Azure.Commands.StorageSync.Evaluation.Models.PSValidationResult</span></span>

## <span data-ttu-id="4c51b-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c51b-142">NOTES</span></span>
* <span data-ttu-id="4c51b-143">Palavras-chave: Azure, AZ, ARM, Resource, Management, storagesync, filesync</span><span class="sxs-lookup"><span data-stu-id="4c51b-143">Keywords: azure, Az, arm, resource, management, storagesync, filesync</span></span>

## <span data-ttu-id="4c51b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c51b-144">RELATED LINKS</span></span>
