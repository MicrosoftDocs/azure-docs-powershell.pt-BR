---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/test-azcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Test-AzContainerRegistryNameAvailability.md
ms.openlocfilehash: 4471835a1ff87a44722fc9e0dd51b0fa279410f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771064"
---
# <span data-ttu-id="7336e-101">Test-AzContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="7336e-101">Test-AzContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="7336e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7336e-102">SYNOPSIS</span></span>
<span data-ttu-id="7336e-103">Verifica a disponibilidade de um nome de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7336e-103">Checks the availability of a container registry name.</span></span>

## <span data-ttu-id="7336e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7336e-104">SYNTAX</span></span>

```
Test-AzContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7336e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7336e-105">DESCRIPTION</span></span>
<span data-ttu-id="7336e-106">O cmdlet Test-AzContainerRegistryNameAvailability verifica se um nome de registro do contêiner é válido e está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="7336e-106">The Test-AzContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="7336e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7336e-107">EXAMPLES</span></span>

### <span data-ttu-id="7336e-108">Exemplo 1: verifica a disponibilidade de um nome de registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="7336e-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="7336e-109">Esse comando verifica a disponibilidade do nome do registro do contêiner \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="7336e-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="7336e-110">OS</span><span class="sxs-lookup"><span data-stu-id="7336e-110">PARAMETERS</span></span>

### <span data-ttu-id="7336e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7336e-111">-DefaultProfile</span></span>
<span data-ttu-id="7336e-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7336e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7336e-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="7336e-113">-Name</span></span>
<span data-ttu-id="7336e-114">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="7336e-114">Container Registry Name.</span></span>

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

### <span data-ttu-id="7336e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7336e-115">CommonParameters</span></span>
<span data-ttu-id="7336e-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7336e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7336e-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7336e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7336e-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7336e-118">INPUTS</span></span>

### <span data-ttu-id="7336e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="7336e-119">System.String</span></span>

## <span data-ttu-id="7336e-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7336e-120">OUTPUTS</span></span>

### <span data-ttu-id="7336e-121">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="7336e-121">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="7336e-122">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7336e-122">NOTES</span></span>

## <span data-ttu-id="7336e-123">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7336e-123">RELATED LINKS</span></span>

[<span data-ttu-id="7336e-124">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7336e-124">New-AzContainerRegistry</span></span>]()

