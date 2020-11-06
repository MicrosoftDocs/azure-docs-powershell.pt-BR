---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Test-AzureRmContainerRegistryNameAvailability.md
ms.openlocfilehash: ad2a97895f4876c008d1740e962bb3b746e67ec8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610830"
---
# <span data-ttu-id="d036a-101">Test-AzureRmContainerRegistryNameAvailability</span><span class="sxs-lookup"><span data-stu-id="d036a-101">Test-AzureRmContainerRegistryNameAvailability</span></span>

## <span data-ttu-id="d036a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d036a-102">SYNOPSIS</span></span>
<span data-ttu-id="d036a-103">Verifica a disponibilidade de um nome de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d036a-103">Checks the availability of a container registry name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d036a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d036a-104">SYNTAX</span></span>

```
Test-AzureRmContainerRegistryNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d036a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d036a-105">DESCRIPTION</span></span>
<span data-ttu-id="d036a-106">O cmdlet **Test-AzureRmContainerRegistryNameAvailability** verifica se um nome de registro de contêiner é válido e está disponível para uso.</span><span class="sxs-lookup"><span data-stu-id="d036a-106">The **Test-AzureRmContainerRegistryNameAvailability** cmdlet checks whether a container registry name is valid and available to use.</span></span>

## <span data-ttu-id="d036a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d036a-107">EXAMPLES</span></span>

### <span data-ttu-id="d036a-108">Exemplo 1: verificar a disponibilidade de um nome de registro de contêiner</span><span class="sxs-lookup"><span data-stu-id="d036a-108">Example 1: Check the availability of a container registry name</span></span>
```
PS C:\>Test-AzureRmContainerRegistryNameAvailability -Name 'SomeRegistryName'

NameAvailable Reason Message
------------- ------ -------
         True
```

<span data-ttu-id="d036a-109">Esse comando verifica a disponibilidade do nome do registro do contêiner `SomeRegistryName` .</span><span class="sxs-lookup"><span data-stu-id="d036a-109">This command checks the availability of the container registry name `SomeRegistryName`.</span></span>

## <span data-ttu-id="d036a-110">OS</span><span class="sxs-lookup"><span data-stu-id="d036a-110">PARAMETERS</span></span>

### <span data-ttu-id="d036a-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="d036a-111">-Name</span></span>
<span data-ttu-id="d036a-112">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="d036a-112">Container Registry Name.</span></span>

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

### <span data-ttu-id="d036a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d036a-113">-DefaultProfile</span></span>
<span data-ttu-id="d036a-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d036a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d036a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d036a-115">CommonParameters</span></span>
<span data-ttu-id="d036a-116">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d036a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d036a-117">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d036a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d036a-118">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d036a-118">INPUTS</span></span>

## <span data-ttu-id="d036a-119">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d036a-119">OUTPUTS</span></span>

### <span data-ttu-id="d036a-120">Microsoft. Azure. Management. ContainerRegistry. Models. RegistryNameStatus</span><span class="sxs-lookup"><span data-stu-id="d036a-120">Microsoft.Azure.Management.ContainerRegistry.Models.RegistryNameStatus</span></span>

## <span data-ttu-id="d036a-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d036a-121">NOTES</span></span>

## <span data-ttu-id="d036a-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d036a-122">RELATED LINKS</span></span>

[<span data-ttu-id="d036a-123">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d036a-123">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

