---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/test-azurermcontainerregistrynameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: da415c21532ea0b2178cc2a75d6a3d09bdc2d50b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431031"
---
# <span data-ttu-id="ea3bc-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ea3bc-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="ea3bc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea3bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ea3bc-103">Verifica a disponibilidade de um nome de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea3bc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea3bc-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea3bc-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea3bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ea3bc-106">O cmdlet Test-AzureRmContainerRegistryNameAvailability verifica se um nome de registro do contêiner é válido e está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-106">The Test-AzureRmContainerRegistryNameAvailability cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="ea3bc-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea3bc-107">EXAMPLES</span></span>

### <span data-ttu-id="ea3bc-108">Exemplo 1: verifica a disponibilidade de um nome de registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="ea3bc-108">Example 1: Checks the availability of a container registry name</span></span>
```powershell
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="ea3bc-109">Esse comando verifica a disponibilidade do nome do registro do contêiner \` SomeRegistryName \` .</span><span class="sxs-lookup"><span data-stu-id="ea3bc-109">This command checks the availability of the container registry name \`SomeRegistryName\`.</span></span>

## <span data-ttu-id="ea3bc-110">OS</span><span class="sxs-lookup"><span data-stu-id="ea3bc-110">PARAMETERS</span></span>

### <span data-ttu-id="ea3bc-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea3bc-111">-Name</span></span>
<span data-ttu-id="ea3bc-112">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-112">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea3bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea3bc-113">-DefaultProfile</span></span>
<span data-ttu-id="ea3bc-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ea3bc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea3bc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea3bc-115">CommonParameters</span></span>
<span data-ttu-id="ea3bc-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea3bc-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea3bc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea3bc-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea3bc-118">INPUTS</span></span>

### <span data-ttu-id="ea3bc-119">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ea3bc-119">None</span></span>
<span data-ttu-id="ea3bc-120">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="ea3bc-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ea3bc-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea3bc-121">OUTPUTS</span></span>

### <span data-ttu-id="ea3bc-122">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="ea3bc-122">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="ea3bc-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea3bc-123">NOTES</span></span>

## <span data-ttu-id="ea3bc-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea3bc-124">RELATED LINKS</span></span>

[<span data-ttu-id="ea3bc-125">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ea3bc-125">New-AzureRmContainerRegistry</span></span>]()

