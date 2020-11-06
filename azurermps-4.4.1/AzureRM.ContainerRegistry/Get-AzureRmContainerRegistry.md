---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: ce2cabd669f779fe94afa80089868aa04753524b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431787"
---
# <span data-ttu-id="fe6c1-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe6c1-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="fe6c1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe6c1-103">Obtém um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fe6c1-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe6c1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe6c1-104">SYNTAX</span></span>

### <span data-ttu-id="fe6c1-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe6c1-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe6c1-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe6c1-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe6c1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe6c1-107">DESCRIPTION</span></span>
<span data-ttu-id="fe6c1-108">O cmdlet **Get-AzureRmContainerRegistry** Obtém um registro de contêiner especificado ou todos os registros de contêiner em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="fe6c1-108">The **Get-AzureRmContainerRegistry** cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="fe6c1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe6c1-109">EXAMPLES</span></span>

### <span data-ttu-id="fe6c1-110">Exemplo 1: obter um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="fe6c1-110">Example 1: Get a specified container registry</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="fe6c1-111">Esse comando obtém o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="fe6c1-111">This command gets the specified container registry.</span></span>

### <span data-ttu-id="fe6c1-112">Exemplo 2: obter todos os registros de contêiner em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fe6c1-112">Example 2: Get all the container registries in a resource group</span></span>
```
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="fe6c1-113">Esse comando obtém todos os registros de contêiner em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe6c1-113">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="fe6c1-114">Exemplo 3: obter todos os registros de contêiner na assinatura</span><span class="sxs-lookup"><span data-stu-id="fe6c1-114">Example 3:  Get all the container registries in the subscription</span></span>
```
PS C:\>Get-AzureRmContainerRegistry

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/AnotherRegistry
ResourceGroupName  : MyResourceGroup
Name               : AnotherRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : anotherregistry.azurecr.io
CreationDate       : 4/13/2017 3:50:49 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : anotherregistry154940
```

<span data-ttu-id="fe6c1-115">Esse comando obtém todos os registros de contêiner na assinatura.</span><span class="sxs-lookup"><span data-stu-id="fe6c1-115">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="fe6c1-116">OS</span><span class="sxs-lookup"><span data-stu-id="fe6c1-116">PARAMETERS</span></span>

### <span data-ttu-id="fe6c1-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe6c1-117">-Name</span></span>
<span data-ttu-id="fe6c1-118">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="fe6c1-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6c1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe6c1-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe6c1-120">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fe6c1-120">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe6c1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe6c1-121">-DefaultProfile</span></span>
<span data-ttu-id="fe6c1-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe6c1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe6c1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe6c1-123">CommonParameters</span></span>
<span data-ttu-id="fe6c1-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe6c1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe6c1-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe6c1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe6c1-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe6c1-126">INPUTS</span></span>

## <span data-ttu-id="fe6c1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe6c1-127">OUTPUTS</span></span>

### <span data-ttu-id="fe6c1-128">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe6c1-128">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="fe6c1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe6c1-129">NOTES</span></span>

## <span data-ttu-id="fe6c1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe6c1-130">RELATED LINKS</span></span>

[<span data-ttu-id="fe6c1-131">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe6c1-131">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="fe6c1-132">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe6c1-132">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="fe6c1-133">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="fe6c1-133">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)

