---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: ce6f235669ebe4a32958229422f4612f3b8cb340
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115938"
---
# <span data-ttu-id="f6a59-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="f6a59-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="f6a59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6a59-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a59-103">Atualizar repositório ACR.</span><span class="sxs-lookup"><span data-stu-id="f6a59-103">Update ACR repository.</span></span>

## <span data-ttu-id="f6a59-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6a59-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6a59-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6a59-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a59-106">Atualizar repositório ACR.</span><span class="sxs-lookup"><span data-stu-id="f6a59-106">Update ACR repository.</span></span>

## <span data-ttu-id="f6a59-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6a59-107">EXAMPLES</span></span>

### <span data-ttu-id="f6a59-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6a59-108">Example 1</span></span>
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

<span data-ttu-id="f6a59-109">Atualizar atributos do alpino do repositório sob o Registro.</span><span class="sxs-lookup"><span data-stu-id="f6a59-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="f6a59-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6a59-110">PARAMETERS</span></span>

### <span data-ttu-id="f6a59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a59-111">-DefaultProfile</span></span>
<span data-ttu-id="f6a59-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a59-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6a59-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="f6a59-113">-DeleteEnabled</span></span>
<span data-ttu-id="f6a59-114">Excluir habilitar.</span><span class="sxs-lookup"><span data-stu-id="f6a59-114">Delete enable.</span></span>

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

### <span data-ttu-id="f6a59-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="f6a59-115">-ListEnabled</span></span>
<span data-ttu-id="f6a59-116">Habilitar lista.</span><span class="sxs-lookup"><span data-stu-id="f6a59-116">List enable.</span></span>

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

### <span data-ttu-id="f6a59-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6a59-117">-Name</span></span>
<span data-ttu-id="f6a59-118">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="f6a59-118">Repository Name.</span></span>

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

### <span data-ttu-id="f6a59-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="f6a59-119">-ReadEnabled</span></span>
<span data-ttu-id="f6a59-120">Habilitar leitura.</span><span class="sxs-lookup"><span data-stu-id="f6a59-120">Read enable.</span></span>

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

### <span data-ttu-id="f6a59-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f6a59-121">-RegistryName</span></span>
<span data-ttu-id="f6a59-122">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a59-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="f6a59-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="f6a59-123">-WriteEnabled</span></span>
<span data-ttu-id="f6a59-124">Habilitar gravação.</span><span class="sxs-lookup"><span data-stu-id="f6a59-124">Write enable.</span></span>

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

### <span data-ttu-id="f6a59-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f6a59-125">-Confirm</span></span>
<span data-ttu-id="f6a59-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6a59-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6a59-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a59-127">-WhatIf</span></span>
<span data-ttu-id="f6a59-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f6a59-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6a59-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6a59-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6a59-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a59-130">CommonParameters</span></span>
<span data-ttu-id="f6a59-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6a59-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a59-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6a59-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a59-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="f6a59-133">INPUTS</span></span>

### <span data-ttu-id="f6a59-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f6a59-134">System.String</span></span>

## <span data-ttu-id="f6a59-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="f6a59-135">OUTPUTS</span></span>

### <span data-ttu-id="f6a59-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="f6a59-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="f6a59-137">Notas</span><span class="sxs-lookup"><span data-stu-id="f6a59-137">NOTES</span></span>

## <span data-ttu-id="f6a59-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6a59-138">RELATED LINKS</span></span>
