---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: 1c0ad2ae46987a526be4e8fda110dada914bd27e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888317"
---
# <span data-ttu-id="531ea-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="531ea-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="531ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="531ea-102">SYNOPSIS</span></span>
<span data-ttu-id="531ea-103">Excluir repositório do ACR.</span><span class="sxs-lookup"><span data-stu-id="531ea-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="531ea-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="531ea-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="531ea-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="531ea-105">DESCRIPTION</span></span>
<span data-ttu-id="531ea-106">Excluir repositório do ACR.</span><span class="sxs-lookup"><span data-stu-id="531ea-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="531ea-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="531ea-107">EXAMPLES</span></span>

### <span data-ttu-id="531ea-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="531ea-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="531ea-109">Excluir teste/busybox15 do repositório no Registro.</span><span class="sxs-lookup"><span data-stu-id="531ea-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="531ea-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="531ea-110">PARAMETERS</span></span>

### <span data-ttu-id="531ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="531ea-111">-DefaultProfile</span></span>
<span data-ttu-id="531ea-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="531ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="531ea-113">-Name</span><span class="sxs-lookup"><span data-stu-id="531ea-113">-Name</span></span>
<span data-ttu-id="531ea-114">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="531ea-114">Repository Name.</span></span>

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

### <span data-ttu-id="531ea-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="531ea-115">-RegistryName</span></span>
<span data-ttu-id="531ea-116">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="531ea-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="531ea-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="531ea-117">-Confirm</span></span>
<span data-ttu-id="531ea-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="531ea-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="531ea-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="531ea-119">-WhatIf</span></span>
<span data-ttu-id="531ea-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="531ea-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="531ea-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="531ea-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="531ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531ea-122">CommonParameters</span></span>
<span data-ttu-id="531ea-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="531ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531ea-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="531ea-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531ea-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="531ea-125">INPUTS</span></span>

### <span data-ttu-id="531ea-126">System.String</span><span class="sxs-lookup"><span data-stu-id="531ea-126">System.String</span></span>

## <span data-ttu-id="531ea-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="531ea-127">OUTPUTS</span></span>

### <span data-ttu-id="531ea-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="531ea-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="531ea-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="531ea-129">NOTES</span></span>

## <span data-ttu-id="531ea-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="531ea-130">RELATED LINKS</span></span>
