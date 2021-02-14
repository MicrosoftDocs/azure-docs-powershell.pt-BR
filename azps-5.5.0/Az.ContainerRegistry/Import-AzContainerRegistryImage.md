---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115944"
---
# <span data-ttu-id="5ca14-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="5ca14-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="5ca14-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ca14-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca14-103">Importar imagem de um registro público/azure para um registro de contêiner do azure.</span><span class="sxs-lookup"><span data-stu-id="5ca14-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="5ca14-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ca14-104">SYNTAX</span></span>

### <span data-ttu-id="5ca14-105">ImportImageByResourceId (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5ca14-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5ca14-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="5ca14-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ca14-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="5ca14-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ca14-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="5ca14-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ca14-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="5ca14-109">DESCRIPTION</span></span>
<span data-ttu-id="5ca14-110">Importar imagem de um registro público/azure para um registro de contêiner do azure.</span><span class="sxs-lookup"><span data-stu-id="5ca14-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="5ca14-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5ca14-111">EXAMPLES</span></span>

### <span data-ttu-id="5ca14-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5ca14-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="5ca14-113">Importar a caixa de trabalho para o ACR.</span><span class="sxs-lookup"><span data-stu-id="5ca14-113">Import busybox to ACR.</span></span> <span data-ttu-id="5ca14-114">Nota:</span><span class="sxs-lookup"><span data-stu-id="5ca14-114">Note:</span></span> 
* <span data-ttu-id="5ca14-115">"biblioteca/" precisa ser adicionar antes da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="5ca14-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="5ca14-116">"busybox:latest" => "library/busybox:latest"</span><span class="sxs-lookup"><span data-stu-id="5ca14-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="5ca14-117">Credencial necessária se o registro de origem não estiver disponível publicamente</span><span class="sxs-lookup"><span data-stu-id="5ca14-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="5ca14-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5ca14-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="5ca14-119">Importe a caixa de trabalho do ACR de origem para o ACR de destino.</span><span class="sxs-lookup"><span data-stu-id="5ca14-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="5ca14-120">Nota:</span><span class="sxs-lookup"><span data-stu-id="5ca14-120">Note:</span></span> 
* <span data-ttu-id="5ca14-121">Credencial necessária se o usuário administrador do registro de origem tiver sido desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5ca14-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="5ca14-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5ca14-122">PARAMETERS</span></span>

### <span data-ttu-id="5ca14-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca14-123">-DefaultProfile</span></span>
<span data-ttu-id="5ca14-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca14-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ca14-125">-Modo</span><span class="sxs-lookup"><span data-stu-id="5ca14-125">-Mode</span></span>
<span data-ttu-id="5ca14-126">Quando forçar, todas as marcas de destino existentes serão substituídas.</span><span class="sxs-lookup"><span data-stu-id="5ca14-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="5ca14-127">Quando NoForce, todas as marcas de destino existentes falharão na operação antes que qualquer cópia comece.</span><span class="sxs-lookup"><span data-stu-id="5ca14-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-128">-Senha</span><span class="sxs-lookup"><span data-stu-id="5ca14-128">-Password</span></span>
<span data-ttu-id="5ca14-129">A senha usada para autenticar com o registro de origem.</span><span class="sxs-lookup"><span data-stu-id="5ca14-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5ca14-130">-RegistryName</span></span>
<span data-ttu-id="5ca14-131">Nome do registro de destino.</span><span class="sxs-lookup"><span data-stu-id="5ca14-131">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca14-132">-ResourceGroupName</span></span>
<span data-ttu-id="5ca14-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5ca14-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="5ca14-134">-SourceImage</span></span>
<span data-ttu-id="5ca14-135">Nome do repositório da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="5ca14-135">Repository name of the source image.</span></span>

<span data-ttu-id="5ca14-136">Especifique uma imagem por repositório ('olá-mundo').</span><span class="sxs-lookup"><span data-stu-id="5ca14-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="5ca14-137">Isso usará a marca "mais recente".</span><span class="sxs-lookup"><span data-stu-id="5ca14-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="5ca14-138">Especifique uma imagem por marca ('hello-world:latest').</span><span class="sxs-lookup"><span data-stu-id="5ca14-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="5ca14-139">Especifique uma imagem por resumo de manifesto baseado em sha256 (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="5ca14-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="5ca14-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="5ca14-141">O identificador de recurso do Registro de Contêineres do Azure de origem.</span><span class="sxs-lookup"><span data-stu-id="5ca14-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="5ca14-142">-SourceRegistryUri</span></span>
<span data-ttu-id="5ca14-143">O endereço do registro de origem (por exemplo, 'mcr.microsoft.com').</span><span class="sxs-lookup"><span data-stu-id="5ca14-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="5ca14-144">-TargetTag</span></span>
<span data-ttu-id="5ca14-145">Lista de cadeias de caracteres do formulário repo \[ \] :tag.</span><span class="sxs-lookup"><span data-stu-id="5ca14-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="5ca14-146">Quando a marca é omitida, a fonte será usada (ou "mais recente" se a marca de origem também for omitida).</span><span class="sxs-lookup"><span data-stu-id="5ca14-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="5ca14-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="5ca14-148">Lista de cadeias de caracteres de nomes de repositório para fazer uma cópia somente de manifesto.</span><span class="sxs-lookup"><span data-stu-id="5ca14-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="5ca14-149">Nenhuma marca será criada.</span><span class="sxs-lookup"><span data-stu-id="5ca14-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-150">-Nome de usuário</span><span class="sxs-lookup"><span data-stu-id="5ca14-150">-Username</span></span>
<span data-ttu-id="5ca14-151">O nome de usuário a ser autenticado com o registro de origem.</span><span class="sxs-lookup"><span data-stu-id="5ca14-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-152">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5ca14-152">-Confirm</span></span>
<span data-ttu-id="5ca14-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ca14-153">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca14-154">-WhatIf</span></span>
<span data-ttu-id="5ca14-155">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5ca14-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ca14-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ca14-156">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ca14-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca14-157">CommonParameters</span></span>
<span data-ttu-id="5ca14-158">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca14-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca14-159">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ca14-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca14-160">Entradas</span><span class="sxs-lookup"><span data-stu-id="5ca14-160">INPUTS</span></span>

### <span data-ttu-id="5ca14-161">System.String</span><span class="sxs-lookup"><span data-stu-id="5ca14-161">System.String</span></span>

## <span data-ttu-id="5ca14-162">Saídas</span><span class="sxs-lookup"><span data-stu-id="5ca14-162">OUTPUTS</span></span>

### <span data-ttu-id="5ca14-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ca14-163">System.Boolean</span></span>

## <span data-ttu-id="5ca14-164">Notas</span><span class="sxs-lookup"><span data-stu-id="5ca14-164">NOTES</span></span>

## <span data-ttu-id="5ca14-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ca14-165">RELATED LINKS</span></span>
