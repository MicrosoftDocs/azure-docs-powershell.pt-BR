---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 759bc79a7ab36f99e01ce1e96b0bb6c3c6a9483b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955715"
---
# <span data-ttu-id="c0224-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c0224-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="c0224-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0224-102">SYNOPSIS</span></span>
<span data-ttu-id="c0224-103">Obtém um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c0224-103">Gets a container registry.</span></span>

## <span data-ttu-id="c0224-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0224-104">SYNTAX</span></span>

### <span data-ttu-id="c0224-105">ListRegistriesParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c0224-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0224-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0224-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0224-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0224-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0224-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0224-108">DESCRIPTION</span></span>
<span data-ttu-id="c0224-109">O cmdlet Get-AzContainerRegistry Obtém um registro de contêiner especificado ou todos os registros de contêiner em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c0224-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="c0224-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0224-110">EXAMPLES</span></span>

### <span data-ttu-id="c0224-111">Exemplo 1: obter um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="c0224-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="c0224-112">Esse comando obtém o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="c0224-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="c0224-113">Exemplo 2: obter todos os registros de contêiner em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c0224-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

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

<span data-ttu-id="c0224-114">Esse comando obtém todos os registros de contêiner em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0224-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="c0224-115">Exemplo 3: obter todos os registros de contêiner na assinatura</span><span class="sxs-lookup"><span data-stu-id="c0224-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

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

<span data-ttu-id="c0224-116">Esse comando obtém todos os registros de contêiner na assinatura.</span><span class="sxs-lookup"><span data-stu-id="c0224-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="c0224-117">OS</span><span class="sxs-lookup"><span data-stu-id="c0224-117">PARAMETERS</span></span>

### <span data-ttu-id="c0224-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0224-118">-DefaultProfile</span></span>
<span data-ttu-id="c0224-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c0224-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0224-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="c0224-120">-IncludeDetail</span></span>
<span data-ttu-id="c0224-121">Mostrar mais detalhes sobre o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c0224-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="c0224-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0224-122">-Name</span></span>
<span data-ttu-id="c0224-123">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="c0224-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="c0224-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0224-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0224-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c0224-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c0224-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0224-126">-ResourceId</span></span>
<span data-ttu-id="c0224-127">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="c0224-127">The container registry resource id</span></span>

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

### <span data-ttu-id="c0224-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0224-128">CommonParameters</span></span>
<span data-ttu-id="c0224-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0224-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0224-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0224-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0224-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0224-131">INPUTS</span></span>

### <span data-ttu-id="c0224-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c0224-132">System.String</span></span>

## <span data-ttu-id="c0224-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0224-133">OUTPUTS</span></span>

### <span data-ttu-id="c0224-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c0224-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="c0224-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0224-135">NOTES</span></span>

## <span data-ttu-id="c0224-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0224-136">RELATED LINKS</span></span>

[<span data-ttu-id="c0224-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c0224-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="c0224-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c0224-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="c0224-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c0224-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

