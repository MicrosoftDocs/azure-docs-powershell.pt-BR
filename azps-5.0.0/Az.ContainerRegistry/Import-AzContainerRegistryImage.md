---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280343"
---
# <span data-ttu-id="b776e-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="b776e-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="b776e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b776e-102">SYNOPSIS</span></span>
<span data-ttu-id="b776e-103">Importar a imagem de um registro público/do Azure para um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="b776e-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="b776e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b776e-104">SYNTAX</span></span>

### <span data-ttu-id="b776e-105">ImportImageByResourceId (padrão)</span><span class="sxs-lookup"><span data-stu-id="b776e-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b776e-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="b776e-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b776e-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="b776e-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b776e-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="b776e-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b776e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b776e-109">DESCRIPTION</span></span>
<span data-ttu-id="b776e-110">Importar a imagem de um registro público/do Azure para um registro de contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="b776e-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="b776e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b776e-111">EXAMPLES</span></span>

### <span data-ttu-id="b776e-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b776e-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="b776e-113">Importar busybox para ACR.</span><span class="sxs-lookup"><span data-stu-id="b776e-113">Import busybox to ACR.</span></span> <span data-ttu-id="b776e-114">Anota</span><span class="sxs-lookup"><span data-stu-id="b776e-114">Note:</span></span> 
* <span data-ttu-id="b776e-115">"library/" precisa ser adicionado antes da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="b776e-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="b776e-116">"busybox: mais recente" => "library/busybox: latest"</span><span class="sxs-lookup"><span data-stu-id="b776e-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="b776e-117">Credenciais necessárias se o registro de origem não estiver disponível publicamente</span><span class="sxs-lookup"><span data-stu-id="b776e-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="b776e-118">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b776e-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="b776e-119">Importar busybox do ACR de origem para o ACR de destino.</span><span class="sxs-lookup"><span data-stu-id="b776e-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="b776e-120">Anota</span><span class="sxs-lookup"><span data-stu-id="b776e-120">Note:</span></span> 
* <span data-ttu-id="b776e-121">Credenciais necessárias se o usuário administrador do registro de origem foi desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b776e-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="b776e-122">OS</span><span class="sxs-lookup"><span data-stu-id="b776e-122">PARAMETERS</span></span>

### <span data-ttu-id="b776e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b776e-123">-DefaultProfile</span></span>
<span data-ttu-id="b776e-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b776e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b776e-125">-Mode</span><span class="sxs-lookup"><span data-stu-id="b776e-125">-Mode</span></span>
<span data-ttu-id="b776e-126">Quando forçar, qualquer marca de destino existente será substituída.</span><span class="sxs-lookup"><span data-stu-id="b776e-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="b776e-127">Quando noforce, todas as marcas de destino existentes falham na operação antes de começar a copiar.</span><span class="sxs-lookup"><span data-stu-id="b776e-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

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

### <span data-ttu-id="b776e-128">-Senha</span><span class="sxs-lookup"><span data-stu-id="b776e-128">-Password</span></span>
<span data-ttu-id="b776e-129">A senha usada para autenticar com o registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b776e-129">The password used to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="b776e-130">-Registryname</span><span class="sxs-lookup"><span data-stu-id="b776e-130">-RegistryName</span></span>
<span data-ttu-id="b776e-131">Nome do registro de destino.</span><span class="sxs-lookup"><span data-stu-id="b776e-131">Target registry name.</span></span>

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

### <span data-ttu-id="b776e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b776e-132">-ResourceGroupName</span></span>
<span data-ttu-id="b776e-133">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b776e-133">Resource group name.</span></span>

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

### <span data-ttu-id="b776e-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="b776e-134">-SourceImage</span></span>
<span data-ttu-id="b776e-135">Nome do repositório da imagem de origem.</span><span class="sxs-lookup"><span data-stu-id="b776e-135">Repository name of the source image.</span></span>

<span data-ttu-id="b776e-136">Especifique uma imagem por repositório (' Olá-mundo ').</span><span class="sxs-lookup"><span data-stu-id="b776e-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="b776e-137">Isso vai usar a marca ' mais recente '.</span><span class="sxs-lookup"><span data-stu-id="b776e-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="b776e-138">Especifique uma imagem por marca (' Olá-mundo: mais recente ').</span><span class="sxs-lookup"><span data-stu-id="b776e-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="b776e-139">Especifique uma imagem por Resumo de manifesto baseado em SHA256 (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="b776e-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="b776e-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="b776e-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="b776e-141">O identificador de recurso do registro de contêiner de origem do Azure.</span><span class="sxs-lookup"><span data-stu-id="b776e-141">The resource identifier of the source Azure Container Registry.</span></span>

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

### <span data-ttu-id="b776e-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="b776e-142">-SourceRegistryUri</span></span>
<span data-ttu-id="b776e-143">O endereço do registro de origem (por exemplo, "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="b776e-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

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

### <span data-ttu-id="b776e-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="b776e-144">-TargetTag</span></span>
<span data-ttu-id="b776e-145">Lista de cadeias de caracteres da marca repositório de formulários \[ : \] .</span><span class="sxs-lookup"><span data-stu-id="b776e-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="b776e-146">Quando a marca for omitida, a origem será usada (ou ' Latest ' se a marca de fonte também estiver omitida).</span><span class="sxs-lookup"><span data-stu-id="b776e-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

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

### <span data-ttu-id="b776e-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="b776e-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="b776e-148">Lista de cadeias de caracteres de nomes de repositório para fazer um manifesto copiar apenas.</span><span class="sxs-lookup"><span data-stu-id="b776e-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="b776e-149">Nenhuma marca será criada.</span><span class="sxs-lookup"><span data-stu-id="b776e-149">No tag will be created.</span></span>

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

### <span data-ttu-id="b776e-150">-Username</span><span class="sxs-lookup"><span data-stu-id="b776e-150">-Username</span></span>
<span data-ttu-id="b776e-151">O nome de usuário para autenticar com o registro de origem.</span><span class="sxs-lookup"><span data-stu-id="b776e-151">The username to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="b776e-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b776e-152">-Confirm</span></span>
<span data-ttu-id="b776e-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b776e-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b776e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b776e-154">-WhatIf</span></span>
<span data-ttu-id="b776e-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b776e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b776e-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b776e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b776e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b776e-157">CommonParameters</span></span>
<span data-ttu-id="b776e-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b776e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b776e-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b776e-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b776e-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b776e-160">INPUTS</span></span>

### <span data-ttu-id="b776e-161">System. String</span><span class="sxs-lookup"><span data-stu-id="b776e-161">System.String</span></span>

## <span data-ttu-id="b776e-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b776e-162">OUTPUTS</span></span>

### <span data-ttu-id="b776e-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b776e-163">System.Boolean</span></span>

## <span data-ttu-id="b776e-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b776e-164">NOTES</span></span>

## <span data-ttu-id="b776e-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b776e-165">RELATED LINKS</span></span>
