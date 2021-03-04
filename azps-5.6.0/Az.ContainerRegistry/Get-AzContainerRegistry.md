---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 969e37173c487b2ed3ee4ab6dad5374208f5ff27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892208"
---
# <span data-ttu-id="8331e-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8331e-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="8331e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8331e-102">SYNOPSIS</span></span>
<span data-ttu-id="8331e-103">Obtém um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="8331e-103">Gets a container registry.</span></span>

## <span data-ttu-id="8331e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8331e-104">SYNTAX</span></span>

### <span data-ttu-id="8331e-105">ListRegistriesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8331e-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8331e-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8331e-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8331e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8331e-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8331e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8331e-108">DESCRIPTION</span></span>
<span data-ttu-id="8331e-109">O Get-AzContainerRegistry cmdlet obtém um registro de contêiner especificado ou todos os registros de contêiner em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8331e-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="8331e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8331e-110">EXAMPLES</span></span>

### <span data-ttu-id="8331e-111">Exemplo 1: Obter um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="8331e-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="8331e-112">Este comando obtém o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="8331e-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="8331e-113">Exemplo 2: Obter todos os registros de contêiner em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8331e-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="8331e-114">Esse comando obtém todos os registros de contêiner em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8331e-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="8331e-115">Exemplo 3: Obter todos os registros de contêiner na assinatura</span><span class="sxs-lookup"><span data-stu-id="8331e-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="8331e-116">Esse comando obtém todos os registros de contêiner na assinatura.</span><span class="sxs-lookup"><span data-stu-id="8331e-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="8331e-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8331e-117">PARAMETERS</span></span>

### <span data-ttu-id="8331e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8331e-118">-DefaultProfile</span></span>
<span data-ttu-id="8331e-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8331e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8331e-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="8331e-120">-IncludeDetail</span></span>
<span data-ttu-id="8331e-121">Mostrar mais detalhes sobre o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="8331e-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="8331e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8331e-122">-Name</span></span>
<span data-ttu-id="8331e-123">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="8331e-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="8331e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8331e-124">-ResourceGroupName</span></span>
<span data-ttu-id="8331e-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8331e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8331e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8331e-126">-ResourceId</span></span>
<span data-ttu-id="8331e-127">A ID de recurso do Registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="8331e-127">The container registry resource id</span></span>

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

### <span data-ttu-id="8331e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8331e-128">CommonParameters</span></span>
<span data-ttu-id="8331e-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8331e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8331e-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8331e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8331e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8331e-131">INPUTS</span></span>

### <span data-ttu-id="8331e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8331e-132">System.String</span></span>

## <span data-ttu-id="8331e-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8331e-133">OUTPUTS</span></span>

### <span data-ttu-id="8331e-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8331e-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="8331e-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="8331e-135">NOTES</span></span>

## <span data-ttu-id="8331e-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8331e-136">RELATED LINKS</span></span>

[<span data-ttu-id="8331e-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8331e-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="8331e-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8331e-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="8331e-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8331e-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

