---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 468c4cfac836ca986d6cfbfd06f35032cca5b6a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431045"
---
# <span data-ttu-id="acb85-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="acb85-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="acb85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="acb85-102">SYNOPSIS</span></span>
<span data-ttu-id="acb85-103">Atualiza um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="acb85-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acb85-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="acb85-104">SYNTAX</span></span>

### <span data-ttu-id="acb85-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="acb85-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acb85-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="acb85-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acb85-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="acb85-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acb85-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acb85-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acb85-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acb85-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="acb85-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="acb85-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acb85-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="acb85-111">DESCRIPTION</span></span>
<span data-ttu-id="acb85-112">O cmdlet Update-AzureRmContainerRegistry atualiza um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="acb85-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="acb85-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="acb85-113">EXAMPLES</span></span>

### <span data-ttu-id="acb85-114">Exemplo 1: habilitar o usuário administrador para um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="acb85-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="acb85-115">Esse comando habilita o usuário administrador para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="acb85-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="acb85-116">Exemplo 2: definir a conta de armazenamento usada por um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="acb85-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="acb85-117">Esse comando define o registro de contêiner especificado para usar um mystorageaccount de conta de armazenamento existente \` \` na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="acb85-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="acb85-118">OS</span><span class="sxs-lookup"><span data-stu-id="acb85-118">PARAMETERS</span></span>

### <span data-ttu-id="acb85-119">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="acb85-119">-DisableAdminUser</span></span>
<span data-ttu-id="acb85-120">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="acb85-120">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-121">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="acb85-121">-EnableAdminUser</span></span>
<span data-ttu-id="acb85-122">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="acb85-122">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="acb85-123">-Name</span></span>
<span data-ttu-id="acb85-124">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="acb85-124">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acb85-125">-ResourceGroupName</span></span>
<span data-ttu-id="acb85-126">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="acb85-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="acb85-127">-StorageAccountName</span></span>
<span data-ttu-id="acb85-128">O nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="acb85-128">The name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="acb85-129">-Tag</span></span>
<span data-ttu-id="acb85-130">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="acb85-130">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="acb85-131">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="acb85-131">For example:</span></span>

<span data-ttu-id="acb85-132">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="acb85-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="acb85-133">-Confirm</span></span>
<span data-ttu-id="acb85-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acb85-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acb85-135">-WhatIf</span></span>
<span data-ttu-id="acb85-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="acb85-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acb85-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="acb85-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acb85-138">-DefaultProfile</span></span>
<span data-ttu-id="acb85-139">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="acb85-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="acb85-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="acb85-140">-ResourceId</span></span>
<span data-ttu-id="acb85-141">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="acb85-141">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="acb85-142">-Sku</span></span>
<span data-ttu-id="acb85-143">SKU do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="acb85-143">Container Registry SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acb85-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acb85-144">CommonParameters</span></span>
<span data-ttu-id="acb85-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acb85-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acb85-146">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acb85-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acb85-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="acb85-147">INPUTS</span></span>

### <span data-ttu-id="acb85-148">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="acb85-148">None</span></span>
<span data-ttu-id="acb85-149">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="acb85-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="acb85-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="acb85-150">OUTPUTS</span></span>

### <span data-ttu-id="acb85-151">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="acb85-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="acb85-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="acb85-152">NOTES</span></span>

## <span data-ttu-id="acb85-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="acb85-153">RELATED LINKS</span></span>

[<span data-ttu-id="acb85-154">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="acb85-154">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="acb85-155">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="acb85-155">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="acb85-156">Remove-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="acb85-156">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

