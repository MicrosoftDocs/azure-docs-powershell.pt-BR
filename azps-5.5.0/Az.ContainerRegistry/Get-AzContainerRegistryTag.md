---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 88bf3648f416efa69576c6b09a0d59f0d0d0fa76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112086"
---
# <span data-ttu-id="f55a4-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="f55a4-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="f55a4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f55a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f55a4-103">Obter ou listar a marca ACR.</span><span class="sxs-lookup"><span data-stu-id="f55a4-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="f55a4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f55a4-104">SYNTAX</span></span>

### <span data-ttu-id="f55a4-105">ListParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f55a4-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f55a4-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="f55a4-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f55a4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f55a4-107">DESCRIPTION</span></span>
<span data-ttu-id="f55a4-108">Obter ou listar a marca ACR.</span><span class="sxs-lookup"><span data-stu-id="f55a4-108">Get or list ACR tag.</span></span>
<span data-ttu-id="f55a4-109">Para usar este cmdlet, execute `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="f55a4-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="f55a4-110">Primeiro.</span><span class="sxs-lookup"><span data-stu-id="f55a4-110">first.</span></span>

## <span data-ttu-id="f55a4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f55a4-111">EXAMPLES</span></span>

### <span data-ttu-id="f55a4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f55a4-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="f55a4-113">Marcas de lista do alpino do repositório sob o Registro.</span><span class="sxs-lookup"><span data-stu-id="f55a4-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="f55a4-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f55a4-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="f55a4-115">Obter a marca mais recente para o alpino do repositório em Registro.</span><span class="sxs-lookup"><span data-stu-id="f55a4-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="f55a4-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f55a4-116">PARAMETERS</span></span>

### <span data-ttu-id="f55a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f55a4-117">-DefaultProfile</span></span>
<span data-ttu-id="f55a4-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f55a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f55a4-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f55a4-119">-Name</span></span>
<span data-ttu-id="f55a4-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="f55a4-120">Tag.</span></span>

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

### <span data-ttu-id="f55a4-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f55a4-121">-RegistryName</span></span>
<span data-ttu-id="f55a4-122">Nome do Registro de Contêineres do Azure.</span><span class="sxs-lookup"><span data-stu-id="f55a4-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="f55a4-123">-NomedoPositor</span><span class="sxs-lookup"><span data-stu-id="f55a4-123">-RepositoryName</span></span>
<span data-ttu-id="f55a4-124">Nome do Repositório.</span><span class="sxs-lookup"><span data-stu-id="f55a4-124">Repository Name.</span></span>

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

### <span data-ttu-id="f55a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f55a4-125">CommonParameters</span></span>
<span data-ttu-id="f55a4-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f55a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f55a4-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f55a4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f55a4-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="f55a4-128">INPUTS</span></span>

### <span data-ttu-id="f55a4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f55a4-129">System.String</span></span>

## <span data-ttu-id="f55a4-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="f55a4-130">OUTPUTS</span></span>

### <span data-ttu-id="f55a4-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="f55a4-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="f55a4-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="f55a4-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="f55a4-133">Notas</span><span class="sxs-lookup"><span data-stu-id="f55a4-133">NOTES</span></span>

## <span data-ttu-id="f55a4-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f55a4-134">RELATED LINKS</span></span>
