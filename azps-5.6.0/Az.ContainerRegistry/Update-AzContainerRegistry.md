---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: aa84186be2b5dc13117397e76722a6826d5314a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885925"
---
# <span data-ttu-id="65b05-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="65b05-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="65b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65b05-102">SYNOPSIS</span></span>
<span data-ttu-id="65b05-103">Atualiza um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="65b05-103">Updates a container registry.</span></span>

## <span data-ttu-id="65b05-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="65b05-104">SYNTAX</span></span>

### <span data-ttu-id="65b05-105">NameResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="65b05-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b05-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b05-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b05-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b05-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b05-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b05-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b05-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b05-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65b05-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65b05-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65b05-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="65b05-111">DESCRIPTION</span></span>
<span data-ttu-id="65b05-112">O Update-AzContainerRegistry cmdlet atualiza um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="65b05-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="65b05-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="65b05-113">EXAMPLES</span></span>

### <span data-ttu-id="65b05-114">Exemplo 1: Habilitar o usuário de administrador para um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="65b05-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="65b05-115">Este comando habilita o usuário de administrador para o registro de contêiner especificado.</span><span class="sxs-lookup"><span data-stu-id="65b05-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="65b05-116">Exemplo 2: definir a conta de armazenamento usada por um registro de contêiner especificado</span><span class="sxs-lookup"><span data-stu-id="65b05-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="65b05-117">Este comando define o registro de contêiner especificado para usar uma conta de armazenamento existente \` mystorageaccount \` na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="65b05-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="65b05-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="65b05-118">PARAMETERS</span></span>

### <span data-ttu-id="65b05-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65b05-119">-DefaultProfile</span></span>
<span data-ttu-id="65b05-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="65b05-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65b05-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="65b05-121">-DisableAdminUser</span></span>
<span data-ttu-id="65b05-122">Habilitar o usuário de administrador para o registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="65b05-122">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="65b05-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="65b05-123">-EnableAdminUser</span></span>
<span data-ttu-id="65b05-124">Habilitar o usuário de administrador para o registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="65b05-124">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="65b05-125">-Name</span><span class="sxs-lookup"><span data-stu-id="65b05-125">-Name</span></span>
<span data-ttu-id="65b05-126">Nome do Registro do Contêiner.</span><span class="sxs-lookup"><span data-stu-id="65b05-126">Container Registry Name.</span></span>

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

### <span data-ttu-id="65b05-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="65b05-127">-NetworkRuleSet</span></span>
<span data-ttu-id="65b05-128">A regra de rede definida para um registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="65b05-128">The network rule set for a container registry.</span></span>

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

### <span data-ttu-id="65b05-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65b05-129">-ResourceGroupName</span></span>
<span data-ttu-id="65b05-130">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="65b05-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="65b05-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65b05-131">-ResourceId</span></span>
<span data-ttu-id="65b05-132">A ID de recurso do Registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="65b05-132">The container registry resource id</span></span>

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

### <span data-ttu-id="65b05-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="65b05-133">-Sku</span></span>
<span data-ttu-id="65b05-134">SKU do Registro de Contêiner.</span><span class="sxs-lookup"><span data-stu-id="65b05-134">Container Registry SKU.</span></span>

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

### <span data-ttu-id="65b05-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="65b05-135">-StorageAccountName</span></span>
<span data-ttu-id="65b05-136">O nome de uma conta de armazenamento existente.</span><span class="sxs-lookup"><span data-stu-id="65b05-136">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="65b05-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="65b05-137">-Tag</span></span>
<span data-ttu-id="65b05-138">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="65b05-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="65b05-139">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="65b05-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="65b05-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65b05-140">-Confirm</span></span>
<span data-ttu-id="65b05-141">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65b05-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65b05-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65b05-142">-WhatIf</span></span>
<span data-ttu-id="65b05-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="65b05-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65b05-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="65b05-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65b05-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65b05-145">CommonParameters</span></span>
<span data-ttu-id="65b05-146">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65b05-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65b05-147">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65b05-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65b05-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65b05-148">INPUTS</span></span>

### <span data-ttu-id="65b05-149">System.String</span><span class="sxs-lookup"><span data-stu-id="65b05-149">System.String</span></span>

## <span data-ttu-id="65b05-150">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="65b05-150">OUTPUTS</span></span>

### <span data-ttu-id="65b05-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="65b05-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="65b05-152">NOTES</span><span class="sxs-lookup"><span data-stu-id="65b05-152">NOTES</span></span>

## <span data-ttu-id="65b05-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="65b05-153">RELATED LINKS</span></span>

[<span data-ttu-id="65b05-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="65b05-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="65b05-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="65b05-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="65b05-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="65b05-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

