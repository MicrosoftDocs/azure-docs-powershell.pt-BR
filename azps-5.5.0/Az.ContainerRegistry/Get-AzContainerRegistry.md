---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 759bc79a7ab36f99e01ce1e96b0bb6c3c6a9483b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100112088"
---
# <span data-ttu-id="5f96f-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5f96f-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="5f96f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5f96f-102">SYNOPSIS</span></span>
<span data-ttu-id="5f96f-103">Obtém um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="5f96f-103">Gets a container registry.</span></span>

## <span data-ttu-id="5f96f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f96f-104">SYNTAX</span></span>

### <span data-ttu-id="5f96f-105">ListRegistriesParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5f96f-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f96f-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f96f-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f96f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f96f-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f96f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f96f-108">DESCRIPTION</span></span>
<span data-ttu-id="5f96f-109">O Get-AzContainerRegistry cmdlet obtém um registro de contêiner especificado ou todos os registros de contêineres em um grupo de recursos ou na assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f96f-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="5f96f-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5f96f-110">EXAMPLES</span></span>

### <span data-ttu-id="5f96f-111">Exemplo 1: Obter um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="5f96f-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="5f96f-112">Esse comando obtém o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="5f96f-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="5f96f-113">Exemplo 2: Obter todos os registros de contêineres em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5f96f-113">Example 2: Get all the container registries in a resource group</span></span>
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

<span data-ttu-id="5f96f-114">Esse comando obtém todos os registros de contêineres em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f96f-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="5f96f-115">Exemplo 3: Obter todos os registros de contêineres na assinatura</span><span class="sxs-lookup"><span data-stu-id="5f96f-115">Example 3:  Get all the container registries in the subscription</span></span>
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

<span data-ttu-id="5f96f-116">Esse comando obtém todos os registros de contêiner na assinatura.</span><span class="sxs-lookup"><span data-stu-id="5f96f-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="5f96f-117">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f96f-117">PARAMETERS</span></span>

### <span data-ttu-id="5f96f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f96f-118">-DefaultProfile</span></span>
<span data-ttu-id="5f96f-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="5f96f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f96f-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="5f96f-120">-IncludeDetail</span></span>
<span data-ttu-id="5f96f-121">Mostrar mais detalhes sobre o registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="5f96f-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="5f96f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f96f-122">-Name</span></span>
<span data-ttu-id="5f96f-123">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="5f96f-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="5f96f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f96f-124">-ResourceGroupName</span></span>
<span data-ttu-id="5f96f-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5f96f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="5f96f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f96f-126">-ResourceId</span></span>
<span data-ttu-id="5f96f-127">A ID do recurso de registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="5f96f-127">The container registry resource id</span></span>

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

### <span data-ttu-id="5f96f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f96f-128">CommonParameters</span></span>
<span data-ttu-id="5f96f-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f96f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f96f-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5f96f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f96f-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="5f96f-131">INPUTS</span></span>

### <span data-ttu-id="5f96f-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5f96f-132">System.String</span></span>

## <span data-ttu-id="5f96f-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="5f96f-133">OUTPUTS</span></span>

### <span data-ttu-id="5f96f-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5f96f-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="5f96f-135">Notas</span><span class="sxs-lookup"><span data-stu-id="5f96f-135">NOTES</span></span>

## <span data-ttu-id="5f96f-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5f96f-136">RELATED LINKS</span></span>

[<span data-ttu-id="5f96f-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5f96f-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="5f96f-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5f96f-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="5f96f-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5f96f-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

