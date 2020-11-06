---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistry.md
ms.openlocfilehash: 3d9580549308c17c92037b3e31a337f11bbe6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426400"
---
# <span data-ttu-id="04dd9-101">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="04dd9-101">Get-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="04dd9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="04dd9-102">SYNOPSIS</span></span>
<span data-ttu-id="04dd9-103">Obtém um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="04dd9-103">Gets a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04dd9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04dd9-104">SYNTAX</span></span>

### <span data-ttu-id="04dd9-105">ListRegistriesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="04dd9-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04dd9-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="04dd9-106">RegistryNameParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04dd9-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04dd9-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="04dd9-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="04dd9-108">DESCRIPTION</span></span>
<span data-ttu-id="04dd9-109">O cmdlet Get-AzureRmContainerRegistry Obtém um registro de contêiner especificado ou todos os registros de contêiner em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="04dd9-109">The Get-AzureRmContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="04dd9-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="04dd9-110">EXAMPLES</span></span>

### <span data-ttu-id="04dd9-111">Exemplo 1: obter um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="04dd9-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="04dd9-112">Esse comando obtém o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="04dd9-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="04dd9-113">Exemplo 2: obter todos os registros de contêiner em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="04dd9-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="04dd9-114">Esse comando obtém todos os registros de contêiner em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="04dd9-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="04dd9-115">Exemplo 3: obter todos os registros de contêiner na assinatura</span><span class="sxs-lookup"><span data-stu-id="04dd9-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="04dd9-116">Esse comando obtém todos os registros de contêiner na assinatura.</span><span class="sxs-lookup"><span data-stu-id="04dd9-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="04dd9-117">OS</span><span class="sxs-lookup"><span data-stu-id="04dd9-117">PARAMETERS</span></span>

### <span data-ttu-id="04dd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04dd9-118">-DefaultProfile</span></span>
<span data-ttu-id="04dd9-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="04dd9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04dd9-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="04dd9-120">-IncludeDetail</span></span>
<span data-ttu-id="04dd9-121">Mostrar mais detalhes sobre o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="04dd9-121">Show more details about the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04dd9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="04dd9-122">-Name</span></span>
<span data-ttu-id="04dd9-123">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="04dd9-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="04dd9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04dd9-124">-ResourceGroupName</span></span>
<span data-ttu-id="04dd9-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="04dd9-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
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

### <span data-ttu-id="04dd9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04dd9-126">-ResourceId</span></span>
<span data-ttu-id="04dd9-127">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="04dd9-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04dd9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04dd9-128">CommonParameters</span></span>
<span data-ttu-id="04dd9-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04dd9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04dd9-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04dd9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04dd9-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="04dd9-131">INPUTS</span></span>

### <span data-ttu-id="04dd9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="04dd9-132">System.String</span></span>

## <span data-ttu-id="04dd9-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="04dd9-133">OUTPUTS</span></span>

### <span data-ttu-id="04dd9-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="04dd9-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="04dd9-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="04dd9-135">NOTES</span></span>

## <span data-ttu-id="04dd9-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="04dd9-136">RELATED LINKS</span></span>

[<span data-ttu-id="04dd9-137">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="04dd9-137">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="04dd9-138">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="04dd9-138">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="04dd9-139">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="04dd9-139">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

