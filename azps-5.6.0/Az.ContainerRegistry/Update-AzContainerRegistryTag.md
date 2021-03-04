---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 68d4eab2088bc1091d812399aade67659d7db31b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885920"
---
# <span data-ttu-id="07f17-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="07f17-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="07f17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f17-102">SYNOPSIS</span></span>
<span data-ttu-id="07f17-103">Atualizar a marca ACR.</span><span class="sxs-lookup"><span data-stu-id="07f17-103">Update ACR tag.</span></span>

## <span data-ttu-id="07f17-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07f17-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f17-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07f17-105">DESCRIPTION</span></span>
<span data-ttu-id="07f17-106">Atualizar a marca ACR.</span><span class="sxs-lookup"><span data-stu-id="07f17-106">Update ACR tag.</span></span>
<span data-ttu-id="07f17-107">Para usar esse cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="07f17-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="07f17-108">primeiro.</span><span class="sxs-lookup"><span data-stu-id="07f17-108">first.</span></span>

## <span data-ttu-id="07f17-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07f17-109">EXAMPLES</span></span>

### <span data-ttu-id="07f17-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07f17-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="07f17-111">Atualizar atributos para a marca mais recente no Registro.</span><span class="sxs-lookup"><span data-stu-id="07f17-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="07f17-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07f17-112">PARAMETERS</span></span>

### <span data-ttu-id="07f17-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f17-113">-DefaultProfile</span></span>
<span data-ttu-id="07f17-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07f17-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f17-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="07f17-115">-DeleteEnabled</span></span>
<span data-ttu-id="07f17-116">Excluir habilitar.</span><span class="sxs-lookup"><span data-stu-id="07f17-116">Delete enable.</span></span>

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

### <span data-ttu-id="07f17-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="07f17-117">-ListEnabled</span></span>
<span data-ttu-id="07f17-118">Listar habilitada.</span><span class="sxs-lookup"><span data-stu-id="07f17-118">List enable.</span></span>

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

### <span data-ttu-id="07f17-119">-Name</span><span class="sxs-lookup"><span data-stu-id="07f17-119">-Name</span></span>
<span data-ttu-id="07f17-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="07f17-120">Tag.</span></span>

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

### <span data-ttu-id="07f17-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="07f17-121">-ReadEnabled</span></span>
<span data-ttu-id="07f17-122">Ler habilitar.</span><span class="sxs-lookup"><span data-stu-id="07f17-122">Read enable.</span></span>

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

### <span data-ttu-id="07f17-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="07f17-123">-RegistryName</span></span>
<span data-ttu-id="07f17-124">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="07f17-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="07f17-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="07f17-125">-RepositoryName</span></span>
<span data-ttu-id="07f17-126">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="07f17-126">Repository Name.</span></span>

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

### <span data-ttu-id="07f17-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="07f17-127">-WriteEnabled</span></span>
<span data-ttu-id="07f17-128">Gravar habilitado.</span><span class="sxs-lookup"><span data-stu-id="07f17-128">Write enable.</span></span>

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

### <span data-ttu-id="07f17-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07f17-129">-Confirm</span></span>
<span data-ttu-id="07f17-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07f17-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f17-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f17-131">-WhatIf</span></span>
<span data-ttu-id="07f17-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07f17-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f17-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07f17-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f17-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f17-134">CommonParameters</span></span>
<span data-ttu-id="07f17-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f17-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f17-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07f17-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f17-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07f17-137">INPUTS</span></span>

### <span data-ttu-id="07f17-138">System.String</span><span class="sxs-lookup"><span data-stu-id="07f17-138">System.String</span></span>

## <span data-ttu-id="07f17-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07f17-139">OUTPUTS</span></span>

### <span data-ttu-id="07f17-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="07f17-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="07f17-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="07f17-141">NOTES</span></span>

## <span data-ttu-id="07f17-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07f17-142">RELATED LINKS</span></span>
