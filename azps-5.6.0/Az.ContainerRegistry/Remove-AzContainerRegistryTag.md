---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 6fbc5b33bb8e9c865b5ea869deed5044ee08198f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885938"
---
# <span data-ttu-id="0c9a4-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="0c9a4-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="0c9a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9a4-103">Desatag marca ACR.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-103">Untag ACR tag.</span></span>

## <span data-ttu-id="0c9a4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0c9a4-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c9a4-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0c9a4-105">DESCRIPTION</span></span>
<span data-ttu-id="0c9a4-106">Desatag marca ACR.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-106">Untag ACR tag.</span></span>
<span data-ttu-id="0c9a4-107">Para usar esse cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="0c9a4-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="0c9a4-108">primeiro.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-108">first.</span></span>

## <span data-ttu-id="0c9a4-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-109">EXAMPLES</span></span>

### <span data-ttu-id="0c9a4-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0c9a4-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="0c9a4-111">Untag alpine:tag under Registry.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="0c9a4-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-112">PARAMETERS</span></span>

### <span data-ttu-id="0c9a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9a4-113">-DefaultProfile</span></span>
<span data-ttu-id="0c9a4-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c9a4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0c9a4-115">-Name</span></span>
<span data-ttu-id="0c9a4-116">Tag.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-116">Tag.</span></span>

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

### <span data-ttu-id="0c9a4-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0c9a4-117">-RegistryName</span></span>
<span data-ttu-id="0c9a4-118">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="0c9a4-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="0c9a4-119">-RepositoryName</span></span>
<span data-ttu-id="0c9a4-120">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-120">Repository Name.</span></span>

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

### <span data-ttu-id="0c9a4-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c9a4-121">-Confirm</span></span>
<span data-ttu-id="0c9a4-122">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c9a4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c9a4-123">-WhatIf</span></span>
<span data-ttu-id="0c9a4-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c9a4-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c9a4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9a4-126">CommonParameters</span></span>
<span data-ttu-id="0c9a4-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c9a4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9a4-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c9a4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9a4-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-129">INPUTS</span></span>

### <span data-ttu-id="0c9a4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0c9a4-130">System.String</span></span>

## <span data-ttu-id="0c9a4-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-131">OUTPUTS</span></span>

### <span data-ttu-id="0c9a4-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0c9a4-132">System.Boolean</span></span>

## <span data-ttu-id="0c9a4-133">NOTES</span><span class="sxs-lookup"><span data-stu-id="0c9a4-133">NOTES</span></span>

## <span data-ttu-id="0c9a4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0c9a4-134">RELATED LINKS</span></span>
