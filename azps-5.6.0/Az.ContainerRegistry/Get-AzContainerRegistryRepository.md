---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: efcd7fb518f66c99fab8b4cd456e8f8cea424ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890293"
---
# <span data-ttu-id="b45ac-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="b45ac-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="b45ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b45ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b45ac-103">Obter ou listar repositórios ACR.</span><span class="sxs-lookup"><span data-stu-id="b45ac-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="b45ac-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b45ac-104">SYNTAX</span></span>

### <span data-ttu-id="b45ac-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b45ac-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b45ac-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="b45ac-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b45ac-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b45ac-107">DESCRIPTION</span></span>
<span data-ttu-id="b45ac-108">Obter ou listar repositórios ACR.</span><span class="sxs-lookup"><span data-stu-id="b45ac-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="b45ac-109">A lista retorna apenas nomes de repositório.</span><span class="sxs-lookup"><span data-stu-id="b45ac-109">List returns repository names only.</span></span>

## <span data-ttu-id="b45ac-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b45ac-110">EXAMPLES</span></span>

### <span data-ttu-id="b45ac-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b45ac-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="b45ac-112">Listar todos os repositórios no Registro.</span><span class="sxs-lookup"><span data-stu-id="b45ac-112">List all repositories in registry.</span></span>

### <span data-ttu-id="b45ac-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b45ac-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="b45ac-114">Listar os três primeiros repositórios no Registro.</span><span class="sxs-lookup"><span data-stu-id="b45ac-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="b45ac-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b45ac-115">Example 3</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -Name alpine

Registry             : registry.azurecr.io
ImageName            : alpine
CreatedTime          : 2020-10-13T05:45:25.5896115Z
LastUpdateTime       : 2021-01-04T08:31:46.2406505Z
ManifestCount        : 7
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="b45ac-116">Obter o repositório alpino no Registro.</span><span class="sxs-lookup"><span data-stu-id="b45ac-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="b45ac-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b45ac-117">PARAMETERS</span></span>

### <span data-ttu-id="b45ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b45ac-118">-DefaultProfile</span></span>
<span data-ttu-id="b45ac-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b45ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b45ac-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b45ac-120">-Name</span></span>
<span data-ttu-id="b45ac-121">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="b45ac-121">Repository Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b45ac-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b45ac-122">-RegistryName</span></span>
<span data-ttu-id="b45ac-123">Nome do Registro do Contêiner do Azure.</span><span class="sxs-lookup"><span data-stu-id="b45ac-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="b45ac-124">-First</span><span class="sxs-lookup"><span data-stu-id="b45ac-124">-First</span></span>
<span data-ttu-id="b45ac-125">Primeiro n resultados.</span><span class="sxs-lookup"><span data-stu-id="b45ac-125">First n results.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b45ac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b45ac-126">CommonParameters</span></span>
<span data-ttu-id="b45ac-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b45ac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b45ac-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b45ac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b45ac-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b45ac-129">INPUTS</span></span>

### <span data-ttu-id="b45ac-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b45ac-130">System.String</span></span>

## <span data-ttu-id="b45ac-131">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b45ac-131">OUTPUTS</span></span>

### <span data-ttu-id="b45ac-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b45ac-132">System.String</span></span>

### <span data-ttu-id="b45ac-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="b45ac-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="b45ac-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="b45ac-134">NOTES</span></span>

## <span data-ttu-id="b45ac-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b45ac-135">RELATED LINKS</span></span>
