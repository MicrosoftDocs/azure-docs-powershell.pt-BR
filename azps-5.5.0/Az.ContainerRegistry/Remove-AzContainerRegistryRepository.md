---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: a99d020bbdef81868fb0e4338c7bc6c722723254
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116494"
---
# <span data-ttu-id="58c6a-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="58c6a-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="58c6a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="58c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="58c6a-103">Exclua o repositório do ACR.</span><span class="sxs-lookup"><span data-stu-id="58c6a-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="58c6a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="58c6a-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58c6a-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="58c6a-105">DESCRIPTION</span></span>
<span data-ttu-id="58c6a-106">Exclua o repositório do ACR.</span><span class="sxs-lookup"><span data-stu-id="58c6a-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="58c6a-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="58c6a-107">EXAMPLES</span></span>

### <span data-ttu-id="58c6a-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="58c6a-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="58c6a-109">Exclua o teste do repositório/busybox15 em Registro.</span><span class="sxs-lookup"><span data-stu-id="58c6a-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="58c6a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58c6a-110">PARAMETERS</span></span>

### <span data-ttu-id="58c6a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c6a-111">-DefaultProfile</span></span>
<span data-ttu-id="58c6a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="58c6a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c6a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="58c6a-113">-Name</span></span>
<span data-ttu-id="58c6a-114">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="58c6a-114">Repository Name.</span></span>

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

### <span data-ttu-id="58c6a-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="58c6a-115">-RegistryName</span></span>
<span data-ttu-id="58c6a-116">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="58c6a-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="58c6a-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="58c6a-117">-Confirm</span></span>
<span data-ttu-id="58c6a-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58c6a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58c6a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58c6a-119">-WhatIf</span></span>
<span data-ttu-id="58c6a-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="58c6a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58c6a-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="58c6a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58c6a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c6a-122">CommonParameters</span></span>
<span data-ttu-id="58c6a-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58c6a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c6a-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58c6a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c6a-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="58c6a-125">INPUTS</span></span>

### <span data-ttu-id="58c6a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="58c6a-126">System.String</span></span>

## <span data-ttu-id="58c6a-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="58c6a-127">OUTPUTS</span></span>

### <span data-ttu-id="58c6a-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="58c6a-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="58c6a-129">Notas</span><span class="sxs-lookup"><span data-stu-id="58c6a-129">NOTES</span></span>

## <span data-ttu-id="58c6a-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="58c6a-130">RELATED LINKS</span></span>
