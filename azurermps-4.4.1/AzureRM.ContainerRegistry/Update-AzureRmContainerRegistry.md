---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 5f59ae54d472d1d831b41f58789625c195961de5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440204"
---
# <span data-ttu-id="70d7a-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70d7a-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="70d7a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="70d7a-102">SYNOPSIS</span></span>
<span data-ttu-id="70d7a-103">Atualiza um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70d7a-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70d7a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="70d7a-104">SYNTAX</span></span>

### <span data-ttu-id="70d7a-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="70d7a-105">Empty (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70d7a-106">EnableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="70d7a-106">EnableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70d7a-107">DisableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="70d7a-107">DisableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70d7a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="70d7a-108">DESCRIPTION</span></span>
<span data-ttu-id="70d7a-109">O cmdlet **Update-AzureRmContainerRegistry** atualiza um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70d7a-109">The **Update-AzureRmContainerRegistry** cmdlet updates a container registry.</span></span>

## <span data-ttu-id="70d7a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="70d7a-110">EXAMPLES</span></span>

### <span data-ttu-id="70d7a-111">Exemplo 1: habilitar o usuário administrador para um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="70d7a-111">Example 1: Enable admin user for a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

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

<span data-ttu-id="70d7a-112">Esse comando habilita o usuário administrador para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="70d7a-112">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="70d7a-113">Exemplo 2: definir a conta de armazenamento usada por um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="70d7a-113">Example 2: Set the storage account used by a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="70d7a-114">Esse comando define o registro de contêiner especificado para usar uma conta de armazenamento existente `mystorageaccount` na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="70d7a-114">This command sets the specified container registry to use an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="70d7a-115">OS</span><span class="sxs-lookup"><span data-stu-id="70d7a-115">PARAMETERS</span></span>

### <span data-ttu-id="70d7a-116">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="70d7a-116">-DisableAdminUser</span></span>
<span data-ttu-id="70d7a-117">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70d7a-117">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: DisableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d7a-118">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="70d7a-118">-EnableAdminUser</span></span>
<span data-ttu-id="70d7a-119">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70d7a-119">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70d7a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="70d7a-120">-Name</span></span>
<span data-ttu-id="70d7a-121">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="70d7a-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="70d7a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70d7a-122">-ResourceGroupName</span></span>
<span data-ttu-id="70d7a-123">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="70d7a-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="70d7a-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="70d7a-124">-StorageAccountName</span></span>
<span data-ttu-id="70d7a-125">O nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="70d7a-125">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="70d7a-126">-Marca</span><span class="sxs-lookup"><span data-stu-id="70d7a-126">-Tag</span></span>
<span data-ttu-id="70d7a-127">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="70d7a-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="70d7a-128">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="70d7a-128">For example:</span></span>

<span data-ttu-id="70d7a-129">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="70d7a-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="70d7a-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="70d7a-130">-Confirm</span></span>
<span data-ttu-id="70d7a-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70d7a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70d7a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70d7a-132">-WhatIf</span></span>
<span data-ttu-id="70d7a-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="70d7a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70d7a-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="70d7a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70d7a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70d7a-135">-DefaultProfile</span></span>
<span data-ttu-id="70d7a-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="70d7a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70d7a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70d7a-137">CommonParameters</span></span>
<span data-ttu-id="70d7a-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70d7a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70d7a-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70d7a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70d7a-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="70d7a-140">INPUTS</span></span>

## <span data-ttu-id="70d7a-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="70d7a-141">OUTPUTS</span></span>

### <span data-ttu-id="70d7a-142">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70d7a-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="70d7a-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="70d7a-143">NOTES</span></span>

## <span data-ttu-id="70d7a-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="70d7a-144">RELATED LINKS</span></span>

[<span data-ttu-id="70d7a-145">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70d7a-145">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="70d7a-146">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70d7a-146">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="70d7a-147">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="70d7a-147">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
