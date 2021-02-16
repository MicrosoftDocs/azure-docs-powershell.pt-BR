---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 48fb77eb9c718a09a7e13e6d6ab5af5bfc60c912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117800"
---
# <span data-ttu-id="1fe9d-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="1fe9d-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="1fe9d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1fe9d-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe9d-103">Atualizar a marca ACR.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-103">Update ACR tag.</span></span>

## <span data-ttu-id="1fe9d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fe9d-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe9d-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1fe9d-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe9d-106">Atualizar a marca ACR.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-106">Update ACR tag.</span></span>
<span data-ttu-id="1fe9d-107">Para usar este cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="1fe9d-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="1fe9d-108">Primeiro.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-108">first.</span></span>

## <span data-ttu-id="1fe9d-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1fe9d-109">EXAMPLES</span></span>

### <span data-ttu-id="1fe9d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1fe9d-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="1fe9d-111">Atualizar atributos para a marca mais recente no Registro.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="1fe9d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fe9d-112">PARAMETERS</span></span>

### <span data-ttu-id="1fe9d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe9d-113">-DefaultProfile</span></span>
<span data-ttu-id="1fe9d-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe9d-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="1fe9d-115">-DeleteEnabled</span></span>
<span data-ttu-id="1fe9d-116">Excluir habilitar.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-116">Delete enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe9d-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="1fe9d-117">-ListEnabled</span></span>
<span data-ttu-id="1fe9d-118">Habilitar lista.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-118">List enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe9d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1fe9d-119">-Name</span></span>
<span data-ttu-id="1fe9d-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-120">Tag.</span></span>

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

### <span data-ttu-id="1fe9d-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="1fe9d-121">-ReadEnabled</span></span>
<span data-ttu-id="1fe9d-122">Habilitar leitura.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-122">Read enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe9d-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="1fe9d-123">-RegistryName</span></span>
<span data-ttu-id="1fe9d-124">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="1fe9d-125">-NomedoPositor</span><span class="sxs-lookup"><span data-stu-id="1fe9d-125">-RepositoryName</span></span>
<span data-ttu-id="1fe9d-126">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-126">Repository Name.</span></span>

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

### <span data-ttu-id="1fe9d-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="1fe9d-127">-WriteEnabled</span></span>
<span data-ttu-id="1fe9d-128">Habilitar gravação.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-128">Write enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe9d-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1fe9d-129">-Confirm</span></span>
<span data-ttu-id="1fe9d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe9d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe9d-131">-WhatIf</span></span>
<span data-ttu-id="1fe9d-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe9d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe9d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe9d-134">CommonParameters</span></span>
<span data-ttu-id="1fe9d-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe9d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe9d-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fe9d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe9d-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="1fe9d-137">INPUTS</span></span>

### <span data-ttu-id="1fe9d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1fe9d-138">System.String</span></span>

## <span data-ttu-id="1fe9d-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="1fe9d-139">OUTPUTS</span></span>

### <span data-ttu-id="1fe9d-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="1fe9d-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="1fe9d-141">Notas</span><span class="sxs-lookup"><span data-stu-id="1fe9d-141">NOTES</span></span>

## <span data-ttu-id="1fe9d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1fe9d-142">RELATED LINKS</span></span>
