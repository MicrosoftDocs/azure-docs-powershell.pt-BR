---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94281420"
---
# <span data-ttu-id="1be21-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1be21-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="1be21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1be21-102">SYNOPSIS</span></span>
<span data-ttu-id="1be21-103">Atualiza um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1be21-103">Updates a container registry.</span></span>

## <span data-ttu-id="1be21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1be21-104">SYNTAX</span></span>

### <span data-ttu-id="1be21-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1be21-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be21-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1be21-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be21-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1be21-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be21-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1be21-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be21-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1be21-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1be21-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1be21-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1be21-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1be21-111">DESCRIPTION</span></span>
<span data-ttu-id="1be21-112">O cmdlet Update-AzContainerRegistry atualiza um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1be21-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="1be21-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1be21-113">EXAMPLES</span></span>

### <span data-ttu-id="1be21-114">Exemplo 1: habilitar o usuário administrador para um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="1be21-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="1be21-115">Esse comando habilita o usuário administrador para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="1be21-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="1be21-116">Exemplo 2: definir a conta de armazenamento usada por um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="1be21-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="1be21-117">Esse comando define o registro de contêiner especificado para usar um mystorageaccount de conta de armazenamento existente \` \` na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="1be21-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="1be21-118">OS</span><span class="sxs-lookup"><span data-stu-id="1be21-118">PARAMETERS</span></span>

### <span data-ttu-id="1be21-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1be21-119">-DefaultProfile</span></span>
<span data-ttu-id="1be21-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="1be21-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1be21-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="1be21-121">-DisableAdminUser</span></span>
<span data-ttu-id="1be21-122">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1be21-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be21-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="1be21-123">-EnableAdminUser</span></span>
<span data-ttu-id="1be21-124">Habilite o usuário administrador para o registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1be21-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be21-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="1be21-125">-Name</span></span>
<span data-ttu-id="1be21-126">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1be21-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be21-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1be21-127">-NetworkRuleSet</span></span>
<span data-ttu-id="1be21-128">A regra de rede definida para um registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1be21-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be21-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1be21-129">-ResourceGroupName</span></span>
<span data-ttu-id="1be21-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1be21-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be21-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1be21-131">-ResourceId</span></span>
<span data-ttu-id="1be21-132">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="1be21-132">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1be21-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="1be21-133">-Sku</span></span>
<span data-ttu-id="1be21-134">SKU do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="1be21-134">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be21-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1be21-135">-StorageAccountName</span></span>
<span data-ttu-id="1be21-136">O nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="1be21-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="1be21-137">-Marca</span><span class="sxs-lookup"><span data-stu-id="1be21-137">-Tag</span></span>
<span data-ttu-id="1be21-138">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="1be21-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="1be21-139">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="1be21-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1be21-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1be21-140">-Confirm</span></span>
<span data-ttu-id="1be21-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1be21-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be21-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1be21-142">-WhatIf</span></span>
<span data-ttu-id="1be21-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1be21-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1be21-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1be21-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1be21-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1be21-145">CommonParameters</span></span>
<span data-ttu-id="1be21-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1be21-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1be21-147">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1be21-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1be21-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1be21-148">INPUTS</span></span>

### <span data-ttu-id="1be21-149">System. String</span><span class="sxs-lookup"><span data-stu-id="1be21-149">System.String</span></span>

## <span data-ttu-id="1be21-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1be21-150">OUTPUTS</span></span>

### <span data-ttu-id="1be21-151">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1be21-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="1be21-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1be21-152">NOTES</span></span>

## <span data-ttu-id="1be21-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1be21-153">RELATED LINKS</span></span>

[<span data-ttu-id="1be21-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1be21-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="1be21-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1be21-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="1be21-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1be21-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

