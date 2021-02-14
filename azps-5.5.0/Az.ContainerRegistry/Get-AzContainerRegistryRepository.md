---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: 7da65515138ff6afa97e6c05f9baa764d6ab920c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115945"
---
# <span data-ttu-id="cb8eb-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="cb8eb-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="cb8eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cb8eb-102">SYNOPSIS</span></span>
<span data-ttu-id="cb8eb-103">Obter ou listar repositórios de ACR.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="cb8eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb8eb-104">SYNTAX</span></span>

### <span data-ttu-id="cb8eb-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cb8eb-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb8eb-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb8eb-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb8eb-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="cb8eb-107">DESCRIPTION</span></span>
<span data-ttu-id="cb8eb-108">Obter ou listar repositórios de ACR.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="cb8eb-109">A lista retorna apenas nomes de repositório.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-109">List returns repository names only.</span></span>

## <span data-ttu-id="cb8eb-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cb8eb-110">EXAMPLES</span></span>

### <span data-ttu-id="cb8eb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cb8eb-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="cb8eb-112">Listar todos os repositórios no Registro.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-112">List all repositories in registry.</span></span>

### <span data-ttu-id="cb8eb-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="cb8eb-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="cb8eb-114">Listar os três primeiros repositórios no Registro.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="cb8eb-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="cb8eb-115">Example 3</span></span>
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

<span data-ttu-id="cb8eb-116">Obter o alpino do repositório sob o Registro.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="cb8eb-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb8eb-117">PARAMETERS</span></span>

### <span data-ttu-id="cb8eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb8eb-118">-DefaultProfile</span></span>
<span data-ttu-id="cb8eb-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb8eb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb8eb-120">-Name</span></span>
<span data-ttu-id="cb8eb-121">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-121">Repository Name.</span></span>

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

### <span data-ttu-id="cb8eb-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="cb8eb-122">-RegistryName</span></span>
<span data-ttu-id="cb8eb-123">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="cb8eb-124">-First</span><span class="sxs-lookup"><span data-stu-id="cb8eb-124">-First</span></span>
<span data-ttu-id="cb8eb-125">Primeiro n resultados.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-125">First n results.</span></span>

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

### <span data-ttu-id="cb8eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb8eb-126">CommonParameters</span></span>
<span data-ttu-id="cb8eb-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb8eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb8eb-128">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb8eb-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb8eb-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="cb8eb-129">INPUTS</span></span>

### <span data-ttu-id="cb8eb-130">System.String</span><span class="sxs-lookup"><span data-stu-id="cb8eb-130">System.String</span></span>

## <span data-ttu-id="cb8eb-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="cb8eb-131">OUTPUTS</span></span>

### <span data-ttu-id="cb8eb-132">System.String</span><span class="sxs-lookup"><span data-stu-id="cb8eb-132">System.String</span></span>

### <span data-ttu-id="cb8eb-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="cb8eb-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="cb8eb-134">Notas</span><span class="sxs-lookup"><span data-stu-id="cb8eb-134">NOTES</span></span>

## <span data-ttu-id="cb8eb-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cb8eb-135">RELATED LINKS</span></span>
