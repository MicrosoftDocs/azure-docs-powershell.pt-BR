---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 0a0701a073101b0611f74a9443473fcd9568ca50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885928"
---
# <span data-ttu-id="69b59-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="69b59-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="69b59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b59-102">SYNOPSIS</span></span>
<span data-ttu-id="69b59-103">Verifica a disponibilidade de um nome de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="69b59-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="69b59-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="69b59-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69b59-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="69b59-105">DESCRIPTION</span></span>
<span data-ttu-id="69b59-106">O Test-AzContainerRegistryNameAvailability cmdlet verifica se um nome de registro de contêiner é válido e disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="69b59-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="69b59-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="69b59-107">EXAMPLES</span></span>

### <span data-ttu-id="69b59-108">Exemplo 1: verifica a disponibilidade de um nome de registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="69b59-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="69b59-109">Este comando verifica a disponibilidade do nome do registro de contêiner \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="69b59-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="69b59-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="69b59-110">PARAMETERS</span></span>

### <span data-ttu-id="69b59-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b59-111">-DefaultProfile</span></span>
<span data-ttu-id="69b59-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="69b59-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69b59-113">-Name</span><span class="sxs-lookup"><span data-stu-id="69b59-113">-Name</span></span>
<span data-ttu-id="69b59-114">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="69b59-114">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69b59-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b59-115">CommonParameters</span></span>
<span data-ttu-id="69b59-116">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b59-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b59-117">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69b59-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b59-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69b59-118">INPUTS</span></span>

### <span data-ttu-id="69b59-119">System.String</span><span class="sxs-lookup"><span data-stu-id="69b59-119">System.String</span></span>

## <span data-ttu-id="69b59-120">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="69b59-120">OUTPUTS</span></span>

### <span data-ttu-id="69b59-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="69b59-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="69b59-122">NOTES</span><span class="sxs-lookup"><span data-stu-id="69b59-122">NOTES</span></span>

## <span data-ttu-id="69b59-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69b59-123">RELATED LINKS</span></span>

[<span data-ttu-id="69b59-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="69b59-124">New-AzContainerRegistry</span></span>]()

