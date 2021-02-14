---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 7e6528630c731b15f906d79de45bc50f94b2a715
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116491"
---
# <span data-ttu-id="5537f-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="5537f-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="5537f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5537f-102">SYNOPSIS</span></span>
<span data-ttu-id="5537f-103">Desatagar marca ACR.</span><span class="sxs-lookup"><span data-stu-id="5537f-103">Untag ACR tag.</span></span>

## <span data-ttu-id="5537f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5537f-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5537f-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="5537f-105">DESCRIPTION</span></span>
<span data-ttu-id="5537f-106">Desatagar marca ACR.</span><span class="sxs-lookup"><span data-stu-id="5537f-106">Untag ACR tag.</span></span>
<span data-ttu-id="5537f-107">Para usar este cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="5537f-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="5537f-108">Primeiro.</span><span class="sxs-lookup"><span data-stu-id="5537f-108">first.</span></span>

## <span data-ttu-id="5537f-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5537f-109">EXAMPLES</span></span>

### <span data-ttu-id="5537f-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5537f-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="5537f-111">Untag alpine:tag under Registry.</span><span class="sxs-lookup"><span data-stu-id="5537f-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="5537f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5537f-112">PARAMETERS</span></span>

### <span data-ttu-id="5537f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5537f-113">-DefaultProfile</span></span>
<span data-ttu-id="5537f-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5537f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5537f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5537f-115">-Name</span></span>
<span data-ttu-id="5537f-116">Tag.</span><span class="sxs-lookup"><span data-stu-id="5537f-116">Tag.</span></span>

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

### <span data-ttu-id="5537f-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5537f-117">-RegistryName</span></span>
<span data-ttu-id="5537f-118">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="5537f-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="5537f-119">-NomedoPositor</span><span class="sxs-lookup"><span data-stu-id="5537f-119">-RepositoryName</span></span>
<span data-ttu-id="5537f-120">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="5537f-120">Repository Name.</span></span>

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

### <span data-ttu-id="5537f-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="5537f-121">-Confirm</span></span>
<span data-ttu-id="5537f-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5537f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5537f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5537f-123">-WhatIf</span></span>
<span data-ttu-id="5537f-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="5537f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5537f-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5537f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5537f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5537f-126">CommonParameters</span></span>
<span data-ttu-id="5537f-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5537f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5537f-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5537f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5537f-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="5537f-129">INPUTS</span></span>

### <span data-ttu-id="5537f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="5537f-130">System.String</span></span>

## <span data-ttu-id="5537f-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="5537f-131">OUTPUTS</span></span>

### <span data-ttu-id="5537f-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5537f-132">System.Boolean</span></span>

## <span data-ttu-id="5537f-133">Notas</span><span class="sxs-lookup"><span data-stu-id="5537f-133">NOTES</span></span>

## <span data-ttu-id="5537f-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5537f-134">RELATED LINKS</span></span>
