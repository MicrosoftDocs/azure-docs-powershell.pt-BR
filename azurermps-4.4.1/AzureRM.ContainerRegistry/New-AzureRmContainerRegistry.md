---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428254"
---
# <span data-ttu-id="e855e-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e855e-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="e855e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e855e-102">SYNOPSIS</span></span>
<span data-ttu-id="e855e-103">Cria um registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="e855e-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e855e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e855e-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e855e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e855e-105">DESCRIPTION</span></span>
<span data-ttu-id="e855e-106">O cmdlet **New-AzureRmContainerRegistry** cria um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e855e-106">The **New-AzureRmContainerRegistry** cmdlet creates a container registry.</span></span>

## <span data-ttu-id="e855e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e855e-107">EXAMPLES</span></span>

### <span data-ttu-id="e855e-108">Exemplo 1: criar um registro de contêiner com uma nova conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e855e-108">Example 1: Create a container registry with a new storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

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

<span data-ttu-id="e855e-109">Esse comando cria um registro de contêiner com uma nova conta de armazenamento no grupo de recursos `MyResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="e855e-109">This command creates a container registry with a new storage account in the resource group `MyResourceGroup`.</span></span>

### <span data-ttu-id="e855e-110">Exemplo 2: criar um registro de contêiner com o usuário administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="e855e-110">Example 2: Create a container registry with admin user enabled.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

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
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

<span data-ttu-id="e855e-111">Esse comando cria um registro de contêiner com o usuário administrador habilitado.</span><span class="sxs-lookup"><span data-stu-id="e855e-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="e855e-112">Exemplo 3: criar um registro de contêiner com uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="e855e-112">Example 3: Create a container registry with an existing storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="e855e-113">Esse comando cria um registro de contêiner com uma conta de armazenamento existente `mystorageaccount` na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="e855e-113">This command creates a container registry with an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="e855e-114">OS</span><span class="sxs-lookup"><span data-stu-id="e855e-114">PARAMETERS</span></span>

### <span data-ttu-id="e855e-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="e855e-115">-EnableAdminUser</span></span>
<span data-ttu-id="e855e-116">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e855e-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e855e-117">-Local</span><span class="sxs-lookup"><span data-stu-id="e855e-117">-Location</span></span>
<span data-ttu-id="e855e-118">Local do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e855e-118">Container Registry Location.</span></span>
<span data-ttu-id="e855e-119">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e855e-119">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e855e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e855e-120">-Name</span></span>
<span data-ttu-id="e855e-121">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e855e-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e855e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e855e-122">-ResourceGroupName</span></span>
<span data-ttu-id="e855e-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e855e-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e855e-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="e855e-124">-Sku</span></span>
<span data-ttu-id="e855e-125">SKU do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e855e-125">Container Registry SKU.</span></span>
<span data-ttu-id="e855e-126">Valores permitidos: Basic.</span><span class="sxs-lookup"><span data-stu-id="e855e-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e855e-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e855e-127">-StorageAccountName</span></span>
<span data-ttu-id="e855e-128">O nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="e855e-128">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e855e-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="e855e-129">-Tag</span></span>
<span data-ttu-id="e855e-130">Marcas de registro de contêineres. pares de chave-valor na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="e855e-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e855e-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="e855e-131">For example:</span></span>

<span data-ttu-id="e855e-132">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e855e-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e855e-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e855e-133">-Confirm</span></span>
<span data-ttu-id="e855e-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e855e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e855e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e855e-135">-WhatIf</span></span>
<span data-ttu-id="e855e-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e855e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e855e-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e855e-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e855e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e855e-138">-DefaultProfile</span></span>
<span data-ttu-id="e855e-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e855e-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e855e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e855e-140">CommonParameters</span></span>
<span data-ttu-id="e855e-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e855e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e855e-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e855e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e855e-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e855e-143">INPUTS</span></span>

## <span data-ttu-id="e855e-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e855e-144">OUTPUTS</span></span>

### <span data-ttu-id="e855e-145">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e855e-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="e855e-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e855e-146">NOTES</span></span>

## <span data-ttu-id="e855e-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e855e-147">RELATED LINKS</span></span>

[<span data-ttu-id="e855e-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e855e-148">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="e855e-149">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e855e-149">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="e855e-150">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e855e-150">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
