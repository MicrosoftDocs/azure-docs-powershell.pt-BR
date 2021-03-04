---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: 45572cbd2255a604e492c7740d1749a0ad968845
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885921"
---
# <span data-ttu-id="d1746-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="d1746-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="d1746-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1746-102">SYNOPSIS</span></span>
<span data-ttu-id="d1746-103">Atualize o repositório do ACR.</span><span class="sxs-lookup"><span data-stu-id="d1746-103">Update ACR repository.</span></span>

## <span data-ttu-id="d1746-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d1746-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1746-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d1746-105">DESCRIPTION</span></span>
<span data-ttu-id="d1746-106">Atualize o repositório do ACR.</span><span class="sxs-lookup"><span data-stu-id="d1746-106">Update ACR repository.</span></span>

## <span data-ttu-id="d1746-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d1746-107">EXAMPLES</span></span>

### <span data-ttu-id="d1746-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d1746-108">Example 1</span></span>
```powershell
Update-AzContainerRegistryRepository -RegistryName registry -Name test/busybox8 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry             : registry.azurecr.io
ImageName            : test/busybox8
CreatedTime          : 2020-12-11T08:57:56.2070002Z
LastUpdateTime       : 2020-12-11T08:57:56.5188237Z
ManifestCount        : 1
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="d1746-109">Atualizar atributos para o repositório alpino no Registro.</span><span class="sxs-lookup"><span data-stu-id="d1746-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="d1746-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d1746-110">PARAMETERS</span></span>

### <span data-ttu-id="d1746-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1746-111">-DefaultProfile</span></span>
<span data-ttu-id="d1746-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d1746-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1746-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="d1746-113">-DeleteEnabled</span></span>
<span data-ttu-id="d1746-114">Excluir habilitar.</span><span class="sxs-lookup"><span data-stu-id="d1746-114">Delete enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1746-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="d1746-115">-ListEnabled</span></span>
<span data-ttu-id="d1746-116">Listar habilitada.</span><span class="sxs-lookup"><span data-stu-id="d1746-116">List enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1746-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d1746-117">-Name</span></span>
<span data-ttu-id="d1746-118">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="d1746-118">Repository Name.</span></span>

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

### <span data-ttu-id="d1746-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="d1746-119">-ReadEnabled</span></span>
<span data-ttu-id="d1746-120">Ler habilitar.</span><span class="sxs-lookup"><span data-stu-id="d1746-120">Read enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1746-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d1746-121">-RegistryName</span></span>
<span data-ttu-id="d1746-122">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="d1746-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="d1746-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="d1746-123">-WriteEnabled</span></span>
<span data-ttu-id="d1746-124">Gravar habilitado.</span><span class="sxs-lookup"><span data-stu-id="d1746-124">Write enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1746-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1746-125">-Confirm</span></span>
<span data-ttu-id="d1746-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1746-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1746-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1746-127">-WhatIf</span></span>
<span data-ttu-id="d1746-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d1746-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1746-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d1746-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1746-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1746-130">CommonParameters</span></span>
<span data-ttu-id="d1746-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1746-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1746-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1746-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1746-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1746-133">INPUTS</span></span>

### <span data-ttu-id="d1746-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d1746-134">System.String</span></span>

## <span data-ttu-id="d1746-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d1746-135">OUTPUTS</span></span>

### <span data-ttu-id="d1746-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="d1746-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="d1746-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="d1746-137">NOTES</span></span>

## <span data-ttu-id="d1746-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d1746-138">RELATED LINKS</span></span>
